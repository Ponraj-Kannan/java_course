---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 2 — HOW A VARIABLE IS CREATED (Step-by-Step)
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Java Variables">
  <template #content>

<div class="slide-h1" style="margin-bottom:10px;">What Happens When a Variable is <span class="highlight">Created?</span></div>

<div class="g2" style="gap:14px;">

<div class="flex-col">

  <div v-click class="section-label">The Statement</div>
  <div v-after style="background:#f6f8fa;border-radius:10px;border:1px solid #e1e4e8;padding:14px;font-family:'Fira Code',monospace;font-size:.88rem;line-height:2.2;">
    <span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">age</span> <span style="color:#c49a00;">=</span> <span style="color:#b45309;">20</span><span style="color:#718096;">;</span>
  </div>

  <div v-click class="section-label" style="margin-top:6px;">Step-by-Step: What Java Does</div>

  <div style="display:flex;flex-direction:column;gap:6px;">
    <div style="display:flex;align-items:flex-start;gap:10px;" v-click>
      <div style="background:var(--red);color:#fff;border-radius:50%;width:24px;height:24px;display:flex;align-items:center;justify-content:center;font-size:.7rem;font-weight:800;flex-shrink:0;">1</div>
      <div class="body-text"><strong>Declaration:</strong> The compiler reserves the name <span class="mono" style="color:var(--blue);">age</span> with type <span class="mono" style="color:var(--red-dark);">int</span> — the type is locked forever.</div>
    </div>
    <div style="display:flex;align-items:flex-start;gap:10px;" v-click>
      <div style="background:var(--blue);color:#fff;border-radius:50%;width:24px;height:24px;display:flex;align-items:center;justify-content:center;font-size:.7rem;font-weight:800;flex-shrink:0;">2</div>
      <div class="body-text"><strong>Memory Allocation:</strong> The JVM allocates a memory slot (4 bytes for <span class="mono">int</span>) on the <strong>stack</strong> to hold the value.</div>
    </div>
    <div style="display:flex;align-items:flex-start;gap:10px;" v-click>
      <div style="background:var(--green);color:#fff;border-radius:50%;width:24px;height:24px;display:flex;align-items:center;justify-content:center;font-size:.7rem;font-weight:800;flex-shrink:0;">3</div>
      <div class="body-text"><strong>Assignment:</strong> The value <span class="mono" style="color:var(--green);">20</span> is stored directly inside that memory slot.</div>
    </div>
    <div style="display:flex;align-items:flex-start;gap:10px;" v-click>
      <div style="background:var(--orange);color:#fff;border-radius:50%;width:24px;height:24px;display:flex;align-items:center;justify-content:center;font-size:.7rem;font-weight:800;flex-shrink:0;">4</div>
      <div class="body-text"><strong>Name Binding:</strong> The compiler maps the name <span class="mono" style="color:var(--blue);">age</span> to that memory location — every time you write <span class="mono">age</span>, Java reads that slot.</div>
    </div>
  </div>

  <div v-click class="callout callout-info" style="margin-top:4px;">
    <div>Steps 1–4 happen at compile-time and JVM startup. Once declared, <strong>the type cannot change</strong> — Java is statically typed.</div>
  </div>

</div>

<div class="flex-col">

  <div v-click class="section-label">Memory Visualization</div>

  <div v-after class="mem-box">
    <div class="mem-header">Stack Memory (Method Frame)</div>
    <div class="mem-row">
      <div class="mem-name">age</div>
      <div class="mem-val">20</div>
      <div class="mem-type">int</div>
    </div>
  </div>

  <div v-click class="section-label" style="margin-top:6px;">Step Flow</div>
  <div v-after style="display:flex;align-items:center;gap:6px;flex-wrap:wrap;">
    <div class="step-box active">Declare Type</div>
    <div class="step-arrow">→</div>
    <div class="step-box active">Allocate Memory</div>
    <div class="step-arrow">→</div>
    <div class="step-box active">Store Value</div>
    <div class="step-arrow">→</div>
    <div class="step-box" style="border-color:var(--green);background:#f0fff4;color:var(--green);">Bind Name</div>
  </div>

  <div v-click class="card card-orange" style="margin-top:6px;">
    <div class="small-text"><strong>Java vs Python:</strong> In Python, a variable is just a <em>label</em> pointing to an object. In Java, a primitive variable <em>directly contains</em> the value in its memory slot — no indirection.</div>
  </div>

  <div v-click class="callout callout-danger" style="margin-top:4px;">
    <div><strong>Local variable rule:</strong> Java does NOT automatically initialize local variables. You <strong>must assign a value before use</strong>, or the compiler will refuse to compile!</div>
  </div>

</div>

</div>

  </template>
</Slide2>
