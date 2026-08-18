---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 25 — THE final KEYWORD FOR VARIABLES
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Naming Conventions">
  <template #content>

<div class="slide-h1" style="margin-bottom:10px;">The <span class="highlight">final</span> Keyword</div>

<div class="g2" style="gap:14px;align-items:start;">

<div class="flex-col">

  <div v-click class="card-navy" style="border-radius:10px;">
    <div style="font-size:.82rem;line-height:1.6;color:var(--slate);">
      <strong style="color:var(--red);">Definition:</strong> A variable declared with the <span class="mono" style="color:var(--red-dark);">final</span> keyword becomes a <strong>constant</strong> — it can be assigned a value <strong>only once</strong>. Any attempt to reassign it causes a <strong>compile-time error</strong>.
    </div>
  </div>

  <div v-click class="section-label">Syntax</div>
  <div v-after style="display:flex;align-items:center;gap:8px;flex-wrap:wrap;font-family:'Fira Code',monospace;font-size:.8rem;">
    <span class="syn-keyword">final</span>
    <span class="syn-keyword">type</span>
    <span class="syn-varname">VARIABLE_NAME</span>
    <span class="syn-operator">=</span>
    <span class="syn-value">value</span>
    <span style="color:var(--muted);">;</span>
  </div>

  <div v-click class="section-label" style="margin-top:6px;">✔ Valid Usage</div>
  <div v-after style="background:#f6f8fa;border-radius:10px;border:1px solid #e1e4e8;padding:12px 14px;font-family:'Fira Code',monospace;font-size:.74rem;line-height:1.9;">
    <span style="color:#ef5050;">final</span> <span style="color:#ef5050;">double</span> <span style="color:#0e6ead;">PI</span> = <span style="color:#b45309;">3.14159</span>;<br>
    <span style="color:#ef5050;">final</span> <span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">MAX_STUDENTS</span> = <span style="color:#b45309;">60</span>;<br>
    <span style="color:#6b7280;">// These are constants — read-only after initialization</span><br>
    <span style="color:#0e6ead;">System</span>.<span style="color:#0e6ead;">out</span>.<span style="color:#2d7a00;">println</span>(<span style="color:#0e6ead;">PI</span>);<span style="color:#6b7280;"> // 3.14159</span>
  </div>

  <div v-click class="section-label" style="margin-top:4px;">✘ Reassignment Attempt</div>
  <div v-after style="background:var(--red-soft);border-radius:10px;border:1px solid var(--red);padding:12px 14px;font-family:'Fira Code',monospace;font-size:.74rem;line-height:1.9;">
    <span style="color:#ef5050;">final</span> <span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">MAX</span> = <span style="color:#b45309;">100</span>;<br>
    <span style="color:#ef5050;">MAX</span> = <span style="color:#b45309;">200</span>; <span style="color:#6b7280;">// ✘ COMPILE ERROR</span>
  </div>

  <div v-click class="callout callout-danger" style="margin-top:4px;">
    <div><strong>Error:</strong> <span class="mono">cannot assign a value to final variable MAX</span></div>
  </div>

</div>

<div class="flex-col">

  <div v-click class="section-label">Where final Can Be Used</div>

  <div v-after style="display:flex;flex-direction:column;gap:6px;">
    <div class="card" style="padding:8px 14px;">
      <div style="display:flex;gap:8px;align-items:flex-start;">
        <span class="pill pill-blue">Local</span>
        <div>
          <div class="body-text"><span class="mono">final int x = 5;</span></div>
          <div class="small-text">Must be initialized at declaration or before first use</div>
        </div>
      </div>
    </div>
    <div v-click class="card" style="padding:8px 14px;">
      <div style="display:flex;gap:8px;align-items:flex-start;">
        <span class="pill pill-green">Instance</span>
        <div>
          <div class="body-text"><span class="mono">final String NAME = "Alice";</span></div>
          <div class="small-text">Every object has its own constant copy</div>
        </div>
      </div>
    </div>
    <div v-click class="card" style="padding:8px 14px;">
      <div style="display:flex;gap:8px;align-items:flex-start;">
        <span class="pill pill-orange">Static Final</span>
        <div>
          <div class="body-text"><span class="mono">static final double TAX = 0.18;</span></div>
          <div class="small-text">True class-level constant — shared and immutable</div>
        </div>
      </div>
    </div>
  </div>

  <div v-click class="callout callout-warn" style="margin-top:6px;">
    <div><strong>Convention:</strong> Name <span class="mono">final</span> variables using <span class="mono">UPPER_SNAKE_CASE</span> to signal to every reader that this is a constant, not a regular variable.</div>
  </div>

  <div v-click class="callout callout-info" style="margin-top:4px;">
    <div><strong>Note:</strong> <span class="mono">final</span> on a reference variable means the <em>reference</em> cannot change (you can't reassign it to a new object), but the object's internal state can still be modified.</div>
  </div>

</div>

</div>

  </template>
</Slide2>
