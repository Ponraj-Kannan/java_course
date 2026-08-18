---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 9 — STRING CONCATENATION + PERFORMANCE
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Java Strings">
  <template #content>

<div class="slide-h1" style="margin-bottom:10px;">String <span class="highlight">Concatenation</span> &amp; Performance</div>

<div class="g2" style="gap:14px;align-items:start;">

<div class="flex-col">

  <div v-click class="card-navy" style="border-radius:10px;">
    <div style="font-size:.82rem;line-height:1.6;color:var(--slate);">
      <strong style="color:var(--red);">String concatenation</strong> joins two or more strings together. In Java, use the <span class="mono">+</span> operator or <span class="mono">.concat()</span> method. Any non-String value (like <span class="mono">int</span>) is automatically converted when combined with <span class="mono">+</span>.
    </div>
  </div>

  <div v-click class="section-label" style="margin-top:8px;">Using the + Operator</div>
  <div v-after class="code-block" style="font-size:.72rem;line-height:1.9;">
    <span style="color:#ef5050;">String</span> <span style="color:#0e6ead;">first</span> = <span style="color:#2d7a00;">"Hello"</span>;<br>
    <span style="color:#ef5050;">String</span> <span style="color:#0e6ead;">last</span>  = <span style="color:#2d7a00;">"World"</span>;<br>
    <span style="color:#ef5050;">String</span> <span style="color:#0e6ead;">result</span> = <span style="color:#0e6ead;">first</span> + <span style="color:#2d7a00;">", "</span> + <span style="color:#0e6ead;">last</span> + <span style="color:#2d7a00;">"!"</span>;<br>
    <span style="color:#0e6ead;">System</span>.<span style="color:#0e6ead;">out</span>.<span style="color:#2d7a00;">println</span>(<span style="color:#0e6ead;">result</span>); <span style="color:#6b7280;">// Hello, World!</span><br>
    <br>
    <span style="color:#6b7280;">// Auto-conversion: int to String</span><br>
    <span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">age</span> = <span style="color:#b45309;">25</span>;<br>
    <span style="color:#0e6ead;">System</span>.<span style="color:#0e6ead;">out</span>.<span style="color:#2d7a00;">println</span>(<span style="color:#2d7a00;">"Age: "</span> + <span style="color:#0e6ead;">age</span>); <span style="color:#6b7280;">// "Age: 25"</span>
  </div>

  <div v-click class="callout callout-success" style="margin-top:4px;">
    <div><strong>Auto-conversion:</strong> When you write <span class="mono">"Age: " + 25</span>, Java automatically calls <span class="mono">String.valueOf(25)</span> and produces <span class="mono">"Age: 25"</span>. No manual cast needed.</div>
  </div>

</div>

<div class="flex-col">
  <div v-click class="section-label">The Performance Problem with + in Loops</div>

  <div v-after class="code-block" style="font-size:.70rem;line-height:1.9;">
    <span style="color:#6b7280;">// BAD — creates N intermediate String objects!</span><br>
    <span style="color:#ef5050;">String</span> <span style="color:#0e6ead;">result</span> = <span style="color:#2d7a00;">""</span>;<br>
    <span style="color:#ef5050;">for</span> (<span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">i</span> = <span style="color:#b45309;">1</span>; <span style="color:#0e6ead;">i</span> &lt;= <span style="color:#b45309;">5</span>; <span style="color:#0e6ead;">i</span>++) {<br>
    <span style="padding-left:20px;display:block;background:#fff5f5;border-left:2px solid var(--red);"><span style="color:#0e6ead;">result</span> = <span style="color:#0e6ead;">result</span> + <span style="color:#0e6ead;">i</span> + <span style="color:#2d7a00;">" "</span>; <span style="color:#6b7280;">// new object each iteration!</span></span>
    }
  </div>

  <div v-click style="display:flex;flex-direction:column;gap:4px;margin-top:6px;font-size:.7rem;background:#f7f8fc;border:1px solid var(--border);border-radius:8px;padding:10px 12px;">
    <div style="font-weight:600;color:var(--navy);margin-bottom:4px;">What happens inside the loop (5 iterations):</div>
    <div v-click style="display:flex;gap:6px;align-items:center;"><span class="pill pill-red" style="min-width:50px;text-align:center;">i=1</span> <span class="mono">""</span> + <span class="mono">"1 "</span> → new String <span class="mono">"1 "</span></div>
    <div v-click style="display:flex;gap:6px;align-items:center;"><span class="pill pill-red" style="min-width:50px;text-align:center;">i=2</span> <span class="mono">"1 "</span> + <span class="mono">"2 "</span> → new String <span class="mono">"1 2 "</span></div>
    <div style="color:var(--slate);font-size:.65rem;">... and so on — 5 throwaway String objects created!</div>
  </div>

  <div v-click class="callout callout-danger" style="margin-top:6px;">
    <div><strong>Performance impact:</strong> Each <span class="mono">+</span> in a loop creates a <strong>new immutable String object</strong>. For 1000 iterations this is extremely wasteful. <strong>Use StringBuilder instead!</strong></div>
  </div>

</div>

</div>

  </template>
</Slide2>
