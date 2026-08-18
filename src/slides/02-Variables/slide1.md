---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 1 — WHAT IS A VARIABLE? (Brief Recap)
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Java Variables">
  <template #content>

<div class="slide-h1" style="margin-bottom:12px;">What is a <span class="highlight">Variable?</span></div>

<div class="g2" style="gap:14px;align-items:start;">

<div class="flex-col">

  <div v-click class="card-navy" style="border-radius:10px;">
    <div style="font-size:.82rem;line-height:1.6;color:var(--slate);">
      <strong style="color:var(--red);">Definition:</strong> A <strong style="color:var(--red);">variable</strong> is a <strong style="color:var(--green);">named storage location</strong> in memory that holds a value of a specific type. It gives a meaningful name to a piece of data your program can read and modify.
    </div>
  </div>

  <div v-click class="callout callout-warn">
    <div><strong>Real-World Analogy:</strong> A variable is like a labelled box — the label is the variable name, the type is what kind of thing the box can hold, and the value is what's currently inside it.</div>
  </div>

  <div v-click style="background:#f6f8fa;border-radius:10px;border:1px solid #e1e4e8;padding:14px;font-family:'Fira Code',monospace;font-size:.78rem;line-height:2;">
    <span style="color:#6b7280;">// Java requires type + name + value</span><br>
    <span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">age</span> = <span style="color:#b45309;">20</span>;<br>
    <span style="color:#ef5050;">String</span> <span style="color:#0e6ead;">name</span> = <span style="color:#2d7a00;">"Alice"</span>;<br>
    <span style="color:#ef5050;">double</span> <span style="color:#0e6ead;">marks</span> = <span style="color:#b45309;">95.5</span>;
  </div>

  <div v-click class="card card-green">
    <div class="small-text"><strong>Key idea:</strong> Unlike Python, Java requires you to declare the <em>type</em> explicitly. Once declared, the variable's type cannot change.</div>
  </div>

</div>

<div class="flex-col">

  <div v-click class="section-label">Variable as a Labelled Typed Box</div>

  <div v-after style="display:flex;flex-direction:column;gap:8px;">
    <div style="display:flex;align-items:center;gap:10px;">
      <div style="background:var(--red-soft);border:2px dashed var(--red);border-radius:10px;padding:10px 18px;min-width:70px;text-align:center;">
        <div style="font-size:.58rem;color:var(--muted);font-weight:700;text-transform:uppercase;letter-spacing:1px;margin-bottom:2px;">Type</div>
        <div style="font-family:'Fira Code',monospace;font-weight:800;color:var(--red-dark);font-size:.78rem;">int</div>
      </div>
      <div style="background:#ebf8ff;border:2px dashed var(--blue);border-radius:10px;padding:10px 18px;min-width:70px;text-align:center;">
        <div style="font-size:.58rem;color:var(--muted);font-weight:700;text-transform:uppercase;letter-spacing:1px;margin-bottom:2px;">Name</div>
        <div style="font-family:'Fira Code',monospace;font-weight:800;color:var(--blue);font-size:.78rem;">age</div>
      </div>
      <div style="color:var(--muted);font-size:1.2rem;font-weight:900;">→</div>
      <div style="background:#f0fff4;border:2px solid var(--green);border-radius:10px;padding:10px 18px;flex:1;text-align:center;">
        <div style="font-size:.58rem;color:var(--muted);font-weight:700;text-transform:uppercase;letter-spacing:1px;margin-bottom:2px;">Value</div>
        <div style="font-family:'Fira Code',monospace;font-weight:800;color:var(--green);font-size:.85rem;">20</div>
      </div>
    </div>
    <div style="display:flex;align-items:center;gap:10px;">
      <div style="background:var(--red-soft);border:2px dashed var(--red);border-radius:10px;padding:10px 18px;min-width:70px;text-align:center;">
        <div style="font-size:.58rem;color:var(--muted);font-weight:700;text-transform:uppercase;letter-spacing:1px;margin-bottom:2px;">Type</div>
        <div style="font-family:'Fira Code',monospace;font-weight:800;color:var(--red-dark);font-size:.78rem;">String</div>
      </div>
      <div style="background:#ebf8ff;border:2px dashed var(--blue);border-radius:10px;padding:10px 18px;min-width:70px;text-align:center;">
        <div style="font-size:.58rem;color:var(--muted);font-weight:700;text-transform:uppercase;letter-spacing:1px;margin-bottom:2px;">Name</div>
        <div style="font-family:'Fira Code',monospace;font-weight:800;color:var(--blue);font-size:.78rem;">name</div>
      </div>
      <div style="color:var(--muted);font-size:1.2rem;font-weight:900;">→</div>
      <div style="background:#f0fff4;border:2px solid var(--green);border-radius:10px;padding:10px 18px;flex:1;text-align:center;">
        <div style="font-size:.58rem;color:var(--muted);font-weight:700;text-transform:uppercase;letter-spacing:1px;margin-bottom:2px;">Value</div>
        <div style="font-family:'Fira Code',monospace;font-weight:800;color:var(--green);font-size:.85rem;">"Alice"</div>
      </div>
    </div>
  </div>

  <div v-click class="card card-blue" style="margin-top:4px;">
    <div class="small-text"><strong>Module focus:</strong> This module covers how variables are <em>created</em>, stored in memory, categorized, scoped, named, and the rules that govern them in Java.</div>
  </div>

</div>

</div>

  </template>
</Slide2>
