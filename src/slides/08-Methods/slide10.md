---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 10 — VARIABLE SCOPE & LIFETIME
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Java Methods">
  <template #content>

<div class="slide-h1" style="margin-bottom:10px;">Variable <span class="highlight">Scope &amp; Lifetime</span></div>

<div class="g2" style="gap:14px;align-items:start;">

<div class="flex-col">

  <div v-click class="card-navy" style="border-radius:10px;">
    <div style="font-size:.82rem;line-height:1.6;color:var(--slate);">
      <strong style="color:var(--red);">Variable Scope</strong> is the region of code where a variable is accessible; <strong style="color:var(--green);">Lifetime</strong> is the duration from when the variable is created in memory until it is destroyed.
    </div>
  </div>

  <div v-click class="section-label" style="margin-top:6px;">3 Levels of Variable Scope in Java</div>

  <div style="display:flex;flex-direction:column;gap:5px;">
    <div v-click class="card" style="padding:6px 10px;border-left:4px solid var(--blue);">
      <div style="font-weight:700;font-size:.70rem;color:var(--navy);">1. Method / Local Scope</div>
      <div style="font-size:.66rem;color:var(--slate);">Declared inside a method; created on stack when method is called, destroyed when method exits.</div>
    </div>
    <div v-click class="card" style="padding:6px 10px;border-left:4px solid var(--orange);">
      <div style="font-weight:700;font-size:.70rem;color:var(--navy);">2. Block Scope ({ ... })</div>
      <div style="font-size:.66rem;color:var(--slate);">Declared inside loops (<span class="mono">for</span>) or <span class="mono">if</span> blocks; exists only within that specific pair of curly braces.</div>
    </div>
    <div v-click class="card" style="padding:6px 10px;border-left:4px solid var(--green);">
      <div style="font-weight:700;font-size:.70rem;color:var(--navy);">3. Class / Static Scope</div>
      <div style="font-size:.66rem;color:var(--slate);">Declared at class level with <span class="mono">static</span>; exists for the entire lifetime of the program.</div>
    </div>
  </div>

</div>

<div class="flex-col">
  <div v-click class="section-label">Scope Boundary Visualization</div>

  <div v-after class="code-block" style="font-size:.68rem;line-height:1.75;">
    <span style="color:#ef5050;">public class</span> <span style="color:#0e6ead;">ScopeDemo</span> {<br>
    <span style="padding-left:16px;display:block;"><span style="color:#ef5050;">static int</span> <span style="color:#0e6ead;">globalCounter</span> = <span style="color:#b45309;">0</span>; <span style="color:#6b7280;">// Class Scope</span></span>
    <br>
    <span style="padding-left:16px;display:block;"><span style="color:#ef5050;">public static void</span> <span style="color:#0e6ead;">demoMethod</span>() {</span>
    <span style="padding-left:32px;display:block;"><span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">localVar</span> = <span style="color:#b45309;">10</span>; <span style="color:#6b7280;">// Method Scope</span></span>
    <br>
    <span style="padding-left:32px;display:block;"><span style="color:#ef5050;">if</span> (localVar &gt; <span style="color:#b45309;">5</span>) {</span>
    <span style="padding-left:48px;display:block;"><span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">blockVar</span> = <span style="color:#b45309;">99</span>; <span style="color:#6b7280;">// Block Scope</span></span>
    <span style="padding-left:48px;display:block;"><span style="color:#0e6ead;">System</span>.<span style="color:#0e6ead;">out</span>.<span style="color:#2d7a00;">println</span>(blockVar); <span style="color:#6b7280;">// OK</span></span>
    <span style="padding-left:32px;display:block;">}</span>
    <span style="padding-left:32px;display:block;background:#fff5f5;border-left:2px solid var(--red);"><span style="color:#6b7280;">// System.out.println(blockVar); → COMPILE ERROR!</span></span>
    <span style="padding-left:16px;display:block;">}</span>
    }
  </div>

  <div v-click class="callout callout-info" style="margin-top:6px;">
    <div><strong>Variable Isolation:</strong> Two different methods can declare local variables with the exact same name without conflict because they live in separate stack frames.</div>
  </div>

</div>

</div>

  </template>
</Slide2>
