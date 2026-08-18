---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 2 — ABS, MIN, MAX
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Java Math Functions">
  <template #content>

<div class="slide-h1" style="margin-bottom:10px;"><span class="highlight">abs()</span>, <span class="highlight">min()</span> &amp; <span class="highlight">max()</span></div>

<div class="g2" style="gap:14px;align-items:start;">

<div class="flex-col">

  <div v-click class="card-navy" style="border-radius:10px;">
    <div style="font-size:.82rem;line-height:1.6;color:var(--slate);">
      These three methods handle <strong>value comparison and sign removal</strong>: returning the absolute (non-negative) value, the smaller of two values, or the larger of two values.
    </div>
  </div>

  <div style="margin-top:6px;">
    <table class="cmp-table" style="font-size:.7rem;">
      <thead v-click><tr><th>Method</th><th>Returns</th><th>Overloaded For</th></tr></thead>
      <tbody>
        <tr v-click><td class="mono" style="color:var(--red-dark);font-weight:600;">Math.abs(x)</td><td>Non-negative value of x</td><td><span class="mono">int, long, float, double</span></td></tr>
        <tr v-click><td class="mono" style="color:var(--red-dark);font-weight:600;">Math.min(a, b)</td><td>Smaller of a and b</td><td><span class="mono">int, long, float, double</span></td></tr>
        <tr v-click><td class="mono" style="color:var(--red-dark);font-weight:600;">Math.max(a, b)</td><td>Larger of a and b</td><td><span class="mono">int, long, float, double</span></td></tr>
      </tbody>
    </table>
  </div>

  <div v-click class="callout callout-warn" style="margin-top:6px;">
    <div><strong>Edge Case:</strong> <span class="mono">Math.abs(Integer.MIN_VALUE)</span> returns <span class="mono">Integer.MIN_VALUE</span> (a negative number!) because the positive equivalent overflows the <span class="mono">int</span> range.</div>
  </div>

</div>

<div class="flex-col">
  <div v-click class="section-label">Code Examples</div>

  <div v-after class="code-block" style="font-size:.70rem;line-height:1.9;">
    <span style="color:#6b7280;">// Math.abs — makes negative positive</span><br>
    <span style="color:#0e6ead;">System</span>.<span style="color:#0e6ead;">out</span>.<span style="color:#2d7a00;">println</span>(<span style="color:#0e6ead;">Math</span>.<span style="color:#2d7a00;">abs</span>(-<span style="color:#b45309;">25</span>));    <span style="color:#2d7a00;">// 25</span><br>
    <span style="color:#0e6ead;">System</span>.<span style="color:#0e6ead;">out</span>.<span style="color:#2d7a00;">println</span>(<span style="color:#0e6ead;">Math</span>.<span style="color:#2d7a00;">abs</span>(-<span style="color:#b45309;">7.5</span>));   <span style="color:#2d7a00;">// 7.5</span><br>
    <span style="color:#0e6ead;">System</span>.<span style="color:#0e6ead;">out</span>.<span style="color:#2d7a00;">println</span>(<span style="color:#0e6ead;">Math</span>.<span style="color:#2d7a00;">abs</span>(<span style="color:#b45309;">42</span>));     <span style="color:#2d7a00;">// 42 (already positive)</span><br>
    <br>
    <span style="color:#6b7280;">// Math.min — smaller of two</span><br>
    <span style="color:#0e6ead;">System</span>.<span style="color:#0e6ead;">out</span>.<span style="color:#2d7a00;">println</span>(<span style="color:#0e6ead;">Math</span>.<span style="color:#2d7a00;">min</span>(<span style="color:#b45309;">10</span>, <span style="color:#b45309;">25</span>));  <span style="color:#2d7a00;">// 10</span><br>
    <span style="color:#0e6ead;">System</span>.<span style="color:#0e6ead;">out</span>.<span style="color:#2d7a00;">println</span>(<span style="color:#0e6ead;">Math</span>.<span style="color:#2d7a00;">min</span>(-<span style="color:#b45309;">3</span>, <span style="color:#b45309;">0</span>));  <span style="color:#2d7a00;">// -3</span><br>
    <br>
    <span style="color:#6b7280;">// Math.max — larger of two</span><br>
    <span style="color:#0e6ead;">System</span>.<span style="color:#0e6ead;">out</span>.<span style="color:#2d7a00;">println</span>(<span style="color:#0e6ead;">Math</span>.<span style="color:#2d7a00;">max</span>(<span style="color:#b45309;">100</span>, <span style="color:#b45309;">200</span>)); <span style="color:#2d7a00;">// 200</span><br>
    <span style="color:#0e6ead;">System</span>.<span style="color:#0e6ead;">out</span>.<span style="color:#2d7a00;">println</span>(<span style="color:#0e6ead;">Math</span>.<span style="color:#2d7a00;">max</span>(-<span style="color:#b45309;">5</span>, -<span style="color:#b45309;">1</span>)); <span style="color:#2d7a00;">// -1</span><br>
    <br>
    <span style="color:#6b7280;">// Chaining — clamp a value to a range [0..100]</span><br>
    <span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">score</span> = <span style="color:#b45309;">115</span>;<br>
    <span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">clamped</span> = <span style="color:#0e6ead;">Math</span>.<span style="color:#2d7a00;">min</span>(<span style="color:#0e6ead;">Math</span>.<span style="color:#2d7a00;">max</span>(<span style="color:#0e6ead;">score</span>, <span style="color:#b45309;">0</span>), <span style="color:#b45309;">100</span>);<br>
    <span style="color:#0e6ead;">System</span>.<span style="color:#0e6ead;">out</span>.<span style="color:#2d7a00;">println</span>(clamped); <span style="color:#2d7a00;">// 100</span>
  </div>

</div>

</div>

  </template>
</Slide2>
