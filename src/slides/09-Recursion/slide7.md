---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 7 — DIRECT vs INDIRECT RECURSION
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Recursion">
  <template #content>

<div class="slide-h1" style="margin-bottom:10px;"><span class="highlight">Direct</span> vs <span class="highlight">Indirect</span> Recursion</div>

<div class="g2" style="gap:14px;align-items:start;">

<div class="flex-col">

  <div v-click class="card-blue" style="text-align:center;">
    <div class="slide-h2" style="color:var(--blue);">Direct Recursion</div>
    <div class="small-text" style="margin-top:4px;">A method calls <strong>itself</strong> directly from within its own body.</div>
  </div>

  <div v-click class="code-block">
    <span style="color:#6b7280;">// Method A calls itself directly</span><br>
    <span style="color:#ef5050;">static void</span> <span style="color:#0e6ead;">countdown</span>(<span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">n</span>) {<br>
    <span style="padding-left:20px;display:block;"><span style="color:#ef5050;">if</span> (<span style="color:#0e6ead;">n</span> == <span style="color:#b45309;">0</span>) {</span>
    <span style="padding-left:40px;display:block;"><span style="color:#0e6ead;">System</span>.<span style="color:#0e6ead;">out</span>.<span style="color:#2d7a00;">println</span>(<span style="color:#2d7a00;">"Done!"</span>);</span>
    <span style="padding-left:40px;display:block;"><span style="color:#ef5050;">return</span>;</span>
    <span style="padding-left:20px;display:block;">}</span>
    <span style="padding-left:20px;display:block;"><span style="color:#0e6ead;">System</span>.<span style="color:#0e6ead;">out</span>.<span style="color:#2d7a00;">println</span>(<span style="color:#0e6ead;">n</span>);</span>
    <span style="padding-left:20px;display:block;background:#ebf8ff;border-left:3px solid var(--blue);"><span style="color:#0e6ead;">countdown</span>(<span style="color:#0e6ead;">n</span> - <span style="color:#b45309;">1</span>); <span style="color:#6b7280;">// calls itself</span></span>
    }
  </div>

  <div v-click class="output-box" style="font-size:.72rem;">3 &nbsp; 2 &nbsp; 1 &nbsp; Done!</div>

  <div v-click class="callout callout-info" style="font-size:.7rem;">
    <div><strong>Most common form.</strong> All the examples covered so far (factorial, sum, Fibonacci) use direct recursion.</div>
  </div>

</div>

<div class="flex-col">

  <div v-click class="card-purple" style="text-align:center;">
    <div class="slide-h2" style="color:var(--purple);">Indirect Recursion</div>
    <div class="small-text" style="margin-top:4px;">Method A calls method B, which then calls method A — forming a <strong>cycle between two or more methods</strong>.</div>
  </div>

  <div v-click class="code-block">
    <span style="color:#6b7280;">// Method A and B call each other</span><br>
    <span style="color:#ef5050;">static void</span> <span style="color:#0e6ead;">methodA</span>(<span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">n</span>) {<br>
    <span style="padding-left:20px;display:block;"><span style="color:#ef5050;">if</span> (<span style="color:#0e6ead;">n</span> &lt;= <span style="color:#b45309;">0</span>) <span style="color:#ef5050;">return</span>;</span>
    <span style="padding-left:20px;display:block;"><span style="color:#0e6ead;">System</span>.<span style="color:#0e6ead;">out</span>.<span style="color:#2d7a00;">print</span>(<span style="color:#2d7a00;">"A"</span>);</span>
    <span style="padding-left:20px;display:block;background:#faf5ff;border-left:3px solid var(--purple);"><span style="color:#0e6ead;">methodB</span>(<span style="color:#0e6ead;">n</span> - <span style="color:#b45309;">1</span>); <span style="color:#6b7280;">// A calls B</span></span>
    }<br>
    <span style="color:#ef5050;">static void</span> <span style="color:#0e6ead;">methodB</span>(<span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">n</span>) {<br>
    <span style="padding-left:20px;display:block;"><span style="color:#ef5050;">if</span> (<span style="color:#0e6ead;">n</span> &lt;= <span style="color:#b45309;">0</span>) <span style="color:#ef5050;">return</span>;</span>
    <span style="padding-left:20px;display:block;"><span style="color:#0e6ead;">System</span>.<span style="color:#0e6ead;">out</span>.<span style="color:#2d7a00;">print</span>(<span style="color:#2d7a00;">"B"</span>);</span>
    <span style="padding-left:20px;display:block;background:#faf5ff;border-left:3px solid var(--purple);"><span style="color:#0e6ead;">methodA</span>(<span style="color:#0e6ead;">n</span> - <span style="color:#b45309;">1</span>); <span style="color:#6b7280;">// B calls A</span></span>
    }
  </div>

  <div v-click class="output-box" style="font-size:.72rem;">methodA(4) → A B A B</div>

  <div v-click class="callout callout-warn" style="font-size:.7rem;">
    <div><strong>Less common</strong> — used in mutual-state machines and parser grammar. Harder to trace; ensure both methods have proper base cases to avoid infinite mutual calling.</div>
  </div>

</div>

</div>

  </template>
</Slide2>
