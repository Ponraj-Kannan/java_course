---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 18 — PRACTICE PROGRAMS
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Operators">
  <template #content>

<div class="slide-h1" style="margin-bottom:10px;">Practice <span class="highlight">Programs</span></div>

<div class="g2" style="gap:14px;">

<div class="flex-col">

  <div v-click class="activity-box">
    <div class="act-title">🖊️ Program 1 — Swap Without Temp Variable</div>
    <div class="act-task">
      Write a Java snippet to swap two integer variables <span class="mono">a = 5</span> and <span class="mono">b = 10</span> without using a third temporary variable.
    </div>
    <div class="hint">💡 Hint: Use bitwise XOR (<span class="mono">^</span>) or arithmetic addition/subtraction (<span class="mono">+</span>, <span class="mono">-</span>).</div>
  </div>

  <div v-click class="activity-box" style="margin-top:4px;">
    <div class="act-title">🖊️ Program 2 — Predict Increment / Decrement</div>
    <div class="act-task">
      Predict the final values of <span class="mono">x</span>, <span class="mono">y</span>, and <span class="mono">z</span> without running Java:<br>
      <span class="mono">int x = 5; int y = x++ + ++x; int z = --y + x--;</span>
    </div>
    <div class="hint">💡 Hint: Trace step-by-step applying prefix vs postfix rules.</div>
  </div>

  <div v-click class="activity-box" style="margin-top:4px;">
    <div class="act-title">🖊️ Program 3 — Integer vs Float Division</div>
    <div class="act-task">
      Prompt the user for total marks (out of 500) and compute the percentage accurately as a <span class="mono">double</span> without truncating decimals.
    </div>
    <div class="hint">💡 Hint: Multiply by <span class="mono">100.0</span> instead of integer <span class="mono">100</span>.</div>
  </div>

</div>

<div class="flex-col">

  <div v-click class="activity-box">
    <div class="act-title">🖊️ Program 4 — Compound Assignment Tracer</div>
    <div class="act-task">
      Start with <span class="mono">int n = 20;</span> and execute in order: <strong>add 10, multiply by 2, modulus 7, left shift 1</strong> using compound assignment operators. Print result.
    </div>
    <div class="hint">💡 Use <span class="mono">+=</span>, <span class="mono">*=</span>, <span class="mono">%=</span>, <span class="mono">&lt;&lt;=</span>.</div>
  </div>

  <div v-click class="activity-box" style="margin-top:4px;">
    <div class="act-title">🖊️ Program 5 — Precedence Quiz</div>
    <div class="act-task">
      Evaluate the boolean outcome of this expression in your head:<br>
      <span class="mono">boolean result = 10 + 2 * 3 &gt; 15 &amp;&amp; !false || 5 == 4;</span>
    </div>
    <div class="hint">💡 Apply precedence: Arithmetic → Relational → NOT → AND → OR.</div>
  </div>

  <div v-click class="callout callout-warn" style="margin-top:4px;">
    <div><strong>Challenge:</strong> Write a single line of Java code using the Ternary Operator to find the maximum of three numbers <span class="mono">a</span>, <span class="mono">b</span>, and <span class="mono">c</span>!</div>
  </div>

</div>

</div>

  </template>
</Slide2>
