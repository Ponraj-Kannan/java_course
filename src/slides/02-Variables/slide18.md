---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 18 — NAMING RULE 2: Cannot start with a digit
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Variable Naming Rules">
  <template #content>

<div class="slide-h1" style="margin-bottom:10px;"><span class="highlight">Rule 2</span> — Cannot Start with a Digit</div>

<div class="g2" style="gap:14px;align-items:start;">

<div class="flex-col">

  <div v-click style="display:flex;gap:10px;align-items:center;margin-bottom:4px;">
    <div style="background:var(--green);color:#fff;border-radius:8px;padding:6px 16px;font-size:.75rem;font-weight:800;">RULE 2</div>
    <div class="body-text" style="font-size:.82rem;">A variable name <strong>cannot begin with a digit</strong> (0–9). Digits are only allowed after the first character.</div>
  </div>

  <div v-click class="section-label">✔ Valid Examples</div>

  <div v-after style="background:#f6f8fa;border-radius:10px;border:1px solid #e1e4e8;padding:12px 14px;font-family:'Fira Code',monospace;font-size:.76rem;line-height:1.9;">
    <span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">score2</span> = <span style="color:#b45309;">90</span>;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#6b7280;">// ✔ digit AFTER a letter</span><br>
    <span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">marks100</span> = <span style="color:#b45309;">95</span>;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#6b7280;">// ✔ digit in middle/end</span><br>
    <span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">student3count</span> = <span style="color:#b45309;">30</span>;&nbsp;&nbsp;<span style="color:#6b7280;">// ✔ digits anywhere else</span>
  </div>

  <div v-click class="callout callout-success" style="margin-top:4px;">
    <div><strong>Why the rule?</strong> The Java compiler needs to distinguish between a number literal (<span class="mono">2score</span> starts like the number <span class="mono">2</span>) and a variable name. Starting with a digit creates ambiguity.</div>
  </div>

</div>

<div class="flex-col">

  <div v-click class="section-label">✘ Invalid Examples</div>

  <div v-after style="background:var(--red-soft);border-radius:10px;border:1px solid var(--red);padding:12px 14px;font-family:'Fira Code',monospace;font-size:.76rem;line-height:1.9;">
    <span style="color:#ef5050;">int</span> <span style="color:#ef5050;">2score</span> = <span style="color:#b45309;">90</span>;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#6b7280;">// ✘ starts with digit 2</span><br>
    <span style="color:#ef5050;">double</span> <span style="color:#ef5050;">3.14value</span> = <span style="color:#b45309;">3.14</span>;<span style="color:#6b7280;"> // ✘ starts with digit</span><br>
    <span style="color:#ef5050;">int</span> <span style="color:#ef5050;">99percent</span> = <span style="color:#b45309;">99</span>;&nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#6b7280;">// ✘ starts with digits</span>
  </div>

  <div v-click class="callout callout-danger" style="margin-top:4px;">
    <div><strong>Compiler error:</strong><br>
    <span class="mono">error: ';' expected</span> — because Java sees <span class="mono">2score</span> as a number token followed by an unexpected identifier.</div>
  </div>

  <div v-click style="margin-top:6px;">
    <div class="section-label">Memory Box — Valid Name</div>
    <div class="mem-box" style="margin-top:4px;">
      <div class="mem-header">Stack Memory</div>
      <div class="mem-row">
        <div class="mem-name">score2</div>
        <div class="mem-val">90</div>
        <div class="mem-type">int</div>
      </div>
      <div class="mem-row">
        <div class="mem-name">marks100</div>
        <div class="mem-val">95</div>
        <div class="mem-type">int</div>
      </div>
    </div>
  </div>

</div>

</div>

  </template>
</Slide2>
