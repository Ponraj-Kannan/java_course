---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 27 — COMMON BEGINNER MISTAKES
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Java Variables">
  <template #content>

<div class="slide-h1" style="margin-bottom:10px;">Common <span class="highlight">Beginner Mistakes</span></div>

<div class="g2" style="gap:14px;align-items:start;">

<div class="flex-col">

  <div v-click style="display:flex;gap:10px;align-items:flex-start;">
    <div style="background:var(--red);color:#fff;border-radius:50%;width:24px;height:24px;display:flex;align-items:center;justify-content:center;font-size:.7rem;font-weight:800;flex-shrink:0;margin-top:2px;">1</div>
    <div>
      <div class="body-text"><strong>Using a local variable without initializing it</strong></div>
      <div style="background:var(--red-soft);border-radius:8px;padding:8px 12px;font-family:'Fira Code',monospace;font-size:.68rem;line-height:1.8;margin-top:4px;">
        <span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">x</span>;<br>
        <span style="color:#0e6ead;">System</span>.<span style="color:#0e6ead;">out</span>.<span style="color:#2d7a00;">println</span>(<span style="color:#0e6ead;">x</span>); <span style="color:#6b7280;">// ERROR: might not be initialized</span>
      </div>
    </div>
  </div>

  <div v-click style="display:flex;gap:10px;align-items:flex-start;">
    <div style="background:var(--orange);color:#fff;border-radius:50%;width:24px;height:24px;display:flex;align-items:center;justify-content:center;font-size:.7rem;font-weight:800;flex-shrink:0;margin-top:2px;">2</div>
    <div>
      <div class="body-text"><strong>Assuming local variables get default values</strong></div>
      <div style="background:var(--red-soft);border-radius:8px;padding:8px 12px;font-family:'Fira Code',monospace;font-size:.68rem;line-height:1.8;margin-top:4px;">
        <span style="color:#ef5050;">void</span> <span style="color:#2d7a00;">compute</span>() {<br>
        &nbsp;&nbsp;<span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">count</span>; <span style="color:#6b7280;">// NOT 0! No default for locals</span><br>
        &nbsp;&nbsp;<span style="color:#0e6ead;">count</span>++; &nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#6b7280;">// ERROR</span><br>
        }
      </div>
    </div>
  </div>

  <div v-click style="display:flex;gap:10px;align-items:flex-start;">
    <div style="background:var(--blue);color:#fff;border-radius:50%;width:24px;height:24px;display:flex;align-items:center;justify-content:center;font-size:.7rem;font-weight:800;flex-shrink:0;margin-top:2px;">3</div>
    <div>
      <div class="body-text"><strong>Confusing instance vs static access</strong></div>
      <div style="background:var(--red-soft);border-radius:8px;padding:8px 12px;font-family:'Fira Code',monospace;font-size:.68rem;line-height:1.8;margin-top:4px;">
        <span style="color:#0e6ead;">Student</span> <span style="color:#0e6ead;">s</span> = <span style="color:#ef5050;">new</span> <span style="color:#0e6ead;">Student</span>();<br>
        <span style="color:#0e6ead;">s</span>.<span style="color:#0e6ead;">totalStudents</span>; <span style="color:#6b7280;">// warning — use Student.totalStudents</span>
      </div>
    </div>
  </div>

</div>

<div class="flex-col">

  <div v-click style="display:flex;gap:10px;align-items:flex-start;">
    <div style="background:var(--purple);color:#fff;border-radius:50%;width:24px;height:24px;display:flex;align-items:center;justify-content:center;font-size:.7rem;font-weight:800;flex-shrink:0;margin-top:2px;">4</div>
    <div>
      <div class="body-text"><strong>Unintentional shadowing (no <span class="mono">this</span>)</strong></div>
      <div style="background:var(--red-soft);border-radius:8px;padding:8px 12px;font-family:'Fira Code',monospace;font-size:.68rem;line-height:1.8;margin-top:4px;">
        <span style="color:#ef5050;">void</span> <span style="color:#2d7a00;">setAge</span>(<span style="color:#ef5050;">int</span> <span style="color:#c49a00;">age</span>) {<br>
        &nbsp;&nbsp;<span style="color:#c49a00;">age</span> = <span style="color:#c49a00;">age</span>; <span style="color:#6b7280;">// assigns param to itself — does nothing!</span><br>
        &nbsp;&nbsp;<span style="color:#6b7280;">// Fix: this.age = age;</span><br>
        }
      </div>
    </div>
  </div>

  <div v-click style="display:flex;gap:10px;align-items:flex-start;">
    <div style="background:var(--green);color:#fff;border-radius:50%;width:24px;height:24px;display:flex;align-items:center;justify-content:center;font-size:.7rem;font-weight:800;flex-shrink:0;margin-top:2px;">5</div>
    <div>
      <div class="body-text"><strong>Invalid variable names (compiler error)</strong></div>
      <div style="background:var(--red-soft);border-radius:8px;padding:8px 12px;font-family:'Fira Code',monospace;font-size:.68rem;line-height:1.8;margin-top:4px;">
        <span style="color:#ef5050;">int</span> <span style="color:#ef5050;">2marks</span> = <span style="color:#b45309;">90</span>;&nbsp;&nbsp;&nbsp;<span style="color:#6b7280;">// ✘ starts with digit</span><br>
        <span style="color:#ef5050;">String</span> <span style="color:#ef5050;">class</span> = <span style="color:#2d7a00;">"A"</span>;&nbsp;<span style="color:#6b7280;">// ✘ reserved keyword</span><br>
        <span style="color:#ef5050;">double</span> <span style="color:#ef5050;">my-price</span> = <span style="color:#b45309;">5</span>;<span style="color:#6b7280;">// ✘ hyphen not allowed</span>
      </div>
    </div>
  </div>

  <div v-click class="callout callout-success" style="margin-top:6px;">
    <div>
      <strong>Quick Fix Checklist:</strong><br>
      ✔ Always initialize local variables before use<br>
      ✔ Use <span class="mono">this.</span> to distinguish instance from local<br>
      ✔ Access static variables via class name<br>
      ✔ Check names against all 6 naming rules
    </div>
  </div>

</div>

</div>

  </template>
</Slide2>
