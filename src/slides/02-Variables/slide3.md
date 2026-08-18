---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 3 — MEMORY VISUALIZATION: PRIMITIVE VARIABLE
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Java Variables">
  <template #content>

<div class="slide-h1" style="margin-bottom:10px;">Memory Visualization — <span class="highlight">Primitive Variable</span></div>

<div class="g2" style="gap:14px;">

<div class="flex-col">

  <div v-click class="card-navy" style="border-radius:10px;">
    <div style="font-size:.82rem;line-height:1.6;color:var(--slate);">
      <strong style="color:var(--red);">Definition:</strong> A <strong>primitive variable</strong> stores its value <strong>directly inside</strong> the variable's memory slot on the stack. The box itself contains the data.
    </div>
  </div>

  <div v-click class="section-label">Code</div>
  <div v-after style="background:#f6f8fa;border-radius:10px;border:1px solid #e1e4e8;padding:14px;font-family:'Fira Code',monospace;font-size:.8rem;line-height:2;">
    <span style="color:#6b7280;">// Declaring a primitive variable</span><br>
    <span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">age</span> = <span style="color:#b45309;">20</span>;<br>
    <span style="color:#6b7280;">// The value 20 lives INSIDE the box 'age'</span>
  </div>

  <div v-click class="section-label" style="margin-top:4px;">Memory Diagram</div>
  <div v-after class="mem-box">
    <div class="mem-header">Stack Memory</div>
    <div class="mem-row">
      <div class="mem-name">age</div>
      <div class="mem-val">20</div>
      <div class="mem-type">int · 4B</div>
    </div>
  </div>

  <div v-click class="callout callout-success" style="margin-top:4px;">
    <div><strong>Key insight:</strong> The value <strong>20</strong> lives physically inside the box labelled <strong>age</strong>. No pointer, no indirection — direct access!</div>
  </div>

</div>

<div class="flex-col">

  <div v-click class="section-label">Visual Box Model</div>

  <div v-after style="display:flex;flex-direction:column;align-items:center;gap:6px;margin-top:4px;">
    <div style="font-size:.65rem;color:var(--muted);text-transform:uppercase;letter-spacing:1px;font-weight:600;">Stack</div>
    <div style="border:3px solid var(--blue);border-radius:12px;padding:6px;background:#ebf8ff;width:100%;max-width:260px;">
      <div style="font-size:.58rem;color:var(--blue);font-weight:700;text-transform:uppercase;letter-spacing:1px;margin-bottom:4px;text-align:center;">Method Frame</div>
      <div style="border:2px solid var(--red);border-radius:8px;padding:14px;background:#fff;text-align:center;">
        <div style="font-size:.58rem;color:var(--muted);font-weight:700;text-transform:uppercase;letter-spacing:1px;margin-bottom:4px;">Variable: <span style="color:var(--blue);">age</span> &nbsp;|&nbsp; Type: <span style="color:var(--red-dark);">int</span></div>
        <div style="font-family:'Fira Code',monospace;font-size:1.4rem;font-weight:800;color:var(--green);">20</div>
        <div style="font-size:.58rem;color:var(--muted);margin-top:4px;">value stored directly here</div>
      </div>
    </div>

  </div>

  <div v-click style="margin-top:8px;display:flex;flex-direction:column;gap:6px;">
    <div class="section-label">More Primitive Variables</div>
    <div class="mem-box">
      <div class="mem-header">Stack Memory</div>
      <div class="mem-row">
        <div class="mem-name">age</div>
        <div class="mem-val">20</div>
        <div class="mem-type">int</div>
      </div>
      <div class="mem-row">
        <div class="mem-name">marks</div>
        <div class="mem-val">95.5</div>
        <div class="mem-type">double</div>
      </div>
      <div class="mem-row">
        <div class="mem-name">pass</div>
        <div class="mem-val">true</div>
        <div class="mem-type">boolean</div>
      </div>
    </div>
  </div>

  <div v-click class="card card-orange" style="margin-top:4px;">
    <div class="small-text">All 8 Java primitive types (<span class="mono">byte, short, int, long, float, double, char, boolean</span>) follow this same direct-storage model.</div>
  </div>

</div>

</div>

  </template>
</Slide2>
