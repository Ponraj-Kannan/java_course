<script setup>
import { ref, reactive, computed, onMounted, onBeforeUnmount, watch } from 'vue';

const fmt = (a) => (a === null || a === undefined ? '—' : '' + a);

defineProps({
  topic: {
    type: String,
    required: true,
  },
  subTopic: {
    type: String,
    default: '',
  }
});

const CODES = {
  java: [
    ['', 'import java.util.Scanner;'], ['', ''],
    ['', 'public class DoWhileLoopDemo {'],
    ['c_main', '    public static void main(String[] args) {'],
    ['c_scan', '        Scanner sc = new Scanner(System.in);'],
    ['c_start', '        int start = sc.nextInt();'],
    ['c_end', '        int end = sc.nextInt();'], ['', ''],
    ['c_init', '        int i = start;'],
    ['c_do', '        do {'],
    ['c_body', '            System.out.print(i + " ");'],
    ['c_incr', '            i++;'],
    ['c_whilehdr', '        } while (i <= end);'],
    ['c_exit', '    }'], ['', '}'],
  ],
  c: [
    ['', '#include <stdio.h>'], ['', ''],
    ['c_main', 'int main() {'],
    ['c_scan', '    int start, end;'],
    [['c_start', 'c_end'], '    scanf("%d %d", &start, &end);'], ['', ''],
    ['c_init', '    int i = start;'],
    ['c_do', '    do {'],
    ['c_body', '        printf("%d ", i);'],
    ['c_incr', '        i++;'],
    ['c_whilehdr', '    } while (i <= end);'], ['', ''],
    ['c_exit', '    return 0;'], ['', '}'],
  ],
  cpp: [
    ['', '#include <iostream>'], ['', 'using namespace std;'], ['', ''],
    ['c_main', 'int main() {'],
    ['c_scan', '    int start, end;'],
    [['c_start', 'c_end'], '    cin >> start >> end;'], ['', ''],
    ['c_init', '    int i = start;'],
    ['c_do', '    do {'],
    ['c_body', '        cout << i << " ";'],
    ['c_incr', '        i++;'],
    ['c_whilehdr', '    } while (i <= end);'], ['', ''],
    ['c_exit', '    return 0;'], ['', '}'],
  ],
  python: [
    ['c_start', 'start = int(input())'],
    ['c_end', 'end = int(input())'], ['', ''],
    ['c_init', 'i = start'],
    ['c_do', 'while True:'],
    ['c_body', '    print(i, end=" ")'],
    ['c_incr', '    i += 1'],
    ['c_whilehdr', '    if not (i <= end): break'],
  ],
};

// ── flowchart geometry (wide balanced 2D post-test layout) ───────
const EDGES = [
  { id: 'e_start_init', d: 'M 90,40 L 90,56' },
  { id: 'e_init_body', d: 'M 145,73 L 265,73' },
  { id: 'e_body_incr', d: 'M 320,90 L 320,118' },
  { id: 'e_incr_cond', d: 'M 320,152 L 320,176' },
  { id: 'e_cond_yes', d: 'M 385,200 L 520,200 L 520,73 L 375,73' },
  { id: 'e_cond_no', d: 'M 255,200 L 135,200' },
];
const EDGE_PATHS = Object.fromEntries(EDGES.map((e) => [e.id, e.d]));

function frame(title, rows) {
  return { title, rows };
}

function isLineActive(lineCode, currentCode) {
  if (!lineCode || !currentCode) return false;
  if (Array.isArray(lineCode)) return lineCode.includes(currentCode);
  return lineCode === currentCode;
}

