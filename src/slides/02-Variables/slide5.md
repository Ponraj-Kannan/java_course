---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 5 — MEMORY VISUALIZATION: MULTIPLE VARIABLES IN A STACK FRAME
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Java Variables">
  <template #content>

<div class="slide-h1" style="margin-bottom:10px;">Memory — <span class="highlight">Stack Frame</span> with Multiple Variables</div>

<div class="g2" style="gap:14px;">

<div class="flex-col">

  <div v-click class="card-navy" style="border-radius:10px;">
    <div style="font-size:.82rem;line-height:1.6;color:var(--slate);">
      <strong style="color:var(--red);">Definition:</strong> When a method runs, Java creates a <strong>stack frame</strong> — a dedicated block of stack memory that holds all local variables declared inside that method. Each variable gets its own labelled slot.
    </div>
  </div>

  <div v-click class="section-label">Example Method</div>
  <div v-after style="background:#f6f8fa;border-radius:10px;border:1px solid #e1e4e8;padding:14px;font-family:'Fira Code',monospace;font-size:.74rem;line-height:1.9;">
    <span style="color:#ef5050;">void</span> <span style="color:#2d7a00;">displayStudent</span>() {<br>
    &nbsp;&nbsp;<span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">age</span> = <span style="color:#b45309;">20</span>;<br>
    &nbsp;&nbsp;<span style="color:#ef5050;">double</span> <span style="color:#0e6ead;">marks</span> = <span style="color:#b45309;">95.5</span>;<br>
    &nbsp;&nbsp;<span style="color:#ef5050;">boolean</span> <span style="color:#0e6ead;">passed</span> = <span style="color:#b45309;">true</span>;<br>
    &nbsp;&nbsp;<span style="color:#ef5050;">String</span> <span style="color:#0e6ead;">name</span> = <span style="color:#2d7a00;">"Alice"</span>;<br>
    }
  </div>

  <div v-click class="callout callout-info" style="margin-top:4px;">
    <div>Each variable in the method gets its own <strong>named slot</strong> in the stack frame. Primitives hold values directly; reference types hold addresses pointing to heap objects.</div>
  </div>

</div>

<div class="flex-col">

  <div v-click class="section-label">Stack Frame Diagram</div>

  <div v-after style="border:3px solid var(--blue);border-radius:12px;padding:8px;background:#ebf8ff;">
    <div style="font-size:.6rem;color:var(--blue);font-weight:700;text-transform:uppercase;letter-spacing:1px;margin-bottom:6px;text-align:center;">Stack — displayStudent() Frame</div>
    <div class="mem-box">
      <div class="mem-header">Local Variables</div>
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
        <div class="mem-name">passed</div>
        <div class="mem-val">true</div>
        <div class="mem-type">boolean</div>
      </div>
      <div class="mem-row">
        <div class="mem-name">name</div>
        <div style="background:#fffaf0;color:var(--orange);padding:6px 12px;font-weight:700;flex:1;display:flex;align-items:center;font-family:'Fira Code',monospace;font-size:.72rem;">ref → heap</div>
        <div class="mem-type">String</div>
      </div>
    </div>
    <div style="margin-top:8px;border:2px solid var(--green);border-radius:8px;padding:8px;background:#f0fff4;text-align:center;">
      <div style="font-size:.58rem;color:var(--green);font-weight:700;text-transform:uppercase;letter-spacing:1px;margin-bottom:4px;">Heap</div>
      <div style="font-family:'Fira Code',monospace;font-size:.82rem;font-weight:700;color:var(--green);">String Object: "Alice"</div>
    </div>
  </div>

  <div v-click class="card card-green" style="margin-top:6px;">
    <div class="small-text"><strong>Lifetime:</strong> When <span class="mono">displayStudent()</span> finishes, its stack frame is destroyed — all local variables (<span class="mono">age, marks, passed, name</span>) cease to exist immediately.</div>
  </div>

</div>

</div>

  </template>
</Slide2>
