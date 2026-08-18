---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 19 — SUMMARY: JAVA OPERATORS
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Operators">
  <template #content>

<div class="slide-h1" style="margin-bottom:10px;">Summary — Java <span class="highlight">Operators</span></div>

<div class="g2" style="gap:14px;align-items:start;">

<div class="flex-col">

  <div v-click class="section-label">What We Covered</div>

  <div style="display:flex;flex-direction:column;gap:5px;">
    <div v-click style="display:flex;gap:8px;align-items:center;" class="card">
      <span class="pill pill-red" style="flex-shrink:0;">Arithmetic</span>
      <span style="font-size:.7rem;color:var(--slate);">+  −  *  /  %  — Math calculations &amp; division gotcha</span>
    </div>
    <div v-click style="display:flex;gap:8px;align-items:center;" class="card">
      <span class="pill pill-purple" style="flex-shrink:0;">Unary</span>
      <span style="font-size:.7rem;color:var(--slate);">+  −  ++  --  !  ~  — Prefix vs Postfix behavior</span>
    </div>
    <div v-click style="display:flex;gap:8px;align-items:center;" class="card">
      <span class="pill pill-blue" style="flex-shrink:0;">Assignment</span>
      <span style="font-size:.7rem;color:var(--slate);">=  +=  -=  *=  /=  %=  — Value updates &amp; shorthand</span>
    </div>
    <div v-click style="display:flex;gap:8px;align-items:center;" class="card">
      <span class="pill pill-orange" style="flex-shrink:0;">Relational</span>
      <span style="font-size:.7rem;color:var(--slate);">==  !=  &gt;  &lt;  &gt;=  &lt;=  — Comparisons (boolean result)</span>
    </div>
    <div v-click style="display:flex;gap:8px;align-items:center;" class="card">
      <span class="pill pill-green" style="flex-shrink:0;">Logical</span>
      <span style="font-size:.7rem;color:var(--slate);">&amp;&amp;  ||  !  — Combining boolean conditions &amp; short-circuit</span>
    </div>
    <div v-click style="display:flex;gap:8px;align-items:center;" class="card">
      <span class="pill pill-navy" style="flex-shrink:0;">Bitwise</span>
      <span style="font-size:.7rem;color:var(--slate);">&amp;  |  ^  ~  &lt;&lt;  &gt;&gt;  &gt;&gt;&gt;  — Bit manipulation &amp; unsigned shift</span>
    </div>
    <div v-click style="display:flex;gap:8px;align-items:center;" class="card">
      <span class="pill" style="background:#f0e6ff;color:#6b21a8;flex-shrink:0;">Special</span>
      <span style="font-size:.7rem;color:var(--slate);">instanceof  ? :  — Object type check &amp; inline decision</span>
    </div>
  </div>

</div>

<div class="flex-col">

  <div v-click class="section-label">Key Exam Takeaways</div>

  <div style="display:flex;flex-direction:column;gap:5px;">
    <div v-click class="callout callout-info">
      <div>Always use <span class="mono">()</span> parentheses to force evaluation order and avoid precedence confusion.</div>
    </div>
    <div v-click class="callout callout-danger">
      <div>Never confuse <span class="mono">=</span> (assignment) with <span class="mono">==</span> (comparison) or compare Strings with <span class="mono">==</span>!</div>
    </div>
    <div v-click class="callout callout-warn">
      <div>Remember: <span class="mono">7 / 2</span> equals <span class="mono">3</span> in Java! Cast to <span class="mono">double</span> (<span class="mono">7.0 / 2</span>) for decimals.</div>
    </div>
  </div>

  <div v-click style="margin-top:6px;">
    <div class="section-label" style="margin-bottom:4px;">Precedence Pipeline</div>
    <div class="step-flow">
      <div class="step-box active">( )</div>
      <div class="step-arrow">→</div>
      <div class="step-box active">++ --</div>
      <div class="step-arrow">→</div>
      <div class="step-box active">* / %</div>
      <div class="step-arrow">→</div>
      <div class="step-box active">+ -</div>
      <div class="step-arrow">→</div>
      <div class="step-box active">Comparisons</div>
      <div class="step-arrow">→</div>
      <div class="step-box active">&amp;&amp; ||</div>
    </div>
  </div>

  <div v-click class="card-navy" style="margin-top:6px;border-radius:10px;">
    <div style="font-size:.78rem;line-height:1.5;color:var(--slate);">
      <strong style="color:var(--red);">Mastering Java Operators:</strong> Every expression, condition, and loop in Java relies on operators. Solidify these foundational concepts for clean, bug-free Java code! ☕
    </div>
  </div>

</div>

</div>

  </template>
</Slide2>
