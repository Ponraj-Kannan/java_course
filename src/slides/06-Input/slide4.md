---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 4 — SCANNER: next() vs nextLine()
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Java Input Methods">
  <template #content>

<div class="slide-h1" style="margin-bottom:10px;">Reading Text — <span class="highlight">next()</span> vs <span class="highlight">nextLine()</span></div>

<div class="g2" style="gap:14px;align-items:start;">

<div class="flex-col">

  <div v-click class="card-blue" style="border-radius:10px;">
    <div style="font-size:.78rem;font-weight:700;color:var(--blue);margin-bottom:4px;">next() — Reads a Single Word (Token)</div>
    <div style="font-size:.74rem;color:var(--slate);line-height:1.5;">Reads input up to the first whitespace (space, tab, or newline). Ignores leading whitespace.</div>
    <div class="code-block" style="margin-top:6px;font-size:.70rem;">
      <span style="color:#ef5050;">String</span> <span style="color:#0e6ead;">word</span> = <span style="color:#0e6ead;">sc</span>.<span style="color:#2d7a00;">next</span>();<br>
      <span style="color:#6b7280;">// User types: "Alice Smith"</span><br>
      <span style="color:#6b7280;">// word stores: "Alice" (stops at space!)</span>
    </div>
  </div>

  <div v-click class="card-green" style="border-radius:10px;margin-top:6px;">
    <div style="font-size:.78rem;font-weight:700;color:var(--green);margin-bottom:4px;">nextLine() — Reads the Entire Line</div>
    <div style="font-size:.74rem;color:var(--slate);line-height:1.5;">Reads all characters until the user hits the <span class="mono">Enter</span> key (<span class="mono">\n</span>). Includes all spaces.</div>
    <div class="code-block" style="margin-top:6px;font-size:.70rem;">
      <span style="color:#ef5050;">String</span> <span style="color:#0e6ead;">fullLine</span> = <span style="color:#0e6ead;">sc</span>.<span style="color:#2d7a00;">nextLine</span>();<br>
      <span style="color:#6b7280;">// User types: "Alice Smith"</span><br>
      <span style="color:#6b7280;">// fullLine stores: "Alice Smith"</span>
    </div>
  </div>

</div>

<div class="flex-col">
  <div v-click class="section-label">Comparison Summary</div>

  <div v-after>
    <table class="cmp-table" style="font-size:.7rem;">
      <thead><tr><th>Feature</th><th>next()</th><th>nextLine()</th></tr></thead>
      <tbody>
        <tr v-click><td>Delimiter</td><td>Whitespace (space/tab/\n)</td><td>Newline (<span class="mono">\n</span>) only</td></tr>
        <tr v-click><td>Spaces preserved?</td><td class="no">No — stops at space</td><td class="yes">Yes — preserves all spaces</td></tr>
        <tr v-click><td>Use case</td><td>Single words, tokens</td><td>Full sentences, addresses, names</td></tr>
      </tbody>
    </table>
  </div>

  <div v-click class="section-label" style="margin-top:8px;">Code Example</div>

  <div v-after class="code-block" style="font-size:.70rem;line-height:1.8;">
    <span style="color:#0e6ead;">System</span>.<span style="color:#0e6ead;">out</span>.<span style="color:#2d7a00;">print</span>(<span style="color:#2d7a00;">"Enter first name: "</span>);<br>
    <span style="color:#ef5050;">String</span> <span style="color:#0e6ead;">first</span> = <span style="color:#0e6ead;">sc</span>.<span style="color:#2d7a00;">next</span>(); <span style="color:#6b7280;">// e.g. "John"</span><br>
    <br>
    <span style="color:#0e6ead;">System</span>.<span style="color:#0e6ead;">out</span>.<span style="color:#2d7a00;">print</span>(<span style="color:#2d7a00;">"Enter full address: "</span>);<br>
    <span style="color:#0e6ead;">sc</span>.<span style="color:#2d7a00;">nextLine</span>(); <span style="color:#6b7280;">// flush newline!</span><br>
    <span style="color:#ef5050;">String</span> <span style="color:#0e6ead;">address</span> = <span style="color:#0e6ead;">sc</span>.<span style="color:#2d7a00;">nextLine</span>(); <span style="color:#6b7280;">// "123 Main St, Chennai"</span>
  </div>

  <div v-click class="callout callout-warn" style="margin-top:4px;">
    <div><strong>Rule of Thumb:</strong> Use <span class="mono">next()</span> when you only need one word without spaces; use <span class="mono">nextLine()</span> when reading full names, sentences, or multi-word text.</div>
  </div>

</div>

</div>

  </template>
</Slide2>
