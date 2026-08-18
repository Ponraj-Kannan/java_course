---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 22 — PRACTICE PROGRAMS
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Data Types">
  <template #content>

<div class="slide-h1" style="margin-bottom:10px;">Practice <span class="highlight">Programs</span></div>

<div class="g2" style="gap:14px;">

<div class="flex-col">

  <div v-click class="activity-box">
    <div class="act-title">🖊️ Program 1 — Primitive Explorer</div>
    <div class="act-task">
      Write a Java program that declares all <strong>8 primitive data types</strong> with valid literals and prints their values alongside their default memory sizes.
    </div>
    <div class="hint">💡 Hint: Remember literal suffixes: <span class="mono">L</span> for long, <span class="mono">f</span> for float!</div>
  </div>

  <div v-click class="activity-box" style="margin-top:4px;">
    <div class="act-title">🖊️ Program 2 — Explicit Narrowing &amp; Truncation</div>
    <div class="act-task">
      Given a student's double percentage <span class="mono">98.75</span>, cast it explicitly to an <span class="mono">int</span> grade score. Print both values and explain what happened to the fractional part.
    </div>
    <div class="hint">💡 Hint: Use explicit cast operator <span class="mono">(int)</span>.</div>
  </div>

  <div v-click class="activity-box" style="margin-top:4px;">
    <div class="act-title">🖊️ Program 3 — Autoboxing Sum</div>
    <div class="act-task">
      Create a wrapper <span class="mono">Integer</span> object from a primitive <span class="mono">int</span>, add it to another primitive <span class="mono">int</span> using unboxing, and print the result.
    </div>
    <div class="hint">💡 Hint: Java compiler performs autoboxing/unboxing automatically.</div>
  </div>

</div>

<div class="flex-col">

  <div v-click class="activity-box">
    <div class="act-title">🖊️ Program 4 — Overflow Predictor</div>
    <div class="act-task">
      Without running Java, predict the exact printed output of this code snippet:<br>
      <span class="mono">byte b = 120; b += 10; System.out.println(b);</span>
    </div>
    <div class="hint">💡 Hint: Remember byte range is -128 to 127! Trace wrap-around.</div>
  </div>

  <div v-click class="activity-box" style="margin-top:4px;">
    <div class="act-title">🖊️ Program 5 — var Quiz</div>
    <div class="act-task">
      Identify which of these 3 declarations are legal in Java 10+:<br>
      <strong>(a)</strong> <span class="mono">var x = 100;</span> &nbsp;
      <strong>(b)</strong> <span class="mono">var y; y = 50;</span> &nbsp;
      <strong>(c)</strong> <span class="mono">var name = "Alice";</span>
    </div>
    <div class="hint">💡 Hint: <span class="mono">var</span> requires immediate initialization!</div>
  </div>

  <div v-click class="callout callout-warn" style="margin-top:4px;">
    <div><strong>Challenge:</strong> Write a Java program using <span class="mono">Integer.parseInt()</span> that reads a numeric string input and checks if it fits within a <span class="mono">byte</span> without overflow!</div>
  </div>

</div>

</div>

  </template>
</Slide2>
