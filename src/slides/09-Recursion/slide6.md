---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 6 — FIBONACCI (BRANCHING RECURSION + TREE)
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Recursion">
  <template #content>

<div class="slide-h1" style="margin-bottom:10px;"><span class="highlight">Fibonacci</span> — Branching Recursion</div>

<div class="g2" style="gap:14px;">

<div class="flex-col">
  <div v-click class="card-navy" style="border-radius:10px;">
    <div style="font-size:.82rem;line-height:1.6;color:var(--slate);">
      <strong style="color:var(--red);">Definition:</strong> The Fibonacci sequence is: <strong>0, 1, 1, 2, 3, 5, 8…</strong> where each number is the sum of the previous two. It demonstrates <strong>branching recursion</strong> — each call spawns two more.
    </div>
  </div>

  <div v-click class="code-block">
    <span style="color:#6b7280;">// fib(n) = fib(n-1) + fib(n-2)</span><br>
    <span style="color:#ef5050;">static int</span> <span style="color:#0e6ead;">fib</span>(<span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">n</span>) {<br>
    <span style="padding-left:20px;display:block;background:#f0fff4;border-left:3px solid var(--green);"><span style="color:#ef5050;">if</span> (<span style="color:#0e6ead;">n</span> &lt;= <span style="color:#b45309;">1</span>) <span style="color:#ef5050;">return</span> <span style="color:#0e6ead;">n</span>; <span style="color:#6b7280;">// fib(0)=0, fib(1)=1</span></span>
    <span style="padding-left:20px;display:block;"><span style="color:#ef5050;">return</span> <span style="color:#0e6ead;">fib</span>(<span style="color:#0e6ead;">n</span> - <span style="color:#b45309;">1</span>) + <span style="color:#0e6ead;">fib</span>(<span style="color:#0e6ead;">n</span> - <span style="color:#b45309;">2</span>);</span>
    }<br>
    <br>
    <span style="color:#6b7280;">// Print first 7 Fibonacci numbers</span><br>
    <span style="color:#ef5050;">for</span> (<span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">i</span> = <span style="color:#b45309;">0</span>; <span style="color:#0e6ead;">i</span> &lt; <span style="color:#b45309;">7</span>; <span style="color:#0e6ead;">i</span>++)<br>
    &nbsp;&nbsp;<span style="color:#0e6ead;">System</span>.<span style="color:#0e6ead;">out</span>.<span style="color:#2d7a00;">print</span>(<span style="color:#0e6ead;">fib</span>(<span style="color:#0e6ead;">i</span>) + <span style="color:#2d7a00;">" "</span>);
  </div>

  <div v-click class="output-box" style="font-size:.72rem;">0  1  1  2  3  5  8</div>

  <div v-click class="callout callout-danger" style="font-size:.7rem;margin-top:4px;">
    <div><strong>Inefficiency warning:</strong> Naive recursive Fibonacci recomputes the same values many times. <span class="mono">fib(30)</span> makes over a million calls! For large n, use dynamic programming or memoization.</div>
  </div>

</div>

<div class="flex-col">
  <div v-click class="section-label">Fibonacci Recursion Tree — fib(4)</div>

  <div v-after style="background:#f7f8fc;border:1px solid var(--border);border-radius:8px;padding:6px 4px 4px;position:relative;height:178px;font-family:'Fira Code',monospace;font-size:.6rem;overflow:hidden;">
    <div style="position:absolute;left:57.5%;top:10px;width:1px;height:10px;background:#94a3b8;"></div>
    <div style="position:absolute;left:35%;right:20%;top:20px;height:1px;background:#94a3b8;"></div>
    <div style="position:absolute;left:35%;top:20px;width:1px;height:20px;background:#94a3b8;"></div>
    <div style="position:absolute;left:80%;top:20px;width:1px;height:20px;background:#94a3b8;"></div>
    <div style="position:absolute;left:35%;top:50px;width:1px;height:8px;background:#94a3b8;"></div>
    <div style="position:absolute;left:20%;right:50%;top:58px;height:1px;background:#94a3b8;"></div>
    <div style="position:absolute;left:20%;top:58px;width:1px;height:20px;background:#94a3b8;"></div>
    <div style="position:absolute;left:50%;top:58px;width:1px;height:20px;background:#94a3b8;"></div>
    <div style="position:absolute;left:80%;top:50px;width:1px;height:8px;background:#94a3b8;"></div>
    <div style="position:absolute;left:70%;right:10%;top:58px;height:1px;background:#94a3b8;"></div>
    <div style="position:absolute;left:70%;top:58px;width:1px;height:20px;background:#94a3b8;"></div>
    <div style="position:absolute;left:90%;top:58px;width:1px;height:20px;background:#94a3b8;"></div>
    <div style="position:absolute;left:20%;top:88px;width:1px;height:8px;background:#94a3b8;"></div>
    <div style="position:absolute;left:10%;right:70%;top:96px;height:1px;background:#94a3b8;"></div>
    <div style="position:absolute;left:10%;top:96px;width:1px;height:20px;background:#94a3b8;"></div>
    <div style="position:absolute;left:30%;top:96px;width:1px;height:20px;background:#94a3b8;"></div>
    <div style="position:absolute;left:57.5%;top:0;transform:translateX(-50%);color:#2b6cb0;font-weight:700;">fib(4)</div>
    <div style="position:absolute;left:35%;top:40px;transform:translateX(-50%);color:#2b6cb0;">fib(3)</div>
    <div style="position:absolute;left:80%;top:40px;transform:translateX(-50%);color:#2b6cb0;">fib(2)</div>
    <div style="position:absolute;left:20%;top:78px;transform:translateX(-50%);color:#dd6b20;">fib(2)</div>
    <div style="position:absolute;left:50%;top:78px;transform:translateX(-50%);color:#dd6b20;">fib(1)</div>
    <div style="position:absolute;left:70%;top:78px;transform:translateX(-50%);color:#dd6b20;">fib(1)</div>
    <div style="position:absolute;left:90%;top:78px;transform:translateX(-50%);color:#dd6b20;">fib(0)</div>
    <div style="position:absolute;left:10%;top:116px;transform:translateX(-50%);color:#276749;font-weight:700;">fib(1)</div>
    <div style="position:absolute;left:30%;top:116px;transform:translateX(-50%);color:#276749;font-weight:700;">fib(0)</div>
    <div style="position:absolute;left:50%;top:116px;transform:translateX(-50%);color:#276749;font-weight:700;">= 1</div>
    <div style="position:absolute;left:70%;top:116px;transform:translateX(-50%);color:#276749;font-weight:700;">= 1</div>
    <div style="position:absolute;left:90%;top:116px;transform:translateX(-50%);color:#276749;font-weight:700;">= 0</div>
    <div style="position:absolute;left:10%;top:132px;transform:translateX(-50%);color:#276749;font-weight:700;">= 1</div>
    <div style="position:absolute;left:30%;top:132px;transform:translateX(-50%);color:#276749;font-weight:700;">= 0</div>
    <div style="position:absolute;bottom:3px;left:0;right:0;text-align:center;color:#276749;font-weight:700;font-size:.65rem;border-top:1px solid #e2e8f0;padding-top:3px;">Result: fib(4) = 3</div>
  </div>

  <div v-click class="callout callout-warn" style="margin-top:6px;font-size:.7rem;">
    <div><strong>Notice:</strong> <span class="mono">fib(2)</span> is computed <em>twice</em>. For larger values, exponential duplicate work occurs. This is why naive recursive Fibonacci has O(2ⁿ) time complexity.</div>
  </div>

  <div v-click class="section-label" style="margin-top:4px;">3-Step Strategy for Fibonacci</div>
  <div v-after class="card-navy" style="border-radius:10px;font-size:.75rem;line-height:1.7;">
    <strong>Step 1 — Base:</strong> fib(0) = 0, fib(1) = 1<br>
    <strong>Step 2 — Recursive:</strong> fib(n) = fib(n-1) + fib(n-2)<br>
    <strong>Step 3 — Trust:</strong> Call fib(n-1) and fib(n-2), add them together.
  </div>

</div>

</div>

  </template>
</Slide2>
