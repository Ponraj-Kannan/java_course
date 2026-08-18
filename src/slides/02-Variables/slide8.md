---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 8 — LOCAL VARIABLES
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Java Variables">
  <template #content>

<div class="slide-h1" style="margin-bottom:10px;"><span class="highlight">Local</span> Variables</div>

<div class="g2" style="gap:14px;">

<div class="flex-col">

  <div v-click class="card-navy" style="border-radius:10px;">
    <div style="font-size:.82rem;line-height:1.6;color:var(--slate);">
      <strong style="color:var(--red);">Definition:</strong> A <strong>local variable</strong> is declared inside a method, constructor, or block. It exists only for the duration of that block's execution and is not accessible from outside.
    </div>
  </div>

  <div style="display:flex;flex-direction:column;gap:5px;">
    <div style="display:flex;gap:10px;align-items:flex-start;" v-click>
      <div style="background:var(--blue);color:#fff;border-radius:6px;padding:3px 10px;font-size:.65rem;font-weight:800;flex-shrink:0;">RULE 1</div>
      <div class="body-text">Must be <strong>explicitly initialized</strong> before use — no default value!</div>
    </div>
    <div style="display:flex;gap:10px;align-items:flex-start;" v-click>
      <div style="background:var(--blue);color:#fff;border-radius:6px;padding:3px 10px;font-size:.65rem;font-weight:800;flex-shrink:0;">RULE 2</div>
      <div class="body-text">Scope is limited to the <strong>enclosing block</strong> <span class="mono">{ }</span> — dies at the closing brace</div>
    </div>
    <div style="display:flex;gap:10px;align-items:flex-start;" v-click>
      <div style="background:var(--blue);color:#fff;border-radius:6px;padding:3px 10px;font-size:.65rem;font-weight:800;flex-shrink:0;">RULE 3</div>
      <div class="body-text">Stored on the <strong>stack</strong> — allocated when block is entered, freed when it exits</div>
    </div>
    <div style="display:flex;gap:10px;align-items:flex-start;" v-click>
      <div style="background:var(--blue);color:#fff;border-radius:6px;padding:3px 10px;font-size:.65rem;font-weight:800;flex-shrink:0;">RULE 4</div>
      <div class="body-text">Cannot use access modifiers like <span class="mono">public</span>, <span class="mono">private</span>, or <span class="mono">static</span></div>
    </div>
  </div>

</div>

<div class="flex-col">

  <div v-click class="section-label">Code Example</div>
  <div v-after style="background:#f6f8fa;border-radius:10px;border:1px solid #e1e4e8;padding:14px;font-family:'Fira Code',monospace;font-size:.72rem;line-height:1.9;">
    <span style="color:#ef5050;">void</span> <span style="color:#2d7a00;">greet</span>() {<br>
    &nbsp;&nbsp;<span style="color:#6b7280;">// Local variable — only lives in this method</span><br>
    &nbsp;&nbsp;<span style="color:#ef5050;">String</span> <span style="color:#0e6ead;">message</span> = <span style="color:#2d7a00;">"Hello, Java!"</span>;<br>
    &nbsp;&nbsp;<span style="color:#6b7280;">// Valid: message is in scope</span><br>
    &nbsp;&nbsp;<span style="color:#0e6ead;">System</span>.<span style="color:#0e6ead;">out</span>.<span style="color:#2d7a00;">println</span>(<span style="color:#0e6ead;">message</span>);<br>
    }<br>
    <span style="color:#6b7280;">// ✘ ERROR: 'message' is out of scope here</span>
  </div>

  <div v-click class="callout callout-danger" style="margin-top:4px;">
    <div><strong>Common error:</strong> Using a local variable without initializing it gives: <span class="mono">variable 'message' might not have been initialized</span></div>
  </div>

  <div v-click style="background:#f6f8fa;border-radius:10px;border:1px solid #e1e4e8;padding:14px;font-family:'Fira Code',monospace;font-size:.72rem;line-height:1.9;margin-top:4px;">
    <span style="color:#6b7280;">// ✘ COMPILE ERROR — not initialized!</span><br>
    <span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">score</span>;<br>
    <span style="color:#0e6ead;">System</span>.<span style="color:#0e6ead;">out</span>.<span style="color:#2d7a00;">println</span>(<span style="color:#0e6ead;">score</span>); <span style="color:#6b7280;">// ERROR</span><br><br>
    <span style="color:#6b7280;">// ✔ Correct — initialize first</span><br>
    <span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">score</span> = <span style="color:#b45309;">0</span>;<br>
    <span style="color:#0e6ead;">System</span>.<span style="color:#0e6ead;">out</span>.<span style="color:#2d7a00;">println</span>(<span style="color:#0e6ead;">score</span>); <span style="color:#6b7280;">// OK: 0</span>
  </div>

</div>

</div>

  </template>
</Slide2>
