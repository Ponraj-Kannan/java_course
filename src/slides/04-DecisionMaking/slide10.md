---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 10 — IF-ELSE-IF CODE EXAMPLE
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Decision-making statements">
  <template #content>
<div class="slide-h1" style="margin-bottom:12px;"><span class="highlight">if-else-if</span> Ladder — Java Example</div>

<div class="g2" style="gap:14px;">

<div class="flex-col" style="gap:10px;">
  <div v-click class="slide-h3">Example: Student Grade Calculator</div>

  <div v-after style="background:#1a1f36;border-radius:10px;padding:12px 16px;font-family:'Fira Code',monospace;font-size:.72rem;line-height:1.75;">
    <span style="color:#ff79c6;">int</span> <span style="color:#f8f8f2;">marks</span> = <span style="color:#bd93f9;">84</span>;<br>
    <span style="color:#8be9fd;">char</span> <span style="color:#f8f8f2;">grade</span>;<br><br>
    <span style="color:#ff79c6;">if</span> <span style="color:#f1fa8c;">(</span><span style="color:#f8f8f2;">marks &gt;= 90</span><span style="color:#f1fa8c;">) {</span><br>
    &nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#f8f8f2;">grade</span> = <span style="color:#f1fa8c;">'A'</span>;<br>
    <span style="color:#f1fa8c;">}</span> <span style="color:#ff79c6;">else if</span> <span style="color:#f1fa8c;">(</span><span style="color:#f8f8f2;">marks &gt;= 80</span><span style="color:#f1fa8c;">) {</span><br>
    &nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#f8f8f2;">grade</span> = <span style="color:#f1fa8c;">'B'</span>;<br>
    <span style="color:#f1fa8c;">}</span> <span style="color:#ff79c6;">else if</span> <span style="color:#f1fa8c;">(</span><span style="color:#f8f8f2;">marks &gt;= 70</span><span style="color:#f1fa8c;">) {</span><br>
    &nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#f8f8f2;">grade</span> = <span style="color:#f1fa8c;">'C'</span>;<br>
    <span style="color:#f1fa8c;">}</span> <span style="color:#ff79c6;">else</span> <span style="color:#f1fa8c;">{</span><br>
    &nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#f8f8f2;">grade</span> = <span style="color:#f1fa8c;">'F'</span>;<br>
    <span style="color:#f1fa8c;">}</span><br>
    <span style="color:#8be9fd;">System</span>.<span style="color:#f8f8f2;">out</span>.<span style="color:#50fa7b;">println</span><span style="color:#f1fa8c;">(</span><span style="color:#f1fa8c;">"Grade: "</span> + <span style="color:#f8f8f2;">grade</span><span style="color:#f1fa8c;">)</span>;
  </div>

  <div v-click class="output-box">
    <span class="prompt">Output (marks = 84):</span><br>
    Grade: B
  </div>
</div>

<div class="flex-col" style="gap:10px;">
  <div v-click class="card card-navy">
    <div class="slide-h3" style="margin-bottom:6px;">Evaluation Breakdown</div>
    <div class="flex-col" style="gap:6px;">
      <div class="body-text">1. <code>marks &gt;= 90</code> (84 &gt;= 90) → <span style="color:var(--red);font-weight:700;">false</span></div>
      <div class="body-text">2. Moves to <code>else if (marks &gt;= 80)</code> (84 &gt;= 80) → <span style="color:var(--green);font-weight:700;">true</span></div>
      <div class="body-text">3. Sets <code>grade = 'B'</code>.</div>
      <div class="body-text">4. Skips <code>else if (marks &gt;= 70)</code> and <code>else</code> completely!</div>
    </div>
  </div>

  <div v-click class="callout callout-warn">
    <div><strong>Order Matters!</strong> Always arrange conditions from most specific to least specific (e.g. highest marks to lowest). Incorrect ordering will lead to logical bugs.</div>
  </div>
</div>

</div>
  </template>
</Slide2>
