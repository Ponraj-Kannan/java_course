---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 10 — ADVANTAGES & DISADVANTAGES
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Recursion">
  <template #content>

<div class="slide-h1" style="margin-bottom:12px;"><span class="highlight">Advantages</span> &amp; <span class="highlight">Disadvantages</span> of Recursion</div>

<div class="g2" style="gap:14px;align-items:start;">

<div class="flex-col">
  <div v-click class="section-label">Advantages</div>

  <div v-click class="card" style="display:flex;gap:10px;align-items:center;border:1px solid var(--green);">
    <div class="icon-circle ic-green">C</div>
    <div>
      <div class="slide-h3">Clean &amp; Elegant Code</div>
      <div class="small-text">Complex problems become short, readable, and mathematically clean.</div>
    </div>
  </div>

  <div v-click class="card" style="display:flex;gap:10px;align-items:center;border:1px solid var(--blue);">
    <div class="icon-circle ic-blue">S</div>
    <div>
      <div class="slide-h3">Solves Naturally Recursive Problems</div>
      <div class="small-text">Trees, graphs, and divide-and-conquer are naturally recursive in structure.</div>
    </div>
  </div>

  <div v-click class="card" style="display:flex;gap:10px;align-items:center;border:1px solid var(--purple);">
    <div class="icon-circle ic-purple">D</div>
    <div>
      <div class="slide-h3">Divide and Conquer</div>
      <div class="small-text">Break a big problem into identical smaller sub-problems effortlessly.</div>
    </div>
  </div>

  <div v-click class="card" style="display:flex;gap:10px;align-items:center;border:1px solid var(--orange);">
    <div class="icon-circle ic-orange">R</div>
    <div>
      <div class="slide-h3">Reduces Code Length</div>
      <div class="small-text">Tower of Hanoi needs ~3 lines recursively — dozens iteratively.</div>
    </div>
  </div>

</div>

<div class="flex-col">
  <div v-click class="section-label">Disadvantages</div>

  <div v-click class="card" style="display:flex;gap:10px;align-items:center;border:1px solid var(--red);">
    <div class="icon-circle ic-red">M</div>
    <div>
      <div class="slide-h3">High Memory Usage</div>
      <div class="small-text">Each call uses a stack frame. Deep recursion can consume significant JVM stack memory.</div>
    </div>
  </div>

  <div v-click class="card" style="display:flex;gap:10px;align-items:center;border:1px solid var(--orange);">
    <div class="icon-circle ic-orange">S</div>
    <div>
      <div class="slide-h3">StackOverflowError Risk</div>
      <div class="small-text">JVM stack has limited depth. Missing base case throws <span class="mono" style="font-size:.65rem;">StackOverflowError</span>.</div>
    </div>
  </div>

  <div v-click class="card" style="display:flex;gap:10px;align-items:center;border:1px solid var(--yellow);">
    <div class="icon-circle" style="background:#fefcbf;color:#b7791f;">T</div>
    <div>
      <div class="slide-h3">Repeated Calculations</div>
      <div class="small-text">Without memoization, Fibonacci recomputes same values many times — O(2ⁿ).</div>
    </div>
  </div>

  <div v-click class="card" style="display:flex;gap:10px;align-items:center;border:1px solid var(--purple);">
    <div class="icon-circle ic-purple">D</div>
    <div>
      <div class="slide-h3">Harder to Debug</div>
      <div class="small-text">Tracing multiple nested calls is more complex than stepping through a loop.</div>
    </div>
  </div>

</div>

</div>

  </template>
</Slide2>
