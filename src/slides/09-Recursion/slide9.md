---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 9 — STACKOVERFLOW ERROR (JAVA-SPECIFIC)
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Recursion">
  <template #content>

<div class="slide-h1" style="margin-bottom:10px;"><span class="highlight">StackOverflowError</span> in Java</div>

<div class="g2" style="gap:14px;">

<div class="flex-col">

  <div v-click class="card-navy" style="border-radius:10px;">
    <div style="font-size:.82rem;line-height:1.6;color:var(--slate);">
      <strong style="color:var(--red);">Definition:</strong> A <strong>StackOverflowError</strong> is a Java runtime error thrown by the JVM when the call stack memory is exhausted — typically caused by a recursive method that never reaches its base case.
    </div>
  </div>

  <div v-click class="section-label" style="margin-top:4px;">What Causes It?</div>

  <div style="display:flex;flex-direction:column;gap:5px;">
    <div v-click class="card card-red">
      <div class="slide-h3" style="color:var(--red-dark);margin-bottom:4px;">1. Missing Base Case</div>
      <div class="code-block" style="font-size:.68rem;margin-top:4px;">
        <span style="color:#6b7280;">// No base case — runs forever!</span><br>
        <span style="color:#ef5050;">static int</span> <span style="color:#0e6ead;">badCount</span>(<span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">n</span>) {<br>
        <span style="padding-left:12px;display:block;"><span style="color:#ef5050;">return</span> <span style="color:#0e6ead;">n</span> + <span style="color:#0e6ead;">badCount</span>(<span style="color:#0e6ead;">n</span> - <span style="color:#b45309;">1</span>); <span style="color:#ef5050;">// never stops</span></span>
        }
      </div>
    </div>
    <div v-click class="card card-orange">
      <div class="slide-h3" style="color:var(--orange);margin-bottom:4px;">2. Base Case Never Reached</div>
      <div class="code-block" style="font-size:.68rem;margin-top:4px;">
        <span style="color:#ef5050;">static int</span> <span style="color:#0e6ead;">bad</span>(<span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">n</span>) {<br>
        <span style="padding-left:12px;display:block;"><span style="color:#ef5050;">if</span> (<span style="color:#0e6ead;">n</span> == -<span style="color:#b45309;">1</span>) <span style="color:#ef5050;">return</span> <span style="color:#b45309;">0</span>; <span style="color:#6b7280;">// skips n=0!</span></span>
        <span style="padding-left:12px;display:block;"><span style="color:#ef5050;">return</span> <span style="color:#0e6ead;">n</span> + <span style="color:#0e6ead;">bad</span>(<span style="color:#0e6ead;">n</span> - <span style="color:#b45309;">1</span>);</span>
        }
      </div>
    </div>
  </div>

</div>

<div class="flex-col">

  <div v-click class="section-label">What the Error Looks Like</div>

  <div v-after class="output-box" style="font-size:.68rem;border-color:#f5c6cb;color:#721c24;background:#fff5f5;line-height:1.8;">
    Exception in thread "main" <br>
    <strong>java.lang.StackOverflowError</strong><br>
    &nbsp;&nbsp;at Main.badCount(Main.java:3)<br>
    &nbsp;&nbsp;at Main.badCount(Main.java:3)<br>
    &nbsp;&nbsp;at Main.badCount(Main.java:3)<br>
    &nbsp;&nbsp;... (repeated hundreds of times)
  </div>

  <div v-click class="section-label" style="margin-top:8px;">How to Recognize &amp; Fix It</div>

  <div style="display:flex;flex-direction:column;gap:6px;">
    <div v-click class="card card-green">
      <div class="slide-h3" style="color:var(--green);margin-bottom:4px;">Fix 1 — Add or correct the base case</div>
      <div class="code-block" style="font-size:.68rem;margin-top:4px;">
        <span style="color:#ef5050;">static int</span> <span style="color:#0e6ead;">fixed</span>(<span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">n</span>) {<br>
        <span style="padding-left:12px;display:block;background:#f0fff4;border-left:2px solid var(--green);"><span style="color:#ef5050;">if</span> (<span style="color:#0e6ead;">n</span> == <span style="color:#b45309;">0</span>) <span style="color:#ef5050;">return</span> <span style="color:#b45309;">0</span>; <span style="color:#6b7280;">// correct base</span></span>
        <span style="padding-left:12px;display:block;"><span style="color:#ef5050;">return</span> <span style="color:#0e6ead;">n</span> + <span style="color:#0e6ead;">fixed</span>(<span style="color:#0e6ead;">n</span> - <span style="color:#b45309;">1</span>);</span>
        }
      </div>
    </div>
    <div v-click class="callout callout-info" style="font-size:.7rem;">
      <div><strong>Fix 2:</strong> If the problem truly requires large depth, convert the recursion to an iterative solution using an explicit <span class="mono">Stack&lt;&gt;</span> data structure — no risk of JVM stack overflow.</div>
    </div>
  </div>

</div>

</div>

  </template>
</Slide2>