function buildSteps(start, end) {
  const steps = [];
  const sV = '' + start;
  const eV = '' + end;
  const baseRows = (iVal) => [['start', sV], ['end', eV], ['i', iVal === null ? '—' : '' + iVal, true]];

  // 1. Enter main()
  steps.push({
    i: null, out: [], curVal: null, stage: 'start', edge: null,
    badge: 'main() → program execution starts', code: 'c_main',
    vars: [frame('main()', [['start', '—'], ['end', '—'], ['i', '—']])],
  });

  // 2. Scanner initialization
  steps.push({
    i: null, out: [], curVal: null, stage: 'start', edge: null,
    badge: 'Scanner sc = new Scanner(System.in) → initialize input reader', code: 'c_scan',
    vars: [frame('main()', [['start', '—'], ['end', '—'], ['i', '—']])],
  });

  // 3. Read start
  steps.push({
    i: null, out: [], curVal: null, stage: 'start', edge: null,
    badge: 'int start = sc.nextInt() → read start = ' + start, code: 'c_start',
    vars: [frame('main()', [['start', sV], ['end', '—'], ['i', '—']])],
  });

  // 4. Read end
  steps.push({
    i: null, out: [], curVal: null, stage: 'start', edge: null,
    badge: 'int end = sc.nextInt() → read end = ' + end, code: 'c_end',
    vars: [frame('main()', baseRows(null))],
  });

  // 5. Initialize i = start
  let i = start;
  steps.push({
    i, out: [], curVal: null, stage: 'init', edge: 'e_start_init',
    badge: 'int i = start → initialize loop counter i = ' + i, code: 'c_init',
    vars: [frame('main()', baseRows(i))],
  });

  let out = [];
  let firstIter = true;
  while (true) {
    // 6. Enter Body directly (runs at least once!)
    out = [...out, i];
    steps.push({
      i, out: out.slice(), curVal: i,
      stage: 'body', edge: firstIter ? 'e_init_body' : 'e_cond_yes',
      badge: 'do { ... } → enter loop body (guaranteed to run at least once)',
      code: 'c_body',
      vars: [frame('main()', baseRows(i))],
    });
    firstIter = false;

    // 7. Increment counter
    const next = i + 1;
    steps.push({
      i: next, out: out.slice(), curVal: null,
      stage: 'incr', edge: 'e_body_incr',
      badge: 'i++ → increment counter from ' + i + ' to ' + next,
      code: 'c_incr',
      vars: [frame('main()', baseRows(next))],
    });
    i = next;

    // 8. Post-test Condition check
    const condTrue = i <= end;
    const rows = baseRows(i).concat([['i <= end', condTrue ? 'true' : 'false', true]]);
    steps.push({
      i, out: out.slice(), curVal: null,
      stage: 'cond', edge: 'e_incr_cond',
      badge: 'while (i <= end) → post-test condition: ' + i + ' <= ' + end + ' (' + (condTrue ? 'true → repeat body' : 'false → exit loop') + ')',
      code: 'c_whilehdr',
      vars: [frame('main()', rows)],
    });

    if (!condTrue) {
      steps.push({
        i, out: out.slice(), curVal: null, stage: 'end', edge: 'e_cond_no',
        badge: 'condition is false → exit do-while loop', code: 'c_exit', done: true,
        vars: [frame('main()', baseRows(i))],
      });
      break;
    }
  }

  return { steps };
}

// ── reactive state ──────────────────────────────────────────────
const inpStart = ref(1);
const inpEnd = ref(5);
const lang = ref('java');
const speed = ref(650);
const si = ref(0);
const playing = ref(false);
const vizHeight = ref(390);
const tableHeight = ref(60);
const leftWidth = ref(58);

const stepsData = reactive(buildSteps(1, 5));
const steps = computed(() => stepsData.steps);
const s = computed(() => steps.value[Math.max(0, Math.min(si.value, steps.value.length - 1))]);
const codeLines = computed(() => CODES[lang.value] || []);

let playTimer = null;

function applyInput() {
  const start = parseInt(inpStart.value, 10);
  const end = parseInt(inpEnd.value, 10);
  if (isNaN(start) || isNaN(end)) {
    alert('Enter valid whole numbers for start and end.');
    return;
  }
  if (end - start > 30) {
    alert('Keep the range to 30 numbers or fewer for a clear visualization.');
    return;
  }
  playing.value = false;
  inpStart.value = start;
  inpEnd.value = end;
  const built = buildSteps(start, end);
  stepsData.steps = built.steps;
  si.value = 0;
}

function stepBy(d) {
  si.value = Math.max(0, Math.min(steps.value.length - 1, si.value + d));
}

function togglePlay() {
  const next = !playing.value;
  if (next && si.value >= steps.value.length - 1) si.value = 0;
  playing.value = next;
}

function tick() {
  clearTimeout(playTimer);
  if (!playing.value) return;
  if (si.value >= steps.value.length - 1) {
    playing.value = false;
    return;
  }
  playTimer = setTimeout(() => {
    si.value = Math.min(steps.value.length - 1, si.value + 1);
    tick();
  }, 2100 - speed.value);
}

watch(playing, (v) => {
  if (v) tick();
  else clearTimeout(playTimer);
});

function resetCode() {
  // read-only
}

// ── keyboard shortcuts ──────────────────────────────────────────
function onKeydown(e) {
  const tag = e.target.tagName;
  if (tag === 'INPUT' || tag === 'SELECT' || tag === 'TEXTAREA') return;
  if (e.key === 'ArrowRight') stepBy(1);
  if (e.key === 'ArrowLeft') stepBy(-1);
  if (e.key === ' ') {
    e.preventDefault();
    togglePlay();
  }
}

// ── resizers ─────────────────────────────────────────────────────
const mainRef = ref(null);
const leftColRef = ref(null);
const hResizerRef = ref(null);
const vizResizerRef = ref(null);
const tableResizerRef = ref(null);

