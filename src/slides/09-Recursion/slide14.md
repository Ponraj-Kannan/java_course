---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 14 — SUMMARY
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Recursion">
  <template #content>

<div class="slide-h1" style="margin-bottom:10px;">Summary — Java <span class="highlight">Recursion</span></div>

<div class="g2" style="gap:14px;align-items:start;">

<div class="flex-col">

  <div v-click class="section-label">What We Covered</div>

  <div style="display:flex;flex-direction:column;gap:5px;">
    <div v-click style="display:flex;gap:8px;align-items:center;" class="card">
      <span class="pill pill-blue" style="flex-shrink:0;">Recursion</span>
      <span style="font-size:.7rem;color:var(--slate);">A method calling itself to solve a smaller version of the same problem</span>
    </div>
    <div v-click style="display:flex;gap:8px;align-items:center;" class="card">
      <span class="pill pill-green" style="flex-shrink:0;">Base Case</span>
      <span style="font-size:.7rem;color:var(--slate);">Mandatory stopping condition — returns a direct value without another call</span>
    </div>
    <div v-click style="display:flex;gap:8px;align-items:center;" class="card">
      <span class="pill pill-red" style="flex-shrink:0;">Recursive Case</span>
      <span style="font-size:.7rem;color:var(--slate);">The call that reduces the problem toward the base case</span>
    </div>
    <div v-click style="display:flex;gap:8px;align-items:center;" class="card">
      <span class="pill pill-orange" style="flex-shrink:0;">Call Stack</span>
      <span style="font-size:.7rem;color:var(--slate);">Stack frames pushed on wind, popped and return values propagate on unwind</span>
    </div>
    <div v-click style="display:flex;gap:8px;align-items:center;" class="card">
      <span class="pill pill-purple" style="flex-shrink:0;">Direct / Indirect</span>
      <span style="font-size:.7rem;color:var(--slate);">Direct: A calls itself. Indirect: A calls B which calls A</span>
    </div>
  </div>

</div>

<div class="flex-col">

  <div v-click class="section-label">Key Exam Takeaways</div>

  <div style="display:flex;flex-direction:column;gap:5px;">
    <div v-click class="callout callout-info">
      <div>Every recursive Java method needs: a <strong>return type</strong>, a <strong>base case</strong>, and a <strong>recursive call with smaller input</strong>.</div>
    </div>
    <div v-click class="callout callout-danger">
      <div>Missing or unreachable base case → <strong>java.lang.StackOverflowError</strong> at runtime.</div>
    </div>
    <div v-click class="callout callout-warn">
      <div>Fibonacci with naive recursion has <strong>O(2ⁿ)</strong> time complexity — use iteration or memoization for large inputs.</div>
    </div>
    <div v-click class="callout callout-success">
      <div>Use <span class="mono">static</span> modifier for recursive helper methods called from <span class="mono">main()</span> without needing an object instance.</div>
    </div>
  </div>

  <div v-click class="card-navy" style="margin-top:6px;border-radius:10px;">
    <div style="font-size:.78rem;line-height:1.5;color:var(--slate);">
      <strong style="color:var(--red);">Mastering Java Recursion:</strong> Once you understand base case + recursive case + call stack, you unlock tree traversal, sorting algorithms, and divide-and-conquer — the building blocks of advanced Java programming. ☕
    </div>
  </div>

</div>

</div>

  </template>
</Slide2>
