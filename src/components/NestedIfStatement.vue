<script setup>
import { ref, reactive, computed, onMounted, onBeforeUnmount, watch } from 'vue';

const fmt = (a) => (a === null || a === undefined ? '—' : '' + a);

defineProps({
  topic: {
    type: String,
    default: 'Decision-making statements',
  },
  subTopic: {
    type: String,
    default: '',
  }
});

const CODES = {
  java: [
    ['', 'import java.util.Scanner;'], ['', ''],
    ['', 'public class LoanApproval {'],
    ['c_main', '    public static void main(String[] args) {'],
    ['c_scan', '        Scanner sc = new Scanner(System.in);'],
    ['c_init', '        int age = sc.nextInt();'],
    ['c_init', '        double salary = sc.nextDouble();'], ['', ''],
    ['c_if_outer', '        if (age >= 21) {'],
    ['c_if_inner', '            if (salary >= 30000) {'],
    ['c_approved', '                System.out.println("Loan Approved!");'],
    ['c_else_inner', '            } else {'],
    ['c_low_salary', '                System.out.println("Loan Denied: Salary too low.");'],
    ['', '            }'],
    ['c_else_outer', '        } else {'],
    ['c_underage', '            System.out.println("Loan Denied: Underage.");'],
    ['', '        }'],
    ['c_exit', '    }'], ['', '}'],
  ],
  c: [
    ['', '#include <stdio.h>'], ['', ''],
    ['c_main', 'int main() {'],
    ['c_scan', '    int age; double salary;'],
    ['c_init', '    scanf("%d %lf", &age, &salary);'], ['', ''],
    ['c_if_outer', '    if (age >= 21) {'],
    ['c_if_inner', '        if (salary >= 30000) {'],
    ['c_approved', '            printf("Loan Approved!\\n");'],
    ['c_else_inner', '        } else {'],
    ['c_low_salary', '            printf("Loan Denied: Salary too low.\\n");'],
    ['', '        }'],
    ['c_else_outer', '    } else {'],
    ['c_underage', '        printf("Loan Denied: Underage.\\n");'],
    ['', '    }'], ['', ''],
    ['c_exit', '    return 0;'], ['', '}'],
  ],
  cpp: [
    ['', '#include <iostream>'], ['', 'using namespace std;'], ['', ''],
    ['c_main', 'int main() {'],
    ['c_scan', '    int age; double salary;'],
    ['c_init', '    cin >> age >> salary;'], ['', ''],
    ['c_if_outer', '    if (age >= 21) {'],
    ['c_if_inner', '        if (salary >= 30000) {'],
    ['c_approved', '            cout << "Loan Approved!" << endl;'],
    ['c_else_inner', '        } else {'],
    ['c_low_salary', '            cout << "Loan Denied: Salary too low." << endl;'],
    ['', '        }'],
    ['c_else_outer', '    } else {'],
    ['c_underage', '        cout << "Loan Denied: Underage." << endl;'],
    ['', '    }'], ['', ''],
    ['c_exit', '    return 0;'], ['', '}'],
  ],
  python: [
    ['c_init', 'age = int(input())'],
    ['c_init', 'salary = float(input())'], ['', ''],
    ['c_if_outer', 'if age >= 21:'],
    ['c_if_inner', '    if salary >= 30000:'],
    ['c_approved', '        print("Loan Approved!")'],
    ['c_else_inner', '    else:'],
    ['c_low_salary', '        print("Loan Denied: Salary too low.")'],
    ['c_else_outer', 'else:'],
    ['c_underage', '    print("Loan Denied: Underage.")'],
  ],
};

