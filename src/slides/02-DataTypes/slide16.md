---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 16 — AUTOBOXING & UNBOXING
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Data Types">
  <template #content>

<div class="slide-h1" style="margin-bottom:10px;">Autoboxing &amp; <span class="highlight">Unboxing</span></div>

<div class="g2" style="gap:14px;">

<div class="flex-col">

  <div v-click class="card-navy" style="border-radius:10px;">
    <div style="font-size:.78rem;line-height:1.5;color:var(--slate);">
      <strong style="color:var(--red);">1. Autoboxing:</strong> The automatic conversion performed by the Java compiler from a primitive type into its corresponding wrapper object (e.g. <span class="mono">int</span> → <span class="mono">Integer</span>).
    </div>
  </div>

  <div v-click class="card-navy" style="border-radius:10px;margin-top:4px;">
    <div style="font-size:.78rem;line-height:1.5;color:var(--slate);">
      <strong style="color:var(--red);">2. Unboxing:</strong> The automatic conversion of a wrapper object back into its corresponding primitive value (e.g. <span class="mono">Integer</span> → <span class="mono">int</span>).
    </div>
  </div>

  <div v-click class="callout callout-info" style="margin-top:6px;">
    <div><strong>Compiler Magic:</strong> Introduced in Java 5 to eliminate repetitive manual object instantiation like <span class="mono">new Integer(5)</span>!</div>
  </div>

</div>

<div class="flex-col">
  <div v-click class="section-label">Code Example in Action</div>

  <div v-after style="background:#f6f8fa;border-radius:10px;border:1px solid #e1e4e8;padding:12px 14px;font-family:'Fira Code',monospace;font-size:.72rem;line-height:1.9;">
    <span style="color:#6b7280;">// 1. Autoboxing: int primitive to Integer object</span><br>
    <span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">num</span> = <span style="color:#b45309;">25</span>;<br>
    <span style="color:#0e6ead;">Integer</span> <span style="color:#0e6ead;">boxedNum</span> = <span style="color:#0e6ead;">num</span>; <span style="color:#6b7280;">// Automatic conversion</span><br><br>
    <span style="color:#6b7280;">// 2. Unboxing: Integer object to int primitive</span><br>
    <span style="color:#0e6ead;">Integer</span> <span style="color:#0e6ead;">obj</span> = <span style="color:#ef5050;">new</span> <span style="color:#0e6ead;">Integer</span>(<span style="color:#b45309;">50</span>);<br>
    <span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">unboxedNum</span> = <span style="color:#0e6ead;">obj</span>; &nbsp;<span style="color:#6b7280;">// Automatic conversion</span>
  </div>

  <div v-click class="callout callout-danger" style="margin-top:6px;">
    <div><strong>NullPointerException Danger:</strong> If a wrapper object is <span class="mono">null</span>, unboxing it to a primitive causes a runtime crash!<br>
    <span class="mono" style="color:var(--red-dark);">Integer x = null; int y = x; // Throws NullPointerException!</span></div>
  </div>

</div>

</div>

  </template>
</Slide2>
