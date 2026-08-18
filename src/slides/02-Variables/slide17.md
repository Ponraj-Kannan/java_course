---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 17 — NAMING RULE 1: Must start with letter, $, or _
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Variable Naming Rules">
  <template #content>

<div class="slide-h1" style="margin-bottom:10px;"><span class="highlight">Rule 1</span> — Valid Starting Characters</div>

<div class="g2" style="gap:14px;align-items:start;">

<div class="flex-col">

  <div v-click style="display:flex;gap:10px;align-items:center;margin-bottom:4px;">
    <div style="background:var(--green);color:#fff;border-radius:8px;padding:6px 16px;font-size:.75rem;font-weight:800;">RULE 1</div>
    <div class="body-text" style="font-size:.82rem;">A variable name must <strong>start with</strong> a letter (a–z, A–Z), a dollar sign <span class="mono">$</span>, or an underscore <span class="mono">_</span>.</div>
  </div>

  <div v-click class="section-label">✔ Valid Examples</div>

  <div v-after style="display:flex;flex-direction:column;gap:6px;">
    <div style="background:#f6f8fa;border-radius:10px;border:1px solid #e1e4e8;padding:12px 14px;font-family:'Fira Code',monospace;font-size:.76rem;line-height:1.9;">
      <span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">age</span> = <span style="color:#b45309;">25</span>;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#6b7280;">// ✔ starts with letter</span><br>
      <span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">_count</span> = <span style="color:#b45309;">0</span>;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#6b7280;">// ✔ starts with underscore</span><br>
      <span style="color:#ef5050;">double</span> <span style="color:#0e6ead;">$price</span> = <span style="color:#b45309;">99.99</span>;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#6b7280;">// ✔ starts with dollar sign</span>
    </div>
    <div class="output-box" style="font-size:.7rem;">25 &nbsp; 0 &nbsp; 99.99</div>
  </div>

</div>

<div class="flex-col">

  <div v-click class="section-label">✘ Invalid Examples</div>

  <div v-after style="background:var(--red-soft);border-radius:10px;border:1px solid var(--red);padding:12px 14px;font-family:'Fira Code',monospace;font-size:.76rem;line-height:1.9;">
    <span style="color:#ef5050;">int</span> <span style="color:#ef5050;">1age</span> = <span style="color:#b45309;">25</span>;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#6b7280;">// ✘ starts with digit</span><br>
    <span style="color:#ef5050;">int</span> <span style="color:#ef5050;">@value</span> = <span style="color:#b45309;">10</span>;&nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#6b7280;">// ✘ starts with @ symbol</span><br>
    <span style="color:#ef5050;">int</span> <span style="color:#ef5050;">-score</span> = <span style="color:#b45309;">5</span>;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#6b7280;">// ✘ starts with hyphen</span>
  </div>

  <div v-click class="callout callout-danger" style="margin-top:4px;">
    <div><strong>Compiler error:</strong> All three statements above produce an error like: <br><span class="mono">error: not a statement</span> or <span class="mono">illegal start of expression</span></div>
  </div>

  <div v-click class="callout callout-info" style="margin-top:4px;">
    <div><strong>Note:</strong> While <span class="mono">$</span> and <span class="mono">_</span> are valid starting characters, they are conventionally reserved: <span class="mono">_</span> is used in older code and constants, <span class="mono">$</span> is used by Java-generated code (e.g. inner classes). Avoid them for regular variables.</div>
  </div>

</div>

</div>

  </template>
</Slide2>
