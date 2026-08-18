---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 13 — VARIABLE LIFETIME
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Java Variables">
  <template #content>

<div class="slide-h1" style="margin-bottom:10px;">Variable <span class="highlight">Lifetime</span></div>

<div class="g2" style="gap:14px;align-items:start;">

<div class="flex-col">

  <div v-click class="card-navy" style="border-radius:10px;">
    <div style="font-size:.82rem;line-height:1.6;color:var(--slate);">
      <strong style="color:var(--red);">Definition:</strong> <strong>Lifetime</strong> is the period during program execution when a variable exists in memory — from the moment it is created to the moment it is destroyed.
    </div>
  </div>

  <div style="display:flex;flex-direction:column;gap:6px;">
    <div  v-click class="card" style="padding:10px 14px;">
      <div style="display:flex;gap:8px;align-items:flex-start;">
        <span class="pill pill-blue" style="flex-shrink:0;">Local</span>
        <div>
          <div class="body-text"><strong>Created:</strong> when the block is entered (at the declaration)</div>
          <div class="body-text"><strong>Destroyed:</strong> when the block exits (closing <span class="mono">}</span>)</div>
          <div style="font-size:.65rem;color:var(--muted);margin-top:2px;">Memory: Stack — freed immediately</div>
        </div>
      </div>
    </div>
    <div v-click class="card" style="padding:10px 14px;">
      <div style="display:flex;gap:8px;align-items:flex-start;">
        <span class="pill pill-green" style="flex-shrink:0;">Instance</span>
        <div>
          <div class="body-text"><strong>Created:</strong> when an object is instantiated with <span class="mono">new</span></div>
          <div class="body-text"><strong>Destroyed:</strong> when the object is garbage collected (no references left)</div>
          <div style="font-size:.65rem;color:var(--muted);margin-top:2px;">Memory: Heap — managed by Garbage Collector</div>
        </div>
      </div>
    </div>
    <div v-click class="card" style="padding:10px 14px;">
      <div style="display:flex;gap:8px;align-items:flex-start;">
        <span class="pill pill-orange" style="flex-shrink:0;">Static</span>
        <div>
          <div class="body-text"><strong>Created:</strong> when the class is loaded by the JVM</div>
          <div class="body-text"><strong>Destroyed:</strong> when the program ends (or class is unloaded)</div>
          <div style="font-size:.65rem;color:var(--muted);margin-top:2px;">Memory: Method Area — longest lifetime</div>
        </div>
      </div>
    </div>

  </div>

</div>

<div class="flex-col">

  <div v-click class="section-label">Lifetime Timeline</div>

  <div v-after style="display:flex;flex-direction:column;gap:8px;margin-top:4px;">
    <div style="display:flex;align-items:center;gap:6px;">
      <span class="pill pill-blue" style="min-width:60px;text-align:center;">Local</span>
      <div style="flex:1;background:var(--blue);border-radius:4px;height:14px;opacity:0.5;max-width:30%;"></div>
      <span style="font-size:.6rem;color:var(--muted);">shortest</span>
    </div>
    <div style="display:flex;align-items:center;gap:6px;">
      <span class="pill pill-green" style="min-width:60px;text-align:center;">Instance</span>
      <div style="flex:1;background:var(--green);border-radius:4px;height:14px;opacity:0.5;max-width:65%;"></div>
      <span style="font-size:.6rem;color:var(--muted);">object lifetime</span>
    </div>
    <div style="display:flex;align-items:center;gap:6px;">
      <span class="pill pill-orange" style="min-width:60px;text-align:center;">Static</span>
      <div style="flex:1;background:var(--orange);border-radius:4px;height:14px;opacity:0.5;"></div>
      <span style="font-size:.6rem;color:var(--muted);">longest (program)</span>
    </div>
    <div style="font-size:.6rem;color:var(--muted);text-align:right;margin-top:2px;">← program start &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; program end →</div>
  </div>

  <div v-click class="callout callout-warn" style="margin-top:8px;">
    <div><strong>Garbage Collection:</strong> Java automatically reclaims heap memory for objects with no more references — you don't manually free memory like in C/C++.</div>
  </div>

  <div v-click class="callout callout-info" style="margin-top:4px;">
    <div><strong>Exam tip:</strong> A local variable's lifetime = its scope. An instance variable's lifetime = the lifetime of its containing object. A static variable's lifetime = the application's lifetime.</div>
  </div>

</div>

</div>

  </template>
</Slide2>
