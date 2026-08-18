---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 4 — JAVA vs OTHER LANGUAGES
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Features of Java — Comparison">
  <template #content>
<div class="slide-h1" style="margin-bottom:12px;">Java <span class="highlight">vs</span> Other Languages</div>

<div>
<table class="cmp-table">
  <thead>
    <tr v-click>
      <th>Feature</th>
      <th>Java</th>
      <th>Python</th>
      <th>C++</th>
    </tr>
  </thead>
  <tbody>
    <tr v-click>
      <td><strong>Type System</strong></td>
      <td><span class="yes">Static (compile-time)</span></td>
      <td><span style="color:#dd6b20;">Dynamic (runtime)</span></td>
      <td><span class="yes">Static (compile-time)</span></td>
    </tr>
    <tr v-click>
      <td><strong>Platform</strong></td>
      <td><span class="yes">JVM (cross-platform)</span></td>
      <td><span class="yes">Interpreter (cross-platform)</span></td>
      <td><span class="no">Native (OS-specific binary)</span></td>
    </tr>
    <tr v-click>
      <td><strong>Memory Management</strong></td>
      <td><span class="yes">Automatic (GC)</span></td>
      <td><span class="yes">Automatic (GC)</span></td>
      <td><span class="no">Manual (malloc/free)</span></td>
    </tr>
    <tr v-click>
      <td><strong>Performance</strong></td>
      <td><span style="color:#dd6b20;">Fast (JIT compiled)</span></td>
      <td><span class="no">Slower (interpreted)</span></td>
      <td><span class="yes">Fastest (native)</span></td>
    </tr>
    <tr v-click>
      <td><strong>Learning Curve</strong></td>
      <td><span style="color:#dd6b20;">Moderate</span></td>
      <td><span class="yes">Very Easy</span></td>
      <td><span class="no">Difficult</span></td>
    </tr>
  </tbody>
</table>
</div>

<div class="g2" style="gap:10px;margin-top:12px;">
<div v-click class="card card-blue">
  <div class="small-text"><strong>Java advantage:</strong> Excellent performance, strong type safety, massive ecosystem — ideal for enterprise & Android apps.</div>
</div>
<div v-click class="card card-red">
  <div class="small-text"><strong>Java trade-off:</strong> More verbose than Python — a Java Hello World needs a class, main method, and <span class="mono">System.out.println()</span>.</div>
</div>
</div>

  </template>
</Slide2>
