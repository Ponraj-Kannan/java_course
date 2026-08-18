---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 1 — INTRODUCTION TO DATA TYPES & JAVA TYPING SYSTEM
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Data Types">
  <template #content>

<div class="slide-h1" style="margin-bottom:10px;">Introduction to <span class="highlight">Data Types</span></div>

<div class="g2" style="gap:14px;align-items:start;">

<div class="flex-col">

  <div v-click class="card-navy" style="border-radius:10px;">
    <div style="font-size:.82rem;line-height:1.6;color:var(--slate);">
      <strong style="color:var(--red);">Definition:</strong> A <strong>data type</strong> specifies the size, layout, and valid range of values that a variable can store in memory, as well as the valid <strong>operations</strong> that can be performed on it.
    </div>
  </div>

  <div v-click class="callout callout-warn">
    <div><strong>Why Data Types Matter:</strong> You can add two numbers, but not a number and a word. Data types prevent invalid operations and optimize memory allocation.</div>
  </div>

  <div v-click style="background:#f6f8fa;border-radius:10px;border:1px solid #e1e4e8;padding:12px 14px;font-family:'Fira Code',monospace;font-size:.74rem;line-height:1.9;">
    <span style="color:#6b7280;">// Java requires explicit type declaration</span><br>
    <span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">age</span> = <span style="color:#b45309;">25</span>; &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#6b7280;">// Stores integer (4 bytes)</span><br>
    <span style="color:#ef5050;">double</span> <span style="color:#0e6ead;">pi</span> = <span style="color:#b45309;">3.14159</span>; &nbsp;&nbsp;&nbsp;<span style="color:#6b7280;">// Stores floating-point (8 bytes)</span><br>
    <span style="color:#0e6ead;">String</span> <span style="color:#0e6ead;">name</span> = <span style="color:#2d7a00;">"Alice"</span>; &nbsp;&nbsp;<span style="color:#6b7280;">// Stores reference to text object</span>
  </div>

</div>

<div class="flex-col">
  <div class="section-label" v-click>Java Typing System Characteristics</div>

  <div v-click class="card-red" style="border-radius:10px;padding:10px 14px;">
    <div style="font-size:.78rem;font-weight:700;color:var(--red-dark);margin-bottom:2px;">1. Statically Typed</div>
    <div style="font-size:.7rem;color:var(--slate);">
      All variable types must be declared and checked at <strong>compile-time</strong> before execution. Once declared, a variable cannot change its data type.
    </div>
  </div>

  <div v-click class="card-navy" style="border-radius:10px;padding:10px 14px;margin-top:4px;">
    <div style="font-size:.78rem;font-weight:700;color:var(--navy-mid);margin-bottom:2px;">2. Strongly Typed</div>
    <div style="font-size:.7rem;color:var(--slate);">
      Java enforces strict type checking. Incompatible types cannot be implicitly mixed without explicit conversion (e.g. assigning a <span class="mono">double</span> to an <span class="mono">int</span> causes a compile error).
    </div>
  </div>

  <div v-click class="callout callout-info" style="margin-top:6px;">
    <div><strong>Benefit:</strong> Static &amp; strong typing catches bugs early at compile-time rather than crashing during program execution!</div>
  </div>

</div>

</div>

  </template>
</Slide2>
