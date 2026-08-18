---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 13 — NESTED LOOPS: SYNTAX + EXECUTION
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Nested Loops">
  <template #content>

<div class="slide-h1" style="margin-bottom:10px;"><span class="highlight">Nested</span> Loops — Syntax &amp; Execution</div>

<div class="g2" style="gap:14px;">

<div class="flex-col">
  <div v-click class="section-label">Syntax &amp; Java Example</div>

  <div v-after style="background:#f6f8fa;border-radius:10px;border:1px solid #e1e4e8;padding:14px;font-family:'Fira Code',monospace;font-size:.72rem;line-height:1.9;">
    <span style="color:#6b7280;">// Outer loop (controls rows)</span><br>
    <span style="color:#ef5050;">for</span> (<span style="color:#0e6ead;">int</span> i = <span style="color:#b45309;">1</span>; i &lt;= <span style="color:#b45309;">3</span>; i++) {<br>
    <span style="padding-left:20px;display:block;color:#6b7280;">// Inner loop (controls columns)</span>
    <span style="padding-left:20px;display:block;"><span style="color:#ef5050;">for</span> (<span style="color:#0e6ead;">int</span> j = <span style="color:#b45309;">1</span>; j &lt;= <span style="color:#b45309;">3</span>; j++) {</span>
    <span style="padding-left:40px;display:block;">System.out.<span style="color:#2d7a00;">println</span>(i + <span style="color:#2d7a00;">" x "</span> + j + <span style="color:#2d7a00;">" = "</span> + (i*j));</span>
    <span style="padding-left:20px;display:block;">}</span>
    }
  </div>

  <div v-click class="output-box" style="font-size:.7rem;">
    1 x 1 = 1 &nbsp; 1 x 2 = 2 &nbsp; 1 x 3 = 3<br>
    2 x 1 = 2 &nbsp; 2 x 2 = 4 &nbsp; 2 x 3 = 6<br>
    3 x 1 = 3 &nbsp; 3 x 2 = 6 &nbsp; 3 x 3 = 9
  </div>

  <div v-click class="callout callout-warn" style="margin-top:6px;">
    <div>For <strong>every single iteration</strong> of the outer loop, the inner loop completes <strong>all</strong> of its iterations.</div>
  </div>
</div>

<div class="flex-col">
  <div v-click class="section-label">Execution Visualization (i x j iterations)</div>

  <div v-after style="overflow-x:auto;">
    <table class="trace-table" style="font-size:.68rem;">
      <thead>
        <tr><th>Outer (i)</th><th>Inner (j)</th><th>i * j</th><th>Total Runs</th></tr>
      </thead>
      <tbody>
        <tr><td>1</td><td>1, 2, 3</td><td>1, 2, 3</td><td>3 iterations</td></tr>
        <tr><td>2</td><td>1, 2, 3</td><td>2, 4, 6</td><td>3 iterations</td></tr>
        <tr><td>3</td><td>1, 2, 3</td><td>3, 6, 9</td><td>3 iterations</td></tr>
        <tr class="hl"><td colspan="3"><strong>Total Execution Count</strong></td><td><strong>9 runs</strong></td></tr>
      </tbody>
    </table>
  </div>

  <div v-click class="card card-blue" style="margin-top:10px;">
    <div class="small-text"><strong>Total Iterations Formula:</strong> Outer Count &times; Inner Count = 3 &times; 3 = 9 total loop body executions.</div>
  </div>
</div>

</div>

  </template>
</Slide2>
