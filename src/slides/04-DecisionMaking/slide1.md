---
theme: default
title: Java Decision Making
titleTemplate: '%s — Java Fundamentals'
highlighter: shiki
lineNumbers: true
drawings:
  persist: false
transition: slide-left
mdc: true
colorSchema: light
fonts:
  sans: 'Nunito'
  mono: 'Fira Code'
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 1 — WHAT IS DECISION MAKING?
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Decision-making statements">
  <template #content>
<div class="slide-h1" style="margin-bottom:12px;">What is <span class="highlight">Decision Making?</span></div>

<div class="g2" style="gap:14px;">

<div class="flex-col" style="gap:10px;">
  <div v-click class="callout callout-info">
    <div style="font-size:.82rem;line-height:1.6;color:var(--slate);">
      <strong>Definition:</strong> <strong style="color:var(--red);">Decision making</strong> (conditional execution) allows a program to evaluate a boolean condition and execute specific code blocks <strong style="color:var(--green);">only when</strong> that condition evaluates to <span style="color:var(--blue);">true</span>.
    </div>
  </div>

  <div v-click class="callout callout-success">
    <div>Think of a <strong>traffic signal</strong> — cars stop when red, prepare when yellow, and move only when green!</div>
  </div>

  <div v-click class="card" style="border:1px solid #ef5050;">
    <div class="slide-h3" style="margin-bottom:8px;">Real-life Analogy</div>
    <div class="body-text">
      <strong>IF</strong> temperature &gt; 35°C<br>
      &nbsp;&nbsp;&nbsp;&nbsp;→ Turn on Air Conditioner ❄️<br>
      <strong>ELSE</strong><br>
      &nbsp;&nbsp;&nbsp;&nbsp;→ Keep Fan Running 🌀
    </div>
  </div>

  <div v-click class="callout callout-warn">
    <div><strong>Key rule:</strong> In Java, decision conditions must always evaluate to a <strong>boolean value</strong> (<code>true</code> or <code>false</code>).</div>
  </div>
</div>

<div class="flex-col" style="gap:10px;">
  <div class="slide-h3" v-click style="margin-bottom:4px;">Conditional Execution Flow</div>

  <div v-after style="display:flex;flex-direction:column;align-items:center;gap:4px;">
    <div class="flow-v-box" style="background:#ebf8ff;border:1px solid #3182ce;color:#2b6cb0;">▶ Program Execution Begins</div>
    <div class="flow-v-arrow">▼</div>
    <div class="flow-v-box" style="background:var(--red-soft);border:2px solid var(--red);color:var(--red-dark);">🔎 Evaluate Boolean Condition</div>
    <div style="display:flex;gap:20px;align-items:flex-start;margin-top:4px;">
      <div class="flex-col" style="align-items:center;gap:4px;">
        <div style="font-size:.7rem;font-weight:800;color:var(--green);">TRUE</div>
        <div class="flow-v-arrow" style="color:var(--green);">▼</div>
        <div class="flow-v-box" style="background:#f0fff4;border:1px solid var(--green);color:var(--green);min-width:100px;">Execute Code Block A</div>
      </div>
      <div class="flex-col" style="align-items:center;gap:4px;">
        <div style="font-size:.7rem;font-weight:800;color:var(--red);">FALSE</div>
        <div class="flow-v-arrow" style="color:var(--red);">▼</div>
        <div class="flow-v-box" style="background:var(--red-soft);border:1px solid var(--red);color:var(--red-dark);min-width:100px;">Execute Code Block B / Skip</div>
      </div>
    </div>
    <div class="flow-v-arrow" style="margin-top:4px;">▼</div>
    <div class="flow-v-box" style="background:#fffff0;border:1px solid var(--yellow);color:#744210;">Continue Sequential Execution</div>
  </div>
</div>

</div>
  </template>
</Slide2>
