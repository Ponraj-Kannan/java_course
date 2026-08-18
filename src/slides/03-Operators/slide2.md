---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 2 — ARITHMETIC OPERATORS
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Operators">
  <template #content>

<div class="slide-h1" style="margin-bottom:10px;">Arithmetic <span class="highlight">Operators</span></div>

<div class="g2" style="gap:14px;">

<div class="flex-col">

  <div v-click class="card-navy" style="border-radius:10px;">
    <div style="font-size:.8rem;line-height:1.6;color:var(--slate);">
      <strong style="color:var(--red);">Definition:</strong> <strong>Arithmetic operators</strong> perform standard mathematical calculations on numeric operands (integers and floating-point numbers).
    </div>
  </div>

  <div>
    <table class="cmp-table" style="font-size:.72rem;margin-top:6px;">
      <thead v-click><tr><th>Operator</th><th>Name</th><th>Example</th><th>Result</th></tr></thead>
      <tbody>
        <tr v-click><td class="mono" style="color:var(--red-dark);font-weight:700;">+</td><td>Addition</td><td class="mono">10 + 3</td><td class="mono yes">13</td></tr>
        <tr v-click><td class="mono" style="color:var(--red-dark);font-weight:700;">-</td><td>Subtraction</td><td class="mono">10 - 3</td><td class="mono yes">7</td></tr>
        <tr v-click><td class="mono" style="color:var(--red-dark);font-weight:700;">*</td><td>Multiplication</td><td class="mono">10 * 3</td><td class="mono yes">30</td></tr>
        <tr v-click><td class="mono" style="color:var(--red-dark);font-weight:700;">/</td><td>Division</td><td class="mono">10 / 3</td><td class="mono yes">3 (int)</td></tr>
        <tr v-click><td class="mono" style="color:var(--red-dark);font-weight:700;">%</td><td>Modulus (Remainder)</td><td class="mono">10 % 3</td><td class="mono yes">1</td></tr>
      </tbody>
    </table>
  </div>

  <div v-click class="callout callout-danger" style="margin-top:6px;">
    <div><strong>Java Exponentiation:</strong> Java has no <span class="mono">**</span> operator! Use <span class="mono">Math.pow(base, exponent)</span> for powers (e.g. <span class="mono">Math.pow(2, 8) == 256.0</span>).</div>
  </div>

</div>

<div class="flex-col">
  <div v-click class="section-label">Code Examples &amp; Gotcha</div>

  <div v-after style="background:#f6f8fa;border-radius:10px;border:1px solid #e1e4e8;padding:12px 14px;font-family:'Fira Code',monospace;font-size:.72rem;line-height:1.9;">
    <span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">a</span> = <span style="color:#b45309;">10</span>, <span style="color:#0e6ead;">b</span> = <span style="color:#b45309;">3</span>;<br>
    <span style="color:#0e6ead;">System</span>.<span style="color:#0e6ead;">out</span>.<span style="color:#2d7a00;">println</span>(<span style="color:#0e6ead;">a</span> + <span style="color:#0e6ead;">b</span>);  <span style="color:#6b7280;">// 13</span><br>
    <span style="color:#0e6ead;">System</span>.<span style="color:#0e6ead;">out</span>.<span style="color:#2d7a00;">println</span>(<span style="color:#0e6ead;">a</span> - <span style="color:#0e6ead;">b</span>);  <span style="color:#6b7280;">// 7</span><br>
    <span style="color:#0e6ead;">System</span>.<span style="color:#0e6ead;">out</span>.<span style="color:#2d7a00;">println</span>(<span style="color:#0e6ead;">a</span> * <span style="color:#0e6ead;">b</span>);  <span style="color:#6b7280;">// 30</span><br>
    <span style="color:#0e6ead;">System</span>.<span style="color:#0e6ead;">out</span>.<span style="color:#2d7a00;">println</span>(<span style="color:#0e6ead;">a</span> / <span style="color:#0e6ead;">b</span>);  <span style="color:#6b7280;">// 3  ← Integer division!</span><br>
    <span style="color:#0e6ead;">System</span>.<span style="color:#0e6ead;">out</span>.<span style="color:#2d7a00;">println</span>(<span style="color:#b45309;">10.0</span> / <span style="color:#b45309;">3</span>);<span style="color:#6b7280;">// 3.3333333333333335</span><br>
    <span style="color:#0e6ead;">System</span>.<span style="color:#0e6ead;">out</span>.<span style="color:#2d7a00;">println</span>(<span style="color:#0e6ead;">a</span> % <span style="color:#0e6ead;">b</span>);  <span style="color:#6b7280;">// 1  ← Remainder</span>
  </div>

  <div v-click class="callout callout-warn" style="margin-top:6px;">
    <div><strong>Integer Division Gotcha:</strong> When dividing two integers in Java, the decimal part is <strong>truncated (dropped)</strong>. To get a precise decimal, cast at least one operand to <span class="mono">double</span>!</div>
  </div>

  <div v-click class="card card-orange" style="margin-top:6px;">
    <div class="small-text"><strong>Real-world use:</strong> Modulus <span class="mono">%</span> is used for even/odd checks (<span class="mono">n % 2 == 0</span>), extracting last digits (<span class="mono">n % 10</span>), and circular clock math.</div>
  </div>

</div>

</div>

  </template>
</Slide2>
