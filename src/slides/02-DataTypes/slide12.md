---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 12 — JAVA LITERALS & NUMERIC UNDERSCORES
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Data Types">
  <template #content>

<div class="slide-h1" style="margin-bottom:10px;">Java Literals &amp; <span class="highlight">Numeric Underscores</span></div>

<div class="g2" style="gap:14px;">

<div class="flex-col">

  <div v-click class="card-navy" style="border-radius:10px;">
    <div style="font-size:.8rem;line-height:1.6;color:var(--slate);">
      <strong style="color:var(--red);">Definition:</strong> A <strong>literal</strong> is a fixed synthetic value written directly in source code without requiring calculation or evaluation.
    </div>
  </div>

  <div>
    <table class="cmp-table" style="font-size:.68rem;margin-top:4px;">
      <thead v-click><tr><th>Literal Category</th><th>Example Syntax</th><th>Note / Suffix</th></tr></thead>
      <tbody>
        <tr v-click><td style="font-weight:700;">Integer</td><td class="mono">100, 0b1010, 0x1A</td><td class="mono">Default int</td></tr>
        <tr v-click><td style="font-weight:700;">Long Integer</td><td class="mono">10000000000L</td><td class="mono">Requires 'L' or 'l'</td></tr>
        <tr v-click><td style="font-weight:700;">Double Floating</td><td class="mono">3.14, 1.5e3</td><td class="mono">Default double</td></tr>
        <tr v-click><td style="font-weight:700;">Float Decimal</td><td class="mono">3.14F</td><td class="mono">Requires 'F' or 'f'</td></tr>
        <tr v-click><td style="font-weight:700;">Character</td><td class="mono">'A', '\n', '\u0041'</td><td class="mono">Single quotes ' '</td></tr>
        <tr v-click><td style="font-weight:700;">String</td><td class="mono">"Java Programming"</td><td class="mono">Double quotes " "</td></tr>
      </tbody>
    </table>
  </div>

</div>

<div class="flex-col">
  <div v-click class="section-label">Underscores in Numeric Literals (Java 7+)</div>

  <div v-after style="background:#f6f8fa;border-radius:10px;border:1px solid #e1e4e8;padding:12px 14px;font-family:'Fira Code',monospace;font-size:.72rem;line-height:1.9;">
    <span style="color:#6b7280;">// Underscores improve visual readability</span><br>
    <span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">million</span> = <span style="color:#b45309;">1_000_000</span>; &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#6b7280;">// Same as 1000000</span><br>
    <span style="color:#ef5050;">long</span> <span style="color:#0e6ead;">creditCard</span> = <span style="color:#b45309;">1234_5678_9012L</span>;<br>
    <span style="color:#ef5050;">double</span> <span style="color:#0e6ead;">price</span> = <span style="color:#b45309;">99_999.99</span>;<br>
    <span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">hex</span> = <span style="color:#b45309;">0xFF_EC_DE_5E</span>;
  </div>

  <div v-click class="callout callout-warn" style="margin-top:6px;">
    <div><strong>Underscore Rules:</strong> You cannot place an underscore at the start/end of a number, next to a decimal point (<span class="mono">3._14</span>), or next to suffixes (<span class="mono">100_L</span>)!</div>
  </div>

</div>

</div>

  </template>
</Slide2>
