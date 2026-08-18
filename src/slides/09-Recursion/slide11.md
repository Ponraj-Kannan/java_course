---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 11 — COMMON BEGINNER MISTAKES
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Recursion">
  <template #content>

<div class="slide-h1" style="margin-bottom:10px;">Common Beginner <span class="highlight">Mistakes</span></div>

<div class="g2" style="gap:12px;align-items:start;">

<div class="flex-col" style="gap:8px;">

  <div v-click class="card card-red">
    <div class="slide-h3" style="color:var(--red-dark);margin-bottom:4px;">1. Forgetting the Base Case</div>
    <div class="code-block" style="font-size:.68rem;margin-top:4px;">
      <span style="color:#6b7280;">// No base case — StackOverflowError!</span><br>
      <span style="color:#ef5050;">static int</span> <span style="color:#0e6ead;">sum</span>(<span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">n</span>) {<br>
      <span style="padding-left:12px;display:block;"><span style="color:#ef5050;">return</span> <span style="color:#0e6ead;">n</span> + <span style="color:#0e6ead;">sum</span>(<span style="color:#0e6ead;">n</span> - <span style="color:#b45309;">1</span>); <span style="color:#6b7280;">// runs forever</span></span>
      }
    </div>
  </div>

  <div v-click class="card card-red">
    <div class="slide-h3" style="color:var(--red-dark);margin-bottom:4px;">2. Base Case Never Reached (Wrong Condition)</div>
    <div class="code-block" style="font-size:.68rem;margin-top:4px;">
      <span style="color:#ef5050;">static int</span> <span style="color:#0e6ead;">sum</span>(<span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">n</span>) {<br>
      <span style="padding-left:12px;display:block;"><span style="color:#ef5050;">if</span> (<span style="color:#0e6ead;">n</span> == -<span style="color:#b45309;">1</span>) <span style="color:#ef5050;">return</span> <span style="color:#b45309;">0</span>; <span style="color:#6b7280;">// skips n=0, overflows!</span></span>
      <span style="padding-left:12px;display:block;"><span style="color:#ef5050;">return</span> <span style="color:#0e6ead;">n</span> + <span style="color:#0e6ead;">sum</span>(<span style="color:#0e6ead;">n</span> - <span style="color:#b45309;">1</span>);</span>
      }
    </div>
  </div>

</div>

<div class="flex-col" style="gap:8px;">

  <div v-click class="card card-orange">
    <div class="slide-h3" style="color:var(--orange);margin-bottom:4px;">3. Off-By-One in the Recursive Call</div>
    <div class="code-block" style="font-size:.68rem;margin-top:4px;">
      <span style="color:#ef5050;">static int</span> <span style="color:#0e6ead;">sum</span>(<span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">n</span>) {<br>
      <span style="padding-left:12px;display:block;"><span style="color:#ef5050;">if</span> (<span style="color:#0e6ead;">n</span> == <span style="color:#b45309;">0</span>) <span style="color:#ef5050;">return</span> <span style="color:#b45309;">0</span>;</span>
      <span style="padding-left:12px;display:block;"><span style="color:#ef5050;">return</span> <span style="color:#0e6ead;">n</span> + <span style="color:#0e6ead;">sum</span>(<span style="color:#0e6ead;">n</span>); <span style="color:#6b7280;">// same n — not shrinking!</span></span>
      }
    </div>
    <div class="callout callout-danger" style="font-size:.68rem;margin-top:4px;">
      <div>The recursive input <strong>must shrink</strong> toward the base case on every call.</div>
    </div>
  </div>

  <div v-click class="card card-orange">
    <div class="slide-h3" style="color:var(--orange);margin-bottom:4px;">4. Using Recursion Where Iteration is Better</div>
    <div style="font-size:.72rem;color:var(--slate);margin-top:4px;line-height:1.6;">Printing 1 to 100 with recursion adds 100 stack frames unnecessarily. For simple counting or accumulation tasks, a <span class="mono">for</span> / <span class="mono">while</span> loop is faster, clearer, and safer.</div>
    <div class="callout callout-warn" style="font-size:.68rem;margin-top:4px;">
      <div><strong>Rule of thumb:</strong> If you wouldn't think of the problem mathematically in terms of itself, use a loop.</div>
    </div>
  </div>

</div>

</div>

  </template>
</Slide2>
