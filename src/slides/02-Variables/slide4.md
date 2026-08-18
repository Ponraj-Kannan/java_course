---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 4 — MEMORY VISUALIZATION: REFERENCE VARIABLE
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Java Variables">
  <template #content>

<div class="slide-h1" style="margin-bottom:10px;">Memory Visualization — <span class="highlight">Reference Variable</span></div>

<div class="g2" style="gap:14px;">

<div class="flex-col">

  <div v-click class="card-navy" style="border-radius:10px;">
    <div style="font-size:.82rem;line-height:1.6;color:var(--slate);">
      <strong style="color:var(--red);">Definition:</strong> A <strong>reference variable</strong> does NOT store the object itself. Instead, it stores a <strong>memory address (reference)</strong> pointing to where the actual object lives on the <strong>heap</strong>.
    </div>
  </div>

  <div v-click class="section-label">Code</div>
  <div v-after style="background:#f6f8fa;border-radius:10px;border:1px solid #e1e4e8;padding:14px;font-family:'Fira Code',monospace;font-size:.8rem;line-height:2;">
    <span style="color:#6b7280;">// Reference variable — stores an address</span><br>
    <span style="color:#ef5050;">String</span> <span style="color:#0e6ead;">name</span> = <span style="color:#2d7a00;">"John"</span>;<br>
    <span style="color:#6b7280;">// 'name' holds a pointer to the String object</span>
  </div>

  <div v-click class="callout callout-warn" style="margin-top:4px;">
    <div><strong>Key contrast:</strong> With a primitive, the box <em>contains</em> the value. With a reference, the box <em>contains an arrow</em> that points to the actual object stored elsewhere in heap memory.</div>
  </div>

  <div v-click class="callout callout-info" style="margin-top:4px;">
    <div><strong>Null:</strong> A reference variable that doesn't point to anything holds the special value <span class="mono">null</span>. Accessing a <span class="mono">null</span> reference causes a <strong>NullPointerException</strong>!</div>
  </div>

</div>

<div class="flex-col">

  <div v-click class="section-label">Stack → Heap Diagram</div>

  <div v-after style="display:flex;gap:16px;align-items:flex-start;margin-top:4px;">
    <!-- Stack side -->
    <div style="flex:1;border:3px solid var(--blue);border-radius:12px;padding:8px;background:#ebf8ff;">
      <div style="font-size:.58rem;color:var(--blue);font-weight:700;text-transform:uppercase;letter-spacing:1px;margin-bottom:6px;text-align:center;">STACK</div>
      <div style="border:2px solid var(--red);border-radius:8px;padding:10px;background:#fff;text-align:center;">
        <div style="font-size:.58rem;color:var(--muted);font-weight:700;text-transform:uppercase;margin-bottom:4px;">name <span style="color:var(--red-dark);">(String)</span></div>
        <div style="font-family:'Fira Code',monospace;font-size:.82rem;font-weight:700;color:var(--navy-mid);">ref: 0xA1F2</div>
        <div style="font-size:.58rem;color:var(--muted);margin-top:3px;">holds address →</div>
      </div>
    </div>
    <!-- Arrow -->
    <div style="display:flex;align-items:center;padding-top:40px;font-size:1.6rem;color:var(--orange);font-weight:900;">→</div>
    <!-- Heap side -->
    <div style="flex:1;border:3px solid var(--green);border-radius:12px;padding:8px;background:#f0fff4;">
      <div style="font-size:.58rem;color:var(--green);font-weight:700;text-transform:uppercase;letter-spacing:1px;margin-bottom:6px;text-align:center;">HEAP</div>
      <div style="border:2px solid var(--green);border-radius:8px;padding:10px;background:#fff;text-align:center;">
        <div style="font-size:.58rem;color:var(--muted);font-weight:700;text-transform:uppercase;margin-bottom:4px;">String Object @ 0xA1F2</div>
        <div style="font-family:'Fira Code',monospace;font-size:1rem;font-weight:800;color:var(--green);">"John"</div>
        <div style="font-size:.58rem;color:var(--muted);margin-top:3px;">actual object lives here</div>
      </div>
    </div>

  </div>

  <div v-click style="margin-top:8px;">
    <div class="section-label" style="margin-bottom:4px;">Primitive vs Reference — Summary</div>
    <table class="cmp-table">
      <thead>
        <tr><th>Aspect</th><th>Primitive (<span class="mono">int age</span>)</th><th>Reference (<span class="mono">String name</span>)</th></tr>
      </thead>
      <tbody>
        <tr v-click><td>Stack holds</td><td class="yes">the value directly</td><td style="color:var(--blue);">a memory address</td></tr>
        <tr v-click><td>Heap used?</td><td class="no">No</td><td class="yes">Yes (object lives there)</td></tr>
        <tr v-click><td>Default value</td><td><span class="mono">0 / false</span></td><td><span class="mono">null</span></td></tr>
      </tbody>
    </table>
  </div>

</div>

</div>

  </template>
</Slide2>
