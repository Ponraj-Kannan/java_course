---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 2 — BASE CASE & RECURSIVE CASE
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Recursion">
  <template #content>

<div class="slide-h1" style="margin-bottom:10px;"><span class="highlight">Base Case</span> &amp; <span class="highlight">Recursive Case</span></div>

<div class="g2" style="gap:14px;">

<div class="flex-col">

  <div v-click class="card-green" style="text-align:center;">
    <div class="slide-h2" style="color:var(--green);">Base Case</div>
    <div class="small-text" style="margin-top:4px;">The <strong>termination condition</strong> — returns a value directly with <strong>no further recursive call</strong>. Every recursive method <em>must</em> have one.</div>
  </div>

  <div v-click class="code-block">
    <span style="color:#6b7280;">// Base case highlighted</span><br>
    <span style="color:#ef5050;">static void</span> <span style="color:#0e6ead;">printNto1</span>(<span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">n</span>) {<br>
    <span style="padding-left:20px;display:block;background:#f0fff4;border-left:3px solid var(--green);"><span style="color:#ef5050;">if</span> (<span style="color:#0e6ead;">n</span> == <span style="color:#b45309;">0</span>) <span style="color:#ef5050;">return</span>; <span style="color:#6b7280;">// BASE CASE</span></span>
    <span style="padding-left:20px;display:block;">System.out.<span style="color:#0e6ead;">println</span>(<span style="color:#0e6ead;">n</span>);</span>
    <span style="padding-left:20px;display:block;"><span style="color:#0e6ead;">printNto1</span>(<span style="color:#0e6ead;">n</span> - <span style="color:#b45309;">1</span>);</span>
    }
  </div>

  <div v-click class="callout callout-danger">
    <div><strong>Missing base case = StackOverflowError!</strong> Java throws <span class="mono">java.lang.StackOverflowError</span> when the call stack is exhausted — the Java equivalent of Python's <span class="mono">RecursionError</span>.</div>
  </div>

  <div v-click class="card-green" style="font-size:.75rem;">
    <strong>Good base cases check for:</strong>
    <div style="margin-top:6px;display:flex;flex-direction:column;gap:3px;">
      <div><span class="pill pill-green">n == 0</span> for counting down to zero</div>
      <div><span class="pill pill-green">n == 1</span> for multiplication-based problems</div>
      <div><span class="pill pill-green">n &lt;= 0</span> for safety when negatives are possible</div>
    </div>
  </div>

</div>

<div class="flex-col">

  <div v-click class="card-blue" style="text-align:center;">
    <div class="slide-h2" style="color:var(--blue);">Recursive Case</div>
    <div class="small-text" style="margin-top:4px;">The step that makes the problem <strong>smaller</strong> and calls the method again. It <strong>must move toward the base case</strong> or it loops forever.</div>
  </div>

  <div v-click class="code-block">
    <span style="color:#ef5050;">static void</span> <span style="color:#0e6ead;">printNto1</span>(<span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">n</span>) {<br>
    <span style="padding-left:20px;display:block;"><span style="color:#ef5050;">if</span> (<span style="color:#0e6ead;">n</span> == <span style="color:#b45309;">0</span>) <span style="color:#ef5050;">return</span>;</span>
    <span style="padding-left:20px;display:block;">System.out.<span style="color:#0e6ead;">println</span>(<span style="color:#0e6ead;">n</span>);</span>
    <span style="padding-left:20px;display:block;background:#ebf8ff;border-left:3px solid var(--blue);"><span style="color:#0e6ead;">printNto1</span>(<span style="color:#0e6ead;">n</span> - <span style="color:#b45309;">1</span>); <span style="color:#6b7280;">// RECURSIVE</span></span>
    }
  </div>

  <div v-click class="section-label" style="margin-top:4px;">Base vs Recursive — Comparison</div>
  <div >
    <table class="cmp-table">
      <thead v-click><tr><th>Aspect</th><th>Base Case</th><th>Recursive Case</th></tr></thead>
      <tbody>
        <tr v-click><td>Purpose</td><td>Stop recursion</td><td>Shrink the problem</td></tr>
        <tr v-click><td>Returns</td><td class="yes">Direct value</td><td>Method call result</td></tr>
        <tr v-click><td>Required?</td><td class="yes">Always — no exceptions</td><td class="yes">Always</td></tr>
        <tr v-click><td>Java keyword</td><td class="mono">return value;</td><td class="mono">return method(n-1);</td></tr>
      </tbody>
    </table>
  </div>

</div>

</div>

  </template>
</Slide2>
