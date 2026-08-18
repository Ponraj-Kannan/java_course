<script setup>
import { ref, reactive, computed, onMounted, onBeforeUnmount, watch } from 'vue';

const fmt = (a) => (a === null || a === undefined ? '—' : '' + a);

defineProps({
  topic: {
    type: String,
    default: 'Nested Loops',
  },
  subTopic: {
    type: String,
    default: '',
  }
});

const CODES = {
  java: [
    ['', 'import java.util.Scanner;'], ['', ''],
    ['', 'public class NestedLoopDemo {'],
    ['c_main', '    public static void main(String[] args) {'],
    ['c_scan', '        Scanner sc = new Scanner(System.in);'],
    ['c_rows', '        int rows = sc.nextInt();'],
    ['c_cols', '        int cols = sc.nextInt();'], ['', ''],
    ['c_for_i', '        for (int i = 1; i <= rows; i++) {'],
    ['c_for_j', '            for (int j = 1; j <= cols; j++) {'],
    ['c_body',  '                System.out.println(i + " x " + j + " = " + (i * j));'],
    ['',        '            }'],
    ['',        '        }'],
    ['c_exit',  '    }'], ['', '}'],
  ],
  c: [
    ['', '#include <stdio.h>'], ['', ''],
    ['c_main', 'int main() {'],
    ['c_scan', '    int rows, cols;'],
    [['c_rows', 'c_cols'], '    scanf("%d %d", &rows, &cols);'], ['', ''],
    ['c_for_i', '    for (int i = 1; i <= rows; i++) {'],
    ['c_for_j', '        for (int j = 1; j <= cols; j++) {'],
    ['c_body',  '            printf("%d x %d = %d\\n", i, j, i * j);'],
    ['',        '        }'],
    ['',        '    }'], ['', ''],
    ['c_exit',  '    return 0;'], ['', '}'],
  ],
  cpp: [
    ['', '#include <iostream>'], ['', 'using namespace std;'], ['', ''],
    ['c_main', 'int main() {'],
    ['c_scan', '    int rows, cols;'],
    [['c_rows', 'c_cols'], '    cin >> rows >> cols;'], ['', ''],
    ['c_for_i', '    for (int i = 1; i <= rows; i++) {'],
    ['c_for_j', '        for (int j = 1; j <= cols; j++) {'],
    ['c_body',  '            cout << i << " x " << j << " = " << (i * j) << endl;'],
    ['',        '        }'],
    ['',        '    }'], ['', ''],
    ['c_exit',  '    return 0;'], ['', '}'],
  ],
  python: [
    ['c_rows', 'rows = int(input())'],
    ['c_cols', 'cols = int(input())'], ['', ''],
    ['c_for_i', 'for i in range(1, rows + 1):'],
    ['c_for_j', '    for j in range(1, cols + 1):'],
    ['c_body',  '        print(f"{i} x {j} = {i * j}")'],
  ],
};

