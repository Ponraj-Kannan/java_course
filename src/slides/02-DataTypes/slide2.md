---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 2 — JAVA PRIMITIVE DATA TYPES (8 PRIMITIVES)
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Data Types">
  <template #content>

<div class="slide-h1" style="margin-bottom:10px;">Java Primitive <span class="highlight">Data Types</span></div>

<div class="g2" style="gap:14px;">

<div class="flex-col">

  <div v-click class="card-navy" style="border-radius:10px;">
    <div style="font-size:.8rem;line-height:1.6;color:var(--slate);">
      <strong style="color:var(--red);">Definition:</strong> <strong>Primitive data types</strong> are the 8 predefined, fundamental building blocks of Java that store raw numeric, character, or logical values directly in memory.
    </div>
  </div>

  <div v-click class="section-label">Categorization</div>
  <div style="display:flex;flex-direction:column;gap:4px;">
    <div v-click class="card" style="padding:6px 12px;">
      <div style="font-size:.7rem;"><strong style="color:var(--red);">Integer Types:</strong> <span class="mono">byte</span>, <span class="mono">short</span>, <span class="mono">int</span> (default for whole numbers), <span class="mono">long</span></div>
    </div>
    <div v-click class="card" style="padding:6px 12px;">
      <div style="font-size:.7rem;"><strong style="color:var(--blue);">Floating-Point Types:</strong> <span class="mono">float</span>, <span class="mono">double</span> (default for decimal numbers)</div>
    </div>
    <div v-click class="card" style="padding:6px 12px;">
      <div style="font-size:.7rem;"><strong style="color:var(--purple);">Textual Character:</strong> <span class="mono">char</span> (16-bit Unicode character)</div>
    </div>
    <div v-click class="card" style="padding:6px 12px;">
      <div style="font-size:.7rem;"><strong style="color:var(--green);">Truth Value:</strong> <span class="mono">boolean</span> (<span class="mono">true</span> / <span class="mono">false</span>)</div>
    </div>
  </div>

  <div v-click class="callout callout-info" style="margin-top:6px;">
    <div><strong>Default Integer &amp; Decimal:</strong> In Java code, literal whole numbers default to <span class="mono">int</span>, and literal decimals default to <span class="mono">double</span>!</div>
  </div>

</div>

<div class="flex-col">

<div>
    <table class="cmp-table" style="font-size:.65rem;margin-top:4px;">
      <thead v-click><tr><th>Type</th><th style="width:100px">Size</th><th>Range / Description</th><th>Default</th></tr></thead>
      <tbody>
        <tr v-click><td class="mono" style="color:var(--red-dark);font-weight:700; font-size:0.8rem;">byte</td><td>1 byte (8 bits)</td><td class="mono">-128 to 127</td><td class="mono">0</td></tr>
        <tr v-click><td class="mono" style="color:var(--red-dark);font-weight:700; font-size:0.8rem;">short</td><td>2 bytes (16 bits)</td><td class="mono">-32,768 to 32,767</td><td class="mono">0</td></tr>
        <tr v-click><td class="mono" style="color:var(--red-dark);font-weight:700; font-size:0.8rem;">int</td><td>4 bytes (32 bits)</td><td class="mono">-2,147,483,648 to 2,147,483,647</td><td class="mono">0</td></tr>
        <tr v-click><td class="mono" style="color:var(--red-dark);font-weight:700; font-size:0.8rem;">long</td><td>8 bytes (64 bits)</td><td class="mono">-9 × 10¹⁸ to 9 × 10¹⁸</td><td class="mono">0L</td></tr>
        <tr v-click><td class="mono" style="color:var(--blue);font-weight:700; font-size:0.8rem;">float</td><td>4 bytes (32 bits)</td><td class="mono">6 to 7 decimal digits</td><td class="mono">0.0f</td></tr>
        <tr v-click><td class="mono" style="color:var(--blue);font-weight:700; font-size:0.8rem;">double</td><td>8 bytes (64 bits)</td><td class="mono">15 to 16 decimal digits</td><td class="mono">0.0d</td></tr>
        <tr v-click><td class="mono" style="color:var(--purple);font-weight:700; font-size:0.8rem;">char</td><td>2 bytes (16 bits)</td><td class="mono">Single Unicode character ('\u0000' to '\uffff')</td><td class="mono">'\u0000'</td></tr>
        <tr v-click><td class="mono" style="color:var(--green);font-weight:700; font-size:0.8rem;">boolean</td><td>1 bit (logical)</td><td class="mono">true or false</td><td class="mono">false</td></tr>
      </tbody>
    </table>
  </div>
</div>

</div>

  </template>
</Slide2>
