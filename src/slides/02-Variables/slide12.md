---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 12 — VARIABLE SCOPE
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Java Variables">
  <template #content>

<div class="slide-h1" style="margin-bottom:10px;">Variable <span class="highlight">Scope</span></div>

<div class="g2" style="gap:14px;">

<div class="flex-col">

  <div v-click class="card-navy" style="border-radius:10px;">
    <div style="font-size:.82rem;line-height:1.6;color:var(--slate);">
      <strong style="color:var(--red);">Definition:</strong> <strong>Scope</strong> is the region of code where a variable is accessible (visible). In Java, scope is determined by the <strong>block</strong> <span class="mono">{ }</span> in which the variable is declared.
    </div>
  </div>

  <div style="display:flex;flex-direction:column;gap:5px;">
    <div v-click class="card" style="padding:8px 14px;">
      <div style="display:flex;gap:8px;align-items:center;">
        <span class="pill pill-orange">Block Scope</span>
        <div class="body-text">Variable declared in <span class="mono">if/for/while { }</span> — dies at the closing brace</div>
      </div>
    </div>
    <div v-click class="card" style="padding:8px 14px;">
      <div style="display:flex;gap:8px;align-items:center;">
        <span class="pill pill-blue">Method Scope</span>
        <div class="body-text">Local variable declared in a method — accessible anywhere in that method</div>
      </div>
    </div>
    <div v-click class="card" style="padding:8px 14px;">
      <div style="display:flex;gap:8px;align-items:center;">
        <span class="pill pill-green">Class Scope</span>
        <div class="body-text">Instance / static variable — accessible in all methods of the class</div>
      </div>
    </div>
  </div>

  <div v-click class="callout callout-info" style="margin-top:4px;">
    <div>Java uses <strong>block scope</strong> — every pair of <span class="mono">{ }</span> creates a new scope level. Variables declared inside a nested block are not visible in the outer block.</div>
  </div>

</div>

<div class="flex-col">

  <div v-click class="section-label">Nested Scope Diagram</div>

  <div v-after style="font-family:'Fira Code',monospace;font-size:.7rem;line-height:1.8;background:#f6f8fa;border-radius:10px;border:1px solid #e1e4e8;padding:14px;">
    <span style="color:#ef5050;">class</span> <span style="color:#0e6ead;">Example</span> {   <span style="color:#6b7280;">// ── CLASS SCOPE ────────┐</span><br>
    &nbsp;&nbsp;<span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">x</span> = <span style="color:#b45309;">10</span>; &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#6b7280;">// x: class scope     │</span><br><br>
    &nbsp;&nbsp;<span style="color:#ef5050;">void</span> <span style="color:#2d7a00;">method</span>() { &nbsp;&nbsp;&nbsp;<span style="color:#6b7280;">// ── METHOD SCOPE ───┐ │</span><br>
    &nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">y</span> = <span style="color:#b45309;">20</span>; &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#6b7280;">// y: method scope   │ │</span><br><br>
    &nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#ef5050;">if</span> (<span style="color:#b45309;">true</span>) { &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#6b7280;">// ── BLOCK SCOPE ──┐ │ │</span><br>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">z</span> = <span style="color:#b45309;">30</span>; &nbsp;&nbsp;&nbsp;<span style="color:#6b7280;">// z: block scope  │ │ │</span><br>
    &nbsp;&nbsp;&nbsp;&nbsp;} &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#6b7280;">// z dies here ────┘ │ │</span><br>
    &nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#6b7280;">// z not accessible    │ │</span><br>
    &nbsp;&nbsp;} &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#6b7280;">// y dies here ──────┘ │</span><br>
    } &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#6b7280;">// x dies here ─────────┘</span>
  </div>

  <div v-click class="callout callout-danger" style="margin-top:6px;">
    <div><strong>Rule:</strong> You can access variables from outer scopes inside inner blocks, but <strong>not the other way around</strong>. Inner → Outer: ✔ &nbsp; Outer → Inner: ✘</div>
  </div>

</div>

</div>

  </template>
</Slide2>
