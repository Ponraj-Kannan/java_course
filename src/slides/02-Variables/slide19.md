---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 19 — NAMING RULE 3: No spaces or special characters (except $ and _)
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Variable Naming Rules">
  <template #content>

<div class="slide-h1" style="margin-bottom:10px;"><span class="highlight">Rule 3</span> — No Spaces or Special Characters</div>

<div class="g2" style="gap:14px;align-items:start;">

<div class="flex-col">

  <div v-click style="display:flex;gap:10px;align-items:center;margin-bottom:4px;">
    <div style="background:var(--green);color:#fff;border-radius:8px;padding:6px 16px;font-size:.75rem;font-weight:800;">RULE 3</div>
    <div class="body-text" style="font-size:.82rem;">A variable name cannot contain <strong>spaces</strong>, hyphens, or special characters like <span class="mono">@, #, !, -, +, *</span>. Only letters, digits, <span class="mono">$</span>, and <span class="mono">_</span> are allowed.</div>
  </div>

  <div v-click class="section-label">✔ Valid Examples</div>

  <div v-after style="background:#f6f8fa;border-radius:10px;border:1px solid #e1e4e8;padding:12px 14px;font-family:'Fira Code',monospace;font-size:.76rem;line-height:1.9;">
    <span style="color:#ef5050;">String</span> <span style="color:#0e6ead;">studentName</span> = <span style="color:#2d7a00;">"Alice"</span>;&nbsp;<span style="color:#6b7280;">// ✔ use camelCase</span><br>
    <span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">total_marks</span> = <span style="color:#b45309;">95</span>;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#6b7280;">// ✔ underscore is OK</span><br>
    <span style="color:#ef5050;">double</span> <span style="color:#0e6ead;">maxScore$</span> = <span style="color:#b45309;">100.0</span>;&nbsp;&nbsp;&nbsp;<span style="color:#6b7280;">// ✔ $ is allowed</span>
  </div>

  <div v-click class="callout callout-info" style="margin-top:4px;">
    <div><strong>Convention tip:</strong> Even though <span class="mono">total_marks</span> is valid, Java convention prefers <span class="mono">totalMarks</span> (camelCase). Use <span class="mono">_</span> mainly in constants: <span class="mono">MAX_VALUE</span>.</div>
  </div>

</div>

<div class="flex-col">

  <div v-click class="section-label">✘ Invalid Examples</div>

  <div v-after style="background:var(--red-soft);border-radius:10px;border:1px solid var(--red);padding:12px 14px;font-family:'Fira Code',monospace;font-size:.76rem;line-height:1.9;">
    <span style="color:#ef5050;">int</span> <span style="color:#ef5050;">my name</span> = <span style="color:#b45309;">10</span>;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#6b7280;">// ✘ space inside name</span><br>
    <span style="color:#ef5050;">int</span> <span style="color:#ef5050;">my-score</span> = <span style="color:#b45309;">50</span>;&nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#6b7280;">// ✘ hyphen not allowed</span><br>
    <span style="color:#ef5050;">int</span> <span style="color:#ef5050;">mark@2</span> = <span style="color:#b45309;">80</span>;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#6b7280;">// ✘ @ symbol not allowed</span><br>
    <span style="color:#ef5050;">int</span> <span style="color:#ef5050;">total+count</span> = <span style="color:#b45309;">5</span>;&nbsp;&nbsp;&nbsp;<span style="color:#6b7280;">// ✘ + is an operator, not valid</span>
  </div>

  <div v-click class="callout callout-danger" style="margin-top:4px;">
    <div>
      <strong>Compiler error for space:</strong> <span class="mono">my name</span> is seen as two separate tokens: <span class="mono">my</span> (a variable) and <span class="mono">name</span> (another token) — causing a syntax error.<br><br>
      <strong>Compiler error for special chars:</strong> <span class="mono">my-score</span> is parsed as <span class="mono">my</span> <span class="mono">-</span> <span class="mono">score</span> (subtraction), not a variable name.
    </div>
  </div>

</div>

</div>

  </template>
</Slide2>
