---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 3 — PRIMITIVE TYPES: byte & short
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Data Types">
  <template #content>

<div class="slide-h1" style="margin-bottom:10px;">Integer Primitives — <span class="highlight">byte &amp; short</span></div>

<div class="g2" style="gap:14px;">

<div class="flex-col">

  <div v-click class="card-navy" style="border-radius:10px;">
    <div style="font-size:.78rem;line-height:1.5;color:var(--slate);">
      <strong style="color:var(--red);">1. byte Definition:</strong> A 1-byte (8-bit) signed 2's complement integer that stores small whole numbers from <strong>-128 to 127</strong> (default: <span class="mono">0</span>).
    </div>
  </div>

  <div v-click class="card-navy" style="border-radius:10px;margin-top:4px;">
    <div style="font-size:.78rem;line-height:1.5;color:var(--slate);">
      <strong style="color:var(--red);">2. short Definition:</strong> A 2-byte (16-bit) signed 2's complement integer that stores whole numbers from <strong>-32,768 to 32,767</strong> (default: <span class="mono">0</span>).
    </div>
  </div>

  <div v-click class="section-label" style="margin-top:4px;">Code Examples</div>
  <div v-after style="background:#f6f8fa;border-radius:10px;border:1px solid #e1e4e8;padding:10px 14px;font-family:'Fira Code',monospace;font-size:.72rem;line-height:1.9;">
    <span style="color:#ef5050;">byte</span> <span style="color:#0e6ead;">age</span> = <span style="color:#b45309;">25</span>;<br>
    <span style="color:#ef5050;">byte</span> <span style="color:#0e6ead;">level</span> = <span style="color:#b45309;">1</span>;<br>
    <span style="color:#ef5050;">short</span> <span style="color:#0e6ead;">yearOfBirth</span> = <span style="color:#b45309;">1998</span>;<br>
    <span style="color:#ef5050;">short</span> <span style="color:#0e6ead;">altitude</span> = <span style="color:#b45309;">8848</span>; <span style="color:#6b7280;">// Mt. Everest height in meters</span>
  </div>

</div>

<div class="flex-col">
  <div v-click class="section-label">Why Use byte &amp; short?</div>

  <div v-click class="card-blue" style="border-radius:8px;padding:8px 12px;">
    <div style="font-size:.72rem;font-weight:700;color:var(--blue);margin-bottom:2px;">Memory Efficiency in Large Arrays</div>
    <div style="font-size:.7rem;color:var(--slate);">A <span class="mono">byte[]</span> array saves 4x memory compared to an <span class="mono">int[]</span> array when storing large datasets (e.g. image pixels, audio buffers).</div>
  </div>

  <div v-click class="mem-box" style="margin-top:6px;">
    <div class="mem-header">Memory Consumption Comparison</div>
    <div class="mem-row">
      <div class="mem-name">byte</div>
      <div class="mem-val">8 bits (1 byte)</div>
      <div class="mem-type">Smallest integer</div>
    </div>
    <div class="mem-row">
      <div class="mem-name">short</div>
      <div class="mem-val">16 bits (2 bytes)</div>
      <div class="mem-type">Half of int</div>
    </div>
  </div>

  <div v-click class="callout callout-warn" style="margin-top:6px;">
    <div><strong>Gotcha:</strong> Arithmetic operations on <span class="mono">byte</span> or <span class="mono">short</span> automatically promote operands to <span class="mono">int</span>! <span class="mono">byte b = 5; b = (byte)(b + 1);</span> requires explicit casting.</div>
  </div>

</div>

</div>

  </template>
</Slide2>
