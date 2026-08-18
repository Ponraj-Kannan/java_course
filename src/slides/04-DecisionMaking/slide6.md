---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 6 — IF-ELSE STATEMENT
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Decision-making statements">
  <template #content>
<div class="slide-h1" style="margin-bottom:12px;">The <span class="highlight">if-else</span> Statement</div>

<div class="g2" style="gap:14px;">

<div class="flex-col" style="gap:10px;">
  <div v-click class="callout callout-info">
    <div style="font-size:.8rem;line-height:1.5;color:var(--slate);">
      <strong>Definition:</strong> An <strong style="color:var(--yellow);">if-else statement</strong> provides a <strong style="color:var(--green);">two-way branch</strong>, executing the <code>if</code> block when the condition evaluates to <code>true</code> and the <code>else</code> block when it evaluates to <code>false</code>.
    </div>
  </div>

  <div v-click class="card" style="border:1px solid var(--green);">
    <div class="slide-h3" style="margin-bottom:8px;">Java Syntax</div>
    <div style="font-family:'Fira Code',monospace;font-size:.78rem;line-height:1.9;background:#1a1f36;padding:10px 14px;border-radius:6px;color:#f8f8f2;">
      <span style="color:#ff79c6;">if</span> <span style="color:#f1fa8c;">(</span><span style="color:#61dafb;">condition</span><span style="color:#f1fa8c;">) {</span><br>
      &nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#a8ff78;">// runs when condition is true</span><br>
      <span style="color:#f1fa8c;">}</span> <span style="color:#ff79c6;">else</span> <span style="color:#f1fa8c;">{</span><br>
      &nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#ff9900;">// runs when condition is false</span><br>
      <span style="color:#f1fa8c;">}</span>
    </div>
  </div>

  <div v-click class="callout callout-info">
    <div><strong>Key rule:</strong> <code>else</code> never has a condition of its own and cannot exist without a preceding <code>if</code>. Exactly <strong>one</strong> of the two blocks will execute!</div>
  </div>
</div>

<div class="flex-col" style="gap:10px;">
  <div class="slide-h3" v-click style="margin-bottom:4px;">Execution Flow</div>

  <div v-after style="display:flex;flex-direction:column;align-items:center;gap:4px;">
    <div class="flow-v-box" style="background:#ebf8ff;border:1px solid #3182ce;color:#2b6cb0;">▶ Reaches if-else statement</div>
    <div class="flow-v-arrow">▼</div>
    <div class="flow-v-box" style="background:var(--red-soft);border:2px solid var(--red);color:var(--red-dark);">🔎 Evaluate (condition)</div>
    <div style="display:flex;gap:20px;align-items:flex-start;margin-top:4px;">
      <div class="flex-col" style="align-items:center;gap:4px;">
        <div style="font-size:.7rem;font-weight:800;color:var(--green);">true</div>
        <div class="flow-v-arrow" style="color:var(--green);">▼</div>
        <div class="flow-v-box" style="background:#f0fff4;border:1px solid var(--green);color:var(--green);min-width:110px;">Execute if block</div>
      </div>
      <div class="flex-col" style="align-items:center;gap:4px;">
        <div style="font-size:.7rem;font-weight:800;color:var(--red);">false</div>
        <div class="flow-v-arrow" style="color:var(--red);">▼</div>
        <div class="flow-v-box" style="background:var(--red-soft);border:1px solid var(--red);color:var(--red-dark);min-width:110px;">Execute else block</div>
      </div>
    </div>
    <div class="flow-v-arrow" style="margin-top:4px;">▼</div>
    <div class="flow-v-box" style="background:#fffff0;border:1px solid var(--yellow);color:#744210;">Continue program</div>
  </div>
</div>

</div>
  </template>
</Slide2>
