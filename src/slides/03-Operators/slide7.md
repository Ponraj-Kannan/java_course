---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 7 — RELATIONAL OPERATORS
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Operators">
  <template #content>

<div class="slide-h1" style="margin-bottom:10px;">Relational <span class="highlight">Operators</span></div>

<div class="g2" style="gap:14px;">

<div class="flex-col">

  <div v-click class="card-navy" style="border-radius:10px;">
    <div style="font-size:.8rem;line-height:1.6;color:var(--slate);">
      <strong style="color:var(--red);">Definition:</strong> <strong>Relational (comparison) operators</strong> compare two operands and evaluate to a <strong>boolean result</strong> — returning either <span class="mono" style="color:var(--green);">true</span> or <span class="mono" style="color:var(--red-dark);">false</span>.
    </div>
  </div>

  <div>
    <table class="cmp-table" style="font-size:.72rem;margin-top:6px;">
      <thead v-click><tr><th>Operator</th><th>Meaning</th><th>Example</th><th>Result</th></tr></thead>
      <tbody>
        <tr v-click><td class="mono" style="color:var(--red-dark);font-weight:700;">==</td><td>Equal to</td><td class="mono">5 == 5</td><td class="yes">true</td></tr>
        <tr v-click><td class="mono" style="color:var(--red-dark);font-weight:700;">!=</td><td>Not equal to</td><td class="mono">5 != 3</td><td class="yes">true</td></tr>
        <tr v-click><td class="mono" style="color:var(--red-dark);font-weight:700;">&gt;</td><td>Greater than</td><td class="mono">7 > 4</td><td class="yes">true</td></tr>
        <tr v-click><td class="mono" style="color:var(--red-dark);font-weight:700;">&lt;</td><td>Less than</td><td class="mono">3 < 9</td><td class="yes">true</td></tr>
        <tr v-click><td class="mono" style="color:var(--red-dark);font-weight:700;">&gt;=</td><td>Greater than or equal</td><td class="mono">5 >= 5</td><td class="yes">true</td></tr>
        <tr v-click><td class="mono" style="color:var(--red-dark);font-weight:700;">&lt;=</td><td>Less than or equal</td><td class="mono">4 <= 3</td><td class="no">false</td></tr>
      </tbody>
    </table>
  </div>

  <div v-click class="callout callout-danger" style="margin-top:6px;">
    <div><strong>Assignment vs Comparison Trap:</strong> In Java, <span class="mono">=</span> is for assignment, while <span class="mono">==</span> is for comparison. Using <span class="mono">=</span> inside an <span class="mono">if</span> condition will trigger a Java compilation error!</div>
  </div>

</div>

<div class="flex-col">
  <div v-click class="section-label">Java Code Examples</div>

  <div v-after style="background:#f6f8fa;border-radius:10px;border:1px solid #e1e4e8;padding:12px 14px;font-family:'Fira Code',monospace;font-size:.72rem;line-height:1.9;">
    <span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">a</span> = <span style="color:#b45309;">10</span>, <span style="color:#0e6ead;">b</span> = <span style="color:#b45309;">7</span>;<br>
    <span style="color:#0e6ead;">System</span>.<span style="color:#0e6ead;">out</span>.<span style="color:#2d7a00;">println</span>(<span style="color:#0e6ead;">a</span> == <span style="color:#0e6ead;">b</span>);  <span style="color:#6b7280;">// false</span><br>
    <span style="color:#0e6ead;">System</span>.<span style="color:#0e6ead;">out</span>.<span style="color:#2d7a00;">println</span>(<span style="color:#0e6ead;">a</span> != <span style="color:#0e6ead;">b</span>);  <span style="color:#6b7280;">// true</span><br>
    <span style="color:#0e6ead;">System</span>.<span style="color:#0e6ead;">out</span>.<span style="color:#2d7a00;">println</span>(<span style="color:#0e6ead;">a</span> &gt; <span style="color:#0e6ead;">b</span>);   <span style="color:#6b7280;">// true</span><br>
    <span style="color:#0e6ead;">System</span>.<span style="color:#0e6ead;">out</span>.<span style="color:#2d7a00;">println</span>(<span style="color:#0e6ead;">a</span> &gt;= <span style="color:#b45309;">10</span>); <span style="color:#6b7280;">// true</span><br>
    <span style="color:#0e6ead;">System</span>.<span style="color:#0e6ead;">out</span>.<span style="color:#2d7a00;">println</span>(<span style="color:#0e6ead;">b</span> &lt; <span style="color:#b45309;">5</span>);   <span style="color:#6b7280;">// false</span>
  </div>

  <div v-click class="section-label" style="margin-top:6px;">Important: Primitives vs Objects</div>
  <div v-after style="background:#fffaf0;border:1px solid var(--orange);border-radius:10px;padding:10px 14px;font-size:.7rem;line-height:1.6;">
    <div><strong>Primitive types</strong> (<span class="mono">int</span>, <span class="mono">double</span>): <span class="mono">==</span> compares actual <strong>values</strong>.<br>
    <strong>Reference objects</strong> (<span class="mono">String</span>): <span class="mono">==</span> compares <strong>memory addresses</strong>! To compare string contents, always use <span class="mono">s1.equals(s2)</span>.</div>
  </div>

  <div v-click class="card card-blue" style="margin-top:6px;">
    <div class="small-text"><strong>Real-world use:</strong> Relational operators form the condition in decision-making statements (<span class="mono">if</span>, <span class="mono">while</span>, <span class="mono">for</span> loops).</div>
  </div>

</div>

</div>

  </template>
</Slide2>
