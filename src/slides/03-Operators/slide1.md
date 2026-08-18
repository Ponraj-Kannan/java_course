---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 1 — INTRODUCTION TO JAVA OPERATORS
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Operators">
  <template #content>

<div class="slide-h1" style="margin-bottom:10px;">Introduction to Java <span class="highlight">Operators</span></div>

<div class="g2" style="gap:14px;align-items:start;">

<div class="flex-col">

  <div v-click class="card-navy" style="border-radius:10px;">
    <div style="font-size:.82rem;line-height:1.6;color:var(--slate);">
      <strong style="color:var(--red);">Definition:</strong> An <strong>operator</strong> is a special <strong>symbol</strong> that instructs the Java compiler to perform a specific <strong>mathematical, relational, or logical operation</strong> on values or variables (called <em>operands</em>).
    </div>
  </div>

  <div v-click class="callout callout-warn">
    <div><strong>Anatomy of an expression:</strong> In <span class="mono">int sum = a + b;</span> the <span class="mono" style="color:var(--red);">+</span> is the operator, while <span class="mono">a</span> and <span class="mono">b</span> are the operands.</div>
  </div>

  <div v-click style="background:#f6f8fa;border-radius:10px;border:1px solid #e1e4e8;padding:14px;font-family:'Fira Code',monospace;font-size:.74rem;line-height:2;">
    <span style="color:#6b7280;">// Java Operator in Action</span><br>
    <span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">a</span> = <span style="color:#b45309;">10</span>; &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#6b7280;">// operand 1</span><br>
    <span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">b</span> = <span style="color:#b45309;">3</span>; &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#6b7280;">// operand 2</span><br>
    <span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">result</span> = <span style="color:#0e6ead;">a</span> <span style="color:#ef5050;">+</span> <span style="color:#0e6ead;">b</span>; &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#6b7280;">// '+' is the operator</span><br>
    <span style="color:#0e6ead;">System</span>.<span style="color:#0e6ead;">out</span>.<span style="color:#2d7a00;">println</span>(<span style="color:#0e6ead;">result</span>); <span style="color:#6b7280;">// 13</span>
  </div>

</div>

<div class="flex-col">
  <div class="section-label" v-click>Java Operator Categories</div>

  <div style="display:flex;flex-direction:column;gap:5px;">
    <div style="display:flex;gap:6px;flex-wrap:wrap;" v-click>
      <span class="pill pill-red">Arithmetic</span>
      <span class="small-text" style="align-self:center;">— +  −  *  /  %</span>
    </div>
    <div style="display:flex;gap:6px;flex-wrap:wrap;" v-click>
      <span class="pill pill-purple">Unary</span>
      <span class="small-text" style="align-self:center;">— +  −  ++  --  !  ~</span>
    </div>
    <div style="display:flex;gap:6px;flex-wrap:wrap;" v-click>
      <span class="pill pill-blue">Assignment</span>
      <span class="small-text" style="align-self:center;">— =  +=  -=  *=  /=  %=</span>
    </div>
    <div style="display:flex;gap:6px;flex-wrap:wrap;" v-click>
      <span class="pill pill-orange">Relational</span>
      <span class="small-text" style="align-self:center;">— ==  !=  >  &lt;  >=  &lt;=</span>
    </div>
    <div style="display:flex;gap:6px;flex-wrap:wrap;" v-click>
      <span class="pill pill-green">Logical</span>
      <span class="small-text" style="align-self:center;">— &amp;&amp;  ||  !</span>
    </div>
    <div style="display:flex;gap:6px;flex-wrap:wrap;" v-click>
      <span class="pill pill-navy">Bitwise</span>
      <span class="small-text" style="align-self:center;">— &amp;  |  ^  ~  &lt;&lt;  &gt;&gt;  &gt;&gt;&gt;</span>
    </div>
    <div style="display:flex;gap:6px;flex-wrap:wrap;" v-click>
      <span class="pill" style="background:#f0e6ff;color:#6b21a8;">Special / Conditional</span>
      <span class="small-text" style="align-self:center;">— instanceof  ? :</span>
    </div>
  </div>

  <div v-click class="callout callout-info" style="margin-top:6px;">
    <div>Operators form the <strong>foundation of expressions and algorithms</strong> in Java — enabling everything from arithmetic calculations to complex logic.</div>
  </div>

</div>

</div>

  </template>
</Slide2>
