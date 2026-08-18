---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 22 — NAMING RULE 6: No length limit but be meaningful
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Variable Naming Rules">
  <template #content>

<div class="slide-h1" style="margin-bottom:10px;"><span class="highlight">Rule 6</span> — No Length Limit, But Be Meaningful</div>

<div class="g2" style="gap:14px;align-items:start;">

<div class="flex-col">

  <div v-click style="display:flex;gap:10px;align-items:center;margin-bottom:4px;">
    <div style="background:var(--purple);color:#fff;border-radius:8px;padding:6px 16px;font-size:.75rem;font-weight:800;">RULE 6</div>
    <div class="body-text" style="font-size:.82rem;">Java imposes <strong>no maximum length</strong> on variable names — they can be as long as needed. However, good names should be <strong>meaningful, descriptive, and concise</strong>.</div>
  </div>

  <div v-click class="section-label">✔ Valid — Meaningful Names</div>

  <div v-after style="background:#f6f8fa;border-radius:10px;border:1px solid #e1e4e8;padding:12px 14px;font-family:'Fira Code',monospace;font-size:.74rem;line-height:1.9;">
    <span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">studentAge</span> = <span style="color:#b45309;">20</span>;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#6b7280;">// ✔ clear, concise</span><br>
    <span style="color:#ef5050;">double</span> <span style="color:#0e6ead;">totalExamMarks</span> = <span style="color:#b45309;">450.5</span>;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#6b7280;">// ✔ descriptive</span><br>
    <span style="color:#ef5050;">boolean</span> <span style="color:#0e6ead;">isStudentEnrolled</span> = <span style="color:#b45309;">true</span>;&nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#6b7280;">// ✔ reads like a question</span>
  </div>

  <div v-click class="callout callout-success" style="margin-top:4px;">
    <div><strong>Golden Rule:</strong> A good variable name tells you <em>what</em> it stores without needing a comment. Code is read far more often than it is written!</div>
  </div>

  <div v-click class="section-label" style="margin-top:6px;">✘ Poor Choices (Compile, but Bad Practice)</div>

  <div v-after style="background:#fffaf0;border-radius:10px;border:1px solid var(--orange);padding:12px 14px;font-family:'Fira Code',monospace;font-size:.74rem;line-height:1.9;">
    <span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">x</span> = <span style="color:#b45309;">20</span>;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#6b7280;">// ⚠ too vague</span><br>
    <span style="color:#ef5050;">double</span> <span style="color:#0e6ead;">a1</span> = <span style="color:#b45309;">450.5</span>;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#6b7280;">// ⚠ no meaning</span><br>
    <span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">numberOfStudentsCurrentlyEnrolledInThisSemester</span> = <span style="color:#b45309;">120</span>;<span style="color:#6b7280;"> // ⚠ too long</span>
  </div>

</div>

<div class="flex-col">

  <div v-click class="section-label">Good vs Bad — Comparison</div>

  <div v-after>
    <table class="cmp-table">
      <thead>
        <tr><th>❌ Poor Name</th><th>✔ Better Name</th><th>Why Better</th></tr>
      </thead>
      <tbody>
        <tr v-click><td class="mono" style="color:var(--red-dark);">x</td><td class="mono" style="color:var(--green);">studentAge</td><td>Descriptive</td></tr>
        <tr v-click><td class="mono" style="color:var(--red-dark);">a1</td><td class="mono" style="color:var(--green);">totalMarks</td><td>Meaningful</td></tr>
        <tr v-click><td class="mono" style="color:var(--red-dark);">flag</td><td class="mono" style="color:var(--green);">isLoggedIn</td><td>Self-documenting</td></tr>
        <tr v-click><td class="mono" style="color:var(--red-dark);">temp</td><td class="mono" style="color:var(--green);">temperatureCelsius</td><td>Unit clear</td></tr>
        <tr v-click><td class="mono" style="color:var(--red-dark);">data2</td><td class="mono" style="color:var(--green);">salesReport</td><td>Context clear</td></tr>
      </tbody>
    </table>
  </div>

  <div v-click class="callout callout-info" style="margin-top:6px;">
    <div><strong>Exception:</strong> Single-letter names (<span class="mono">i, j, k</span>) are acceptable for <strong>loop counters only</strong>. This is a widely accepted convention.</div>
  </div>

</div>

</div>

  </template>
</Slide2>
