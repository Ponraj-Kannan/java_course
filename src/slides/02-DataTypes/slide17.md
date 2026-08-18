---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 17 — TYPE INFERENCE WITH var (JAVA 10+)
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Data Types">
  <template #content>

<div class="slide-h1" style="margin-bottom:10px;">Type Inference with <span class="highlight">var (Java 10+)</span></div>

<div class="g2" style="gap:14px;">

<div class="flex-col">

  <div v-click class="card-navy" style="border-radius:10px;">
    <div style="font-size:.8rem;line-height:1.6;color:var(--slate);">
      <strong style="color:var(--red);">Definition:</strong> The <span class="mono">var</span> keyword allows the Java compiler to automatically <strong>infer the data type</strong> of a local variable based on its initialization expression at compile-time.
    </div>
  </div>

  <div v-click class="section-label" style="margin-top:4px;">Allowed Code Examples</div>
  <div v-after style="background:#f6f8fa;border-radius:10px;border:1px solid #e1e4e8;padding:12px 14px;font-family:'Fira Code',monospace;font-size:.72rem;line-height:1.9;">
    <span style="color:#ef5050;">var</span> <span style="color:#0e6ead;">count</span> = <span style="color:#b45309;">10</span>; &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#6b7280;">// Inferred as int</span><br>
    <span style="color:#ef5050;">var</span> <span style="color:#0e6ead;">rate</span> = <span style="color:#b45309;">4.5</span>; &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#6b7280;">// Inferred as double</span><br>
    <span style="color:#ef5050;">var</span> <span style="color:#0e6ead;">message</span> = <span style="color:#2d7a00;">"Hello"</span>; <span style="color:#6b7280;">// Inferred as String</span><br>
    <span style="color:#ef5050;">var</span> <span style="color:#0e6ead;">list</span> = <span style="color:#ef5050;">new</span> <span style="color:#0e6ead;">ArrayList</span>&lt;<span style="color:#0e6ead;">String</span>&gt;();
  </div>

  <div v-click class="callout callout-info" style="margin-top:4px;">
    <div><strong>Still Statically Typed:</strong> <span class="mono">var</span> does NOT make Java dynamically typed! The type is resolved at compile-time and can never change.</div>
  </div>

</div>

<div class="flex-col">

  <div v-click class="section-label">Where var CANNOT Be Used</div>

  <div v-click class="card-red" style="border-radius:8px;padding:8px 12px;">
    <div style="font-size:.72rem;font-weight:700;color:var(--red-dark);margin-bottom:2px;">1. Without Immediate Initialization</div>
    <div style="font-size:.68rem;" class="mono"><span style="color:var(--red-dark);">✗ var x;</span> <span style="color:var(--muted);">(Compiler cannot infer type)</span></div>
  </div>

  <div v-click class="card-red" style="border-radius:8px;padding:8px 12px;margin-top:4px;">
    <div style="font-size:.72rem;font-weight:700;color:var(--red-dark);margin-bottom:2px;">2. Initialized with null</div>
    <div style="font-size:.68rem;" class="mono"><span style="color:var(--red-dark);">✗ var obj = null;</span> <span style="color:var(--muted);">(null has no specific type)</span></div>
  </div>

  <div v-click class="card-red" style="border-radius:8px;padding:8px 12px;margin-top:4px;">
    <div style="font-size:.72rem;font-weight:700;color:var(--red-dark);margin-bottom:2px;">3. Class Fields or Method Parameters</div>
    <div style="font-size:.68rem;" class="mono"><span style="color:var(--red-dark);">✗ void print(var input) { }</span> <span style="color:var(--muted);">(Allowed ONLY in local variables)</span></div>
  </div>

</div>

</div>

  </template>
</Slide2>
