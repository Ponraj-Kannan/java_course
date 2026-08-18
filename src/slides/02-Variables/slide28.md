---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 28 — CODING PRACTICE
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Java Variables">
  <template #content>

<div class="slide-h1" style="margin-bottom:10px;">Coding <span class="highlight">Practice</span></div>

<div class="g2" style="gap:14px;align-items:start;">

<div class="flex-col">

  <div class="activity-box">
    <div class="act-title">🖥 Java Variables Exercises</div>

    <div class="act-task" v-click>
      <div style="font-size:.7rem;font-weight:700;color:var(--navy);margin-bottom:4px;">Exercise 1 — All Three Categories</div>
      <div style="font-size:.72rem;color:var(--slate);">Create a class <span class="mono">Student</span> with a <strong>local variable</strong> inside a method, an <strong>instance variable</strong>, and a <strong>static variable</strong>. Print all three values from the main method.</div>
      <div class="hint">💡 Hint: instance vars accessed via object, static via class name</div>
    </div>

    <div class="act-task" v-click>
      <div style="font-size:.7rem;font-weight:700;color:var(--navy);margin-bottom:4px;">Exercise 2 — Shadowing &amp; this</div>
      <div style="font-size:.72rem;color:var(--slate);">Write a class <span class="mono">Circle</span> with an instance variable <span class="mono">radius</span>. Create a constructor that takes a parameter also named <span class="mono">radius</span>. First write it <em>without</em> <span class="mono">this</span> (observe the bug), then fix it using <span class="mono">this.radius = radius</span>.</div>
      <div class="hint">💡 Print the radius after construction to verify the fix</div>
    </div>

    <div class="act-task" v-click>
      <div style="font-size:.7rem;font-weight:700;color:var(--navy);margin-bottom:4px;">Exercise 3 — Trigger and Fix the Uninitialized Error</div>
      <div style="font-size:.72rem;color:var(--slate);">Intentionally declare a local <span class="mono">int score;</span> and try to print it. Observe the compiler error. Then fix it by initializing to <span class="mono">0</span> and run again.</div>
      <div class="hint">💡 Error message: "variable score might not have been initialized"</div>
    </div>

  </div>

</div>

<div class="flex-col">

  <div class="activity-box">

    <div class="act-task" v-click>
      <div style="font-size:.7rem;font-weight:700;color:var(--navy);margin-bottom:4px;">Exercise 4 — Valid or Invalid Names?</div>
      <div style="font-size:.72rem;color:var(--slate);">For each name below, state whether it is valid or invalid, and which rule it violates:</div>
      <div style="font-family:'Fira Code',monospace;font-size:.68rem;color:var(--navy);margin-top:6px;line-height:1.8;">
        <span style="color:var(--muted);">a)</span> <span>_totalMarks</span>&nbsp;&nbsp;
        <span style="color:var(--muted);">b)</span> <span>3rdPlace</span>&nbsp;&nbsp;
        <span style="color:var(--muted);">c)</span> <span>for</span><br>
        <span style="color:var(--muted);">d)</span> <span>student Name</span>&nbsp;&nbsp;
        <span style="color:var(--muted);">e)</span> <span>$salary</span>&nbsp;&nbsp;
        <span style="color:var(--muted);">f)</span> <span>my@email</span>
      </div>
      <div class="hint">💡 Refer to the 6 naming rules summary slide</div>
    </div>

    <div class="act-task" v-click>
      <div style="font-size:.7rem;font-weight:700;color:var(--navy);margin-bottom:4px;">Exercise 5 — Rename for Conventions</div>
      <div style="font-size:.72rem;color:var(--slate);">Rename these poorly-named variables to follow Java conventions:</div>
      <div style="background:#f6f8fa;border-radius:8px;padding:8px 12px;font-family:'Fira Code',monospace;font-size:.68rem;line-height:1.8;margin-top:6px;">
        <span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">X</span> = <span style="color:#b45309;">20</span>; <span style="color:#6b7280;">// → ?</span><br>
        <span style="color:#ef5050;">double</span> <span style="color:#0e6ead;">TOTAL_marks</span> = <span style="color:#b45309;">450.0</span>; <span style="color:#6b7280;">// → ?</span><br>
        <span style="color:#ef5050;">static</span> <span style="color:#ef5050;">final</span> <span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">maxSize</span> = <span style="color:#b45309;">100</span>; <span style="color:#6b7280;">// → ?</span>
      </div>
      <div class="hint">💡 Variables: camelCase | Constants: UPPER_SNAKE_CASE</div>
    </div>

    <div v-click class="callout callout-info" style="margin-top:6px;">
      <div><strong>Bonus:</strong> Write a class that demonstrates <span class="mono">final</span> on all three variable categories (local, instance, static). Try to reassign each and document the error messages.</div>
    </div>

  </div>

</div>

</div>

  </template>
</Slide2>