function initHResizer() {
  const rsz = hResizerRef.value;
  const main = mainRef.value;
  if (!rsz || !main) return;
  let dragging = false, startX = 0, startW = 0;

  const onDown = (e) => {
    dragging = true;
    startX = e.clientX;
    startW = leftColRef.value.offsetWidth;
    rsz.classList.add('drag');
    document.body.style.userSelect = 'none';
  };
  const onMove = (e) => {
    if (!dragging) return;
    const mainW = main.offsetWidth;
    const newW = Math.max(200, Math.min(mainW - 200, startW + e.clientX - startX));
    leftWidth.value = (newW / mainW) * 100;
  };
  const onUp = () => {
    if (!dragging) return;
    dragging = false;
    rsz.classList.remove('drag');
    document.body.style.userSelect = '';
  };
  rsz.addEventListener('mousedown', onDown);
  document.addEventListener('mousemove', onMove);
  document.addEventListener('mouseup', onUp);
  return () => {
    rsz.removeEventListener('mousedown', onDown);
    document.removeEventListener('mousemove', onMove);
    document.removeEventListener('mouseup', onUp);
  };
}

function initVResizer(elRef, valueRef, minH, maxH) {
  const rsz = elRef.value;
  if (!rsz) return;
  let dragging = false, startY = 0, startH = 0;

  const onDown = (e) => {
    dragging = true;
    startY = e.clientY;
    startH = valueRef.value;
    rsz.classList.add('drag');
    document.body.style.userSelect = 'none';
    e.preventDefault();
  };
  const onMove = (e) => {
    if (!dragging) return;
    valueRef.value = Math.max(minH, Math.min(maxH, startH + (e.clientY - startY)));
  };
  const onUp = () => {
    if (!dragging) return;
    dragging = false;
    rsz.classList.remove('drag');
    document.body.style.userSelect = '';
  };
  rsz.addEventListener('mousedown', onDown);
  document.addEventListener('mousemove', onMove);
  document.addEventListener('mouseup', onUp);
  return () => {
    rsz.removeEventListener('mousedown', onDown);
    document.removeEventListener('mousemove', onMove);
    document.removeEventListener('mouseup', onUp);
  };
}

let cleanupFns = [];

onMounted(() => {
  document.addEventListener('keydown', onKeydown);
  cleanupFns.push(initHResizer());
  cleanupFns.push(initVResizer(vizResizerRef, vizHeight, 160, 500));
  cleanupFns.push(initVResizer(tableResizerRef, tableHeight, 50, 200));
});

onBeforeUnmount(() => {
  document.removeEventListener('keydown', onKeydown);
  clearTimeout(playTimer);
  cleanupFns.forEach((fn) => fn && fn());
});
</script>

