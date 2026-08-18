---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 24 — NAMING CONVENTIONS & RULES vs CONVENTIONS
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Naming Conventions">
  <template #content>

<div class="slide-h1" style="margin-bottom:10px;">Naming <span class="highlight">Conventions</span></div>

<div class="g2" style="gap:14px;align-items:start;">

<div class="flex-col">

  <div v-click class="card-navy" style="border-radius:10px;">
    <div style="font-size:.82rem;line-height:1.6;color:var(--slate);">
      <strong style="color:var(--red);">Definition:</strong> <strong>Naming conventions</strong> are community-agreed style guidelines — not enforced by the compiler. Violating them still compiles, but it's considered <em>bad practice</em> and hurts readability.
    </div>
  </div>

  <div v-click style="display:flex;flex-direction:column;gap:5px;">
    <div class="card" style="padding:8px 14px;">
      <div style="display:flex;gap:8px;align-items:flex-start;">
        <span class="pill pill-blue">camelCase</span>
        <div>
          <div class="body-text">For <strong>variables and methods</strong></div>
          <div class="small-text"><span class="mono" style="color:var(--green);">studentAge</span>, <span class="mono" style="color:var(--green);">totalMarks</span>, <span class="mono" style="color:var(--green);">calculateGrade()</span></div>
        </div>
      </div>
    </div>
    <div v-click class="card" style="padding:8px 14px;">
      <div style="display:flex;gap:8px;align-items:flex-start;">
        <span class="pill pill-green">PascalCase</span>
        <div>
          <div class="body-text">For <strong>class names</strong></div>
          <div class="small-text"><span class="mono" style="color:var(--green);">StudentRecord</span>, <span class="mono" style="color:var(--green);">BankAccount</span>, <span class="mono" style="color:var(--green);">HelloWorld</span></div>
        </div>
      </div>
    </div>
    <div v-click class="card" style="padding:8px 14px;">
      <div style="display:flex;gap:8px;align-items:flex-start;">
        <span class="pill pill-orange">UPPER_SNAKE</span>
        <div>
          <div class="body-text">For <strong>constants</strong> (<span class="mono">static final</span>)</div>
          <div class="small-text"><span class="mono" style="color:var(--green);">MAX_SIZE</span>, <span class="mono" style="color:var(--green);">PI_VALUE</span>, <span class="mono" style="color:var(--green);">TAX_RATE</span></div>
        </div>
      </div>
    </div>
    <div v-click class="card" style="padding:8px 14px;">
      <div style="display:flex;gap:8px;align-items:flex-start;">
        <span class="pill pill-red">Meaningful</span>
        <div>
          <div class="body-text">Use <strong>descriptive names</strong>, not single letters (except loop counters <span class="mono">i, j, k</span>)</div>
        </div>
      </div>
    </div>
  </div>

</div>

<div class="flex-col">

  <div v-click class="section-label">Rules vs Conventions — Key Distinction</div>

  <div v-after>
    <table class="cmp-table">
      <thead>
        <tr><th>Aspect</th><th>Naming Rules</th><th>Naming Conventions</th></tr>
      </thead>
      <tbody>
        <tr v-click><td>Enforced by</td><td style="color:var(--red);font-weight:600;">Compiler</td><td style="color:var(--blue);font-weight:600;">Community / Team</td></tr>
        <tr v-click><td>Violation result</td><td class="no">Compile error</td><td class="yes">Still compiles</td></tr>
        <tr v-click><td>Example rule</td><td class="mono">int 2x = 5; // error</td><td class="mono">int X = 5; // bad style</td></tr>
        <tr v-click><td>Goal</td><td>Correctness</td><td>Readability &amp; Teamwork</td></tr>
      </tbody>
    </table>
  </div>

  <div v-click class="section-label" style="margin-top:8px;">Convention Examples</div>

  <div v-after style="background:#f6f8fa;border-radius:10px;border:1px solid #e1e4e8;padding:12px 14px;font-family:'Fira Code',monospace;font-size:.7rem;line-height:1.9;">
    <span style="color:#6b7280;">// ✔ Following conventions</span><br>
    <span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">studentAge</span> = <span style="color:#b45309;">20</span>;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#6b7280;">// camelCase variable</span><br>
    <span style="color:#ef5050;">static</span> <span style="color:#ef5050;">final</span> <span style="color:#ef5050;">double</span> <span style="color:#0e6ead;">MAX_MARKS</span> = <span style="color:#b45309;">100.0</span>;&nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#6b7280;">// UPPER_SNAKE constant</span><br>
    <span style="color:#6b7280;">// ✘ Compiles but breaks conventions</span><br>
    <span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">StudentAge</span> = <span style="color:#b45309;">20</span>;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#6b7280;">// PascalCase for variable — bad</span><br>
    <span style="color:#ef5050;">static</span> <span style="color:#ef5050;">final</span> <span style="color:#ef5050;">double</span> <span style="color:#0e6ead;">maxMarks</span> = <span style="color:#b45309;">100.0</span>;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#6b7280;">// camelCase for constant — bad</span>
  </div>

</div>

</div>

  </template>
</Slide2>
