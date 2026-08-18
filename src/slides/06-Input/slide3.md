---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 3 — SCANNER: READING PRIMITIVE TYPES
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Java Input Methods">
  <template #content>

<div class="slide-h1" style="margin-bottom:10px;">Scanner — Reading <span class="highlight">Primitive Types</span></div>

<div class="g2" style="gap:14px;align-items:start;">

<div class="flex-col">

  <div style="margin-top:2px;">
    <table class="cmp-table" style="font-size:.7rem;">
      <thead v-click><tr><th>Method</th><th>Return Type</th><th>Example Input</th></tr></thead>
      <tbody>
        <tr v-click><td class="mono" style="color:var(--red-dark);font-weight:600;">nextInt()</td><td class="mono">int</td><td class="mono">25</td></tr>
        <tr v-click><td class="mono" style="color:var(--red-dark);font-weight:600;">nextDouble()</td><td class="mono">double</td><td class="mono">98.6</td></tr>
        <tr v-click><td class="mono" style="color:var(--red-dark);font-weight:600;">nextFloat()</td><td class="mono">float</td><td class="mono">3.14f</td></tr>
        <tr v-click><td class="mono" style="color:var(--red-dark);font-weight:600;">nextLong()</td><td class="mono">long</td><td class="mono">9876543210L</td></tr>
        <tr v-click><td class="mono" style="color:var(--red-dark);font-weight:600;">nextBoolean()</td><td class="mono">boolean</td><td class="mono">true / false</td></tr>
        <tr v-click><td class="mono" style="color:var(--red-dark);font-weight:600;">nextByte()</td><td class="mono">byte</td><td class="mono">127</td></tr>
        <tr v-click><td class="mono" style="color:var(--red-dark);font-weight:600;">nextShort()</td><td class="mono">short</td><td class="mono">32000</td></tr>
      </tbody>
    </table>
  </div>

  <div v-click class="callout callout-danger" style="margin-top:8px;">
    <div><strong>InputMismatchException:</strong> If you call <span class="mono">nextInt()</span> and the user enters <span class="mono">"hello"</span> or <span class="mono">3.14</span>, Java throws an <span class="mono">InputMismatchException</span> and crashes.</div>
  </div>

</div>

<div class="flex-col">
  <div v-click class="section-label">Reading Multiple Primitive Values</div>

  <div v-after class="code-block" style="font-size:.70rem;line-height:1.8;">
    <span style="color:#ef5050;">Scanner</span> <span style="color:#0e6ead;">sc</span> = <span style="color:#ef5050;">new</span> <span style="color:#0e6ead;">Scanner</span>(<span style="color:#0e6ead;">System</span>.<span style="color:#0e6ead;">in</span>);<br>
    <br>
    <span style="color:#0e6ead;">System</span>.<span style="color:#0e6ead;">out</span>.<span style="color:#2d7a00;">print</span>(<span style="color:#2d7a00;">"Enter roll no: "</span>);<br>
    <span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">roll</span> = <span style="color:#0e6ead;">sc</span>.<span style="color:#2d7a00;">nextInt</span>();<br>
    <br>
    <span style="color:#0e6ead;">System</span>.<span style="color:#0e6ead;">out</span>.<span style="color:#2d7a00;">print</span>(<span style="color:#2d7a00;">"Enter GPA: "</span>);<br>
    <span style="color:#ef5050;">double</span> <span style="color:#0e6ead;">gpa</span> = <span style="color:#0e6ead;">sc</span>.<span style="color:#2d7a00;">nextDouble</span>();<br>
    <br>
    <span style="color:#0e6ead;">System</span>.<span style="color:#0e6ead;">out</span>.<span style="color:#2d7a00;">print</span>(<span style="color:#2d7a00;">"Hostel resident (true/false)? "</span>);<br>
    <span style="color:#ef5050;">boolean</span> <span style="color:#0e6ead;">isHosteller</span> = <span style="color:#0e6ead;">sc</span>.<span style="color:#2d7a00;">nextBoolean</span>();<br>
    <br>
    <span style="color:#0e6ead;">System</span>.<span style="color:#0e6ead;">out</span>.<span style="color:#2d7a00;">printf</span>(<span style="color:#2d7a00;">"Roll: %d | GPA: %.2f | Hosteller: %b%n"</span>, <span style="color:#0e6ead;">roll</span>, <span style="color:#0e6ead;">gpa</span>, <span style="color:#0e6ead;">isHosteller</span>);
  </div>

  <div v-click class="callout callout-info" style="margin-top:6px;">
    <div><strong>Reading a single character:</strong> Scanner has no <span class="mono">nextChar()</span>. To read a single <span class="mono">char</span>, use: <span class="mono">char c = sc.next().charAt(0);</span></div>
  </div>

</div>

</div>

  </template>
</Slide2>