// ── flowchart geometry (clean 3-column nested-loop) ──────────
//  Left col  (x≈80):  Start → i=1 → i≤rows? → End (No straight down)
//  Centre col (x≈280): j=1 → j≤cols? → print → j++ → right-rail back
//  Right col  (x≈430): i++   (j≤cols? No exits right to here)
//  Bottom rail (y≈310):  i++ → left to x=15 → up to left tip of i≤rows?
const EDGES = [
  { id: 'e_start_init_i',  d: 'M 80,38 L 80,62' },
  { id: 'e_init_i_cond_i', d: 'M 80,96 L 80,123' },
  { id: 'e_cond_i_yes',    d: 'M 145,145 L 240,145' },
  { id: 'e_cond_i_no',     d: 'M 80,167 L 80,290' },
  { id: 'e_init_j_cond_j', d: 'M 290,161 L 290,203' },
  { id: 'e_cond_j_yes',    d: 'M 290,247 L 290,265' },
  { id: 'e_body_incr_j',   d: 'M 290,299 L 290,320' },
  { id: 'e_incr_j_loop',   d: 'M 240,336 L 185,336 L 185,225 L 225,225' },
  { id: 'e_cond_j_no',     d: 'M 355,225 L 400,225' },
  { id: 'e_incr_i_loop',   d: 'M 450,241 L 450,375 L 15,375 L 15,145' },
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

function buildSteps(numRows, numCols) {
  const steps = [];
  const rS = '' + numRows;
  const cS = '' + numCols;
  const baseRows = (iVal, jVal, prodVal) => [
    ['rows', rS],
    ['cols', cS],
    ['i', iVal === null ? '—' : '' + iVal, true],
    ['j', jVal === null ? '—' : '' + jVal, true],
    ['i * j', prodVal === null ? '—' : '' + prodVal, true],
  ];

  // 1. Enter main()
  steps.push({
    i: null, j: null, out: [], curVal: null,
    stage: 'start', edge: null,
    badge: 'main() → program execution starts',
    code: 'c_main',
    vars: [frame('main()', [['rows', '—'], ['cols', '—'], ['i', '—'], ['j', '—']])],
  });

  // 2. Scanner initialization
  steps.push({
    i: null, j: null, out: [], curVal: null,
    stage: 'start', edge: null,
    badge: 'Scanner sc = new Scanner(System.in) → initialize input reader',
    code: 'c_scan',
    vars: [frame('main()', [['rows', '—'], ['cols', '—'], ['i', '—'], ['j', '—']])],
  });

  // 3. Read rows
  steps.push({
    i: null, j: null, out: [], curVal: null,
    stage: 'start', edge: null,
    badge: 'int rows = sc.nextInt() → read rows = ' + numRows,
    code: 'c_rows',
    vars: [frame('main()', [['rows', rS], ['cols', '—'], ['i', '—'], ['j', '—']])],
  });

  // 4. Read cols
  steps.push({
    i: null, j: null, out: [], curVal: null,
    stage: 'start', edge: null,
    badge: 'int cols = sc.nextInt() → read cols = ' + numCols,
    code: 'c_cols',
    vars: [frame('main()', baseRows(null, null, null))],
  });

  let out = [];

  // Outer loop init
  let i = 1;
  steps.push({
    i, j: null, out: out.slice(), curVal: null,
    stage: 'init_i', edge: 'e_start_init_i',
    badge: 'Outer Loop: for (int i = 1; ...) → initialize row index i = ' + i,
    code: 'c_for_i',
    vars: [frame('main()', baseRows(i, null, null))],
  });

  let firstOuter = true;
  while (true) {
    const outerTrue = i <= numRows;
    steps.push({
      i, j: null, out: out.slice(), curVal: null,
      stage: 'cond_i', edge: firstOuter ? 'e_init_i_cond_i' : 'e_incr_i_loop',
      badge: 'Outer Check: i (' + i + ') <= rows (' + numRows + ') → ' + (outerTrue ? 'true → enter outer iteration' : 'false → exit outer loop'),
      code: 'c_for_i',
      vars: [frame('main()', baseRows(i, null, null))],
    });
    firstOuter = false;

    if (!outerTrue) {
      steps.push({
        i, j: null, out: out.slice(), curVal: null,
        stage: 'end', edge: 'e_cond_i_no',
        badge: 'Outer loop finished → control reaches End',
        code: 'c_exit', done: true,
        vars: [frame('main()', baseRows(i, null, null))],
      });
      break;
    }

    // Inner loop init
    let j = 1;
    steps.push({
      i, j, out: out.slice(), curVal: null,
      stage: 'init_j', edge: 'e_cond_i_yes',
      badge: 'Inner Loop: for (int j = 1; ...) → initialize column index j = ' + j,
      code: 'c_for_j',
      vars: [frame('main()', baseRows(i, j, null))],
    });

    let firstInner = true;
    while (true) {
      const innerTrue = j <= numCols;
      steps.push({
        i, j, out: out.slice(), curVal: null,
        stage: 'cond_j', edge: firstInner ? 'e_init_j_cond_j' : 'e_incr_j_loop',
        badge: 'Inner Check: j (' + j + ') <= cols (' + numCols + ') → ' + (innerTrue ? 'true → enter inner body' : 'false → finish row ' + i),
        code: 'c_for_j',
        vars: [frame('main()', baseRows(i, j, null))],
      });
      firstInner = false;

      if (!innerTrue) {
        // Inner loop finishes, transition to outer increment
        steps.push({
          i, j, out: out.slice(), curVal: null,
          stage: 'cond_j_no', edge: 'e_cond_j_no',
          badge: 'Inner loop complete for row ' + i + ' → advance outer loop',
          code: 'c_for_j',
          vars: [frame('main()', baseRows(i, j, null))],
        });
        break;
      }

      // Inner body execution
      const prod = i * j;
      const entry = i + ' x ' + j + ' = ' + prod;
      out = [...out, entry];
      steps.push({
        i, j, out: out.slice(), curVal: entry,
        stage: 'body', edge: 'e_cond_j_yes',
        badge: 'print: ' + entry + ' → output cell (' + i + ', ' + j + ')',
        code: 'c_body',
        vars: [frame('main()', baseRows(i, j, prod))],
      });

      // Inner increment
      const nextJ = j + 1;
      steps.push({
        i, j: nextJ, out: out.slice(), curVal: null,
        stage: 'incr_j', edge: 'e_body_incr_j',
        badge: 'j++ → column becomes ' + nextJ,
        code: 'c_for_j',
        vars: [frame('main()', baseRows(i, nextJ, null))],
      });
      j = nextJ;
    }

    // Outer increment
    const nextI = i + 1;
    steps.push({
      i: nextI, j: null, out: out.slice(), curVal: null,
      stage: 'incr_i', edge: null,
      badge: 'i++ → row index becomes ' + nextI,
      code: 'c_for_i',
      vars: [frame('main()', baseRows(nextI, null, null))],
    });
    i = nextI;
  }

  return { steps };
}

// ── reactive state ──────────────────────────────────────────────
const inpRows = ref(3);
const inpCols = ref(3);
const lang = ref('java');
const speed = ref(650);
const si = ref(0);
const playing = ref(false);
const vizHeight = ref(390);
const tableHeight = ref(60);
const leftWidth = ref(58);

const stepsData = reactive(buildSteps(3, 3));
const steps = computed(() => stepsData.steps);
const s = computed(() => steps.value[Math.max(0, Math.min(si.value, steps.value.length - 1))]);
const codeLines = computed(() => CODES[lang.value] || []);

let playTimer = null;

function applyInput() {
  const r = parseInt(inpRows.value, 10);
  const c = parseInt(inpCols.value, 10);
  if (isNaN(r) || isNaN(c) || r < 1 || c < 1) {
    alert('Enter valid positive numbers for rows and columns.');
    return;
  }
  if (r * c > 36) {
    alert('Keep total cell count to 36 or fewer for clear visualization.');
    return;
  }
  playing.value = false;
  inpRows.value = r;
  inpCols.value = c;
  const built = buildSteps(r, c);
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
      <label>Rows (i)</label>
      <input type="number" v-model="inpRows" class="ll-num-input" min="1" max="5" />
      <label>Cols (j)</label>
      <input type="number" v-model="inpCols" class="ll-num-input" min="1" max="5" />
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
              <div class="ll-ptr-chip">Outer: i = <b class="ll-c-blue">{{ fmt(s.i) }}</b></div>
              <div class="ll-ptr-chip">Inner: j = <b class="ll-c-purple">{{ fmt(s.j) }}</b></div>
              <div v-if="s.curVal !== null && s.curVal !== undefined" class="ll-ptr-chip">
                output: <b class="ll-c-orange">{{ s.curVal }}</b>
              </div>
            </div>

            <!-- FLOWCHART -->
            <div class="ll-flow-wrap">
              <svg viewBox="0 0 560 390" class="fc-svg" xmlns="http://www.w3.org/2000/svg">
                <defs>
                  <marker id="nlfc-arrow" viewBox="0 0 10 10" refX="9" refY="5" markerWidth="6" markerHeight="6" orient="auto-start-reverse">
                    <path d="M 0 1.5 L 9 5 L 0 8.5 z" class="fc-arrowhead" />
                  </marker>
                  <marker id="nlfc-arrow-active" viewBox="0 0 10 10" refX="9" refY="5" markerWidth="7" markerHeight="7" orient="auto-start-reverse">
                    <path d="M 0 0.5 L 9 5 L 0 9.5 z" class="fc-arrowhead-active" />
                  </marker>
                </defs>

                <!-- LEFT COL: Start -->
                <g class="fc-node node-start" :class="{ 'fc-node-active': s.stage === 'start' }">
                  <rect x="35" y="10" width="90" height="28" rx="14" class="fc-shape fc-shape-term" />
                  <text x="80" y="27" class="fc-label">Start</text>
                </g>

                <!-- LEFT COL: i = 1 -->
                <g class="fc-node node-init-i" :class="{ 'fc-node-active': s.stage === 'init_i' }">
                  <rect x="30" y="62" width="100" height="34" rx="7" class="fc-shape fc-shape-init" />
                  <text x="80" y="78" class="fc-label font-mono">i = 1</text>
                  <text x="80" y="89" class="fc-sublabel">init outer row</text>
                </g>

                <!-- LEFT COL: Outer condition i <= rows -->
                <g class="fc-node node-cond-i" :class="{ 'fc-node-active': s.stage === 'cond_i' }">
                  <polygon points="80,123  145,145  80,167  15,145" class="fc-shape fc-shape-cond" />
                  <text x="80" y="142" class="fc-label fc-label-sm font-mono font-bold">i &lt;= rows ?</text>
                  <text x="80" y="154" class="fc-sublabel">outer check</text>
                </g>

                <!-- LEFT COL: End (No → straight down) -->
                <g class="fc-node node-end" :class="{ 'fc-node-active': s.stage === 'end' }">
                  <rect x="35" y="290" width="90" height="28" rx="14" class="fc-shape fc-shape-term" />
                  <text x="80" y="307" class="fc-label">End</text>
                </g>

                <!-- CENTRE COL: j = 1 (centre-y aligned with i<=rows? right tip at y=145) -->
                <g class="fc-node node-init-j" :class="{ 'fc-node-active': s.stage === 'init_j' }">
                  <rect x="240" y="129" width="100" height="32" rx="7" class="fc-shape fc-shape-init" />
                  <text x="290" y="145" class="fc-label font-mono">j = 1</text>
                  <text x="290" y="155" class="fc-sublabel">init inner col</text>
                </g>

                <!-- CENTRE COL: Inner condition j <= cols -->
                <g class="fc-node node-cond-j" :class="{ 'fc-node-active': s.stage === 'cond_j' }">
                  <polygon points="290,203  355,225  290,247  225,225" class="fc-shape fc-shape-cond" />
                  <text x="290" y="222" class="fc-label fc-label-sm font-mono font-bold">j &lt;= cols ?</text>
                  <text x="290" y="234" class="fc-sublabel">inner check</text>
                </g>

                <!-- CENTRE COL: print(i * j) -->
                <g class="fc-node node-body" :class="{ 'fc-node-active': s.stage === 'body' }">
                  <rect x="240" y="265" width="100" height="34" rx="7" class="fc-shape fc-shape-body" />
                  <text x="290" y="281" class="fc-label font-mono font-bold">print(i * j)</text>
                  <text x="290" y="292" class="fc-sublabel">inner body</text>
                </g>

                <!-- CENTRE COL: j++ -->
                <g class="fc-node node-incr-j" :class="{ 'fc-node-active': s.stage === 'incr_j' }">
                  <rect x="240" y="320" width="100" height="32" rx="7" class="fc-shape fc-shape-incr" />
                  <text x="290" y="336" class="fc-label font-mono font-bold">j++</text>
                  <text x="290" y="346" class="fc-sublabel">inner incr</text>
                </g>

                <!-- RIGHT COL: i++ (centre-y aligned with j<=cols? right tip at y=225) -->
                <g class="fc-node node-incr-i" :class="{ 'fc-node-active': s.stage === 'incr_i' }">
                  <rect x="400" y="209" width="110" height="32" rx="7" class="fc-shape fc-shape-incr" />
                  <text x="455" y="225" class="fc-label font-mono font-bold">i++</text>
                  <text x="455" y="235" class="fc-sublabel">outer incr</text>
                </g>

                <!-- edges -->
                <path
                  v-for="edge in EDGES"
                  :key="edge.id"
                  :d="edge.d"
                  class="fc-edge"
                  :class="{ 'fc-edge-active': s.edge === edge.id }"
                  :marker-end="s.edge === edge.id ? 'url(#nlfc-arrow-active)' : 'url(#nlfc-arrow)'"
                />

                <!-- Outer Yes badge (i<=rows? → j=1) -->
                <g transform="translate(152, 126)">
                  <rect x="0" y="0" width="30" height="16" rx="4" class="fc-badge-yes" />
                  <text x="15" y="11" class="fc-badge-yes-text">Yes</text>
                </g>

                <!-- Outer No badge (i<=rows? → End, straight down) -->
                <g transform="translate(84, 174)">
                  <rect x="0" y="0" width="28" height="16" rx="4" class="fc-badge-no" />
                  <text x="14" y="11" class="fc-badge-no-text">No</text>
                </g>

                <!-- Inner Yes badge (j<=cols? → print) -->
                <g transform="translate(294, 249)">
                  <rect x="0" y="0" width="30" height="16" rx="4" class="fc-badge-yes" />
                  <text x="15" y="11" class="fc-badge-yes-text">Yes</text>
                </g>

                <!-- Inner No badge (j<=cols? → i++, going right) -->
                <g transform="translate(358, 207)">
                  <rect x="0" y="0" width="28" height="16" rx="4" class="fc-badge-no" />
                  <text x="14" y="11" class="fc-badge-no-text">No</text>
                </g>
              </svg>
            </div>

            <div class="ll-outbox ll-outbox-grid">
              <span class="ll-outlabel">Output Grid:</span>
              <div class="ll-grid-wrap">
                <span v-for="(v, idx) in s.out" :key="idx" class="ll-outv-chip">{{ v }}</span>
              </div>
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
              >
                {{ f.title }}(<span v-for="(r, i) in f.rows" :key="i">
                  <span v-if="i > 0">, </span>
                  <span class="ll-fname">{{ r[0] }}</span>=<span
                    :class="r[2] ? 'll-c-blue' : 'll-c-orange'"
                    style="font-weight:700"
                  >{{ r[1] }}</span>
                </span>)
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
  --purple: #8b5cf6;
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
  width: 55px;
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
.ll-c-purple { color: var(--purple); }
.ll-c-orange { color: var(--orange); }
.ll-c-green { color: var(--green); }

.ll-outbox {
  margin: 2px 14px 6px;
  background: var(--surface2);
  border: 1px solid var(--border);
  border-radius: var(--radius-sm);
  padding: 5px 12px;
  font-family: 'Consolas', monospace;
  font-size: 12.5px;
  min-height: 30px;
  display: flex;
  align-items: center;
  gap: 6px;
  width: calc(100% - 28px);
}
.ll-outbox-grid {
  flex-direction: column;
  align-items: flex-start;
}
.ll-grid-wrap {
  display: flex;
  flex-wrap: wrap;
  gap: 6px;
}
.ll-outv-chip {
  background: #ffffff;
  border: 1px solid var(--border);
  padding: 2px 6px;
  border-radius: 4px;
  font-weight: 500;
  color: var(--green);
  animation: ll-pop .3s ease;
  font-size: 0.7rem;
}
.ll-outlabel {
  color: var(--muted);
  font-size: 11px;
  font-weight: 500;
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
  max-width: 560px;
  max-height: 395px;
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
  font-size: 11px;
  font-weight: 700;
  fill: #1e293b;
  text-anchor: middle;
  pointer-events: none;
  transition: fill .25s;
}
.fc-label-sm {
  font-size: 10px;
}
.fc-sublabel {
  font-family: 'Segoe UI', system-ui, sans-serif;
  font-size: 8px;
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
  font-size: 9.5px;
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
  font-size: 9.5px;
  font-weight: 700;
  fill: #dc2626;
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
.fc-node.node-init-i.fc-node-active .fc-shape { fill: #dbeafe; stroke: #2563eb; }
.fc-node.node-cond-i.fc-node-active .fc-shape { fill: #ede9fe; stroke: #7c3aed; }
.fc-node.node-init-j.fc-node-active .fc-shape { fill: #dbeafe; stroke: #2563eb; }
.fc-node.node-cond-j.fc-node-active .fc-shape { fill: #ede9fe; stroke: #7c3aed; }
.fc-node.node-body.fc-node-active .fc-shape   { fill: #dcfce7; stroke: #16a34a; }
.fc-node.node-incr-j.fc-node-active .fc-shape { fill: #ffedd5; stroke: #ea580c; }
.fc-node.node-incr-i.fc-node-active .fc-shape { fill: #ffedd5; stroke: #ea580c; }
.fc-node.node-end.fc-node-active .fc-shape    { fill: #fee2e2; stroke: #dc2626; }

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
