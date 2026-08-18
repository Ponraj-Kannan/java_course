---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 6 — SCANNER: INPUT VALIDATION (hasNext...())
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Java Input Methods">
  <template #content>

<div class="slide-h1" style="margin-bottom:10px;">Scanner — <span class="highlight">Input Validation</span></div>

<div class="g2" style="gap:14px;align-items:start;">

<div class="flex-col">

  <div v-click class="card-navy" style="border-radius:10px;">
    <div style="font-size:.82rem;line-height:1.6;color:var(--slate);">
      The <span class="mono">hasNext...()</span> methods check whether the next token in the input matches the expected data type <strong>before reading it</strong>, returning <span class="mono">true</span> or <span class="mono">false</span>. This prevents the program from crashing with an <span class="mono">InputMismatchException</span>.
    </div>
  </div>

  <div style="margin-top:6px;">
    <table class="cmp-table" style="font-size:.7rem;">
      <thead v-click><tr><th>Validation Method</th><th>Checks For</th><th>Safe To Call</th></tr></thead>
      <tbody>
        <tr v-click><td class="mono" style="color:var(--red-dark);font-weight:600;">hasNextInt()</td><td>Valid <span class="mono">int</span> token</td><td class="mono">nextInt()</td></tr>
        <tr v-click><td class="mono" style="color:var(--red-dark);font-weight:600;">hasNextDouble()</td><td>Valid <span class="mono">double</span> token</td><td class="mono">nextDouble()</td></tr>
        <tr v-click><td class="mono" style="color:var(--red-dark);font-weight:600;">hasNextBoolean()</td><td><span class="mono">true</span> or <span class="mono">false</span></td><td class="mono">nextBoolean()</td></tr>
        <tr v-click><td class="mono" style="color:var(--red-dark);font-weight:600;">hasNext()</td><td>Any token available</td><td class="mono">next()</td></tr>
        <tr v-click><td class="mono" style="color:var(--red-dark);font-weight:600;">hasNextLine()</td><td>Another line available</td><td class="mono">nextLine()</td></tr>
      </tbody>
    </table>
  </div>

</div>

<div class="flex-col">
  <div v-click class="section-label">Validation Loop Pattern (Robust Input)</div>

  <div v-after class="code-block" style="font-size:.70rem;line-height:1.8;">
    <span style="color:#ef5050;">Scanner</span> <span style="color:#0e6ead;">sc</span> = <span style="color:#ef5050;">new</span> <span style="color:#0e6ead;">Scanner</span>(<span style="color:#0e6ead;">System</span>.<span style="color:#0e6ead;">in</span>);<br>
    <br>
    <span style="color:#0e6ead;">System</span>.<span style="color:#0e6ead;">out</span>.<span style="color:#2d7a00;">print</span>(<span style="color:#2d7a00;">"Enter a positive integer: "</span>);<br>
    <br>
    <span style="color:#6b7280;">// Keep asking until user enters a valid integer</span><br>
    <span style="color:#ef5050;">while</span> (!<span style="color:#0e6ead;">sc</span>.<span style="color:#2d7a00;">hasNextInt</span>()) {<br>
    <span style="padding-left:16px;display:block;"><span style="color:#0e6ead;">System</span>.<span style="color:#0e6ead;">out</span>.<span style="color:#2d7a00;">println</span>(<span style="color:#2d7a00;">"Invalid input! That is not an int."</span>);</span>
    <span style="padding-left:16px;display:block;"><span style="color:#0e6ead;">System</span>.<span style="color:#0e6ead;">out</span>.<span style="color:#2d7a00;">print</span>(<span style="color:#2d7a00;">"Please enter an integer: "</span>);</span>
    <span style="padding-left:16px;display:block;background:#fff5f5;border-left:2px solid var(--red);"><span style="color:#0e6ead;">sc</span>.<span style="color:#2d7a00;">next</span>(); <span style="color:#6b7280;">// discard invalid token</span></span>
    }<br>
    <br>
    <span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">number</span> = <span style="color:#0e6ead;">sc</span>.<span style="color:#2d7a00;">nextInt</span>();<br>
    <span style="color:#0e6ead;">System</span>.<span style="color:#0e6ead;">out</span>.<span style="color:#2d7a00;">println</span>(<span style="color:#2d7a00;">"You entered: "</span> + <span style="color:#0e6ead;">number</span>);
  </div>

  <div v-click class="callout callout-success" style="margin-top:6px;">
    <div><strong>Best Practice:</strong> Always discard the invalid token using <span class="mono">sc.next()</span> inside the loop, otherwise the loop will repeat infinitely checking the same invalid token!</div>
  </div>

</div>

</div>

  </template>
</Slide2>