<template>
  <div class="slide-wrapper">
    <div class="navbar">
      <h2 class="navbar-title">{{ topic }}</h2>
      <img src="../assets/logo.png" />
    </div>
    <div class="slide-body">
      <div class="row-main">
        <div class="ll-root">
    <!-- TOOLBAR -->
    <div class="ll-toolbar">
      <label>Start</label>
      <input type="number" v-model="inpStart" class="ll-num-input" />
      <label>End</label>
      <input type="number" v-model="inpEnd" class="ll-num-input" />
      <button class="ll-viz-btn" @click="applyInput">▶ Visualize</button>

      <div class="ll-nav-controls">
        <button class="ll-nav-btn" title="First step" @click="stepBy(-steps.length)">«</button>
        <button class="ll-nav-btn" @click="stepBy(-1)">‹ Prev</button>
        <button class="ll-play-btn" @click="togglePlay">{{ playing ? '⏸ Pause' : '▶ Play' }}</button>
        <button class="ll-nav-btn" @click="stepBy(1)">Next ›</button>
        <button class="ll-nav-btn" title="Last step" @click="stepBy(steps.length)">»</button>
      </div>
    </div>

    <!-- MAIN -->
    <div class="ll-main" ref="mainRef">
      <div class="ll-left-col" ref="leftColRef" :style="{ width: leftWidth + '%' }">
        <!-- VIZ -->
        <div class="ll-viz-wrap" :style="{ height: vizHeight + 'px' }">
          <div class="ll-perm-area">
            <div class="ll-ptrs">
              <div class="ll-ptr-chip">i = <b class="ll-c-blue">{{ fmt(s.i) }}</b></div>
              <div v-if="s.curVal !== null && s.curVal !== undefined" class="ll-ptr-chip">
                printing <b class="ll-c-orange">{{ s.curVal }}</b>
              </div>
            </div>

            <!-- FLOWCHART -->
            <div class="ll-flow-wrap">
              <svg viewBox="0 0 540 240" class="fc-svg" xmlns="http://www.w3.org/2000/svg">
                <defs>
                  <marker id="dwfc-arrow" viewBox="0 0 10 10" refX="9" refY="5" markerWidth="6" markerHeight="6" orient="auto-start-reverse">
                    <path d="M 0 1.5 L 9 5 L 0 8.5 z" class="fc-arrowhead" />
                  </marker>
                  <marker id="dwfc-arrow-active" viewBox="0 0 10 10" refX="9" refY="5" markerWidth="7" markerHeight="7" orient="auto-start-reverse">
                    <path d="M 0 0.5 L 9 5 L 0 9.5 z" class="fc-arrowhead-active" />
                  </marker>
                </defs>

                <!-- Left col: Start -->
                <g class="fc-node node-start" :class="{ 'fc-node-active': s.stage === 'start' }">
                  <rect x="45" y="12" width="90" height="28" rx="14" class="fc-shape fc-shape-term" />
                  <text x="90" y="29" class="fc-label">Start</text>
                </g>

                <!-- Left col: Init -->
                <g class="fc-node node-init" :class="{ 'fc-node-active': s.stage === 'init' }">
                  <rect x="35" y="56" width="110" height="34" rx="7" class="fc-shape fc-shape-init" />
                  <text x="90" y="72" class="fc-label font-mono">i = start</text>
                  <text x="90" y="83" class="fc-sublabel">initialize</text>
                </g>

                <!-- Left col: End -->
                <g class="fc-node node-end" :class="{ 'fc-node-active': s.stage === 'end' }">
                  <rect x="45" y="186" width="90" height="28" rx="14" class="fc-shape fc-shape-term" />
                  <text x="90" y="204" class="fc-label">End</text>
                </g>

                <!-- Centre-right: print(i) -->
                <g class="fc-node node-body" :class="{ 'fc-node-active': s.stage === 'body' }">
                  <rect x="265" y="56" width="110" height="34" rx="7" class="fc-shape fc-shape-body" />
                  <text x="320" y="72" class="fc-label font-mono font-bold">print(i)</text>
                  <text x="320" y="83" class="fc-sublabel">loop body (runs ≥ 1)</text>
                </g>

                <!-- Centre-right: i++ -->
                <g class="fc-node node-incr" :class="{ 'fc-node-active': s.stage === 'incr' }">
                  <rect x="265" y="118" width="110" height="34" rx="7" class="fc-shape fc-shape-incr" />
                  <text x="320" y="134" class="fc-label font-mono font-bold">i++</text>
                  <text x="320" y="145" class="fc-sublabel">increment</text>
                </g>

                <!-- Centre-right: Condition Diamond (post-test) -->
                <g class="fc-node node-cond" :class="{ 'fc-node-active': s.stage === 'cond' }">
                  <polygon points="320,176  385,200  320,224  255,200" class="fc-shape fc-shape-cond" />
                  <text x="320" y="197" class="fc-label fc-label-sm font-mono font-bold">i &lt;= end ?</text>
                  <text x="320" y="209" class="fc-sublabel">post-test condition</text>
                </g>

                <!-- edges -->
                <path
                  v-for="edge in EDGES"
                  :key="edge.id"
                  :d="edge.d"
                  class="fc-edge"
                  :class="{ 'fc-edge-active': s.edge === edge.id }"
                  :marker-end="s.edge === edge.id ? 'url(#dwfc-arrow-active)' : 'url(#dwfc-arrow)'"
                />

                <!-- Yes badge: right rail -->
                <g transform="translate(392, 132)">
                  <rect x="0" y="0" width="30" height="16" rx="4" class="fc-badge-yes" />
                  <text x="15" y="11" class="fc-badge-yes-text">Yes</text>
                </g>

                <!-- No badge: going left to End -->
                <g transform="translate(182, 182)">
                  <rect x="0" y="0" width="28" height="16" rx="4" class="fc-badge-no" />
                  <text x="14" y="11" class="fc-badge-no-text">No</text>
                </g>

                <!-- Annotations -->
                <text x="202" y="66" class="fc-loopback-hint">→ body executes first</text>
                <text x="486" y="140" class="fc-loopback-hint" style="font-size:8px;fill:#94a3b8;text-anchor:middle">loop</text>
                <text x="486" y="150" class="fc-loopback-hint" style="font-size:8px;fill:#94a3b8;text-anchor:middle">back</text>
              </svg>
            </div>

            <div class="ll-outbox">
              <span class="ll-outlabel">Output:</span>
              <span v-for="(v, i) in s.out" :key="i" class="ll-outv">{{ v }}</span>
            </div>
          </div>
        </div>
        <div class="ll-vresizer" ref="vizResizerRef"></div>

        <!-- LEGEND -->
        <div class="ll-legend">
          <span class="ll-leg"><span class="ll-legdot ll-legdot-existing"></span>step / decision</span>
          <span class="ll-leg"><span class="ll-legdot ll-legdot-cur"></span>currently executing</span>
          <span class="ll-leg"><span class="fc-leg-edge"></span>active flow</span>
        </div>

        <!-- VAR FRAMES -->
        <div class="ll-table-area" :style="{ height: tableHeight + 'px' }">
          <div class="ll-table-title">Variable frame — innermost = current</div>
          <div class="ll-stack-line">
            <template v-if="s.vars && s.vars.length">
              <div
                v-for="(f, depth) in s.vars"
                :key="depth"
                class="ll-frame"
                :class="{ 'll-frame-cur': depth === s.vars.length - 1 }"
                :style="{ marginLeft: depth * 14 + 'px' }"
              >
                {{ f.title }}(<span v-for="(r, i) in f.rows" :key="i">
                  <span v-if="i > 0">, </span>
                  <span class="ll-fname">{{ r[0] }}</span>=<span
                    :class="r[2] ? 'll-c-blue' : (depth === s.vars.length - 1 ? 'll-c-orange' : 'll-c-green')"
                    style="font-weight:700"
                  >{{ r[1] }}</span>
                </span>)<span v-if="depth === s.vars.length - 1" class="ll-now"> ◄ current</span>
              </div>
            </template>
            <template v-else>—</template>
          </div>
        </div>
        <div class="ll-vresizer" ref="tableResizerRef"></div>

        <!-- BADGE -->
        <div class="ll-badge-wrap">
          <div class="ll-badge">{{ s.badge }}</div>
        </div>
      </div>

      <div class="ll-resizer" ref="hResizerRef"></div>

      <!-- CODE PANEL -->
      <div class="ll-right-col">
        <div class="ll-code-panel">
          <div class="ll-code-header">
            <select v-model="lang" class="ll-lang-select">
              <option value="java">Java</option>
              <option value="c">C</option>
              <option value="cpp">C++</option>
              <option value="python">Python</option>
            </select>
            <button class="ll-reset-btn" @click="resetCode">↺ Reset</button>
          </div>
          <div class="ll-code-scroll">
            <pre class="ll-pre"><span
              v-for="(line, i) in codeLines"
              :key="i"
              class="ll-codeline"
              :class="{ 'll-hl': isLineActive(line[0], s.code) }"
            >{{ line[1] === '' ? ' ' : line[1] }}
