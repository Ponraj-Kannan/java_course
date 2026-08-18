---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 12 — DEBUGGING RECURSIVE METHODS IN JAVA
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Recursion">
  <template #content>

<div class="slide-h1" style="margin-bottom:10px;"><span class="highlight">Debugging</span> Recursive Methods</div>

<div class="g2" style="gap:14px;">

<div class="flex-col">
  <div v-click class="section-label">Technique — Add System.out.println() Traces</div>

  <div v-after class="code-block">
    <span style="color:#ef5050;">static int</span> <span style="color:#0e6ead;">factorial</span>(<span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">n</span>) {<br>
    <span style="padding-left:20px;display:block;color:#6b7280;">// Debug: trace entry</span>
    <span style="padding-left:20px;display:block;"><span style="color:#0e6ead;">System</span>.<span style="color:#0e6ead;">out</span>.<span style="color:#2d7a00;">println</span>(<span style="color:#2d7a00;">"Called: factorial("</span> + <span style="color:#0e6ead;">n</span> + <span style="color:#2d7a00;">")"</span>);</span>
    <span style="padding-left:20px;display:block;"><span style="color:#ef5050;">if</span> (<span style="color:#0e6ead;">n</span> == <span style="color:#b45309;">1</span>) <span style="color:#ef5050;">return</span> <span style="color:#b45309;">1</span>;</span>
    <span style="padding-left:20px;display:block;"><span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">result</span> = <span style="color:#0e6ead;">n</span> * <span style="color:#0e6ead;">factorial</span>(<span style="color:#0e6ead;">n</span> - <span style="color:#b45309;">1</span>);</span>
    <span style="padding-left:20px;display:block;"><span style="color:#0e6ead;">System</span>.<span style="color:#0e6ead;">out</span>.<span style="color:#2d7a00;">println</span>(<span style="color:#2d7a00;">"Returning: "</span> + <span style="color:#0e6ead;">result</span> + <span style="color:#2d7a00;">" for n="</span> + <span style="color:#0e6ead;">n</span>);</span>
    <span style="padding-left:20px;display:block;"><span style="color:#ef5050;">return</span> <span style="color:#0e6ead;">result</span>;</span>
    }
  </div>

  <div v-click class="output-box" style="font-size:.68rem;line-height:1.8;">
    <span class="prompt">// factorial(3) output:</span><br>
    Called: factorial(3)<br>
    Called: factorial(2)<br>
    Called: factorial(1)<br>
    Returning: 1 for n=1<br>
    Returning: 2 for n=2<br>
    Returning: 6 for n=3
  </div>

  <div v-click class="callout callout-success" style="font-size:.7rem;">
    <div><strong>Debug Tips:</strong> <span class="pill pill-green">print at entry</span> <span class="pill pill-blue">print at return</span> <span class="pill pill-orange">use indentation per depth</span></div>
  </div>

</div>

<div class="flex-col">
  <div v-click class="section-label">3-Step Recursive Problem-Solving Strategy</div>

  <div v-after style="display:flex;flex-direction:column;gap:6px;">
    <div class="card" style="display:flex;gap:10px;align-items:center;border:1px solid var(--red);">
      <div class="icon-circle ic-red" style="font-size:.9rem;">1</div>
      <div>
        <div class="slide-h3">Identify the Base Case</div>
        <div class="small-text">When is the answer trivially known? (n==0, n==1, empty input)</div>
      </div>
    </div>
    <div v-click class="card" style="display:flex;gap:10px;align-items:center;border:1px solid var(--blue);">
      <div class="icon-circle ic-blue" style="font-size:.9rem;">2</div>
      <div>
        <div class="slide-h3">Define the Recursive Case</div>
        <div class="small-text">How does the current problem relate to a smaller version of itself?</div>
      </div>
    </div>
    <div v-click class="card" style="display:flex;gap:10px;align-items:center;border:1px solid var(--green);">
      <div class="icon-circle ic-green" style="font-size:.9rem;">3</div>
      <div>
        <div class="slide-h3">Trust the Recursion</div>
        <div class="small-text">Assume the recursive call works correctly. Build your solution around it.</div>
      </div>
    </div>
  </div>

  <div v-click class="callout callout-info" style="margin-top:4px;font-size:.7rem;">
    <div><strong>Tip:</strong> Write the base case first, then the recursive case. Never start from the recursive case — you'll spiral without knowing when to stop.</div>
  </div>

</div>

</div>

  </template>
</Slide2>
