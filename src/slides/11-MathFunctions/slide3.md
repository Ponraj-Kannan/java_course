---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 3 — pow(), sqrt(), cbrt()
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Java Math Functions">
  <template #content>

<div class="slide-h1" style="margin-bottom:10px;"><span class="highlight">pow()</span>, <span class="highlight">sqrt()</span> &amp; <span class="highlight">cbrt()</span></div>

<div class="g2" style="gap:14px;align-items:start;">

<div class="flex-col">

  <div v-click class="card-navy" style="border-radius:10px;">
    <div style="font-size:.82rem;line-height:1.6;color:var(--slate);">
      These methods perform <strong>exponentiation and root extraction</strong>: raising a number to any power, computing the square root, and computing the cube root.
    </div>
  </div>

  <div style="margin-top:6px;">
    <table class="cmp-table" style="font-size:.7rem;">
      <thead v-click><tr><th>Method</th><th>Meaning</th><th>Return Type</th></tr></thead>
      <tbody>
        <tr v-click><td class="mono" style="color:var(--red-dark);font-weight:600;">Math.pow(a, b)</td><td>a<sup>b</sup> (a raised to the power b)</td><td class="mono">double</td></tr>
        <tr v-click><td class="mono" style="color:var(--red-dark);font-weight:600;">Math.sqrt(x)</td><td>√x — square root of x</td><td class="mono">double</td></tr>
        <tr v-click><td class="mono" style="color:var(--red-dark);font-weight:600;">Math.cbrt(x)</td><td>∛x — cube root of x</td><td class="mono">double</td></tr>
      </tbody>
    </table>
  </div>

  <div v-click class="callout callout-warn" style="margin-top:6px;">
    <div><strong>Always Returns double:</strong> Even <span class="mono">Math.pow(2, 10)</span> returns <span class="mono">1024.0</span> (a double). Cast to <span class="mono">int</span> with <span class="mono">(int) Math.pow(2, 10)</span> when integer result needed.</div>
  </div>

  <div v-click class="callout callout-danger" style="margin-top:4px;">
    <div><strong>NaN Gotcha:</strong> <span class="mono">Math.sqrt(-4)</span> does not throw an exception — it silently returns <span class="mono">NaN</span> (Not a Number). Always validate input before computing roots of negative numbers!</div>
  </div>

</div>

<div class="flex-col">
  <div v-click class="section-label">Code Examples</div>

  <div v-after class="code-block" style="font-size:.70rem;line-height:1.9;">
    <span style="color:#6b7280;">// Exponentiation</span><br>
    <span style="color:#0e6ead;">System</span>.<span style="color:#0e6ead;">out</span>.<span style="color:#2d7a00;">println</span>(<span style="color:#0e6ead;">Math</span>.<span style="color:#2d7a00;">pow</span>(<span style="color:#b45309;">2</span>, <span style="color:#b45309;">8</span>));   <span style="color:#2d7a00;">// 256.0</span><br>
    <span style="color:#0e6ead;">System</span>.<span style="color:#0e6ead;">out</span>.<span style="color:#2d7a00;">println</span>(<span style="color:#0e6ead;">Math</span>.<span style="color:#2d7a00;">pow</span>(<span style="color:#b45309;">9</span>, <span style="color:#b45309;">0.5</span>)); <span style="color:#2d7a00;">// 3.0 (same as sqrt)</span><br>
    <span style="color:#0e6ead;">System</span>.<span style="color:#0e6ead;">out</span>.<span style="color:#2d7a00;">println</span>(<span style="color:#0e6ead;">Math</span>.<span style="color:#2d7a00;">pow</span>(<span style="color:#b45309;">5</span>, -<span style="color:#b45309;">1</span>)); <span style="color:#2d7a00;">// 0.2 (reciprocal)</span><br>
    <br>
    <span style="color:#6b7280;">// Square root</span><br>
    <span style="color:#0e6ead;">System</span>.<span style="color:#0e6ead;">out</span>.<span style="color:#2d7a00;">println</span>(<span style="color:#0e6ead;">Math</span>.<span style="color:#2d7a00;">sqrt</span>(<span style="color:#b45309;">49</span>));   <span style="color:#2d7a00;">// 7.0</span><br>
    <span style="color:#0e6ead;">System</span>.<span style="color:#0e6ead;">out</span>.<span style="color:#2d7a00;">println</span>(<span style="color:#0e6ead;">Math</span>.<span style="color:#2d7a00;">sqrt</span>(<span style="color:#b45309;">2</span>));    <span style="color:#2d7a00;">// 1.4142135...</span><br>
    <span style="color:#0e6ead;">System</span>.<span style="color:#0e6ead;">out</span>.<span style="color:#2d7a00;">println</span>(<span style="color:#0e6ead;">Math</span>.<span style="color:#2d7a00;">sqrt</span>(-<span style="color:#b45309;">4</span>));   <span style="color:#2d7a00;">// NaN ⚠️</span><br>
    <br>
    <span style="color:#6b7280;">// Cube root (handles negatives correctly)</span><br>
    <span style="color:#0e6ead;">System</span>.<span style="color:#0e6ead;">out</span>.<span style="color:#2d7a00;">println</span>(<span style="color:#0e6ead;">Math</span>.<span style="color:#2d7a00;">cbrt</span>(<span style="color:#b45309;">27</span>));  <span style="color:#2d7a00;">// 3.0</span><br>
    <span style="color:#0e6ead;">System</span>.<span style="color:#0e6ead;">out</span>.<span style="color:#2d7a00;">println</span>(<span style="color:#0e6ead;">Math</span>.<span style="color:#2d7a00;">cbrt</span>(-<span style="color:#b45309;">8</span>));  <span style="color:#2d7a00;">// -2.0 ✓ (unlike sqrt)</span><br>
    <br>
    <span style="color:#6b7280;">// Cast pow to int when needed</span><br>
    <span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">val</span> = (<span style="color:#ef5050;">int</span>) <span style="color:#0e6ead;">Math</span>.<span style="color:#2d7a00;">pow</span>(<span style="color:#b45309;">10</span>, <span style="color:#b45309;">3</span>); <span style="color:#2d7a00;">// 1000</span>
  </div>

</div>

</div>

  </template>
</Slide2>
