<!-- ═══════════════════════════════════════════════════════
     SLIDE 1 — INTRODUCTION TO METHODS IN JAVA
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Java Methods">
  <template #content>

<div class="slide-h1" style="margin-bottom:10px;">Introduction to <span class="highlight">Methods</span></div>

<div class="g2" style="gap:14px;align-items:start;">

<div class="flex-col">

  <div v-click class="card-navy" style="border-radius:10px;">
    <div style="font-size:.82rem;line-height:1.6;color:var(--slate);">
      A <strong style="color:var(--red);">method</strong> in Java is a <strong>named, reusable block of code</strong> that performs a specific task and only executes when it is explicitly called (invoked).
    </div>
  </div>

  <div v-click class="callout callout-warn">
    <div><strong>Java vs Other Languages:</strong> In Java, all methods must be declared <strong>inside a class</strong>. Standalone functions outside classes do not exist in Java.</div>
  </div>

  <div v-click class="section-label" style="margin-top:6px;">Simple Method Example</div>

  <div v-after class="code-block" style="font-size:.70rem;line-height:1.8;">
    <span style="color:#ef5050;">public class</span> <span style="color:#0e6ead;">GreetingDemo</span> {<br>
    <span style="padding-left:16px;display:block;"><span style="color:#6b7280;">// 1. Method definition</span></span>
    <span style="padding-left:16px;display:block;background:#f0fff4;border-left:2px solid var(--green);"><span style="color:#ef5050;">public static void</span> <span style="color:#0e6ead;">sayHello</span>() {<br>&nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#0e6ead;">System</span>.<span style="color:#0e6ead;">out</span>.<span style="color:#2d7a00;">println</span>(<span style="color:#2d7a00;">"Hello, welcome to Java!"</span>);<br>}</span>
    <br>
    <span style="padding-left:16px;display:block;"><span style="color:#ef5050;">public static void</span> <span style="color:#0e6ead;">main</span>(<span style="color:#ef5050;">String</span>[] <span style="color:#0e6ead;">args</span>) {</span>
    <span style="padding-left:32px;display:block;"><span style="color:#6b7280;">// 2. Method call (can be called multiple times)</span></span>
    <span style="padding-left:32px;display:block;"><span style="color:#0e6ead;">sayHello</span>(); <span style="color:#6b7280;">// executes sayHello()</span></span>
    <span style="padding-left:32px;display:block;"><span style="color:#0e6ead;">sayHello</span>(); <span style="color:#6b7280;">// reuses the same logic</span></span>
    <span style="padding-left:16px;display:block;">}</span>
    }
  </div>

</div>

<div class="flex-col">
  <div class="section-label" v-click>Why Do We Use Methods?</div>

  <div style="display:flex;flex-direction:column;gap:8px;">
    <div v-click class="card" style="display:flex;gap:10px;align-items:flex-start;border:1px solid var(--blue);">
      <span class="pill pill-blue" style="flex-shrink:0;min-width:95px;text-align:center;">Reusability</span>
      <div>
        <div style="font-size:.75rem;font-weight:700;color:var(--navy);">DRY Principle (Don't Repeat Yourself)</div>
        <div style="font-size:.68rem;color:var(--slate);">Write the logic once in a method, and call it hundreds of times across your program.</div>
      </div>
    </div>
    <div v-click class="card" style="display:flex;gap:10px;align-items:flex-start;border:1px solid var(--green);">
      <span class="pill pill-green" style="flex-shrink:0;min-width:95px;text-align:center;">Modularity</span>
      <div>
        <div style="font-size:.75rem;font-weight:700;color:var(--navy);">Divide &amp; Conquer</div>
        <div style="font-size:.68rem;color:var(--slate);">Break complex, monolithic programs into smaller, manageable, and testable sub-units.</div>
      </div>
    </div>
    <div v-click class="card" style="display:flex;gap:10px;align-items:flex-start;border:1px solid var(--orange);">
      <span class="pill pill-orange" style="flex-shrink:0;min-width:95px;text-align:center;">Readability</span>
      <div>
        <div style="font-size:.75rem;font-weight:700;color:var(--navy);">Clean Code &amp; Abstraction</div>
        <div style="font-size:.68rem;color:var(--slate);">Meaningful method names describe <em>what</em> is being done without cluttering high-level flow.</div>
      </div>
    </div>
    <div v-click class="card" style="display:flex;gap:10px;align-items:flex-start;border:1px solid var(--purple);">
      <span class="pill pill-purple" style="flex-shrink:0;min-width:95px;text-align:center;">Maintenance</span>
      <div>
        <div style="font-size:.75rem;font-weight:700;color:var(--navy);">Single Point of Modification</div>
        <div style="font-size:.68rem;color:var(--slate);">Bug fixes or algorithmic updates only need to be applied in one place.</div>
      </div>
    </div>
  </div>

  <div v-click class="callout callout-info" style="margin-top:6px;">
    <div>Methods provide <strong>abstraction</strong>: callers only need to know what inputs to give and what output to expect, not internal details.</div>
  </div>

</div>

</div>

  </template>
</Slide2>
