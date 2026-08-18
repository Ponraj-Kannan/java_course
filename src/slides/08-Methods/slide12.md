---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 12 — COMMON MISTAKES & PITFALLS
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Java Methods">
  <template #content>

<div class="slide-h1" style="margin-bottom:10px;">Common <span class="highlight">Mistakes</span> to Avoid</div>

<div class="g2" style="gap:12px;align-items:start;">

<div class="flex-col" style="gap:7px;">

  <div v-click class="card-red" style="border-radius:10px;">
    <div style="font-size:.76rem;font-weight:700;color:var(--red-dark);margin-bottom:3px;">Mistake 1 — Missing Return on Conditional Branch</div>
    <div style="background:#fff8f8;border-radius:6px;padding:6px 10px;font-family:'Fira Code',monospace;font-size:.64rem;line-height:1.7;">
      <span style="color:#6b7280;">// ❌ Wrong — what if x &lt;= 0? Compile Error!</span><br>
      <span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">check</span>(<span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">x</span>) { <span style="color:#ef5050;">if</span> (x &gt; <span style="color:#b45309;">0</span>) <span style="color:#ef5050;">return</span> <span style="color:#b45309;">1</span>; }<br>
      <span style="color:#6b7280;">// ✓ Correct — every branch must return</span><br>
      <span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">check</span>(<span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">x</span>) { <span style="color:#ef5050;">if</span> (x &gt; <span style="color:#b45309;">0</span>) <span style="color:#ef5050;">return</span> <span style="color:#b45309;">1</span>; <span style="color:#ef5050;">return</span> <span style="color:#b45309;">0</span>; }
    </div>
  </div>

  <div v-click class="card-red" style="border-radius:10px;">
    <div style="font-size:.76rem;font-weight:700;color:var(--red-dark);margin-bottom:3px;">Mistake 2 — Non-Static Method from Static Context</div>
    <div style="background:#fff8f8;border-radius:6px;padding:6px 10px;font-family:'Fira Code',monospace;font-size:.64rem;line-height:1.7;">
      <span style="color:#6b7280;">// ❌ Calling instance method directly inside main():</span><br>
      <span style="color:#ef5050;">void</span> <span style="color:#0e6ead;">greet</span>() { ... }<br>
      <span style="color:#ef5050;">public static void</span> <span style="color:#0e6ead;">main</span>(...) { <span style="color:#0e6ead;">greet</span>(); <span style="color:#6b7280;">// Error!</span> }<br>
      <span style="color:#6b7280;">// ✓ Fix: make greet() static OR create an object</span>
    </div>
  </div>

  <div v-click class="card-red" style="border-radius:10px;">
    <div style="font-size:.76rem;font-weight:700;color:var(--red-dark);margin-bottom:3px;">Mistake 3 — Overloading by Return Type Only</div>
    <div style="background:#fff8f8;border-radius:6px;padding:6px 10px;font-family:'Fira Code',monospace;font-size:.64rem;line-height:1.7;">
      <span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">calc</span>(<span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">a</span>) { ... }<br>
      <span style="color:#ef5050;">double</span> <span style="color:#0e6ead;">calc</span>(<span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">a</span>) { ... } <span style="color:#6b7280;">// ❌ Duplicate method error!</span>
    </div>
  </div>

</div>

<div class="flex-col" style="gap:7px;">

  <div v-click class="card-red" style="border-radius:10px;">
    <div style="font-size:.76rem;font-weight:700;color:var(--red-dark);margin-bottom:3px;">Mistake 4 — Assuming Primitives Change in Caller</div>
    <div style="background:#fff8f8;border-radius:6px;padding:6px 10px;font-family:'Fira Code',monospace;font-size:.64rem;line-height:1.7;">
      <span style="color:#ef5050;">static void</span> <span style="color:#0e6ead;">swap</span>(<span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">a</span>, <span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">b</span>) { <span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">t</span>=a; a=b; b=t; }<br>
      <span style="color:#6b7280;">// swap(x, y) DOES NOT SWAP x and y in main()!</span><br>
      <span style="color:#6b7280;">// Java is pass-by-value — only local copies were swapped.</span>
    </div>
  </div>

  <div v-click class="card-red" style="border-radius:10px;">
    <div style="font-size:.76rem;font-weight:700;color:var(--red-dark);margin-bottom:3px;">Mistake 5 — Missing Base Case in Recursion</div>
    <div style="background:#fff8f8;border-radius:6px;padding:6px 10px;font-family:'Fira Code',monospace;font-size:.64rem;line-height:1.7;">
      <span style="color:#ef5050;">static void</span> <span style="color:#0e6ead;">countDown</span>(<span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">n</span>) {<br>
      &nbsp;&nbsp;<span style="color:#0e6ead;">countDown</span>(n - <span style="color:#b45309;">1</span>); <span style="color:#6b7280;">// ❌ Infinite recursion!</span><br>
      }<br>
      <span style="color:#6b7280;">// Result: java.lang.StackOverflowError</span>
    </div>
  </div>

  <div v-click class="callout callout-warn" style="margin-top:2px;">
    <div><strong>Exam Tip:</strong> Whenever analyzing code questions involving method parameters, always check if types are primitives (unchanged) or arrays/objects (mutable)!</div>
  </div>

</div>

</div>

  </template>
</Slide2>
