---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 19 — COMMON BEGINNER MISTAKES
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Data Types">
  <template #content>

<div class="slide-h1" style="margin-bottom:10px;">Common Beginner <span class="highlight">Mistakes</span></div>

<div class="g2" style="gap:14px;">

<div class="flex-col">

  <div v-click class="card-red" style="border-radius:10px;padding:10px 14px;">
    <div style="font-size:.78rem;font-weight:700;color:var(--red-dark);margin-bottom:2px;">1. Primitive Overflow Wrap-Around</div>
    <div style="font-size:.7rem;color:var(--slate);">
      Adding 1 to a maximum primitive value wraps around to the minimum value without warning!
    </div>
    <div style="font-size:.68rem;margin-top:4px;" class="mono">
      <span style="color:#ef5050;">byte</span> b = <span style="color:#b45309;">127</span>; b++; <span style="color:var(--muted);">(b becomes -128!)</span>
    </div>
  </div>

  <div v-click class="card-red" style="border-radius:10px;padding:10px 14px;">
    <div style="font-size:.78rem;font-weight:700;color:var(--red-dark);margin-bottom:2px;">2. Floating-Point Precision Loss</div>
    <div style="font-size:.7rem;color:var(--slate);">
      <span class="mono">float</span> has only 6–7 decimal digits of precision. Use <span class="mono">double</span> or <span class="mono">BigDecimal</span> for financial math!
    </div>
    <div style="font-size:.68rem;margin-top:4px;" class="mono">
      <span style="color:var(--red-dark);">✗ float price = 3.1415926535f;</span> <span style="color:var(--muted);">(loses precision)</span><br>
      <span style="color:var(--green);">✓ double price = 3.1415926535;</span>
    </div>
  </div>

</div>

<div class="flex-col">

  <div v-click class="card-red" style="border-radius:10px;padding:10px 14px;">
    <div style="font-size:.78rem;font-weight:700;color:var(--red-dark);margin-bottom:2px;">3. Confusing char (' ') with String (" ")</div>
    <div style="font-size:.7rem;color:var(--slate);">
      <span class="mono">char</span> uses single quotes <span class="mono">'A'</span>. <span class="mono">String</span> uses double quotes <span class="mono">"A"</span>. They are completely different types in Java!
    </div>
    <div style="font-size:.68rem;margin-top:4px;" class="mono">
      <span style="color:var(--red-dark);">✗ char c = "A";</span> <span style="color:var(--muted);">(Compile error!)</span><br>
      <span style="color:var(--green);">✓ char c = 'A'; String s = "A";</span>
    </div>
  </div>

  <div v-click class="card-red" style="border-radius:10px;padding:10px 14px;">
    <div style="font-size:.78rem;font-weight:700;color:var(--red-dark);margin-bottom:2px;">4. Unboxing NullPointerException</div>
    <div style="font-size:.7rem;color:var(--slate);">
      Assigning a <span class="mono">null</span> wrapper object to a primitive variable crashes at runtime.
    </div>
    <div style="font-size:.68rem;margin-top:4px;" class="mono">
      <span style="color:#0e6ead;">Integer</span> val = <span style="color:#ef5050;">null</span>;<br>
      <span style="color:#ef5050;">int</span> x = val; <span style="color:var(--muted);">(Throws NullPointerException!)</span>
    </div>
  </div>

</div>

</div>

  </template>
</Slide2>
