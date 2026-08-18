---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 8 — RECURSION VS ITERATION
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Recursion">
  <template #content>

<div class="slide-h1" style="margin-bottom:10px;"><span class="highlight">Recursion</span> vs <span class="highlight">Iteration</span></div>

<div class="g2" style="gap:14px;">

<div class="flex-col">
  <div v-click class="section-label">Side-by-Side — Factorial in Java</div>

  <div v-after class="g2" style="gap:8px;">
    <div class="flex-col">
      <div class="section-label" style="color:var(--blue);">Iteration (Loop)</div>
      <div class="code-block" style="font-size:.66rem;line-height:1.8;">
        <span style="color:#ef5050;">static int</span> <span style="color:#0e6ead;">factLoop</span>(<span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">n</span>) {<br>
        <span style="padding-left:12px;display:block;"><span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">result</span> = <span style="color:#b45309;">1</span>;</span>
        <span style="padding-left:12px;display:block;"><span style="color:#ef5050;">for</span> (<span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">i</span> = <span style="color:#b45309;">1</span>; <span style="color:#0e6ead;">i</span> &lt;= <span style="color:#0e6ead;">n</span>; <span style="color:#0e6ead;">i</span>++)</span>
        <span style="padding-left:24px;display:block;"><span style="color:#0e6ead;">result</span> *= <span style="color:#0e6ead;">i</span>;</span>
        <span style="padding-left:12px;display:block;"><span style="color:#ef5050;">return</span> <span style="color:#0e6ead;">result</span>;</span>
        }
      </div>
    </div>
    <div class="flex-col">
      <div class="section-label" style="color:var(--red);">Recursion</div>
      <div class="code-block" style="font-size:.66rem;line-height:1.8;">
        <span style="color:#ef5050;">static int</span> <span style="color:#0e6ead;">factRec</span>(<span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">n</span>) {<br>
        <span style="padding-left:12px;display:block;"><span style="color:#ef5050;">if</span> (<span style="color:#0e6ead;">n</span> == <span style="color:#b45309;">1</span>)</span>
        <span style="padding-left:24px;display:block;"><span style="color:#ef5050;">return</span> <span style="color:#b45309;">1</span>;</span>
        <span style="padding-left:12px;display:block;"><span style="color:#ef5050;">return</span> <span style="color:#0e6ead;">n</span> * <span style="color:#0e6ead;">factRec</span>(<span style="color:#0e6ead;">n</span>-<span style="color:#b45309;">1</span>);</span>
        }
      </div>
    </div>
  </div>

  <div v-click class="callout callout-success" style="margin-top:6px;font-size:.7rem;">
    <div>Recursion mirrors the <strong>mathematical definition</strong>: n! = n × (n−1)! — cleaner, but iteration uses less memory.</div>
  </div>

  <div v-click class="section-label" style="margin-top:4px;">Best-Use Cases for Recursion</div>
  <div v-after style="display:flex;flex-wrap:wrap;gap:6px;margin-top:4px;">
    <span class="pill pill-blue">Tree traversal</span>
    <span class="pill pill-green">Sorting (Merge/Quick)</span>
    <span class="pill pill-purple">Fibonacci</span>
    <span class="pill pill-orange">Tower of Hanoi</span>
    <span class="pill pill-red">Binary Search</span>
    <span class="pill pill-navy">Maze solving</span>
  </div>

</div>

<div class="flex-col">
  <div v-click class="section-label">Detailed Comparison Table</div>
  <div>
    <table class="cmp-table">
      <thead v-click><tr><th>Feature</th><th>Recursion</th><th>Iteration</th></tr></thead>
      <tbody>
        <tr v-click><td>Code length</td><td class="yes">Usually shorter</td><td>Longer</td></tr>
        <tr v-click><td>Readability</td><td class="yes">High (math-like)</td><td>Moderate</td></tr>
        <tr v-click><td>Memory usage</td><td class="no">More (call stack)</td><td class="yes">Less</td></tr>
        <tr v-click><td>Speed</td><td class="no">Slower (overhead)</td><td class="yes">Faster</td></tr>
        <tr v-click><td>StackOverflowError</td><td class="no">Risk exists</td><td class="yes">None</td></tr>
        <tr v-click><td>Base case needed</td><td class="no">Yes — mandatory</td><td class="yes">No</td></tr>
        <tr v-click><td>Best for</td><td>Trees, DFS, D&C</td><td>Simple loops</td></tr>
      </tbody>
    </table>
  </div>

  <div v-click class="callout callout-info" style="margin-top:6px;font-size:.7rem;">
    <div><strong>When to choose recursion:</strong> When the problem is naturally tree-shaped, divide-and-conquer, or its mathematical definition is recursive — and memory isn't a bottleneck.</div>
  </div>

</div>

</div>

  </template>
</Slide2>
