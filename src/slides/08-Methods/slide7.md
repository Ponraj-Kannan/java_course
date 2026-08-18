---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 7 — STATIC METHODS vs INSTANCE METHODS
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Java Methods">
  <template #content>

<div class="slide-h1" style="margin-bottom:10px;"><span class="highlight">Static</span> vs <span class="highlight">Instance</span> Methods</div>

<div class="g2" style="gap:14px;align-items:start;">

<div class="flex-col">

  <div v-click class="card-navy" style="border-radius:10px;">
    <div style="font-size:.82rem;line-height:1.6;color:var(--slate);">
      <strong style="color:var(--blue);">Static methods</strong> belong to the class itself and can be called directly without creating an object; <strong style="color:var(--green);">instance methods</strong> belong to objects and require an instantiated object to be called.
    </div>
  </div>

  <div style="margin-top:6px;">
    <table class="cmp-table" style="font-size:.68rem;">
      <thead v-click><tr><th>Feature</th><th>Static Method</th><th>Instance Method</th></tr></thead>
      <tbody>
        <tr v-click><td>Keyword</td><td class="mono">static</td><td>No <span class="mono">static</span> keyword</td></tr>
        <tr v-click><td>Calling Syntax</td><td class="mono">ClassName.method()</td><td class="mono">objectName.method()</td></tr>
        <tr v-click><td>Object required?</td><td class="yes">No object needed</td><td class="no">Must create object first</td></tr>
        <tr v-click><td>Access instance data?</td><td class="no">Cannot access instance vars / <span class="mono">this</span></td><td class="yes">Can access instance vars &amp; <span class="mono">this</span></td></tr>
        <tr v-click><td>Typical Use Case</td><td>Utility methods (e.g. <span class="mono">Math.sqrt()</span>)</td><td>Object behavior (e.g. <span class="mono">car.drive()</span>)</td></tr>
      </tbody>
    </table>
  </div>

</div>

<div class="flex-col">
  <div v-click class="section-label">Code Example — Static vs Instance</div>

  <div v-after class="code-block" style="font-size:.68rem;line-height:1.75;">
    <span style="color:#ef5050;">public class</span> <span style="color:#0e6ead;">Calculator</span> {<br>
    <span style="padding-left:16px;display:block;background:#ebf8ff;border-left:2px solid var(--blue);"><span style="color:#6b7280;">// 1. Static utility method</span><br><span style="color:#ef5050;">public static int</span> <span style="color:#0e6ead;">square</span>(<span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">n</span>) {<br>&nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#ef5050;">return</span> n * n;<br>}</span>
    <br>
    <span style="padding-left:16px;display:block;background:#f0fff4;border-left:2px solid var(--green);"><span style="color:#6b7280;">// 2. Instance method (operates on object state)</span><br><span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">memory</span> = <span style="color:#b45309;">0</span>;<br><span style="color:#ef5050;">public void</span> <span style="color:#0e6ead;">addToMemory</span>(<span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">val</span>) {<br>&nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#0e6ead;">this</span>.<span style="color:#0e6ead;">memory</span> += val;<br>}</span>
    }<br>
    <br>
    <span style="color:#6b7280;">// Calling in main():</span><br>
    <span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">sq</span> = <span style="color:#0e6ead;">Calculator</span>.<span style="color:#2d7a00;">square</span>(<span style="color:#b45309;">5</span>); <span style="color:#6b7280;">// No object needed!</span><br>
    <span style="color:#0e6ead;">Calculator</span> <span style="color:#0e6ead;">calc</span> = <span style="color:#ef5050;">new</span> <span style="color:#0e6ead;">Calculator</span>(); <span style="color:#6b7280;">// Create object</span><br>
    <span style="color:#0e6ead;">calc</span>.<span style="color:#2d7a00;">addToMemory</span>(<span style="color:#b45309;">10</span>); <span style="color:#6b7280;">// Call on instance</span>
  </div>

  <div v-click class="callout callout-danger" style="margin-top:6px;">
    <div><strong>Static Trap:</strong> A static method <strong>cannot directly call a non-static method</strong> or access non-static variables without creating an object instance first!</div>
  </div>

</div>

</div>

  </template>
</Slide2>
