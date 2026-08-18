---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 5 — PRIMITIVE TYPES: float & double
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Data Types">
  <template #content>

<div class="slide-h1" style="margin-bottom:10px;">Floating-Point Primitives — <span class="highlight">float &amp; double</span></div>

<div class="g2" style="gap:14px;">

<div class="flex-col">

  <div v-click class="card-navy" style="border-radius:10px;">
    <div style="font-size:.78rem;line-height:1.5;color:var(--slate);">
      <strong style="color:var(--red);">1. float Definition:</strong> A 4-byte (32-bit) IEEE 754 single-precision floating-point type for fractional numbers with <strong>6–7 decimal digits</strong> of precision (requires <span class="mono">f</span> / <span class="mono">F</span> suffix).
    </div>
  </div>

  <div v-click class="card-navy" style="border-radius:10px;margin-top:4px;">
    <div style="font-size:.78rem;line-height:1.5;color:var(--slate);">
      <strong style="color:var(--red);">2. double Definition:</strong> An 8-byte (64-bit) IEEE 754 double-precision floating-point type and <strong>Java's default type for decimals</strong>, offering <strong>15–16 decimal digits</strong> of precision.
    </div>
  </div>

  <div v-click class="section-label" style="margin-top:4px;">Code Examples</div>
  <div v-after style="background:#f6f8fa;border-radius:10px;border:1px solid #e1e4e8;padding:10px 14px;font-family:'Fira Code',monospace;font-size:.72rem;line-height:1.9;">
    <span style="color:#6b7280;">// float requires explicit 'f' or 'F' suffix</span><br>
    <span style="color:#ef5050;">float</span> <span style="color:#0e6ead;">g</span> = <span style="color:#b45309;">9.81f</span>;<br>
    <span style="color:#ef5050;">float</span> <span style="color:#0e6ead;">price</span> = <span style="color:#b45309;">19.99F</span>;<br><br>
    <span style="color:#6b7280;">// double is default for all decimal literals</span><br>
    <span style="color:#ef5050;">double</span> <span style="color:#0e6ead;">pi</span> = <span style="color:#b45309;">3.141592653589793</span>;<br>
    <span style="color:#ef5050;">double</span> <span style="color:#0e6ead;">rate</span> = <span style="color:#b45309;">0.05d</span>; <span style="color:#6b7280;">// 'd' suffix is optional</span>
  </div>

</div>

<div class="flex-col">

  <div v-click class="card-red" style="border-radius:10px;padding:10px 14px;">
    <div style="font-size:.78rem;font-weight:700;color:var(--red-dark);margin-bottom:2px;">Float Literal Suffix Gotcha</div>
    <div style="font-size:.7rem;color:var(--slate);">
      Writing <span class="mono">float f = 3.14;</span> causes a <strong>compile-time error</strong>! In Java, <span class="mono">3.14</span> is treated as a <span class="mono">double</span> by default. You MUST write <span class="mono">3.14f</span>!
    </div>
  </div>

  <div v-click class="mem-box" style="margin-top:6px;">
    <div class="mem-header">Precision Comparison</div>
    <div class="mem-row">
      <div class="mem-name">float</div>
      <div class="mem-val">4 bytes (32-bit)</div>
      <div class="mem-type">6–7 digits</div>
    </div>
    <div class="mem-row">
      <div class="mem-name">double</div>
      <div class="mem-val">8 bytes (64-bit)</div>
      <div class="mem-type">15–16 digits</div>
    </div>
  </div>

  <div v-click class="callout callout-info" style="margin-top:6px;">
    <div><strong>Best Practice:</strong> Always use <span class="mono">double</span> for general math and scientific formulas. Use <span class="mono">BigDecimal</span> for exact currency/monetary calculations to prevent floating-point rounding errors!</div>
  </div>

</div>

</div>

  </template>
</Slide2>
