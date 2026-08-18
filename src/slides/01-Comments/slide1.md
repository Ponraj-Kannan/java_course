---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 1 — WHAT IS A COMMENT?
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Comments">
  <template #content>

<div class="slide-h1" style="margin-bottom:10px;">What is a <span class="highlight">Comment?</span></div>

<div class="g2" style="gap:14px;align-items:start;">

<div class="flex-col">

  <div v-click class="card-navy" style="border-radius:10px;">
    <div style="font-size:.82rem;line-height:1.6;color:var(--slate);">
      <strong style="color:var(--red);">Definition:</strong> A <strong>comment</strong> is a line or block of text in source code that is <strong>completely ignored by the Java compiler</strong>. It exists only for human readers — to explain, clarify, or document the code.
    </div>
  </div>

  <div v-click class="callout callout-success">
    <div><strong>Key fact:</strong> Comments are stripped out during compilation — they generate <strong>zero bytecode</strong> and have <strong>zero impact</strong> on runtime performance or program output.</div>
  </div>

  <div v-click class="section-label">Why Use Comments?</div>

  <div style="display:flex;flex-direction:column;gap:5px;">
    <div v-click class="card" style="padding:8px 14px;">
      <div style="display:flex;gap:8px;align-items:center;">
        <span class="pill pill-blue">Readability</span>
        <div class="body-text">Explain <em>why</em> code exists, not just <em>what</em> it does</div>
      </div>
    </div>
    <div v-click class="card" style="padding:8px 14px;">
      <div style="display:flex;gap:8px;align-items:center;">
        <span class="pill pill-green">Documentation</span>
        <div class="body-text">Describe classes, methods, and parameters for API users</div>
      </div>
    </div>
    <div v-click class="card" style="padding:8px 14px;">
      <div style="display:flex;gap:8px;align-items:center;">
        <span class="pill pill-orange">Debugging</span>
        <div class="body-text">Temporarily disable code blocks during testing without deleting them</div>
      </div>
    </div>
  </div>

</div>

<div class="flex-col">

  <div v-click class="section-label">Java Comment Types — At a Glance</div>

  <div>
    <table class="cmp-table">
      <thead v-click>
        <tr><th>Type</th><th>Syntax</th><th>Spans</th></tr>
      </thead>
      <tbody>
        <tr v-click><td><strong>Single-line</strong></td><td class="mono" style="color:var(--green);">// text</td><td>One line</td></tr>
        <tr v-click><td><strong>Multi-line</strong></td><td class="mono" style="color:var(--blue);">/* text */</td><td>Multiple lines</td></tr>
        <tr v-click><td><strong>Documentation</strong></td><td class="mono" style="color:var(--orange);">/** text */</td><td>Multiple lines + tags</td></tr>
      </tbody>
    </table>
  </div>

  <div v-click style="background:#f6f8fa;border-radius:10px;border:1px solid #e1e4e8;padding:14px;font-family:'Fira Code',monospace;font-size:.76rem;line-height:2;margin-top:4px;">
    <span style="color:#6b7280;">// This is a single-line comment</span><br>
    <br>
    <span style="color:#6b7280;">/* This is a</span><br>
    <span style="color:#6b7280;">&nbsp;&nbsp; multi-line comment */</span><br>
    <br>
    <span style="color:#6b7280;">/** Javadoc comment for documentation */</span>
  </div>

</div>

</div>

  </template>
</Slide2>
