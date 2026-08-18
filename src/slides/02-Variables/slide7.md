---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 7 — TYPES OF VARIABLES IN JAVA (Overview)
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Java Variables">
  <template #content>

<div class="slide-h1" style="margin-bottom:10px;">Types of <span class="highlight">Variables</span> in Java</div>

<div class="g2" style="gap:14px;align-items:start;">

<div class="flex-col">

  <div v-click class="card-navy" style="border-radius:10px;">
    <div style="font-size:.82rem;line-height:1.6;color:var(--slate);">
      Java classifies variables into <strong style="color:var(--red);">three categories</strong> based on where they are declared — inside a method, inside a class, or shared across all objects. Each category has its own scope, lifetime, and rules.
    </div>
  </div>

  <div style="display:flex;flex-direction:column;gap:6px;">
    <div v-click class="card" style="padding:10px 14px;">
      <div style="display:flex;gap:10px;align-items:center;">
        <span class="pill pill-blue">Local Variable</span>
        <div class="body-text">Declared <strong>inside a method or block</strong> — exists only while that block executes</div>
      </div>
    </div>
    <div v-click class="card" style="padding:10px 14px;">
      <div style="display:flex;gap:10px;align-items:center;">
        <span class="pill pill-green">Instance Variable</span>
        <div class="body-text">Declared <strong>inside a class, outside methods</strong> — tied to each object instance</div>
      </div>
    </div>
    <div v-click class="card" style="padding:10px 14px;">
      <div style="display:flex;gap:10px;align-items:center;">
        <span class="pill pill-orange">Static Variable</span>
        <div class="body-text">Declared with <span class="mono">static</span> keyword — <strong>shared across all objects</strong> of the class</div>
      </div>
    </div>
  </div>

</div>

<div class="flex-col">

  <div v-click class="section-label">Comparison Overview</div>

  <div>
    <table class="cmp-table">
      <thead v-click>
        <tr><th>Feature</th><th>Local</th><th>Instance</th><th>Static</th></tr>
      </thead>
      <tbody>
        <tr v-click><td>Declared inside</td><td>Method / Block</td><td>Class body</td><td>Class body</td></tr>
        <tr v-click><td>Keyword</td><td class="mono">—</td><td class="mono">—</td><td class="mono">static</td></tr>
        <tr v-click><td>Default value?</td><td class="no">No (must init)</td><td class="yes">Yes</td><td class="yes">Yes</td></tr>
        <tr v-click><td>Tied to</td><td style="color:var(--blue);">Method call</td><td style="color:var(--green);">Object</td><td style="color:var(--orange);">Class</td></tr>
        <tr v-click><td>Memory</td><td>Stack</td><td>Heap (via object)</td><td>Method area</td></tr>
      </tbody>
    </table>
  </div>

  <div v-click class="callout callout-info" style="margin-top:8px;">
    <div>The next three slides cover each category in detail with code examples and memory diagrams.</div>
  </div>

</div>

</div>

  </template>
</Slide2>
