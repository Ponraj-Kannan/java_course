---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 13 — TYPE CASTING (WIDENING VS NARROWING)
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Data Types">
  <template #content>

<div class="slide-h1" style="margin-bottom:10px;">Type Casting — <span class="highlight">Widening &amp; Narrowing</span></div>

<div class="g2" style="gap:14px;">

<div class="flex-col">

  <div v-click class="card-navy" style="border-radius:10px;">
    <div style="font-size:.8rem;line-height:1.6;color:var(--slate);">
      <strong style="color:var(--red);">Definition:</strong> <strong>Type casting</strong> is the conversion of a variable or expression from one primitive data type to another.
    </div>
  </div>

  <div v-click class="section-label" style="margin-top:4px;">1. Widening Casting (Implicit / Automatic)</div>
  <div v-after class="card-green" style="padding:8px 12px;font-size:.7rem;color:var(--slate);">
    Converts a smaller data type to a larger data type automatically. <strong>No data loss!</strong>
  </div>
  <div v-after style="background:#f6f8fa;border-radius:8px;border:1px solid #e1e4e8;padding:8px 12px;font-family:'Fira Code',monospace;font-size:.7rem;">
    <span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">myInt</span> = <span style="color:#b45309;">9</span>;<br>
    <span style="color:#ef5050;">double</span> <span style="color:#0e6ead;">myDouble</span> = <span style="color:#0e6ead;">myInt</span>; <span style="color:#6b7280;">// Implicit: 9.0</span>
  </div>

  <div v-click class="section-label" style="margin-top:4px;">2. Narrowing Casting (Explicit / Manual)</div>
  <div v-after class="card-red" style="padding:8px 12px;font-size:.7rem;color:var(--slate);">
    Converts a larger type to a smaller type manually using <span class="mono">(type)</span>. <strong>May lose data!</strong>
  </div>
  <div v-after style="background:#f6f8fa;border-radius:8px;border:1px solid #e1e4e8;padding:8px 12px;font-family:'Fira Code',monospace;font-size:.7rem;">
    <span style="color:#ef5050;">double</span> <span style="color:#0e6ead;">pi</span> = <span style="color:#b45309;">3.14159</span>;<br>
    <span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">intPi</span> = (<span style="color:#ef5050;">int</span>) <span style="color:#0e6ead;">pi</span>; <span style="color:#6b7280;">// Explicit: 3 (truncated!)</span>
  </div>

</div>

<div class="flex-col">

  <div v-click class="section-label">Widening Type Hierarchy Pipeline</div>
  <div v-after class="step-flow" style="margin-top:4px;">
    <div class="step-box active">byte</div>
    <div class="step-arrow">→</div>
    <div class="step-box active">short</div>
    <div class="step-arrow">→</div>
    <div class="step-box active">char</div>
    <div class="step-arrow">→</div>
    <div class="step-box active">int</div>
    <div class="step-arrow">→</div>
    <div class="step-box active">long</div>
    <div class="step-arrow">→</div>
    <div class="step-box active">float</div>
    <div class="step-arrow">→</div>
    <div class="step-box active">double</div>
  </div>

  <div v-click class="callout callout-warn" style="margin-top:10px;">
    <div><strong>Data Truncation Warning:</strong> Explicit narrowing from <span class="mono">double</span> to <span class="mono">int</span> or <span class="mono">int</span> to <span class="mono">byte</span> discards fractional parts or causes overflow wrap-around!</div>
  </div>

</div>

</div>

  </template>
</Slide2>
