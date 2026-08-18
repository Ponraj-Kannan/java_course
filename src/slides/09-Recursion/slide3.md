---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 3 — FACTORIAL: CLASSIC EXAMPLE + CALL DIAGRAM
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Recursion">
  <template #content>

<div class="slide-h1" style="margin-bottom:10px;"><span class="highlight">Factorial</span> — Classic Recursion Example</div>

<div class="g2" style="gap:14px;">

<div class="flex-col">

  <div v-click class="section-label">Two Phases of Recursion</div>

  <div class="g2" style="gap:8px;">
    <div v-click class="card-blue" style="text-align:center;">
      <div class="slide-h3" style="color:var(--blue);">Winding Phase</div>
      <div class="small-text" style="margin-top:4px;">Method keeps calling itself — stack frames pile up.</div>
    </div>
    <div v-click class="card-purple" style="text-align:center;">
      <div class="slide-h3" style="color:var(--purple);">Unwinding Phase</div>
      <div class="small-text" style="margin-top:4px;">Base case hit — frames return values and pop off one by one.</div>
    </div>
  </div>

  <div v-click class="code-block" style="margin-top:6px;">
    <span style="color:#6b7280;">// factorial(n) = n × (n-1) × ... × 1</span><br>
    <span style="color:#ef5050;">static int</span> <span style="color:#0e6ead;">factorial</span>(<span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">n</span>) {<br>
    <span style="padding-left:20px;display:block;"><span style="color:#ef5050;">if</span> (<span style="color:#0e6ead;">n</span> == <span style="color:#b45309;">1</span>) <span style="color:#ef5050;">return</span> <span style="color:#b45309;">1</span>; <span style="color:#6b7280;">// base case</span></span>
    <span style="padding-left:20px;display:block;"><span style="color:#ef5050;">return</span> <span style="color:#0e6ead;">n</span> * <span style="color:#0e6ead;">factorial</span>(<span style="color:#0e6ead;">n</span> - <span style="color:#b45309;">1</span>); <span style="color:#6b7280;">// recursive</span></span>
    }
  </div>

  <div v-click class="output-box" style="font-size:.72rem;">factorial(4) = 24</div>

  <div v-click class="callout callout-warn" style="font-size:.7rem;">
    <div><strong>Think of recursion in two directions:</strong> DOWN (calling, each frame waiting) and UP (returning, results combining). The final answer travels back up the chain.</div>
  </div>

</div>

<div class="flex-col">
  <div v-click class="section-label">Step-by-Step — factorial(4) Winding</div>

  <div style="display:flex;flex-direction:column;gap:3px;padding:4px 0;">
    <div v-click style="display:flex;align-items:center;gap:6px;">
      <div class="flow-node flow-call" style="flex:1;">factorial(4)</div>
      <div class="small-text">→ 4 * factorial(3)</div>
    </div>
    <div v-click style="display:flex;align-items:center;gap:6px;padding-left:14px;">
      <div class="flow-node flow-call" style="flex:1;">factorial(3)</div>
      <div class="small-text">→ 3 * factorial(2)</div>
    </div>
    <div v-click style="display:flex;align-items:center;gap:6px;padding-left:28px;">
      <div class="flow-node flow-call" style="flex:1;">factorial(2)</div>
      <div class="small-text">→ 2 * factorial(1)</div>
    </div>
    <div v-click style="display:flex;align-items:center;gap:6px;padding-left:42px;">
      <div class="flow-node flow-end" style="flex:1;">factorial(1) = 1</div>
      <div class="small-text">Base case!</div>
    </div>
  </div>

  <div v-click class="section-label" style="margin-top:4px;">Unwinding — return values propagate up</div>

  <div style="display:flex;flex-direction:column;gap:3px;padding:4px 0;">
    <div v-click style="display:flex;align-items:center;gap:6px;padding-left:28px;">
      <div class="flow-node flow-return" style="flex:1;">factorial(2) = 2 × 1 = 2</div>
    </div>
    <div v-click style="display:flex;align-items:center;gap:6px;padding-left:14px;">
      <div class="flow-node flow-return" style="flex:1;">factorial(3) = 3 × 2 = 6</div>
    </div>
    <div v-click style="display:flex;align-items:center;gap:6px;">
      <div class="flow-node flow-body" style="flex:1;">factorial(4) = 4 × 6 = <strong>24</strong></div>
    </div>
  </div>

  <div v-click class="card card-green" style="margin-top:4px;">
    <div class="small-text"><strong>Pattern:</strong> <span class="pill pill-blue">Down</span> divides the problem. <span class="pill pill-purple">Up</span> combines the answers.</div>
  </div>

</div>

</div>

  </template>
</Slide2>
