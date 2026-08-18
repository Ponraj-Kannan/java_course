---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 23 — SUMMARY: JAVA DATA TYPES
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Data Types">
  <template #content>

<div class="slide-h1" style="margin-bottom:10px;">Summary — Java <span class="highlight">Data Types</span></div>

<div class="g2" style="gap:14px;align-items:start;">

<div class="flex-col">

  <div v-click class="section-label">What We Covered</div>

  <div style="display:flex;flex-direction:column;gap:5px;">
    <div v-click style="display:flex;gap:8px;align-items:center;" class="card">
      <span class="pill pill-red" style="flex-shrink:0;">8 Primitives</span>
      <span style="font-size:.7rem;color:var(--slate);"><span class="mono">byte, short, int, long, float, double, char, boolean</span></span>
    </div>
    <div v-click style="display:flex;gap:8px;align-items:center;" class="card">
      <span class="pill pill-blue" style="flex-shrink:0;">Reference Types</span>
      <span style="font-size:.7rem;color:var(--slate);"><span class="mono">String</span>, Arrays, Classes, Interfaces — Store Heap addresses</span>
    </div>
    <div v-click style="display:flex;gap:8px;align-items:center;" class="card">
      <span class="pill pill-purple" style="flex-shrink:0;">Literals &amp; _</span>
      <span style="font-size:.7rem;color:var(--slate);">Constants, suffixes (<span class="mono">L</span>, <span class="mono">f</span>), and Java 7+ underscores (<span class="mono">1_000_000</span>)</span>
    </div>
    <div v-click style="display:flex;gap:8px;align-items:center;" class="card">
      <span class="pill pill-orange" style="flex-shrink:0;">Type Casting</span>
      <span style="font-size:.7rem;color:var(--slate);">Widening (implicit, safe) vs Narrowing (explicit <span class="mono">(type)</span>, truncation)</span>
    </div>
    <div v-click style="display:flex;gap:8px;align-items:center;" class="card">
      <span class="pill pill-green" style="flex-shrink:0;">Wrappers &amp; Auto</span>
      <span style="font-size:.7rem;color:var(--slate);"><span class="mono">Integer</span>, <span class="mono">Double</span> &amp; automatic Autoboxing / Unboxing</span>
    </div>
    <div v-click style="display:flex;gap:8px;align-items:center;" class="card">
      <span class="pill pill-navy" style="flex-shrink:0;">var Inference</span>
      <span style="font-size:.7rem;color:var(--slate);">Java 10+ local variable type inference (compile-time resolved)</span>
    </div>
  </div>

</div>

<div class="flex-col">

  <div v-click class="section-label">Key Exam Takeaways</div>

  <div style="display:flex;flex-direction:column;gap:5px;">
    <div v-click class="callout callout-info">
      <div>Primitives store raw values directly on Stack; Reference types store Heap memory pointers!</div>
    </div>
    <div v-click class="callout callout-danger">
      <div>Never unbox a <span class="mono">null</span> wrapper variable to avoid <span class="mono">NullPointerException</span>!</div>
    </div>
    <div v-click class="callout callout-warn">
      <div>Remember: Literal decimals default to <span class="mono">double</span> and literal integers default to <span class="mono">int</span> in Java.</div>
    </div>
  </div>

  <div v-click style="margin-top:6px;">
    <div class="section-label" style="margin-bottom:4px;">Widening Hierarchy Pipeline</div>
    <div class="step-flow">
      <div class="step-box active">byte</div>
      <div class="step-arrow">→</div>
      <div class="step-box active">short / char</div>
      <div class="step-arrow">→</div>
      <div class="step-box active">int</div>
      <div class="step-arrow">→</div>
      <div class="step-box active">long</div>
      <div class="step-arrow">→</div>
      <div class="step-box active">float</div>
      <div class="step-arrow">→</div>
      <div class="step-box active">double</div>
    </div>
  </div>

  <div v-click class="card-navy" style="margin-top:6px;border-radius:10px;">
    <div style="font-size:.78rem;line-height:1.5;color:var(--slate);">
      <strong style="color:var(--red);">Mastering Java Data Types:</strong> A strong understanding of primitives, memory allocation, and wrappers is essential for writing efficient, type-safe Java programs! ☕
    </div>
  </div>

</div>

</div>

  </template>
</Slide2>
