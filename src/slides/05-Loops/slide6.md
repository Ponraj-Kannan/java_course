---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 6 — WHILE LOOP TRACING (SUM OF DIGITS)
═══════════════════════════════════════════════════════ -->

<Slide2 topic="While Loop">
  <template #content>

<div class="slide-h1" style="margin-bottom:10px;">While Loop — <span class="highlight">Tracing (Sum of Digits)</span></div>

<div class="g2" style="gap:14px;">

<div class="flex-col">
  <div v-click class="section-label">Java Code Example</div>
  <div v-after style="background:#f6f8fa;border-radius:10px;border:1px solid #e1e4e8;padding:16px 18px;font-family:'Fira Code',monospace;font-size:.76rem;line-height:1.9;">
    <span style="color:#0e6ead;">int</span> num = <span style="color:#b45309;">1234</span>;<br>
    <span style="color:#0e6ead;">int</span> sum = <span style="color:#b45309;">0</span>;<br>
    <br>
    <span style="color:#ef5050;">while</span> (num &gt; <span style="color:#b45309;">0</span>) {<br>
    <span style="padding-left:20px;display:block;"><span style="color:#0e6ead;">int</span> digit = num % <span style="color:#b45309;">10</span>; <span style="color:#6b7280;">// extract last digit</span></span>
    <span style="padding-left:20px;display:block;">sum += digit; <span style="color:#6b7280;">// add to sum</span></span>
    <span style="padding-left:20px;display:block;">num /= <span style="color:#b45309;">10</span>; <span style="color:#6b7280;">// remove last digit</span></span>
    }<br>
    System.out.<span style="color:#2d7a00;">println</span>(<span style="color:#2d7a00;">"Sum = "</span> + sum);
  </div>

  <div v-click class="callout callout-info" style="margin-top:8px;">
    <div><strong>Java Integer Division:</strong> <code>1234 / 10</code> yields <code>123</code> (truncates remainder), making <code>num /= 10</code> an ideal pattern for digit processing.</div>
  </div>
</div>

<div class="flex-col">
  <div v-click class="section-label">Step-by-Step Trace: num = 1234</div>
  <div>
    <table class="trace-table" style="font-size:.68rem;">
      <thead v-click>
        <tr><th>Iter</th><th>num</th><th>num &gt; 0</th><th>digit (%10)</th><th>sum</th><th>num /= 10</th></tr>
      </thead>
      <tbody>
        <tr v-click><td>1</td><td>1234</td><td class="yes">true</td><td>4</td><td>4</td><td>123</td></tr>
        <tr v-click><td>2</td><td>123</td><td class="yes">true</td><td>3</td><td>7</td><td>12</td></tr>
        <tr v-click><td>3</td><td>12</td><td class="yes">true</td><td>2</td><td>9</td><td>1</td></tr>
        <tr v-click><td>4</td><td>1</td><td class="yes">true</td><td>1</td><td>10</td><td>0</td></tr>
        <tr v-click class="hl"><td>5</td><td>0</td><td class="no">false</td><td>-</td><td>10</td><td>Exit Loop</td></tr>
      </tbody>
    </table>
  </div>

  <div v-click class="output-box" style="margin-top:8px;font-size:.72rem;">
    <span class="comment">// Console Output</span><br>
    Sum = 10
  </div>
</div>

</div>

  </template>
</Slide2>
