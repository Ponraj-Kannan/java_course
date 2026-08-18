---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 5 — SUM OF N NATURAL NUMBERS (LINEAR RECURSION)
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Recursion">
  <template #content>

<div class="slide-h1" style="margin-bottom:10px;">Sum of N Natural Numbers — <span class="highlight">Linear Recursion</span></div>

<div class="g2" style="gap:14px;">

<div class="flex-col">
  <div v-click class="section-label">Java Code</div>

  <div v-after class="code-block">
    <span style="color:#6b7280;">// sum(n) = 1 + 2 + ... + n</span><br>
    <span style="color:#ef5050;">static int</span> <span style="color:#0e6ead;">sum</span>(<span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">n</span>) {<br>
    <span style="padding-left:20px;display:block;background:#f0fff4;border-left:3px solid var(--green);"><span style="color:#ef5050;">if</span> (<span style="color:#0e6ead;">n</span> == <span style="color:#b45309;">0</span>) <span style="color:#ef5050;">return</span> <span style="color:#b45309;">0</span>; <span style="color:#6b7280;">// base case</span></span>
    <span style="padding-left:20px;display:block;background:#ebf8ff;border-left:3px solid var(--blue);"><span style="color:#ef5050;">return</span> <span style="color:#0e6ead;">n</span> + <span style="color:#0e6ead;">sum</span>(<span style="color:#0e6ead;">n</span> - <span style="color:#b45309;">1</span>); <span style="color:#6b7280;">// recursive case</span></span>
    }<br>
    <br>
    <span style="color:#6b7280;">// In main():</span><br>
    <span style="color:#0e6ead;">System</span>.<span style="color:#0e6ead;">out</span>.<span style="color:#2d7a00;">println</span>(<span style="color:#0e6ead;">sum</span>(<span style="color:#b45309;">3</span>)); <span style="color:#6b7280;">// 6</span>
  </div>

  <div v-click class="section-label" style="margin-top:6px;">Execution Trace Table</div>

  <div>
    <table class="trace-table">
      <thead v-click><tr><th>Call</th><th>n</th><th>Action</th><th>Returns</th></tr></thead>
      <tbody>
        <tr v-click><td>1st</td><td>3</td><td>3 + sum(2)</td><td>waits</td></tr>
        <tr v-click><td>2nd</td><td>2</td><td>2 + sum(1)</td><td>waits</td></tr>
        <tr v-click><td>3rd</td><td>1</td><td>1 + sum(0)</td><td>waits</td></tr>
        <tr v-click style="background:#f0fff4;"><td>4th</td><td>0</td><td>base case</td><td><strong>0</strong></td></tr>
        <tr v-click><td>3rd</td><td>unwind</td><td>1 + 0</td><td>1</td></tr>
        <tr v-click><td>2nd</td><td>unwind</td><td>2 + 1</td><td>3</td></tr>
        <tr v-click style="background:#ebf8ff;"><td>1st</td><td>unwind</td><td>3 + 3</td><td><strong>6</strong></td></tr>
      </tbody>
    </table>
  </div>

</div>

<div class="flex-col">
  <div v-click class="section-label">Call Flow Diagram</div>

  <div style="display:flex;flex-direction:column;align-items:center;gap:3px;padding:4px 0;">
    <div class="flow-node flow-start" style="width:240px;" v-click>sum(3) called</div>
    <div class="flow-arrow" v-after>▼</div>
    <div class="flow-node flow-call" style="width:240px;" v-click>sum(3) = 3 + sum(2)</div>
    <div class="flow-arrow" v-after>▼</div>
    <div class="flow-node flow-call" style="width:240px;" v-click>sum(2) = 2 + sum(1)</div>
    <div class="flow-arrow" v-after>▼</div>
    <div class="flow-node flow-call" style="width:240px;" v-click>sum(1) = 1 + sum(0)</div>
    <div class="flow-arrow" v-after>▼</div>
    <div class="flow-node flow-end" style="width:240px;" v-click>sum(0) = 0 (base case)</div>
    <div class="flow-arrow" v-after>▲</div>
    <div class="flow-node flow-return" style="width:240px;" v-click>returns 1</div>
    <div class="flow-arrow" v-after>▲</div>
    <div class="flow-node flow-return" style="width:240px;" v-click>returns 3</div>
    <div class="flow-arrow" v-after>▲</div>
    <div class="flow-node flow-body" style="width:240px;" v-click>returns <strong>6</strong></div>
  </div>

  <div v-click class="callout callout-success" style="margin-top:6px;font-size:.7rem;">
    <div>Each call <strong>waits</strong> for the one below to complete. Results are <strong>assembled on the way back up</strong>.</div>
  </div>

</div>

</div>

  </template>
</Slide2>
