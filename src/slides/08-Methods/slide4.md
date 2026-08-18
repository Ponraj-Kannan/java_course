---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 4 — RETURN TYPES & THE return STATEMENT
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Java Methods">
  <template #content>

<div class="slide-h1" style="margin-bottom:10px;">Return Types &amp; The <span class="highlight">return</span> Statement</div>

<div class="g2" style="gap:14px;align-items:start;">

<div class="flex-col">

  <div v-click class="card-navy" style="border-radius:10px;">
    <div style="font-size:.82rem;line-height:1.6;color:var(--slate);">
      The <strong style="color:var(--red);">return type</strong> declares the data type a method sends back to its caller; the <strong style="color:var(--green);">return</strong> statement immediately terminates method execution and transfers control/data back.
    </div>
  </div>

  <div style="margin-top:6px;">
    <table class="cmp-table" style="font-size:.7rem;">
      <thead v-click><tr><th>Category</th><th>Return Type</th><th>Return Statement Syntax</th></tr></thead>
      <tbody>
        <tr v-click><td>No Return</td><td class="mono" style="color:var(--blue);font-weight:700;">void</td><td><span class="mono">return;</span> (optional, only for early exit)</td></tr>
        <tr v-click><td>Primitive</td><td class="mono" style="color:var(--green);font-weight:700;">int, double, boolean</td><td><span class="mono">return val;</span> (mandatory)</td></tr>
        <tr v-click><td>Object / Reference</td><td class="mono" style="color:var(--purple);font-weight:700;">String, int[], Object</td><td><span class="mono">return ref;</span> (mandatory)</td></tr>
      </tbody>
    </table>
  </div>

  <div v-click class="callout callout-danger" style="margin-top:6px;">
    <div><strong>All Paths Must Return:</strong> If your method has <span class="mono">if-else</span> branches, Java compiler checks that <strong>every possible branch</strong> ends in a <span class="mono">return</span> statement of the matching type!</div>
  </div>

</div>

<div class="flex-col">
  <div v-click class="section-label">Code Examples — Returning Values vs Void</div>

  <div v-after class="code-block" style="font-size:.68rem;line-height:1.75;">
    <span style="color:#6b7280;">// 1. Value-returning method (must return int on all paths)</span><br>
    <span style="color:#ef5050;">public static int</span> <span style="color:#0e6ead;">findMax</span>(<span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">a</span>, <span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">b</span>) {<br>
    <span style="padding-left:16px;display:block;"><span style="color:#ef5050;">if</span> (a &gt; b) {</span>
    <span style="padding-left:32px;display:block;"><span style="color:#ef5050;">return</span> a; <span style="color:#6b7280;">// path 1</span></span>
    <span style="padding-left:16px;display:block;">} <span style="color:#ef5050;">else</span> {</span>
    <span style="padding-left:32px;display:block;"><span style="color:#ef5050;">return</span> b; <span style="color:#6b7280;">// path 2</span></span>
    <span style="padding-left:16px;display:block;">}</span>
    }<br>
    <br>
    <span style="color:#6b7280;">// 2. Void method with early exit</span><br>
    <span style="color:#ef5050;">public static void</span> <span style="color:#0e6ead;">printGrade</span>(<span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">score</span>) {<br>
    <span style="padding-left:16px;display:block;"><span style="color:#ef5050;">if</span> (score &lt; <span style="color:#b45309;">0</span> || score &gt; <span style="color:#b45309;">100</span>) {</span>
    <span style="padding-left:32px;display:block;background:#fff5f5;border-left:2px solid var(--red);"><span style="color:#0e6ead;">System</span>.<span style="color:#0e6ead;">out</span>.<span style="color:#2d7a00;">println</span>(<span style="color:#2d7a00;">"Invalid score!"</span>);<br><span style="color:#ef5050;">return</span>; <span style="color:#6b7280;">// exits method immediately</span></span>
    <span style="padding-left:16px;display:block;">}</span>
    <span style="padding-left:16px;display:block;"><span style="color:#0e6ead;">System</span>.<span style="color:#0e6ead;">out</span>.<span style="color:#2d7a00;">println</span>(<span style="color:#2d7a00;">"Valid score: "</span> + score);</span>
    }
  </div>

  <div v-click class="callout callout-info" style="margin-top:6px;">
    <div><strong>Unreachable Code:</strong> Any code placed immediately after an unconditional <span class="mono">return</span> statement produces a <em>"Unreachable statement"</em> compilation error.</div>
  </div>

</div>

</div>

  </template>
</Slide2>
