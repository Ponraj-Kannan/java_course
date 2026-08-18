---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 20 — NAMING RULE 4: Case-Sensitive
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Variable Naming Rules">
  <template #content>

<div class="slide-h1" style="margin-bottom:10px;"><span class="highlight">Rule 4</span> — Case-Sensitive</div>

<div class="g2" style="gap:14px;align-items:start;">

<div class="flex-col">

  <div v-click style="display:flex;gap:10px;align-items:center;margin-bottom:4px;">
    <div style="background:var(--blue);color:#fff;border-radius:8px;padding:6px 16px;font-size:.75rem;font-weight:800;">RULE 4</div>
    <div class="body-text" style="font-size:.82rem;">Java is <strong>case-sensitive</strong>. Variable names that differ only in capitalization are treated as <strong>completely separate, independent variables</strong>.</div>
  </div>

  <div v-click class="card-navy" style="border-radius:10px;">
    <div style="font-size:.82rem;line-height:1.6;color:var(--slate);">
      <span class="mono">age</span>, <span class="mono">Age</span>, and <span class="mono">AGE</span> are <strong style="color:var(--red);">three different variables</strong> — they occupy separate memory slots and can hold different values simultaneously.
    </div>
  </div>

  <div v-click class="section-label">✔ Valid — Three Distinct Variables</div>

  <div v-after style="background:#f6f8fa;border-radius:10px;border:1px solid #e1e4e8;padding:12px 14px;font-family:'Fira Code',monospace;font-size:.76rem;line-height:1.9;">
    <span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">age</span> = <span style="color:#b45309;">20</span>;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#6b7280;">// variable 1</span><br>
    <span style="color:#ef5050;">int</span> <span style="color:#c49a00;">Age</span> = <span style="color:#b45309;">30</span>;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#6b7280;">// variable 2 — different!</span><br>
    <span style="color:#ef5050;">int</span> <span style="color:#ef5050;">AGE</span> = <span style="color:#b45309;">40</span>;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#6b7280;">// variable 3 — different!</span><br>
    <span style="color:#0e6ead;">System</span>.<span style="color:#0e6ead;">out</span>.<span style="color:#2d7a00;">println</span>(<span style="color:#0e6ead;">age</span> + <span style="color:#2d7a00;">" "</span> + <span style="color:#c49a00;">Age</span> + <span style="color:#2d7a00;">" "</span> + <span style="color:#ef5050;">AGE</span>);
  </div>
  <div v-click class="output-box" style="font-size:.72rem;">20 &nbsp; 30 &nbsp; 40</div>

</div>

<div class="flex-col">

  <div v-click class="section-label">Memory — Three Separate Slots</div>

  <div v-after class="mem-box">
    <div class="mem-header">Stack Memory</div>
    <div class="mem-row">
      <div class="mem-name">age</div>
      <div class="mem-val">20</div>
      <div class="mem-type">int</div>
    </div>
    <div class="mem-row">
      <div class="mem-name" style="color:var(--orange);">Age</div>
      <div class="mem-val">30</div>
      <div class="mem-type">int</div>
    </div>
    <div class="mem-row">
      <div class="mem-name" style="color:var(--purple);">AGE</div>
      <div class="mem-val">40</div>
      <div class="mem-type">int</div>
    </div>
  </div>

  <div v-click class="callout callout-danger" style="margin-top:6px;">
    <div><strong>Beginner Trap:</strong> If you declare <span class="mono">int count = 5;</span> and then later try to print <span class="mono">Count</span> (capital C) or <span class="mono">COUNT</span>, Java will give a <strong>cannot find symbol</strong> compile error — it cannot find a variable by that exact casing.</div>
  </div>

  <div v-click class="callout callout-warn" style="margin-top:4px;">
    <div><strong>Convention:</strong> Although all three variations compile, never create variables that differ only in case. It is confusing and error-prone. Use descriptive, camelCase names instead.</div>
  </div>

</div>

</div>

  </template>
</Slide2>
