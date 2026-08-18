---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 5 — COMMON BEGINNER MISTAKES
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Comments">
  <template #content>

<div class="slide-h1" style="margin-bottom:10px;">Common Beginner <span class="highlight">Mistakes</span></div>

<div class="g2" style="gap:12px;align-items:start;">

<div class="flex-col" style="gap:8px;">

  <div v-click class="card card-red">
    <div class="slide-h3" style="color:var(--red-dark);margin-bottom:4px;">1. Over-commenting Every Line</div>
    <div class="body-text">Adding a comment to every single statement creates noise and hides the real explanations that matter.</div>
    <div style="font-family:'Fira Code',monospace;font-size:.68rem;background:#fff;padding:8px;border-radius:6px;margin-top:6px;line-height:1.8;">
      <span style="color:#ef5050;">// Declare integer variable x</span><br>
      <span style="color:#0e6ead;">int</span> x = <span style="color:#b45309;">5</span>; <span style="color:#ef5050;">// set x to 5</span><br>
      <span style="color:#ef5050;">// Print x</span><br>
      System.out.<span style="color:#2d7a00;">println</span>(x); <span style="color:#ef5050;">// print</span>
    </div>
  </div>

  <div v-click class="card card-red">
    <div class="slide-h3" style="color:var(--red-dark);margin-bottom:4px;">2. Leaving Outdated / Stale Comments</div>
    <div class="body-text">Changing code but forgetting to update the comment creates a contradiction that misleads every reader.</div>
    <div style="font-family:'Fira Code',monospace;font-size:.68rem;background:#fff;padding:8px;border-radius:6px;margin-top:6px;line-height:1.8;">
      <span style="color:#ef5050;">// Returns the discount as a percentage</span><br>
      <span style="color:#0e6ead;">double</span> getDiscount() {<br>
      &nbsp;&nbsp;<span style="color:#ef5050;">return</span> <span style="color:#b45309;">0.15</span>; <span style="color:#6b7280;">// ← now returns a decimal, not %!</span><br>
      }
    </div>
  </div>

</div>

<div class="flex-col" style="gap:8px;">

  <div v-click class="card card-orange">
    <div class="slide-h3" style="color:var(--orange);margin-bottom:4px;">3. Unclosed Multi-line Comment</div>
    <div class="body-text">Forgetting the closing <span class="mono">*/</span> causes the compiler to eat all subsequent code as a comment — a compile error.</div>
    <div style="font-family:'Fira Code',monospace;font-size:.68rem;background:#fff;padding:8px;border-radius:6px;margin-top:6px;line-height:1.8;">
      <span style="color:#ef5050;">/*</span><br>
      <span style="color:#ef5050;">&nbsp; This initializes the counter</span><br>
      <span style="color:#6b7280;">// ✘ missing closing */  ← everything below is now commented out!</span><br>
      <span style="color:#ef5050;">int</span> count = <span style="color:#b45309;">0</span>; <span style="color:#ef5050;">// compiler never sees this</span>
    </div>
    <div class="callout callout-danger" style="margin-top:6px;font-size:.7rem;">
      <div><strong>Compiler error:</strong> <span class="mono">error: reached end of file while parsing</span></div>
    </div>
  </div>

  <div v-click class="card card-orange">
    <div class="slide-h3" style="color:var(--orange);margin-bottom:4px;">4. Commenting Out Dead Code Permanently</div>
    <div class="body-text">Using comments to keep old, unused code "just in case" clutters the file. Use <strong>version control</strong> (Git) instead — it remembers everything.</div>
    <div style="font-family:'Fira Code',monospace;font-size:.68rem;background:#fff;padding:8px;border-radius:6px;margin-top:6px;line-height:1.8;">
      <span style="color:#ef5050;">// int result = a * b; // old formula</span><br>
      <span style="color:#ef5050;">// result = result + 5; // was this needed?</span><br>
      <span style="color:#0e6ead;">int</span> result = (a + b) * <span style="color:#b45309;">2</span>;
    </div>
  </div>

</div>

</div>

  </template>
</Slide2>
