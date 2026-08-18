---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 13 — WHY/WHEN TO USE RECURSION
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Recursion">
  <template #content>

<div class="slide-h1" style="margin-bottom:10px;">When to <span class="highlight">Use Recursion</span> vs Iteration</div>

<div class="g2" style="gap:14px;align-items:start;">

<div class="flex-col">

  <div v-click class="section-label">Recursion Naturally Fits These Problems</div>

  <div style="display:flex;flex-direction:column;gap:6px;">
    <div v-click class="card" style="display:flex;gap:8px;align-items:center;border:1px solid var(--blue);">
      <span class="pill pill-blue" style="flex-shrink:0;min-width:70px;text-align:center;">Tree</span>
      <div class="body-text">Tree traversal — left subtree, right subtree each recursively solved</div>
    </div>
    <div v-click class="card" style="display:flex;gap:8px;align-items:center;border:1px solid var(--green);">
      <span class="pill pill-green" style="flex-shrink:0;min-width:70px;text-align:center;">D&amp;C</span>
      <div class="body-text">Divide and Conquer — Merge Sort, Quick Sort, Binary Search</div>
    </div>
    <div v-click class="card" style="display:flex;gap:8px;align-items:center;border:1px solid var(--purple);">
      <span class="pill pill-purple" style="flex-shrink:0;min-width:70px;text-align:center;">Math</span>
      <div class="body-text">Mathematical sequences — factorial, Fibonacci, power, GCD</div>
    </div>
    <div v-click class="card" style="display:flex;gap:8px;align-items:center;border:1px solid var(--orange);">
      <span class="pill pill-orange" style="flex-shrink:0;min-width:70px;text-align:center;">Backtrack</span>
      <div class="body-text">Backtracking problems — N-Queens, Sudoku solver, maze traversal</div>
    </div>
  </div>

  <div v-click class="callout callout-success" style="margin-top:4px;">
    <div><strong>Ask yourself:</strong> "Can this problem be expressed as a smaller version of itself?" If yes, recursion is a natural fit.</div>
  </div>

</div>

<div class="flex-col">

  <div v-click class="section-label">Use Iteration Instead When…</div>

  <div style="display:flex;flex-direction:column;gap:6px;">
    <div v-click class="card" style="display:flex;gap:8px;align-items:center;border:1px solid var(--red);">
      <span class="pill pill-red" style="flex-shrink:0;min-width:70px;text-align:center;">Simple</span>
      <div class="body-text">Simple counting, summing, or printing — a loop is clearer and faster</div>
    </div>
    <div v-click class="card" style="display:flex;gap:8px;align-items:center;border:1px solid var(--red);">
      <span class="pill pill-red" style="flex-shrink:0;min-width:70px;text-align:center;">Large n</span>
      <div class="body-text">Input could be very large — recursion risks StackOverflowError</div>
    </div>
    <div v-click class="card" style="display:flex;gap:8px;align-items:center;border:1px solid var(--red);">
      <span class="pill pill-red" style="flex-shrink:0;min-width:70px;text-align:center;">Perf</span>
      <div class="body-text">Performance-critical code — iteration avoids method call overhead</div>
    </div>
  </div>

  <div v-click class="section-label" style="margin-top:8px;">Decision Flow</div>

  <div v-after class="step-flow" style="flex-wrap:wrap;">
    <div class="step-box active">Problem self-similar?</div>
    <div class="step-arrow">→</div>
    <div class="step-box" style="border-color:var(--green);background:#f0fff4;color:var(--green);">YES → Use Recursion</div>
    <div class="step-arrow">|</div>
    <div class="step-box" style="border-color:var(--orange);background:#fffaf0;color:var(--orange);">NO → Use a Loop</div>
  </div>

  <div v-click class="callout callout-warn" style="margin-top:6px;font-size:.7rem;">
    <div>In Java, recursion and loops are interchangeable — every recursive method can be converted to an iterative one and vice versa, though some conversions are non-trivial.</div>
  </div>

</div>

</div>

  </template>
</Slide2>