</span></pre>
          </div>
        </div>
      </div>
    </div>

    <!-- FOOTER -->
    <div class="ll-footer">
      Step {{ si + 1 }} / {{ steps.length }}
      <span class="ll-speed-wrap">
        Speed
        <input type="range" min="100" max="2000" step="100" v-model.number="speed" />
      </span>
    </div>
  </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.ll-root * {
  box-sizing: border-box;
}
.ll-root {
  --coral: #F04D4D;
  --coral-dark: #d93e3e;
  --coral-light: #fff0f0;
  --bg: #f5f6fa;
  --surface: #ffffff;
  --surface2: #f1f4f9;
  --border: #e2e8f0;
  --border2: #cbd5e1;
  --text: #1e293b;
  --text2: #475569;
  --muted: #94a3b8;
  --blue: #3b82f6;
  --blue-light: #eff6ff;
  --green: #22c55e;
  --green-light: #f0fdf4;
  --orange: #f97316;
  --orange-light: #fff7ed;
  --node: #1d4ed8;
  --nodeNew: #15803d;
  --nodeCur: #c2410c;
  --shadow-sm: 0 1px 3px rgba(0,0,0,.08), 0 1px 2px rgba(0,0,0,.04);
  --radius: 8px;
  --radius-sm: 6px;

  background: var(--bg);
  color: var(--text);
  font-family: 'Segoe UI', system-ui, sans-serif;
  font-size: 13px;
  display: flex;
  flex-direction: column;
  height: 50vh;
  min-height: 600px;
  overflow: hidden;
  width: 100%;
}

@keyframes ll-pop {
  from { transform: scale(.3); opacity: 0; }
  to { transform: scale(1); opacity: 1; }
}

.slide-wrapper {
  margin-top: -10px;
  margin-left: -30px;
  width: 107%;
  max-height: 100%;
  font-size: 0.8rem;
  font-weight: 400;
}
.slide-body {
  display: flex;
  flex-direction: column;
  border-radius: 4px;
  height: 100%;
}

.navbar {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: center;
  gap: 0.75rem;
  padding: 0 10px;
  background-color: #ffffff;
  position: fixed;
  width: 94.7%;
}

.navbar > img {
  height: 30px;
}

.navbar-title {
  margin: 0;
  font-size: 1.5rem;
  font-weight: 700;
  background-color: #ef5050;
  color: #ffffff;
  width: 80%;
  padding-left: 10px;
  margin-left: -10px;
  border-radius: 5px;
}
.row-main {
  width: 100%;
  height: 90%;
  margin-top: 37px;
  overflow-x: auto;
  overflow-y: auto;
  scrollbar-width: thin;
}

