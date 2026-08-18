---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 4 — PRIMITIVE TYPES: int & long
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Data Types">
  <template #content>

<div class="slide-h1" style="margin-bottom:10px;">Integer Primitives — <span class="highlight">int &amp; long</span></div>

<div class="g2" style="gap:14px;">

<div class="flex-col">

  <div v-click class="card-navy" style="border-radius:10px;">
    <div style="font-size:.78rem;line-height:1.5;color:var(--slate);">
      <strong style="color:var(--red);">1. int Definition:</strong> A 4-byte (32-bit) signed integer and Java's <strong>default type for whole numbers</strong>, ranging from <strong>-2,147,483,648 to 2,147,483,647</strong>.
    </div>
  </div>

  <div v-click class="card-navy" style="border-radius:10px;margin-top:4px;">
    <div style="font-size:.78rem;line-height:1.5;color:var(--slate);">
      <strong style="color:var(--red);">2. long Definition:</strong> An 8-byte (64-bit) signed integer used when whole values exceed the 32-bit <span class="mono">int</span> capacity, ranging from <strong>-9 × 10¹⁸ to 9 × 10¹⁸</strong>.
    </div>
  </div>

  <div v-click class="section-label" style="margin-top:4px;">Code Examples</div>
  <div v-after style="background:#f6f8fa;border-radius:10px;border:1px solid #e1e4e8;padding:10px 14px;font-family:'Fira Code',monospace;font-size:.72rem;line-height:1.9;">
    <span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">count</span> = <span style="color:#b45309;">50000</span>;<br>
    <span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">population</span> = <span style="color:#b45309;">1400000000</span>; <span style="color:#6b7280;">// Fits in int</span><br><br>
    <span style="color:#6b7280;">// Must add 'L' suffix for values exceeding int range!</span><br>
    <span style="color:#ef5050;">long</span> <span style="color:#0e6ead;">worldPop</span> = <span style="color:#b45309;">8000000000L</span>;<br>
    <span style="color:#ef5050;">long</span> <span style="color:#0e6ead;">lightYearMeters</span> = <span style="color:#b45309;">9460730472580800L</span>;
  </div>

</div>

<div class="flex-col">
  <div v-click class="section-label">Crucial Long Suffix Rule</div>

  <div v-click class="card-red" style="border-radius:10px;padding:10px 14px;">
    <div style="font-size:.78rem;font-weight:700;color:var(--red-dark);margin-bottom:2px;">Literal Integer Suffix 'L'</div>
    <div style="font-size:.7rem;color:var(--slate);">
      In Java, all integer literals default to <span class="mono">int</span>. Writing <span class="mono">long pop = 8000000000;</span> causes a <strong>compile error</strong> because the literal itself overflows <span class="mono">int</span>! Always append <span class="mono">L</span> or <span class="mono">l</span>.
    </div>
  </div>

  <div v-click class="mem-box" style="margin-top:6px;">
    <div class="mem-header">int vs long Specification</div>
    <div class="mem-row">
      <div class="mem-name">int</div>
      <div class="mem-val">4 bytes (32 bits)</div>
      <div class="mem-type">Standard default</div>
    </div>
    <div class="mem-row">
      <div class="mem-name">long</div>
      <div class="mem-val">8 bytes (64 bits)</div>
      <div class="mem-type">Requires 'L' suffix</div>
    </div>
  </div>

  <div v-click class="card card-green" style="margin-top:6px;">
    <div class="small-text"><strong>Real-world use:</strong> Use <span class="mono">int</span> for array indices, counts, loop counters. Use <span class="mono">long</span> for Unix timestamps in milliseconds (<span class="mono">System.currentTimeMillis()</span>), financial balances, and astronomical distances.</div>
  </div>

</div>

</div>

  </template>
</Slide2>
