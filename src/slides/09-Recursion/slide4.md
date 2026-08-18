---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 4 — CALL STACK DIAGRAM (STACK FRAMES)
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Recursion">
  <template #content>

<div class="slide-h1" style="margin-bottom:10px;">Java <span class="highlight">Call Stack</span></div>

<div class="g2" style="gap:14px;">

<div class="flex-col">

  <div v-click class="card-navy" style="border-radius:10px;">
    <div style="font-size:.8rem;line-height:1.7;color:var(--slate);">
      The <strong style="color:var(--red);">call stack</strong> is a memory region that tracks all active method calls. Each call gets a <strong style="color:var(--blue);">stack frame</strong> holding its local variables, parameter values, and the return address back to the caller.
    </div>
  </div>

  <div v-click class="code-block" style="margin-top:4px;">
    <span style="color:#ef5050;">static int</span> <span style="color:#0e6ead;">factorial</span>(<span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">n</span>) {<br>
    <span style="padding-left:20px;display:block;"><span style="color:#ef5050;">if</span> (<span style="color:#0e6ead;">n</span> == <span style="color:#b45309;">1</span>) <span style="color:#ef5050;">return</span> <span style="color:#b45309;">1</span>;</span>
    <span style="padding-left:20px;display:block;"><span style="color:#ef5050;">return</span> <span style="color:#0e6ead;">n</span> * <span style="color:#0e6ead;">factorial</span>(<span style="color:#0e6ead;">n</span> - <span style="color:#b45309;">1</span>);</span>
    }<br>
    <span style="color:#6b7280;">// factorial(3) called from main()</span>
  </div>

  <div v-click class="callout callout-warn" style="font-size:.7rem;">
    <div><strong>Stack overflow risk!</strong> Deep recursion fills the JVM stack. Java's default stack size allows roughly <strong>500–1000 frames</strong> (JVM-dependent). Unlike Python, there's no built-in call to increase this at runtime.</div>
  </div>

  <div v-click class="card-orange" style="font-size:.75rem;">
    <strong>Each stack frame stores:</strong>
    <div style="display:flex;gap:6px;flex-wrap:wrap;margin-top:6px;">
      <span class="pill pill-orange">parameter n</span>
      <span class="pill pill-blue">local variables</span>
      <span class="pill pill-purple">return address</span>
      <span class="pill pill-red">partial result</span>
    </div>
  </div>

</div>

<div class="flex-col">

  <div v-click class="section-label">Stack Growth — factorial(3) Winding</div>

  <div style="background:#f7f8fc;border:1px solid var(--border);border-radius:10px;padding:12px 16px;">
    <div v-after class="small-text" style="text-align:center;margin-bottom:8px;font-weight:700;">CALL STACK (grows downward ↓)</div>
    <div v-click class="stack-frame top">factorial(3) &nbsp; n=3 &nbsp; waiting for factorial(2)...</div>
    <div v-click class="stack-frame middle">factorial(2) &nbsp; n=2 &nbsp; waiting for factorial(1)...</div>
    <div v-click class="stack-frame" style="border-color:var(--blue);background:#ebf8ff;color:#2b6cb0;">factorial(1) &nbsp; n=1 &nbsp; returns 1 ← base case</div>
    <div class="small-text" style="text-align:center;margin-top:8px;" v-click>▲ Stack unwinds from here</div>
  </div>

  <div v-click class="section-label" style="margin-top:8px;">Stack Unwinding — frames pop and return</div>

  <div style="background:#f7f8fc;border:1px solid var(--border);border-radius:10px;padding:12px 16px;">
    <div class="stack-frame done" v-click>factorial(1) → returns 1 &nbsp; ✔ popped</div>
    <div class="stack-frame done" v-click>factorial(2) → 2 × 1 = 2 &nbsp; ✔ popped</div>
    <div class="stack-frame done" v-click>factorial(3) → 3 × 2 = 6 &nbsp; ✔ popped</div>
    <div class="small-text" style="text-align:center;margin-top:8px;color:var(--green);font-weight:700;" v-click>Final result: 6 returned to main()</div>
  </div>

</div>

</div>

  </template>
</Slide2>