/* TOOLBAR */
.ll-toolbar {
  display: flex;
  align-items: center;
  gap: 8px;
  padding: 7px 16px;
  background: var(--surface);
  border-bottom: 1px solid var(--border);
  flex-shrink: 0;
  flex-wrap: wrap;
  box-shadow: var(--shadow-sm);
}
.ll-toolbar label {
  font-size: 11px;
  color: var(--muted);
  white-space: nowrap;
  font-weight: 500;
}
.ll-num-input {
  background: var(--surface);
  border: 1px solid var(--border2);
  color: var(--text);
  border-radius: var(--radius-sm);
  padding: 5px 8px;
  font-size: 13px;
  font-family: monospace;
  transition: border-color .15s;
  width: 60px;
}
.ll-num-input:focus {
  outline: none;
  border-color: var(--coral);
  box-shadow: 0 0 0 3px rgba(240,77,77,.1);
}
.ll-viz-btn {
  background: var(--coral);
  color: #fff;
  border: none;
  padding: 6px 16px;
  border-radius: var(--radius-sm);
  cursor: pointer;
  font-size: 12px;
  font-weight: 600;
  box-shadow: var(--shadow-sm);
  transition: filter .15s;
}
.ll-viz-btn:hover { filter: brightness(1.08); }

.ll-nav-controls {
  display: flex;
  margin-left: auto;
  align-items: center;
  gap: 4px;
  flex-shrink: 0;
}
.ll-nav-btn {
  background: var(--surface2);
  border: 1px solid var(--border2);
  color: var(--text2);
  padding: 5px 11px;
  border-radius: var(--radius-sm);
  cursor: pointer;
  font-size: 12px;
  font-weight: 500;
  transition: all .15s;
  white-space: nowrap;
}
.ll-nav-btn:hover {
  background: var(--surface);
  border-color: var(--coral);
  color: var(--coral);
}
.ll-play-btn {
  background: var(--blue-light);
  border: 1px solid var(--blue);
  color: var(--blue);
  min-width: 72px;
  font-weight: 600;
  padding: 5px 11px;
  border-radius: var(--radius-sm);
  cursor: pointer;
  font-size: 12px;
  transition: all .15s;
}
.ll-play-btn:hover {
  background: var(--blue);
  color: #fff;
}

/* MAIN LAYOUT */
.ll-main {
  display: flex;
  flex: 1;
  overflow: hidden;
  position: relative;
}
.ll-left-col {
  display: flex;
  flex-direction: column;
  overflow: hidden;
  min-width: 200px;
  max-width: 72%;
}
.ll-resizer {
  width: 5px;
  cursor: col-resize;
  background: var(--border);
  flex-shrink: 0;
  transition: background .15s;
  position: relative;
  z-index: 20;
}
.ll-resizer:hover,
.ll-resizer.drag {
  background: var(--coral);
}
.ll-right-col {
  display: flex;
  flex-direction: column;
  flex: 1;
  overflow: hidden;
  min-width: 200px;
  height: 78%;
}

/* VIZ AREA */
.ll-viz-wrap {
  flex-shrink: 0;
  background: var(--surface);
  border-bottom: 1px solid var(--border);
  position: relative;
  overflow: auto;
}
.ll-perm-area {
  display: flex;
  flex-direction: column;
  align-items: stretch;
  min-height: 100%;
}
.ll-ptrs {
  display: flex;
  gap: 8px;
  flex-wrap: wrap;
  padding: 6px 14px 2px;
  min-height: 28px;
}
.ll-ptr-chip {
  background: var(--surface2);
  border: 1px solid var(--border);
  border-radius: var(--radius-sm);
  padding: 2px 8px;
  font-size: 11.5px;
  font-family: monospace;
  box-shadow: var(--shadow-sm);
  align-self: flex-start;
}
.ll-c-blue { color: var(--blue); }
.ll-c-orange { color: var(--orange); }
.ll-c-green { color: var(--green); }

.ll-outbox {
  margin: 2px 14px 6px;
  background: var(--surface2);
  border: 1px solid var(--border);
  border-radius: var(--radius-sm);
  padding: 5px 12px;
  font-family: 'Consolas', monospace;
  font-size: 13.5px;
  min-height: 30px;
  display: flex;
  align-items: center;
  gap: 4px;
  width: calc(100% - 28px);
}
.ll-outlabel {
  color: var(--muted);
  font-size: 11px;
  margin-right: 6px;
  font-weight: 500;
}
.ll-outv {
  color: var(--text);
  font-weight: 500;
  margin-right: 8px;
  animation: ll-pop .3s ease;
  font-size: 0.7rem;
}

/* FLOWCHART */
.ll-flow-wrap {
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 2px 10px 4px;
  background: #ffffff;
  border-radius: 8px;
}
.fc-svg {
  width: 100%;
  max-width: 540px;
  max-height: 245px;
  height: auto;
  display: block;
  overflow: visible;
}

