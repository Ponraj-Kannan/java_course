---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 3 — FOR LOOP TRACING
═══════════════════════════════════════════════════════ -->

<Slide2 topic="For Loop">
  <template #content>

<div class="slide-h1" style="margin-bottom:10px;">For Loop — <span class="highlight">Tracing</span></div>

<div class="g2" style="gap:14px;">

<div class="flex-col">
  <div v-click class="section-label">Java Code Example</div>
  <div v-after style="background:#f6f8fa;border-radius:10px;border:1px solid #e1e4e8;padding:16px 18px;font-family:'Fira Code',monospace;font-size:.78rem;line-height:2;">
    <span style="color:#6b7280;">// Print numbers 1 to 5</span><br>
    <span style="color:#ef5050;">for</span> (<span style="color:#0e6ead;">int</span> i = <span style="color:#b45309;">1</span>; i &lt;= <span style="color:#b45309;">5</span>; i++) {<br>
    <span style="padding-left:20px;display:block;">System.out.<span style="color:#2d7a00;">println</span>(<span style="color:#2d7a00;">"i = "</span> + i);</span>
    }
  </div>

  <div v-click class="card card-navy" style="margin-top:10px;">
    <div style="font-size:.75rem;line-height:1.6;color:var(--slate);">
      <strong style="color:var(--navy);">Variable Scope:</strong> The counter variable <code>i</code> is declared inside the <code>for</code> loop header, so its scope is strictly limited to the loop body.
    </div>
  </div>
</div>

<div class="flex-col">
  <div v-after class="section-label">Step-by-Step Trace: i = 1 to 5</div>
  <div>
    <table class="trace-table">
      <thead v-after>
        <tr><th>Iteration</th><th>i</th><th>Condition (i &lt;= 5)</th><th>Output</th><th>After i++</th></tr>
      </thead>
      <tbody>
        <tr v-click><td>1</td><td>1</td><td class="yes">true</td><td>i = 1</td><td>2</td></tr>
        <tr v-click><td>2</td><td>2</td><td class="yes">true</td><td>i = 2</td><td>3</td></tr>
        <tr v-click><td>3</td><td>3</td><td class="yes">true</td><td>i = 3</td><td>4</td></tr>
        <tr v-click><td>4</td><td>4</td><td class="yes">true</td><td>i = 4</td><td>5</td></tr>
        <tr v-click><td>5</td><td>5</td><td class="yes">true</td><td>i = 5</td><td>6</td></tr>
        <tr v-click class="hl"><td>6</td><td>6</td><td class="no">false</td><td>Loop Exits</td><td>-</td></tr>
      </tbody>
    </table>
  </div>

  <div v-click class="output-box" style="margin-top:8px;font-size:.72rem;">
    <span class="comment">// Console Output</span><br>
    i = 1<br>i = 2<br>i = 3<br>i = 4<br>i = 5
  </div>
</div>

</div>

  </template>
</Slide2>
