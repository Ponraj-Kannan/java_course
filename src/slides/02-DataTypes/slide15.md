---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 15 — JAVA WRAPPER CLASSES
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Data Types">
  <template #content>

<div class="slide-h1" style="margin-bottom:10px;">Java <span class="highlight">Wrapper Classes</span></div>

<div class="g2" style="gap:14px;">

<div class="flex-col">

  <div v-click class="card-navy" style="border-radius:10px;">
    <div style="font-size:.8rem;line-height:1.6;color:var(--slate);">
      <strong style="color:var(--red);">Definition:</strong> <strong>Wrapper classes</strong> encapsulate primitive data values into reference objects within the <span class="mono">java.lang</span> package, allowing primitives to be treated as objects.
    </div>
  </div>

  <div>
    <table class="cmp-table" style="font-size:.68rem;margin-top:4px;">
      <thead v-click><tr><th>Primitive Type</th><th>Wrapper Class</th><th>Utility Example Method</th></tr></thead>
      <tbody>
        <tr v-click><td class="mono">int</td><td class="mono yes">Integer</td><td class="mono">Integer.parseInt("100")</td></tr>
        <tr v-click><td class="mono">double</td><td class="mono yes">Double</td><td class="mono">Double.parseDouble("3.14")</td></tr>
        <tr v-click><td class="mono">char</td><td class="mono yes">Character</td><td class="mono">Character.isDigit('5')</td></tr>
        <tr v-click><td class="mono">boolean</td><td class="mono yes">Boolean</td><td class="mono">Boolean.valueOf("true")</td></tr>
        <tr v-click><td class="mono">byte, short, long, float</td><td class="mono yes">Byte, Short, Long, Float</td><td class="mono">Long.MAX_VALUE</td></tr>
      </tbody>
    </table>
  </div>

</div>

<div class="flex-col">
  <div v-click class="section-label">Why Wrapper Classes are Needed</div>

  <div v-click class="card-blue" style="border-radius:8px;padding:8px 12px;">
    <div style="font-size:.72rem;font-weight:700;color:var(--blue);margin-bottom:2px;">1. Collections &amp; Generics</div>
    <div style="font-size:.7rem;color:var(--slate);">Java data structures (like <span class="mono">ArrayList&lt;Integer&gt;</span>) can only store objects, not primitives!</div>
  </div>

  <div v-click class="card-green" style="border-radius:8px;padding:8px 12px;margin-top:4px;">
    <div style="font-size:.72rem;font-weight:700;color:var(--green);margin-bottom:2px;">2. Static Utility Methods</div>
    <div style="font-size:.7rem;color:var(--slate);">Parsing strings to numbers (<span class="mono">Integer.parseInt()</span>), min/max constants (<span class="mono">Integer.MAX_VALUE</span>).</div>
  </div>

  <div v-click class="card-orange" style="border-radius:8px;padding:8px 12px;margin-top:4px;">
    <div style="font-size:.72rem;font-weight:700;color:var(--orange);margin-bottom:2px;">3. Support for null Values</div>
    <div style="font-size:.7rem;color:var(--slate);">Wrapper variables can hold <span class="mono">null</span> to represent missing or uninitialized data in database models.</div>
  </div>

</div>

</div>

  </template>
</Slide2>
