---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 26 — VARIABLE SHADOWING
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Naming Conventions">
  <template #content>

<div class="slide-h1" style="margin-bottom:10px;">Variable <span class="highlight">Shadowing</span></div>

<div class="g2" style="gap:14px;">

<div class="flex-col">

  <div v-click class="card-navy" style="border-radius:10px;">
    <div style="font-size:.82rem;line-height:1.6;color:var(--slate);">
      <strong style="color:var(--red);">Definition:</strong> <strong>Variable shadowing</strong> occurs when a <strong>local variable</strong> (e.g. a method parameter or local declaration) has the <strong>same name</strong> as an instance variable. Inside that method, the local variable <em>shadows</em> (hides) the instance variable.
    </div>
  </div>

  <div v-click class="section-label">Code — Shadowing in Action</div>
  <div v-after style="background:#f6f8fa;border-radius:10px;border:1px solid #e1e4e8;padding:14px;font-family:'Fira Code',monospace;font-size:.72rem;line-height:1.9;">
    <span style="color:#ef5050;">class</span> <span style="color:#0e6ead;">Student</span> {<br>
    &nbsp;&nbsp;<span style="color:#6b7280;">// Instance variable</span><br>
    &nbsp;&nbsp;<span style="color:#ef5050;">String</span> <span style="color:#0e6ead;">name</span> = <span style="color:#2d7a00;">"Instance Alice"</span>;<br><br>
    &nbsp;&nbsp;<span style="color:#ef5050;">void</span> <span style="color:#2d7a00;">setName</span>(<span style="color:#ef5050;">String</span> <span style="color:#c49a00;">name</span>) { <span style="color:#6b7280;">// param shadows instance var</span><br>
    &nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#6b7280;">// 'name' here refers to PARAMETER, not instance var!</span><br>
    &nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#0e6ead;">System</span>.<span style="color:#0e6ead;">out</span>.<span style="color:#2d7a00;">println</span>(<span style="color:#c49a00;">name</span>); <span style="color:#6b7280;">// prints parameter</span><br>
    &nbsp;&nbsp;}<br>
    }
  </div>

  <div v-click class="callout callout-danger" style="margin-top:4px;">
    <div><strong>Problem:</strong> Inside <span class="mono">setName()</span>, writing <span class="mono">name = name;</span> assigns the parameter to itself — the instance variable is never updated!</div>
  </div>

</div>

<div class="flex-col">

  <div v-click class="section-label">Shadowing Diagram</div>

  <div v-after style="display:flex;gap:12px;align-items:flex-start;">
    <div style="flex:1;border:2px solid var(--green);border-radius:10px;padding:8px;background:#f0fff4;">
      <div style="font-size:.58rem;color:var(--green);font-weight:700;text-transform:uppercase;letter-spacing:1px;margin-bottom:4px;text-align:center;">Class Scope (Instance)</div>
      <div class="mem-box">
        <div class="mem-row">
          <div class="mem-name">name</div>
          <div class="mem-val">"Instance Alice"</div>
        </div>
      </div>
      <div style="font-size:.58rem;color:var(--muted);margin-top:4px;text-align:center;">← hidden by local</div>
    </div>
    <div style="flex:1;border:2px solid var(--orange);border-radius:10px;padding:8px;background:#fffaf0;">
      <div style="font-size:.58rem;color:var(--orange);font-weight:700;text-transform:uppercase;letter-spacing:1px;margin-bottom:4px;text-align:center;">Method Scope (Local/Param)</div>
      <div class="mem-box">
        <div class="mem-row">
          <div class="mem-name">name</div>
          <div class="mem-val">"Bob"</div>
        </div>
      </div>
      <div style="font-size:.58rem;color:var(--muted);margin-top:4px;text-align:center;">← shadows instance var</div>
    </div>
  </div>

  <div v-click class="section-label" style="margin-top:6px;">✔ Solution — Use <span class="mono">this</span></div>
  <div v-after style="background:#f6f8fa;border-radius:10px;border:1px solid #e1e4e8;padding:12px 14px;font-family:'Fira Code',monospace;font-size:.72rem;line-height:1.9;">
    <span style="color:#ef5050;">void</span> <span style="color:#2d7a00;">setName</span>(<span style="color:#ef5050;">String</span> <span style="color:#c49a00;">name</span>) {<br>
    &nbsp;&nbsp;<span style="color:#6b7280;">// 'this.name' = instance variable</span><br>
    &nbsp;&nbsp;<span style="color:#6b7280;">// 'name' alone = parameter (local)</span><br>
    &nbsp;&nbsp;<span style="color:#ef5050;">this</span>.<span style="color:#0e6ead;">name</span> = <span style="color:#c49a00;">name</span>; <span style="color:#6b7280;">// ✔ correct assignment</span><br>
    }
  </div>

  <div v-click class="callout callout-success" style="margin-top:4px;">
    <div><strong><span class="mono">this</span> keyword:</strong> Inside a class method, <span class="mono">this.variableName</span> <strong>always refers to the instance variable</strong>, resolving any ambiguity caused by shadowing.</div>
  </div>

</div>

</div>

  </template>
</Slide2>
