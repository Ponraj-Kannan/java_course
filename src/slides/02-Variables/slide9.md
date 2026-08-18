---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 9 — INSTANCE VARIABLES
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Java Variables">
  <template #content>

<div class="slide-h1" style="margin-bottom:10px;"><span class="highlight">Instance</span> Variables</div>

<div class="g2" style="gap:14px;">

<div class="flex-col">

  <div v-click class="card-navy" style="border-radius:10px;">
    <div style="font-size:.82rem;line-height:1.6;color:var(--slate);">
      <strong style="color:var(--red);">Definition:</strong> An <strong>instance variable</strong> is declared inside a class body but outside any method. Every object created from the class gets its own copy of instance variables, stored on the heap.
    </div>
  </div>

  <div v-click class="section-label">Code Example</div>
  <div v-after style="background:#f6f8fa;border-radius:10px;border:1px solid #e1e4e8;padding:14px;font-family:'Fira Code',monospace;font-size:.72rem;line-height:1.9;">
    <span style="color:#ef5050;">class</span> <span style="color:#0e6ead;">Student</span> {<br>
    &nbsp;&nbsp;<span style="color:#6b7280;">// Instance variables — one copy per object</span><br>
    &nbsp;&nbsp;<span style="color:#ef5050;">String</span> <span style="color:#0e6ead;">name</span>; &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#6b7280;">// defaults to null</span><br>
    &nbsp;&nbsp;<span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">age</span>; &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#6b7280;">// defaults to 0</span><br>
    &nbsp;&nbsp;<span style="color:#ef5050;">double</span> <span style="color:#0e6ead;">marks</span>; &nbsp;&nbsp;&nbsp;<span style="color:#6b7280;">// defaults to 0.0</span><br>
    &nbsp;&nbsp;<span style="color:#ef5050;">boolean</span> <span style="color:#0e6ead;">active</span>; <span style="color:#6b7280;">// defaults to false</span><br>
    }
  </div>

  <div v-click style="background:#f6f8fa;border-radius:10px;border:1px solid #e1e4e8;padding:14px;font-family:'Fira Code',monospace;font-size:.72rem;line-height:1.9;margin-top:4px;">
    <span style="color:#6b7280;">// Each object has its OWN copy</span><br>
    <span style="color:#0e6ead;">Student</span> <span style="color:#0e6ead;">s1</span> = <span style="color:#ef5050;">new</span> <span style="color:#0e6ead;">Student</span>();<br>
    <span style="color:#0e6ead;">s1</span>.<span style="color:#0e6ead;">name</span> = <span style="color:#2d7a00;">"Alice"</span>;<br>
    <span style="color:#0e6ead;">Student</span> <span style="color:#0e6ead;">s2</span> = <span style="color:#ef5050;">new</span> <span style="color:#0e6ead;">Student</span>();<br>
    <span style="color:#0e6ead;">s2</span>.<span style="color:#0e6ead;">name</span> = <span style="color:#2d7a00;">"Bob"</span>; <span style="color:#6b7280;">// separate from s1.name</span>
  </div>

</div>

<div class="flex-col">

  <div v-click class="section-label">Memory Diagram — Two Objects</div>

  <div v-after style="display:flex;gap:12px;">
    <div style="flex:1;border:2px solid var(--green);border-radius:10px;padding:8px;background:#f0fff4;">
      <div style="font-size:.58rem;color:var(--green);font-weight:700;text-transform:uppercase;letter-spacing:1px;margin-bottom:4px;text-align:center;">Heap — s1 (Student)</div>
      <div class="mem-box">
        <div class="mem-row">
          <div class="mem-name">name</div>
          <div class="mem-val">"Alice"</div>
        </div>
        <div class="mem-row">
          <div class="mem-name">age</div>
          <div class="mem-val">0</div>
        </div>
        <div class="mem-row">
          <div class="mem-name">marks</div>
          <div class="mem-val">0.0</div>
        </div>
      </div>
    </div>
    <div style="flex:1;border:2px solid var(--blue);border-radius:10px;padding:8px;background:#ebf8ff;">
      <div style="font-size:.58rem;color:var(--blue);font-weight:700;text-transform:uppercase;letter-spacing:1px;margin-bottom:4px;text-align:center;">Heap — s2 (Student)</div>
      <div class="mem-box">
        <div class="mem-row">
          <div class="mem-name">name</div>
          <div class="mem-val">"Bob"</div>
        </div>
        <div class="mem-row">
          <div class="mem-name">age</div>
          <div class="mem-val">0</div>
        </div>
        <div class="mem-row">
          <div class="mem-name">marks</div>
          <div class="mem-val">0.0</div>
        </div>
      </div>
    </div>
  </div>

  <div v-click class="callout callout-success" style="margin-top:6px;">
    <div><strong>Key point:</strong> Instance variables automatically get <strong>default values</strong> (0, null, false) — unlike local variables! You never need to initialize them explicitly (though it's good practice).</div>
  </div>

  <div v-click class="card card-orange" style="margin-top:4px;">
    <div class="small-text"><strong>Access:</strong> Instance variables are accessed using the object reference: <span class="mono">s1.name</span>. Inside the class, you can use them directly or with <span class="mono">this.name</span>.</div>
  </div>

</div>

</div>

  </template>
</Slide2>
