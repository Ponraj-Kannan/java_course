---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 5 — ASSIGNMENT OPERATORS
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Operators">
  <template #content>

<div class="slide-h1" style="margin-bottom:10px;">Assignment <span class="highlight">Operators</span></div>

<div class="g2" style="gap:14px;">

<div class="flex-col">

  <div v-click class="card-navy" style="border-radius:10px;">
    <div style="font-size:.8rem;line-height:1.6;color:var(--slate);">
      <strong style="color:var(--red);">Definition:</strong> <strong>Assignment operators</strong> evaluate the expression on the right and store the result in the variable on the left. Compound operators (<span class="mono">+=</span>, <span class="mono">-=</span>, …) offer a <strong>shorthand</strong> for combining arithmetic with assignment.
    </div>
  </div>

  <div>
    <table class="cmp-table" style="font-size:.7rem;margin-top:6px;">
      <thead v-click><tr><th>Operator</th><th>Example</th><th>Equivalent to</th></tr></thead>
      <tbody>
        <tr v-click><td class="mono" style="color:var(--red-dark);font-weight:700;">=</td><td class="mono">x = 5</td><td class="mono">x = 5</td></tr>
        <tr v-click><td class="mono" style="color:var(--red-dark);font-weight:700;">+=</td><td class="mono">x += 3</td><td class="mono">x = x + 3</td></tr>
        <tr v-click><td class="mono" style="color:var(--red-dark);font-weight:700;">-=</td><td class="mono">x -= 2</td><td class="mono">x = x - 2</td></tr>
        <tr v-click><td class="mono" style="color:var(--red-dark);font-weight:700;">*=</td><td class="mono">x *= 4</td><td class="mono">x = x * 4</td></tr>
        <tr v-click><td class="mono" style="color:var(--red-dark);font-weight:700;">/=</td><td class="mono">x /= 2</td><td class="mono">x = x / 2</td></tr>
        <tr v-click><td class="mono" style="color:var(--red-dark);font-weight:700;">%=</td><td class="mono">x %= 3</td><td class="mono">x = x % 3</td></tr>
      </tbody>
    </table>
  </div>

</div>

<div class="flex-col">
  <div v-click class="section-label">Code Examples</div>

  <div v-after style="background:#f6f8fa;border-radius:10px;border:1px solid #e1e4e8;padding:12px 14px;font-family:'Fira Code',monospace;font-size:.72rem;line-height:1.9;">
    <span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">x</span> = <span style="color:#b45309;">10</span>;<br>
    <span style="color:#0e6ead;">x</span> += <span style="color:#b45309;">5</span>;  <span style="color:#6b7280;">// x becomes 15</span><br>
    <span style="color:#0e6ead;">x</span> -= <span style="color:#b45309;">3</span>;  <span style="color:#6b7280;">// x becomes 12</span><br>
    <span style="color:#0e6ead;">x</span> *= <span style="color:#b45309;">2</span>;  <span style="color:#6b7280;">// x becomes 24</span><br>
    <span style="color:#0e6ead;">x</span> /= <span style="color:#b45309;">4</span>;  <span style="color:#6b7280;">// x becomes 6</span><br>
    <span style="color:#0e6ead;">x</span> %= <span style="color:#b45309;">4</span>;  <span style="color:#6b7280;">// x becomes 2</span><br>
    <span style="color:#0e6ead;">System</span>.<span style="color:#0e6ead;">out</span>.<span style="color:#2d7a00;">println</span>(<span style="color:#0e6ead;">x</span>); <span style="color:#6b7280;">// 2</span>
  </div>

  <div style="margin-top:6px;">
    <div v-click class="section-label" style="margin-bottom:4px;">Step-by-Step Trace</div>
    <table class="trace-table" style="font-size:.68rem;">
      <thead>
        <tr v-after><th>Statement</th><th>Calculation</th><th>x Value</th></tr>
      </thead>
      <tbody>
        <tr v-click><td class="mono">int x = 10</td><td>Initial value</td><td class="mono h2">10</td></tr>
        <tr v-click><td class="mono">x += 5</td><td>10 + 5</td><td class="mono h2">15</td></tr>
        <tr v-click><td class="mono">x -= 3</td><td>15 - 3</td><td class="mono h2">12</td></tr>
        <tr v-click><td class="mono">x *= 2</td><td>12 * 2</td><td class="mono h2">24</td></tr>
        <tr v-click><td class="mono">x /= 4</td><td>24 / 4</td><td class="mono h2">6</td></tr>
        <tr v-click><td class="mono">x %= 4</td><td>6 % 4</td><td class="mono h2">2</td></tr>
      </tbody>
    </table>
  </div>

</div>

</div>

  </template>
</Slide2>