/* Shapes & Colors */
.fc-shape {
  fill: #ffffff;
  stroke: #cbd5e1;
  stroke-width: 2;
  transition: fill .25s ease, stroke .25s ease, filter .25s ease;
  filter: drop-shadow(0 1px 2px rgba(15, 23, 42, 0.06));
}
.fc-shape-term {
  stroke: #64748b;
  fill: #f8fafc;
}
.fc-shape-init {
  stroke: #3b82f6;
  fill: #eff6ff;
}
.fc-shape-cond {
  stroke: #8b5cf6;
  fill: #f5f3ff;
}
.fc-shape-body {
  stroke: #22c55e;
  fill: #f0fdf4;
}
.fc-shape-incr {
  stroke: #f97316;
  fill: #fff7ed;
}

/* Typography inside Nodes */
.fc-label {
  font-family: 'Segoe UI', system-ui, sans-serif;
  font-size: 11.5px;
  font-weight: 700;
  fill: #1e293b;
  text-anchor: middle;
  pointer-events: none;
  transition: fill .25s;
}
.fc-label-sm {
  font-size: 11px;
}
.fc-sublabel {
  font-family: 'Segoe UI', system-ui, sans-serif;
  font-size: 8.5px;
  font-weight: 600;
  fill: #64748b;
  text-anchor: middle;
  pointer-events: none;
}
.font-mono {
  font-family: 'Fira Code', 'Consolas', monospace;
}
.font-bold {
  font-weight: 700;
}

/* Edges & Markers */
.fc-edge {
  fill: none;
  stroke: #cbd5e1;
  stroke-width: 2;
  stroke-linecap: round;
  stroke-linejoin: round;
  transition: stroke .2s;
}
.fc-arrowhead {
  fill: #94a3b8;
}
.fc-arrowhead-active {
  fill: #ef5050;
}

/* Branch Badges */
.fc-badge-yes {
  fill: #f0fff4;
  stroke: #86efac;
  stroke-width: 1.2;
}
.fc-badge-yes-text {
  font-family: 'Segoe UI', system-ui, sans-serif;
  font-size: 10px;
  font-weight: 700;
  fill: #16a34a;
  text-anchor: middle;
}

.fc-badge-no {
  fill: #fef2f2;
  stroke: #fca5a5;
  stroke-width: 1.2;
}
.fc-badge-no-text {
  font-family: 'Segoe UI', system-ui, sans-serif;
  font-size: 10px;
  font-weight: 700;
  fill: #dc2626;
  text-anchor: middle;
}

.fc-loopback-hint {
  font-family: 'Segoe UI', system-ui, sans-serif;
  font-size: 9.5px;
  font-weight: 600;
  fill: #94a3b8;
  text-anchor: middle;
}

/* Active Flow & Animated Edge */
.fc-edge-active {
  stroke: #ef5050;
  stroke-width: 2.5;
  stroke-dasharray: 6 4;
  animation: fc-flow .55s linear infinite;
}
@keyframes fc-flow {
  to { stroke-dashoffset: -20; }
}

/* Active Node Highlights */
.fc-node.fc-node-active .fc-shape {
  stroke-width: 2.8;
  filter: drop-shadow(0 0 4px rgba(99, 102, 241, 0.35));
}

