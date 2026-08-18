---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 16 — COMMON BEGINNER MISTAKES
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Operators">
  <template #content>

<div class="slide-h1" style="margin-bottom:10px;">Common Beginner <span class="highlight">Mistakes</span></div>

<div class="g2" style="gap:14px;">

<div class="flex-col">

  <div v-click class="card-red" style="border-radius:10px;padding:10px 14px;">
    <div style="font-size:.78rem;font-weight:700;color:var(--red-dark);margin-bottom:2px;">1. Assignment (=) vs Equality (==)</div>
    <div style="font-size:.7rem;color:var(--slate);">
      Writing <span class="mono">if (x = 5)</span> causes a <strong>compile-time error</strong> in Java because <span class="mono">x = 5</span> returns an <span class="mono">int</span>, not a <span class="mono">boolean</span>!
    </div>
    <div style="font-size:.68rem;margin-top:4px;" class="mono">
      <span style="color:var(--red-dark);">✗ if (x = 5)</span> &nbsp;&nbsp; <span style="color:var(--green);">✓ if (x == 5)</span>
    </div>
  </div>

  <div v-click class="card-red" style="border-radius:10px;padding:10px 14px;">
    <div style="font-size:.78rem;font-weight:700;color:var(--red-dark);margin-bottom:2px;">2. Integer Division Truncation</div>
    <div style="font-size:.7rem;color:var(--slate);">
      Dividing integers drops decimals (<span class="mono">7 / 2</span> gives <span class="mono">3</span>, not <span class="mono">3.5</span>). Cast at least one operand to <span class="mono">double</span>!
    </div>
    <div style="font-size:.68rem;margin-top:4px;" class="mono">
      <span style="color:var(--red-dark);">✗ double avg = 7 / 2;</span> <span style="color:var(--muted);">(gives 3.0)</span><br>
      <span style="color:var(--green);">✓ double avg = 7.0 / 2;</span> <span style="color:var(--muted);">(gives 3.5)</span>
    </div>
  </div>

</div>

<div class="flex-col">

  <div v-click class="card-red" style="border-radius:10px;padding:10px 14px;">
    <div style="font-size:.78rem;font-weight:700;color:var(--red-dark);margin-bottom:2px;">3. Postfix vs Prefix Confusion</div>
    <div style="font-size:.7rem;color:var(--slate);">
      Expecting <span class="mono">b = a++</span> to update <span class="mono">b</span> immediately with the incremented value.
    </div>
    <div style="font-size:.68rem;margin-top:4px;" class="mono">
      <span style="color:#ef5050;">int</span> a = 5;<br>
      <span style="color:#ef5050;">int</span> b = a++; <span style="color:var(--muted);">// b is 5! Use ++a if you want b = 6</span>
    </div>
  </div>

  <div v-click class="card-red" style="border-radius:10px;padding:10px 14px;">
    <div style="font-size:.78rem;font-weight:700;color:var(--red-dark);margin-bottom:2px;">4. Comparing Strings with ==</div>
    <div style="font-size:.7rem;color:var(--slate);">
      Using <span class="mono">==</span> checks memory reference identity, not text content equality.
    </div>
    <div style="font-size:.68rem;margin-top:4px;" class="mono">
      <span style="color:var(--red-dark);">✗ if (str1 == str2)</span> <span style="color:var(--muted);">(compares memory address)</span><br>
      <span style="color:var(--green);">✓ if (str1.equals(str2))</span> <span style="color:var(--muted);">(compares text value)</span>
    </div>
  </div>

</div>

</div>

  </template>
</Slide2>
