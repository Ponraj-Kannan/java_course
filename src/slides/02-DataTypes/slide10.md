---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 10 — PRIMITIVE VS REFERENCE TYPES
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Data Types">
  <template #content>

<div class="slide-h1" style="margin-bottom:10px;">Primitive vs Reference <span class="highlight">Types</span></div>

<div class="g2" style="gap:14px;">

<div class="flex-col">

  <div v-click class="card-navy" style="border-radius:10px;">
    <div style="font-size:.8rem;line-height:1.6;color:var(--slate);">
      <strong style="color:var(--red);">Definition:</strong> <strong>Primitive types</strong> store raw values directly on the call <strong>Stack</strong>, while <strong>reference types</strong> store memory pointers on the Stack that point to objects allocated on the <strong>Heap</strong>.
    </div>
  </div>

  <div>
    <table class="cmp-table" style="font-size:.65rem;margin-top:4px;">
      <thead v-click><tr><th>Feature</th><th>Primitive Types</th><th>Reference Types</th></tr></thead>
      <tbody>
        <tr v-click><td style="font-weight:700;">Stored Content</td><td class="mono">Actual value directly</td><td class="mono">Memory reference address</td></tr>
        <tr v-click><td style="font-weight:700;">Memory Region</td><td class="mono">Stack memory</td><td class="mono">Stack (ref) &amp; Heap (object)</td></tr>
        <tr v-click><td style="font-weight:700;">Default Value</td><td class="mono">0, 0.0, false, '\u0000'</td><td class="mono">null</td></tr>
        <tr v-click><td style="font-weight:700;">Can be null?</td><td class="mono no">No</td><td class="mono yes">Yes</td></tr>
        <tr v-click><td style="font-weight:700;">Methods</td><td class="mono no">No methods</td><td class="mono yes">Supports method calls</td></tr>
      </tbody>
    </table>
  </div>

</div>

<div class="flex-col">
  <div v-click class="section-label">Conceptual Memory Layout</div>

  <div v-after style="background:#f7f8fc;border-radius:10px;border:1px solid var(--border);padding:10px 14px;font-size:.7rem;">
    <div style="display:flex;gap:16px;align-items:center;">
      <div style="flex:1;">
        <div style="font-weight:700;color:var(--red-dark);margin-bottom:4px;">STACK MEMORY</div>
        <div style="background:var(--red-soft);border:1px solid var(--red);border-radius:6px;padding:6px;font-family:'Fira Code',monospace;font-size:.65rem;">
          int age = 25; <span style="color:var(--green);">(raw 25)</span><br>
          String str = <span style="color:var(--blue);">0x00A1</span>; <span style="color:var(--blue);">(pointer)</span>
        </div>
      </div>
      <div style="font-size:1.2rem;color:var(--muted);">→</div>
      <div style="flex:1;">
        <div style="font-weight:700;color:var(--blue);margin-bottom:4px;">HEAP MEMORY</div>
        <div style="background:#ebf8ff;border:1px solid var(--blue);border-radius:6px;padding:6px;font-family:'Fira Code',monospace;font-size:.65rem;">
          @ 0x00A1:<br>
          "Hello Java" <span style="color:#2b6cb0;">(Object)</span>
        </div>
      </div>
    </div>
  </div>

  <div v-click class="callout callout-info" style="margin-top:6px;">
    <div><strong>Key Distinction:</strong> Primitive comparisons (<span class="mono">a == b</span>) check value equality, whereas reference comparisons (<span class="mono">s1 == s2</span>) check if both point to the same memory address!</div>
  </div>

</div>

</div>

  </template>
</Slide2>