.fc-node.node-start.fc-node-active .fc-shape { fill: #fee2e2; stroke: #ef4444; }
.fc-node.node-init.fc-node-active .fc-shape  { fill: #dbeafe; stroke: #2563eb; }
.fc-node.node-cond.fc-node-active .fc-shape  { fill: #ede9fe; stroke: #7c3aed; }
.fc-node.node-body.fc-node-active .fc-shape  { fill: #dcfce7; stroke: #16a34a; }
.fc-node.node-incr.fc-node-active .fc-shape  { fill: #ffedd5; stroke: #ea580c; }
.fc-node.node-end.fc-node-active .fc-shape   { fill: #fee2e2; stroke: #dc2626; }

.fc-node.fc-node-active .fc-label {
  fill: #0f172a !important;
  font-weight: 800;
}
.fc-node.fc-node-active .fc-sublabel {
  fill: #334155 !important;
  font-weight: 700;
}

.fc-node.fc-node-active {
  animation: fc-pulse 1.2s ease-in-out infinite;
}
@keyframes fc-pulse {
  0%, 100% { filter: drop-shadow(0 0 0 rgba(99,102,241,0)); }
  50% { filter: drop-shadow(0 0 4px rgba(99,102,241,.35)); }
}

.fc-leg-edge {
  width: 16px;
  height: 0;
  border-top: 2px dashed #ef5050;
  display: inline-block;
}

/* RESIZERS */
.ll-vresizer {
  height: 5px;
  cursor: row-resize;
  background: var(--border);
  flex-shrink: 0;
  transition: background .15s;
  position: relative;
  z-index: 20;
}
.ll-vresizer:hover,
.ll-vresizer.drag {
  background: var(--coral);
}

/* LEGEND */
.ll-legend {
  display: flex;
  flex-wrap: wrap;
  gap: 6px 14px;
  padding: 6px 12px;
  border-bottom: 1px solid var(--border);
  flex-shrink: 0;
  background: var(--surface2);
}
.ll-leg {
  display: flex;
  align-items: center;
  gap: 5px;
  font-size: 11px;
  color: var(--text2);
}
.ll-legdot {
  width: 11px;
  height: 11px;
  border-radius: 3px;
  flex-shrink: 0;
  display: inline-block;
}
.ll-legdot-existing {
  background: var(--node);
  border: 1.5px solid var(--blue);
}
.ll-legdot-cur {
  background: var(--nodeCur);
  border: 1.5px solid var(--orange);
}

/* VAR FRAMES */
.ll-table-area {
  flex-shrink: 0;
  padding: 8px 14px;
  border-bottom: 1px solid var(--border);
  overflow: auto;
  background: var(--surface);
}
.ll-table-title {
  font-size: 10px;
  color: var(--muted);
  margin-bottom: 4px;
  font-style: italic;
}
.ll-stack-line {
  font-family: 'Consolas', monospace;
  font-size: 12px;
  line-height: 1.8;
}
.ll-frame {
  font-family: 'Consolas', monospace;
  font-size: 11.5px;
  color: var(--text2);
  padding: 1px 0;
  white-space: nowrap;
}
.ll-frame-cur {
  color: var(--orange);
  background: var(--orange-light);
  border-radius: 4px;
  padding: 1px 5px;
}
.ll-fname { color: var(--text2); }
.ll-now {
  color: var(--orange);
  font-size: 10px;
  margin-left: 6px;
}

/* BADGE */
.ll-badge-wrap {
  padding: 6px 10px;
  border-bottom: 1px solid var(--border);
  flex-shrink: 0;
  min-height: 36px;
  display: flex;
  align-items: center;
  background: var(--surface);
}
.ll-badge {
  display: inline-block;
  padding: 4px 12px;
  border-radius: var(--radius-sm);
  border-left: 3px solid var(--coral);
  background: var(--coral-light);
  font-size: 11px;
  color: var(--coral-dark);
  line-height: 1.4;
  word-break: break-word;
  font-weight: 500;
}

/* CODE PANEL */
.ll-code-panel {
  display: flex;
  flex-direction: column;
  height: 100%;
  overflow: hidden;
}
.ll-code-header {
  display: flex;
  align-items: center;
  gap: 8px;
  padding: 8px 14px;
  background: var(--surface);
  border-bottom: 1px solid var(--border);
  flex-shrink: 0;
  box-shadow: var(--shadow-sm);
}
.ll-lang-select {
  background: var(--surface2);
  border: 1px solid var(--border2);
  color: var(--text);
  padding: 5px 28px 5px 10px;
  border-radius: var(--radius-sm);
  font-size: 12px;
  font-weight: 500;
  cursor: pointer;
  min-width: 110px;
  transition: border-color .15s;
  appearance: none;
  background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='10' height='6' viewBox='0 0 10 6'%3E%3Cpath d='M0 0l5 6 5-6z' fill='%2394a3b8'/%3E%3C/svg%3E");
  background-repeat: no-repeat;
  background-position: right 10px center;
}
.ll-lang-select:focus {
  outline: none;
  border-color: var(--coral);
  box-shadow: 0 0 0 3px rgba(240,77,77,.1);
}
.ll-reset-btn {
  margin-left: auto;
  background: var(--surface2);
  border: 1px solid var(--border2);
  color: var(--coral);
  padding: 5px 11px;
  border-radius: var(--radius-sm);
  cursor: pointer;
  font-size: 11px;
  font-weight: 500;
  transition: all .15s;
}
.ll-reset-btn:hover {
  background: var(--coral-light);
  border-color: var(--coral);
}
.ll-code-scroll {
  flex: 1;
  overflow: auto;
  padding: 14px 16px;
  background: #f8fafc;
}
.ll-pre {
  font-family: 'Cascadia Code', 'Fira Code', 'Consolas', monospace;
  font-size: 12px;
  line-height: 1.65;
  white-space: pre;
  color: var(--text);
  margin: 0;
}
.ll-codeline {
  display: block;
  margin: 0 -16px;
  padding: 0 16px;
}
.ll-hl {
  background: #dcfce7;
  color: #15803d;
  border-radius: 3px;
  border-left: 2px solid var(--green);
}

/* FOOTER */
.ll-footer {
  padding: 4px 16px;
  font-size: 11px;
  color: var(--muted);
  border-top: 1px solid var(--border);
  background: var(--surface);
  flex-shrink: 0;
  display: flex;
  align-items: center;
}
.ll-speed-wrap {
  display: flex;
  align-items: center;
  gap: 5px;
  margin-left: 16px;
}
.ll-speed-wrap input[type=range] {
  width: 90px;
  accent-color: var(--coral);
}
</style>
