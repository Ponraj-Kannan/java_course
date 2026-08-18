---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 9 — REFERENCE (NON-PRIMITIVE) DATA TYPES
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Data Types">
  <template #content>

<div class="slide-h1" style="margin-bottom:10px;">Reference <span class="highlight">(Non-Primitive) Types</span></div>

<div class="g2" style="gap:14px;">

<div class="flex-col">

  <div v-click class="card-navy" style="border-radius:10px;">
    <div style="font-size:.8rem;line-height:1.6;color:var(--slate);">
      <strong style="color:var(--red);">Definition:</strong> <strong>Reference data types</strong> are non-primitive types created by programmers or Java libraries that store a <strong>memory reference (address)</strong> pointing to an object in memory.
    </div>
  </div>

  <div style="display:flex;flex-direction:column;gap:5px;margin-top:4px;">
    <div v-click class="card-blue" style="border-radius:8px;padding:8px 12px;">
      <div style="font-size:.72rem;font-weight:700;color:var(--blue);margin-bottom:2px;font-family:'Fira Code',monospace;">String</div>
      <div style="font-size:.7rem;color:var(--slate);">Represents a sequence of characters (e.g. <span class="mono">"Hello"</span>)</div>
    </div>
    <div v-click class="card-green" style="border-radius:8px;padding:8px 12px;">
      <div style="font-size:.72rem;font-weight:700;color:var(--green);margin-bottom:2px;font-family:'Fira Code',monospace;">Arrays</div>
      <div style="font-size:.7rem;color:var(--slate);">Holds a fixed-size sequence of elements of the same type (e.g. <span class="mono">int[]</span>)</div>
    </div>
    <div v-click class="card-purple" style="border-radius:8px;padding:8px 12px;">
      <div style="font-size:.72rem;font-weight:700;color:var(--purple);margin-bottom:2px;font-family:'Fira Code',monospace;">Classes &amp; Interfaces</div>
      <div style="font-size:.7rem;color:var(--slate);">User-defined custom objects or API classes (e.g. <span class="mono">Scanner</span>, <span class="mono">Student</span>)</div>
    </div>
  </div>

</div>

<div class="flex-col">
  <div v-click class="section-label">Code Examples</div>

  <div v-after style="background:#f6f8fa;border-radius:10px;border:1px solid #e1e4e8;padding:12px 14px;font-family:'Fira Code',monospace;font-size:.72rem;line-height:1.9;">
    <span style="color:#6b7280;">// Reference variable holding memory address</span><br>
    <span style="color:#0e6ead;">String</span> <span style="color:#0e6ead;">greeting</span> = <span style="color:#2d7a00;">"Hello Java"</span>;<br>
    <span style="color:#ef5050;">int</span>[] <span style="color:#0e6ead;">numbers</span> = { <span style="color:#b45309;">10</span>, <span style="color:#b45309;">20</span>, <span style="color:#b45309;">30</span> };<br>
    <span style="color:#0e6ead;">Scanner</span> <span style="color:#0e6ead;">scanner</span> = <span style="color:#ef5050;">new</span> <span style="color:#0e6ead;">Scanner</span>(<span style="color:#0e6ead;">System</span>.<span style="color:#0e6ead;">in</span>);<br><br>
    <span style="color:#6b7280;">// Uninitialized reference defaults to null</span><br>
    <span style="color:#0e6ead;">String</span> <span style="color:#0e6ead;">unassigned</span>; <span style="color:#6b7280;">// null</span>
  </div>

  <div v-click class="callout callout-warn" style="margin-top:6px;">
    <div><strong>Default Value for Reference Types:</strong> Unlike primitive types which default to zero or false, all reference type fields default to <span class="mono" style="color:var(--red-dark);">null</span> when uninitialized!</div>
  </div>

</div>

</div>

  </template>
</Slide2>
