---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 8 — PRIMITIVE DATA TYPES PRACTICE
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Data Types">
  <template #content>

<div class="slide-h1" style="margin-bottom:10px;">Primitive Data Types <span class="highlight">Practice</span></div>

<div class="g2" style="gap:14px;">

<div class="flex-col">

  <div v-click class="activity-box">
    <div class="act-title">🖊️ Task 1 — Primitive Selection Challenge</div>
    <div class="act-task">
      Choose the most memory-optimal primitive type for each scenario:<br>
      <strong>(a)</strong> Student age (0 to 120)<br>
      <strong>(b)</strong> World population (8,000,000,000)<br>
      <strong>(c)</strong> Semester GPA (3.85)<br>
      <strong>(d)</strong> User logged in status
    </div>
    <div class="hint">💡 Consider memory size, range, and default literal rules!</div>
  </div>

  <div v-click class="activity-box" style="margin-top:4px;">
    <div class="act-title">🖊️ Task 2 — Byte Overflow Tracer</div>
    <div class="act-task">
      Without running Java, predict the exact printed output:<br>
      <span class="mono">byte b = 127; b += 2; System.out.println(b);</span>
    </div>
    <div class="hint">💡 Hint: 8-bit signed byte range wraps around from 127!</div>
  </div>

</div>

<div class="flex-col">

  <div v-click class="activity-box">
    <div class="act-title">🖊️ Task 3 — Literal Suffix Debugger</div>
    <div class="act-task">
      Fix the two compile-time errors in this Java snippet:<br>
      <span class="mono" style="color:var(--red-dark);">float pi = 3.14159;</span><br>
      <span class="mono" style="color:var(--red-dark);">long totalUsers = 5000000000;</span>
    </div>
    <div class="hint">💡 Hint: What literal suffixes are required for float &amp; long?</div>
  </div>

  <div v-click class="activity-box" style="margin-top:4px;">
    <div class="act-title">🖊️ Task 4 — Char Unicode &amp; ASCII Math</div>
    <div class="act-task">
      Predict the output of:<br>
      <span class="mono">char ch = 'A'; ch++;</span><br>
      <span class="mono">System.out.println(ch);</span><br>
      <span class="mono">System.out.println((int)ch);</span>
    </div>
    <div class="hint">💡 Hint: 'A' has ASCII code 65!</div>
  </div>

</div>

</div>

  </template>
</Slide2>