// ── flowchart geometry (clean nested branching layout) ───────────
const EDGES = [
  { id: 'e_start_init', d: 'M 270,38 L 270,52' },
  { id: 'e_init_c_outer', d: 'M 270,86 L 270,102' },
  { id: 'e_outer_yes', d: 'M 195,124 L 180,124 L 180,168' },
  { id: 'e_outer_no', d: 'M 345,124 L 440,124 L 440,260' },
  { id: 'e_inner_yes', d: 'M 95,192 L 90,192 L 90,260' },
  { id: 'e_inner_no', d: 'M 265,192 L 270,192 L 270,260' },
  { id: 'e_app_end', d: 'M 90,296 L 90,322 L 270,322 L 270,345' },
  { id: 'e_sal_end', d: 'M 270,296 L 270,345' },
  { id: 'e_und_end', d: 'M 440,296 L 440,322 L 270,322 L 270,345' },
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

function buildSteps(ageVal, salaryVal) {
  const steps = [];
  const aV = '' + ageVal;
  const sV = '' + salaryVal;

  // 1. Enter main()
  steps.push({
    age: null, salary: null, out: [], curVal: null,
    stage: 'start', edge: null,
    badge: 'main() → program execution starts',
    code: 'c_main',
    vars: [frame('main()', [['age', '—'], ['salary', '—']])],
  });

  // 2. Scanner init
  steps.push({
    age: null, salary: null, out: [], curVal: null,
    stage: 'start', edge: null,
    badge: 'Scanner sc = new Scanner(System.in) → initialize input reader',
    code: 'c_scan',
    vars: [frame('main()', [['age', '—'], ['salary', '—']])],
  });

  // 3. Read inputs
  steps.push({
    age: ageVal, salary: salaryVal, out: [], curVal: null,
    stage: 'init', edge: 'e_start_init',
    badge: 'Read inputs: age = ' + ageVal + ', salary = ' + salaryVal,
    code: 'c_init',
    vars: [frame('main()', [['age', aV], ['salary', sV]])],
  });

  // 4. Outer condition: age >= 21 ?
  const ageOk = ageVal >= 21;
  steps.push({
    age: ageVal, salary: salaryVal, out: [], curVal: null,
    stage: 'cond_outer', edge: 'e_init_c_outer',
    badge: 'if (age >= 21) → ' + ageVal + ' >= 21 (' + (ageOk ? 'true → enter outer if' : 'false → jump to outer else') + ')',
    code: 'c_if_outer',
    vars: [frame('main()', [['age', aV], ['salary', sV], ['age >= 21', ageOk ? 'true' : 'false', true]])],
  });

  if (ageOk) {
    // 5a. Inner condition: salary >= 30000 ?
    const salOk = salaryVal >= 30000;
    steps.push({
      age: ageVal, salary: salaryVal, out: [], curVal: null,
      stage: 'cond_inner', edge: 'e_outer_yes',
      badge: 'if (salary >= 30000) → ' + salaryVal + ' >= 30000 (' + (salOk ? 'true → Approved' : 'false → Denied: Low Salary') + ')',
      code: 'c_if_inner',
      vars: [frame('main()', [
        ['age', aV],
        ['salary', sV],
        ['age >= 21', 'true'],
        ['salary >= 30000', salOk ? 'true' : 'false', true]
      ])],
    });

    if (salOk) {
      // 6a. Loan Approved
      const outStr = 'Loan Approved!';
      steps.push({
        age: ageVal, salary: salaryVal, out: [outStr], curVal: outStr,
        stage: 'approved', edge: 'e_inner_yes',
        badge: 'Execute inner if: print("Loan Approved!")',
        code: 'c_approved',
        vars: [frame('main()', [['age', aV], ['salary', sV], ['status', '"Approved"']])],
      });

      // 7a. End
      steps.push({
        age: ageVal, salary: salaryVal, out: [outStr], curVal: null,
        stage: 'end', edge: 'e_app_end',
        badge: 'Program execution completed successfully.',
        code: 'c_exit', done: true,
        vars: [frame('main()', [['age', aV], ['salary', sV]])],
      });
    } else {
      // 6b. Denied: Salary too low
      const outStr = 'Loan Denied: Salary too low.';
      steps.push({
        age: ageVal, salary: salaryVal, out: [outStr], curVal: outStr,
        stage: 'low_salary', edge: 'e_inner_no',
        badge: 'Execute inner else: print("Loan Denied: Salary too low.")',
        code: 'c_low_salary',
        vars: [frame('main()', [['age', aV], ['salary', sV], ['status', '"Denied: Low Salary"']])],
      });

      // 7b. End
      steps.push({
        age: ageVal, salary: salaryVal, out: [outStr], curVal: null,
        stage: 'end', edge: 'e_sal_end',
        badge: 'Program execution completed.',
        code: 'c_exit', done: true,
        vars: [frame('main()', [['age', aV], ['salary', sV]])],
      });
    }
  } else {
    // 5b. Denied: Underage
    const outStr = 'Loan Denied: Underage.';
    steps.push({
      age: ageVal, salary: salaryVal, out: [outStr], curVal: outStr,
      stage: 'underage', edge: 'e_outer_no',
      badge: 'Execute outer else: print("Loan Denied: Underage.")',
      code: 'c_underage',
      vars: [frame('main()', [['age', aV], ['salary', sV], ['status', '"Denied: Underage"']])],
    });

    // 6c. End
    steps.push({
      age: ageVal, salary: salaryVal, out: [outStr], curVal: null,
      stage: 'end', edge: 'e_und_end',
      badge: 'Program execution completed.',
      code: 'c_exit', done: true,
      vars: [frame('main()', [['age', aV], ['salary', sV]])],
    });
  }

  return { steps };
}

// ── reactive state ──────────────────────────────────────────────
const inpAge = ref(25);
const inpSalary = ref(45000);
const lang = ref('java');
const speed = ref(650);
const si = ref(0);
const playing = ref(false);
const vizHeight = ref(440);
const tableHeight = ref(60);
const leftWidth = ref(58);

const stepsData = reactive(buildSteps(25, 45000));
const steps = computed(() => stepsData.steps);
const s = computed(() => steps.value[Math.max(0, Math.min(si.value, steps.value.length - 1))]);
const codeLines = computed(() => CODES[lang.value] || []);

let playTimer = null;

function applyInput() {
  const aVal = parseInt(inpAge.value, 10);
  const sVal = parseFloat(inpSalary.value);
  if (isNaN(aVal) || isNaN(sVal)) {
    alert('Please enter valid numbers for age and salary.');
    return;
  }
  playing.value = false;
  inpAge.value = aVal;
  inpSalary.value = sVal;
  const built = buildSteps(aVal, sVal);
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
  // read-only reset
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
  cleanupFns.push(initVResizer(vizResizerRef, vizHeight, 200, 600));
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
      <label>Age</label>
      <input type="number" v-model="inpAge" class="ll-num-input" style="width:58px" />
      <label>Salary</label>
      <input type="number" v-model="inpSalary" class="ll-num-input" style="width:80px" />
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
              <div class="ll-ptr-chip">age = <b class="ll-c-blue">{{ fmt(s.age) }}</b></div>
              <div class="ll-ptr-chip">salary = <b class="ll-c-purple">{{ fmt(s.salary) }}</b></div>
              <div v-if="s.age !== null" class="ll-ptr-chip">
                age &gt;= 21 : <b :class="s.age >= 21 ? 'll-c-green' : 'll-c-orange'">{{ s.age >= 21 ? 'true' : 'false' }}</b>
              </div>
              <div v-if="s.salary !== null && s.age >= 21" class="ll-ptr-chip">
                salary &gt;= 30k : <b :class="s.salary >= 30000 ? 'll-c-green' : 'll-c-orange'">{{ s.salary >= 30000 ? 'true' : 'false' }}</b>
              </div>
            </div>

            <!-- FLOWCHART -->
            <div class="ll-flow-wrap">
              <svg viewBox="0 0 540 400" class="fc-svg" xmlns="http://www.w3.org/2000/svg">
                <defs>
                  <marker id="nest-arrow" viewBox="0 0 10 10" refX="9" refY="5" markerWidth="6" markerHeight="6" orient="auto-start-reverse">
                    <path d="M 0 1.5 L 9 5 L 0 8.5 z" class="fc-arrowhead" />
                  </marker>
                  <marker id="nest-arrow-active" viewBox="0 0 10 10" refX="9" refY="5" markerWidth="7" markerHeight="7" orient="auto-start-reverse">
                    <path d="M 0 0.5 L 9 5 L 0 9.5 z" class="fc-arrowhead-active" />
                  </marker>
                </defs>

                <!-- Start -->
                <g class="fc-node node-start" :class="{ 'fc-node-active': s.stage === 'start' }">
                  <rect x="225" y="10" width="90" height="28" rx="14" class="fc-shape fc-shape-term" />
                  <text x="270" y="27" class="fc-label">Start</text>
                </g>

                <!-- Init inputs -->
                <g class="fc-node node-init" :class="{ 'fc-node-active': s.stage === 'init' }">
                  <rect x="165" y="52" width="210" height="34" rx="7" class="fc-shape fc-shape-init" />
                  <text x="270" y="68" class="fc-label font-mono">age = {{ inpAge }}, salary = {{ inpSalary }}</text>
                  <text x="270" y="79" class="fc-sublabel">read inputs</text>
                </g>

                <!-- Outer Condition: age >= 21 ? -->
                <g class="fc-node node-cond" :class="{ 'fc-node-active': s.stage === 'cond_outer' }">
                  <polygon points="270,102  345,124  270,146  195,124" class="fc-shape fc-shape-cond" />
                  <text x="270" y="121" class="fc-label fc-label-sm font-mono font-bold">age &gt;= 21 ?</text>
                  <text x="270" y="133" class="fc-sublabel">outer check</text>
                </g>

                <!-- Inner Condition: salary >= 30000 ? -->
                <g class="fc-node node-cond" :class="{ 'fc-node-active': s.stage === 'cond_inner' }">
                  <polygon points="180,168  265,192  180,216  95,192" class="fc-shape fc-shape-cond" />
                  <text x="180" y="189" class="fc-label fc-label-sm font-mono font-bold">salary &gt;= 30000 ?</text>
                  <text x="180" y="201" class="fc-sublabel">inner check</text>
                </g>

                <!-- Action 1: Loan Approved -->
                <g class="fc-node node-body" :class="{ 'fc-node-active': s.stage === 'approved' }">
                  <rect x="20" y="260" width="140" height="36" rx="7" class="fc-shape fc-shape-body" />
                  <text x="90" y="276" class="fc-label font-mono font-bold">print("Approved!")</text>
                  <text x="90" y="288" class="fc-sublabel">loan granted</text>
                </g>

                <!-- Action 2: Denied: Salary too low -->
                <g class="fc-node node-else" :class="{ 'fc-node-active': s.stage === 'low_salary' }">
                  <rect x="195" y="260" width="150" height="36" rx="7" class="fc-shape fc-shape-else" />
                  <text x="270" y="276" class="fc-label font-mono font-bold">print("Low Salary")</text>
                  <text x="270" y="288" class="fc-sublabel">denied: &lt; 30k</text>
                </g>

                <!-- Action 3: Denied: Underage -->
                <g class="fc-node node-else" :class="{ 'fc-node-active': s.stage === 'underage' }">
                  <rect x="365" y="260" width="150" height="36" rx="7" class="fc-shape fc-shape-else" />
                  <text x="440" y="276" class="fc-label font-mono font-bold">print("Underage")</text>
                  <text x="440" y="288" class="fc-sublabel">denied: &lt; 21</text>
                </g>

                <!-- End -->
                <g class="fc-node node-end" :class="{ 'fc-node-active': s.stage === 'end' }">
                  <rect x="225" y="345" width="90" height="28" rx="14" class="fc-shape fc-shape-term" />
                  <text x="270" y="363" class="fc-label">End</text>
                </g>

                <!-- Static Edges -->
                <path
                  v-for="edge in EDGES"
                  :key="edge.id"
                  :d="edge.d"
                  class="fc-edge"
                  marker-end="url(#nest-arrow)"
                />

                <!-- Active Animated Flow Edge (Rendered on top) -->
                <path
                  v-if="s.edge && EDGE_PATHS[s.edge]"
                  :d="EDGE_PATHS[s.edge]"
                  class="fc-edge fc-edge-active"
                  marker-end="url(#nest-arrow-active)"
                />

                <!-- Badges -->
                <g transform="translate(145, 106)">
                  <rect x="0" y="0" width="28" height="15" rx="3.5" class="fc-badge-yes" />
                  <text x="14" y="10.5" class="fc-badge-yes-text">Yes</text>
                </g>

                <g transform="translate(370, 106)">
                  <rect x="0" y="0" width="26" height="15" rx="3.5" class="fc-badge-no" />
                  <text x="13" y="10.5" class="fc-badge-no-text">No</text>
                </g>

                <g transform="translate(70, 174)">
                  <rect x="0" y="0" width="28" height="15" rx="3.5" class="fc-badge-yes" />
                  <text x="14" y="10.5" class="fc-badge-yes-text">Yes</text>
                </g>

                <g transform="translate(275, 174)">
                  <rect x="0" y="0" width="26" height="15" rx="3.5" class="fc-badge-no" />
                  <text x="13" y="10.5" class="fc-badge-no-text">No</text>
                </g>
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
          <span class="ll-leg"><span class="ll-legdot ll-legdot-existing"></span>decision / outcome</span>
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
  --purple-light: #f5f3ff;
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
  max-height: 400px;
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
.fc-shape-else {
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
  font-size: 8.5px;
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
  font-size: 8.5px;
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
.fc-node.node-init.fc-node-active .fc-shape  { fill: #dbeafe; stroke: #2563eb; }
.fc-node.node-cond.fc-node-active .fc-shape  { fill: #ede9fe; stroke: #7c3aed; }
.fc-node.node-body.fc-node-active .fc-shape  { fill: #dcfce7; stroke: #16a34a; }
.fc-node.node-else.fc-node-active .fc-shape  { fill: #ffedd5; stroke: #ea580c; }
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
