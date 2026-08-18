---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 2 — SCANNER METHODS FOR DIFFERENT TYPES
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Input Methods">
  <template #content>

<div class="slide-h1" style="margin-bottom:10px;">Scanner Methods for Different <span class="highlight">Data Types</span></div>

<div class="g2" style="gap:14px;">

<div class="flex-col">

  <div v-click class="card-navy" style="border-radius:10px;">
    <div style="font-size:.8rem;line-height:1.6;color:var(--slate);">
      <strong style="color:var(--red);">Definition:</strong> Each <span class="mono">Scanner</span> method reads and converts input into <strong>one specific type</strong>. Calling the wrong method for the typed data throws an <span class="mono">InputMismatchException</span>.
    </div>
  </div>

  <div>
    <table class="cmp-table" style="font-size:.7rem;margin-top:6px;">
      <thead v-click><tr><th>Method</th><th>Reads</th><th>Example Input</th></tr></thead>
      <tbody>
        <tr v-click><td class="mono" style="color:var(--red-dark);font-weight:700;">nextInt()</td><td>int</td><td class="mono">42</td></tr>
        <tr v-click><td class="mono" style="color:var(--red-dark);font-weight:700;">nextDouble()</td><td>double</td><td class="mono">3.14</td></tr>
        <tr v-click><td class="mono" style="color:var(--red-dark);font-weight:700;">nextLong()</td><td>long</td><td class="mono">10000000000</td></tr>
        <tr v-click><td class="mono" style="color:var(--red-dark);font-weight:700;">nextBoolean()</td><td>boolean</td><td class="mono">true</td></tr>
        <tr v-click><td class="mono" style="color:var(--red-dark);font-weight:700;">next()</td><td>one word (String)</td><td class="mono">Hello</td></tr>
        <tr v-click><td class="mono" style="color:var(--red-dark);font-weight:700;">nextLine()</td><td>whole line (String)</td><td class="mono">Hello World</td></tr>
      </tbody>
    </table>
  </div>

  <div v-click class="callout callout-warn" style="margin-top:6px;">
    <div><strong><span class="mono">next()</span> vs <span class="mono">nextLine()</span>:</strong> <span class="mono">next()</span> stops at the <strong>first space</strong>, while <span class="mono">nextLine()</span> reads the <strong>entire line</strong>, spaces included.</div>
  </div>

</div>

<div class="flex-col">
  <div v-click class="section-label">Code Example</div>

  <div v-after style="background:#f6f8fa;border-radius:10px;border:1px solid #e1e4e8;padding:12px 14px;font-family:'Fira Code',monospace;font-size:.72rem;line-height:1.9;">
    <span style="color:#0e6ead;">Scanner</span> <span style="color:#0e6ead;">sc</span> = <span style="color:#805ad5;">new</span> <span style="color:#0e6ead;">Scanner</span>(<span style="color:#0e6ead;">System</span>.<span style="color:#0e6ead;">in</span>);<br><br>
    <span style="color:#6b7280;">// user types: 25</span><br>
    <span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">age</span> = <span style="color:#0e6ead;">sc</span>.<span style="color:#2d7a00;">nextInt</span>();<br><br>
    <span style="color:#6b7280;">// user types: 5.9</span><br>
    <span style="color:#ef5050;">double</span> <span style="color:#0e6ead;">height</span> = <span style="color:#0e6ead;">sc</span>.<span style="color:#2d7a00;">nextDouble</span>();<br><br>
    <span style="color:#6b7280;">// user types: John Smith</span><br>
    <span style="color:#0e6ead;">String</span> <span style="color:#0e6ead;">fullName</span> = <span style="color:#0e6ead;">sc</span>.<span style="color:#2d7a00;">nextLine</span>();<br><br>
    <span style="color:#0e6ead;">System</span>.<span style="color:#0e6ead;">out</span>.<span style="color:#2d7a00;">println</span>(<span style="color:#0e6ead;">fullName</span>); <span style="color:#6b7280;">// John Smith</span>
  </div>

  <div v-click class="card card-blue" style="margin-top:6px;">
    <div class="small-text"><strong>Tip:</strong> Always check the method's return type matches the variable you're storing it in — <span class="mono">nextInt()</span> returns <span class="mono">int</span>, never <span class="mono">String</span>.</div>
  </div>

</div>

</div>

  </template>
</Slide2>
