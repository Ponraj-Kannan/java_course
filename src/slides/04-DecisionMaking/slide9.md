---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 9 — IF-ELSE-IF LADDER
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Decision-making statements">
  <template #content>
<div class="slide-h1" style="margin-bottom:12px;">The <span class="highlight">if-else-if</span> Ladder</div>

<div class="g2" style="gap:14px;">

<div class="flex-col" style="gap:10px;">
  <div v-click class="callout callout-info">
    <div style="font-size:.8rem;line-height:1.5;color:var(--slate);">
      <strong>Definition:</strong> The <strong style="color:var(--blue);">if-else-if ladder</strong> evaluates multiple conditions sequentially from top to bottom, executing <strong style="color:var(--green);">only the block corresponding to the first true condition</strong> and skipping all remaining branches.
    </div>
  </div>

  <div v-click class="card" style="border:1px solid var(--green);">
    <div class="slide-h3" style="margin-bottom:8px;">Java Syntax</div>
    <div style="font-family:'Fira Code',monospace;font-size:.74rem;line-height:1.9;background:#1a1f36;padding:8px 12px;border-radius:6px;color:#f8f8f2;">
      <span style="color:#ff79c6;">if</span> <span style="color:#f1fa8c;">(</span><span style="color:#61dafb;">condition1</span><span style="color:#f1fa8c;">) {</span><br>
      &nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#a8ff78;">// block 1</span><br>
      <span style="color:#f1fa8c;">}</span> <span style="color:#ff79c6;">else if</span> <span style="color:#f1fa8c;">(</span><span style="color:#61dafb;">condition2</span><span style="color:#f1fa8c;">) {</span><br>
      &nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#a8ff78;">// block 2</span><br>
      <span style="color:#f1fa8c;">}</span> <span style="color:#ff79c6;">else</span> <span style="color:#f1fa8c;">{</span><br>
      &nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#636e80;">// default fallback block</span><br>
      <span style="color:#f1fa8c;">}</span>
    </div>
  </div>
</div>

<div class="flex-col" style="gap:10px;">
  <div v-click style="display:flex;flex-direction:column;align-items:center;gap:4px;">
    <div class="slide-h3" style="margin-bottom:8px;">Execution Order</div>
    <div class="flow-v-box" style="background:var(--red-soft);border:2px solid var(--red);color:var(--red-dark);">if (condition1)?</div>
    <div style="display:flex;width:100%;justify-content:space-between;padding:0 20px;">
      <div style="font-size:.68rem;font-weight:800;color:var(--green);">TRUE → run block 1 &amp; exit ladder</div>
      <div style="font-size:.68rem;font-weight:800;color:var(--red);">FALSE ↓</div>
    </div>
    <div class="flow-v-box" style="background:#ebf8ff;border:2px solid var(--blue);color:#2b6cb0;">else if (condition2)?</div>
    <div style="display:flex;width:100%;justify-content:space-between;padding:0 20px;">
      <div style="font-size:.68rem;font-weight:800;color:var(--green);">TRUE → run block 2 &amp; exit ladder</div>
      <div style="font-size:.68rem;font-weight:800;color:var(--red);">FALSE ↓</div>
    </div>
    <div class="flow-v-box" style="background:#fffaf0;border:2px solid var(--orange);color:#c05621;">else (fallback block)</div>
    <div class="flow-v-arrow">▼</div>
    <div class="flow-v-box" style="background:#f0fff4;border:1px solid var(--green);color:var(--green);">Continue program</div>
  </div>
</div>

</div>
  </template>
</Slide2>
