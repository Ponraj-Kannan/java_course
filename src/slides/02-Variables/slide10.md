---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 10 — STATIC (CLASS) VARIABLES
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Java Variables">
  <template #content>

<div class="slide-h1" style="margin-bottom:10px;"><span class="highlight">Static</span> (Class) Variables</div>

<div class="g2" style="gap:14px;">

<div class="flex-col">

  <div v-click class="card-navy" style="border-radius:10px;">
    <div style="font-size:.82rem;line-height:1.6;color:var(--slate);">
      <strong style="color:var(--red);">Definition:</strong> A <strong>static variable</strong> (also called a class variable) is declared with the <span class="mono" style="color:var(--red-dark);">static</span> keyword inside a class. There is <strong>only ONE copy</strong> of it, shared among all objects of that class.
    </div>
  </div>

  <div v-click class="section-label">Code Example</div>
  <div v-click style="background:#f6f8fa;border-radius:10px;border:1px solid #e1e4e8;padding:14px;font-family:'Fira Code',monospace;font-size:.72rem;line-height:1.9;">
    <span style="color:#ef5050;">class</span> <span style="color:#0e6ead;">Student</span> {<br>
    &nbsp;&nbsp;<span style="color:#6b7280;">// Static — shared by ALL Student objects</span><br>
    &nbsp;&nbsp;<span style="color:#ef5050;">static</span> <span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">totalStudents</span> = <span style="color:#b45309;">0</span>;<br><br>
    &nbsp;&nbsp;<span style="color:#6b7280;">// Instance — each object has its own</span><br>
    &nbsp;&nbsp;<span style="color:#ef5050;">String</span> <span style="color:#0e6ead;">name</span>;<br><br>
    &nbsp;&nbsp;<span style="color:#0e6ead;">Student</span>(<span style="color:#ef5050;">String</span> <span style="color:#0e6ead;">n</span>) {<br>
    &nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#0e6ead;">name</span> = <span style="color:#0e6ead;">n</span>;<br>
    &nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#0e6ead;">totalStudents</span>++; <span style="color:#6b7280;">// shared counter</span><br>
    &nbsp;&nbsp;}<br>
    }
  </div>

  <div v-click style="background:#f6f8fa;border-radius:10px;border:1px solid #e1e4e8;padding:10px 14px;font-family:'Fira Code',monospace;font-size:.72rem;line-height:1.9;margin-top:4px;">
    <span style="color:#ef5050;">new</span> <span style="color:#0e6ead;">Student</span>(<span style="color:#2d7a00;">"Alice"</span>);<br>
    <span style="color:#ef5050;">new</span> <span style="color:#0e6ead;">Student</span>(<span style="color:#2d7a00;">"Bob"</span>);<br>
    <span style="color:#6b7280;">// Access via class name (recommended)</span><br>
    <span style="color:#0e6ead;">System</span>.<span style="color:#0e6ead;">out</span>.<span style="color:#2d7a00;">println</span>(<span style="color:#0e6ead;">Student</span>.<span style="color:#0e6ead;">totalStudents</span>);<span style="color:#6b7280;"> // 2</span>
  </div>

</div>

<div class="flex-col">

  <div v-click class="section-label">Memory — One Shared Copy</div>

  <div v-after style="display:flex;flex-direction:column;gap:8px;">
    <div style="border:2px solid var(--orange);border-radius:10px;padding:8px;background:#fffaf0;">
      <div style="font-size:.58rem;color:var(--orange);font-weight:700;text-transform:uppercase;letter-spacing:1px;margin-bottom:4px;text-align:center;">Method Area (Class-Level Memory)</div>
      <div class="mem-box">
        <div class="mem-header">Static Variables — Student class</div>
        <div class="mem-row">
          <div class="mem-name">totalStudents</div>
          <div class="mem-val">2</div>
          <div class="mem-type">int</div>
        </div>
      </div>
    </div>
    <div style="display:flex;gap:8px;">
      <div style="flex:1;border:2px solid var(--green);border-radius:8px;padding:6px;background:#f0fff4;text-align:center;">
        <div style="font-size:.58rem;color:var(--green);font-weight:700;text-transform:uppercase;margin-bottom:3px;">Heap — s1</div>
        <div style="font-family:'Fira Code',monospace;font-size:.7rem;color:var(--navy);">name: "Alice"</div>
      </div>
      <div style="flex:1;border:2px solid var(--blue);border-radius:8px;padding:6px;background:#ebf8ff;text-align:center;">
        <div style="font-size:.58rem;color:var(--blue);font-weight:700;text-transform:uppercase;margin-bottom:3px;">Heap — s2</div>
        <div style="font-family:'Fira Code',monospace;font-size:.7rem;color:var(--navy);">name: "Bob"</div>
      </div>
    </div>

  </div>

  <div v-click class="callout callout-warn" style="margin-top:6px;">
    <div><strong>Best practice:</strong> Always access static variables using the <strong>class name</strong> (<span class="mono">Student.totalStudents</span>), not through an object reference. This makes the static nature obvious.</div>
  </div>

  <div v-click class="card card-purple" style="margin-top:4px;">
    <div class="small-text"><strong>Common use cases:</strong> Counters, constants (<span class="mono">static final PI = 3.14</span>), shared configuration values, utility method parameters.</div>
  </div>

</div>

</div>

  </template>
</Slide2>
