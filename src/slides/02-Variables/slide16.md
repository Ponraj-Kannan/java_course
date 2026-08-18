---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 16 — NAMING RULES: OVERVIEW (QUICK REFERENCE)
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Variable Naming Rules">
  <template #content>

<div class="slide-h1" style="margin-bottom:10px;">Naming Rules — <span class="highlight">Quick Reference</span></div>

<div class="g2" style="gap:14px;">

<div class="flex-col">

  <div v-click class="card-navy" style="border-radius:10px;">
    <div style="font-size:.82rem;line-height:1.6;color:var(--slate);">
      <strong style="color:var(--red);">Definition:</strong> <strong>Naming rules</strong> are enforced by the Java compiler. Violating any of these rules is a <strong>compile-time error</strong> — your program will not run.
    </div>
  </div>

  <div style="display:flex;flex-direction:column;gap:5px;">
    <div style="display:flex;gap:10px;align-items:flex-start;" v-click>
      <div style="background:var(--green);color:#fff;border-radius:6px;padding:3px 10px;font-size:.65rem;font-weight:800;flex-shrink:0;">RULE 1</div>
      <div class="body-text">Must start with a <strong>letter (a–z, A–Z)</strong>, a <strong>dollar sign ($)</strong>, or an <strong>underscore (_)</strong></div>
    </div>
    <div style="display:flex;gap:10px;align-items:flex-start;" v-click>
      <div style="background:var(--green);color:#fff;border-radius:6px;padding:3px 10px;font-size:.65rem;font-weight:800;flex-shrink:0;">RULE 2</div>
      <div class="body-text"><strong>Cannot start with a digit</strong> (0–9) — digits are only allowed after the first character</div>
    </div>
    <div style="display:flex;gap:10px;align-items:flex-start;" v-click>
      <div style="background:var(--green);color:#fff;border-radius:6px;padding:3px 10px;font-size:.65rem;font-weight:800;flex-shrink:0;">RULE 3</div>
      <div class="body-text"><strong>No spaces</strong> and no special characters except <span class="mono">$</span> and <span class="mono">_</span> (no @, #, !, -, etc.)</div>
    </div>
    <div style="display:flex;gap:10px;align-items:flex-start;" v-click>
      <div style="background:var(--blue);color:#fff;border-radius:6px;padding:3px 10px;font-size:.65rem;font-weight:800;flex-shrink:0;">RULE 4</div>
      <div class="body-text"><strong>Case-sensitive</strong> — <span class="mono">age</span>, <span class="mono">Age</span>, and <span class="mono">AGE</span> are three different variables</div>
    </div>
    <div style="display:flex;gap:10px;align-items:flex-start;" v-click>
      <div style="background:var(--red);color:#fff;border-radius:6px;padding:3px 10px;font-size:.65rem;font-weight:800;flex-shrink:0;">RULE 5</div>
      <div class="body-text"><strong>Cannot be a reserved keyword</strong> — e.g. <span class="mono" style="color:var(--red-dark);">int</span>, <span class="mono" style="color:var(--red-dark);">class</span>, <span class="mono" style="color:var(--red-dark);">for</span>, <span class="mono" style="color:var(--red-dark);">static</span></div>
    </div>
    <div style="display:flex;gap:10px;align-items:flex-start;" v-click>
      <div style="background:var(--purple);color:#fff;border-radius:6px;padding:3px 10px;font-size:.65rem;font-weight:800;flex-shrink:0;">RULE 6</div>
      <div class="body-text"><strong>No length limit</strong> — technically can be any length, but should be meaningful and concise</div>
    </div>
  </div>

</div>

<div class="flex-col">

  <div v-click class="section-label">Valid vs Invalid — Quick Check</div>

  <div>
    <table class="cmp-table">
      <thead v-click>
        <tr><th>Name</th><th>Valid?</th><th>Reason</th></tr>
      </thead>
      <tbody>
        <tr v-click><td class="mono">studentName</td><td class="yes">✔ Valid</td><td>Starts with letter</td></tr>
        <tr v-click><td class="mono">_count</td><td class="yes">✔ Valid</td><td>Starts with underscore</td></tr>
        <tr v-click><td class="mono">$price</td><td class="yes">✔ Valid</td><td>Starts with dollar sign</td></tr>
        <tr v-click><td class="mono">score2</td><td class="yes">✔ Valid</td><td>Letter first, digit after</td></tr>
        <tr v-click><td class="mono">2score</td><td class="no">✘ Invalid</td><td>Starts with digit (Rule 2)</td></tr>
        <tr v-click><td class="mono">my-name</td><td class="no">✘ Invalid</td><td>Contains hyphen (Rule 3)</td></tr>
        <tr v-click><td class="mono">int</td><td class="no">✘ Invalid</td><td>Reserved keyword (Rule 5)</td></tr>
        <tr v-click><td class="mono">my name</td><td class="no">✘ Invalid</td><td>Contains space (Rule 3)</td></tr>
      </tbody>
    </table>
  </div>

  <div v-click class="callout callout-warn" style="margin-top:6px;">
    <div>The following slides cover each rule individually with a detailed valid and invalid example.</div>
  </div>

</div>

</div>

  </template>
</Slide2>
