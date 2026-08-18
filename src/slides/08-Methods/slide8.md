---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 8 — METHOD OVERLOADING
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Java Methods">
  <template #content>

<div class="slide-h1" style="margin-bottom:10px;">Method <span class="highlight">Overloading</span></div>

<div class="g2" style="gap:14px;align-items:start;">

<div class="flex-col">

  <div v-click class="card-navy" style="border-radius:10px;">
    <div style="font-size:.82rem;line-height:1.6;color:var(--slate);">
      <strong style="color:var(--red);">Method Overloading</strong> is a feature that allows multiple methods in the same class to share the <strong>same name</strong> as long as their <strong>parameter lists are different</strong> (compile-time polymorphism).
    </div>
  </div>

  <div v-click class="section-label" style="margin-top:6px;">3 Ways to Differentiate Parameter Lists</div>

  <div style="display:flex;flex-direction:column;gap:5px;">
    <div v-click class="card" style="padding:6px 10px;border-left:4px solid var(--blue);">
      <div style="font-weight:700;font-size:.70rem;color:var(--navy);">1. Different Number of Parameters</div>
      <div class="mono" style="font-size:.64rem;color:var(--blue);">add(int a, int b) vs add(int a, int b, int c)</div>
    </div>
    <div v-click class="card" style="padding:6px 10px;border-left:4px solid var(--green);">
      <div style="font-weight:700;font-size:.70rem;color:var(--navy);">2. Different Data Types</div>
      <div class="mono" style="font-size:.64rem;color:var(--green);">print(int n) vs print(double d) vs print(String s)</div>
    </div>
    <div v-click class="card" style="padding:6px 10px;border-left:4px solid var(--orange);">
      <div style="font-weight:700;font-size:.70rem;color:var(--navy);">3. Different Sequence of Parameter Types</div>
      <div class="mono" style="font-size:.64rem;color:var(--orange);">display(String name, int id) vs display(int id, String name)</div>
    </div>
  </div>

  <div v-click class="callout callout-danger" style="margin-top:6px;">
    <div><strong>The Golden Rule:</strong> Changing the <strong>return type alone</strong> does NOT overload a method. <span class="mono">int add(int a, int b)</span> and <span class="mono">double add(int a, int b)</span> causes a compile error!</div>
  </div>

</div>

<div class="flex-col">
  <div v-click class="section-label">Code Example — Overloaded add()</div>

  <div v-after class="code-block" style="font-size:.68rem;line-height:1.75;">
    <span style="color:#ef5050;">public class</span> <span style="color:#0e6ead;">MathHelper</span> {<br>
    <span style="padding-left:16px;display:block;"><span style="color:#6b7280;">// 1. Two ints</span><br><span style="color:#ef5050;">public static int</span> <span style="color:#0e6ead;">add</span>(<span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">a</span>, <span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">b</span>) { <span style="color:#ef5050;">return</span> a + b; }</span>
    <br>
    <span style="padding-left:16px;display:block;"><span style="color:#6b7280;">// 2. Three ints</span><br><span style="color:#ef5050;">public static int</span> <span style="color:#0e6ead;">add</span>(<span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">a</span>, <span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">b</span>, <span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">c</span>) { <span style="color:#ef5050;">return</span> a + b + c; }</span>
    <br>
    <span style="padding-left:16px;display:block;"><span style="color:#6b7280;">// 3. Two doubles</span><br><span style="color:#ef5050;">public static double</span> <span style="color:#0e6ead;">add</span>(<span style="color:#ef5050;">double</span> <span style="color:#0e6ead;">a</span>, <span style="color:#ef5050;">double</span> <span style="color:#0e6ead;">b</span>) { <span style="color:#ef5050;">return</span> a + b; }</span>
    }<br>
    <br>
    <span style="color:#6b7280;">// Java determines the correct method at compile time:</span><br>
    <span style="color:#0e6ead;">MathHelper</span>.<span style="color:#2d7a00;">add</span>(<span style="color:#b45309;">10</span>, <span style="color:#b45309;">20</span>);&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#6b7280;">// calls (int, int) → 30</span><br>
    <span style="color:#0e6ead;">MathHelper</span>.<span style="color:#2d7a00;">add</span>(<span style="color:#b45309;">1</span>, <span style="color:#b45309;">2</span>, <span style="color:#b45309;">3</span>);&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#6b7280;">// calls (int, int, int) → 6</span><br>
    <span style="color:#0e6ead;">MathHelper</span>.<span style="color:#2d7a00;">add</span>(<span style="color:#b45309;">2.5</span>, <span style="color:#b45309;">4.5</span>);&nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#6b7280;">// calls (double, double) → 7.0</span>
  </div>

  <div v-click class="callout callout-info" style="margin-top:6px;">
    <div><strong>Built-in Overloading:</strong> <span class="mono">System.out.println()</span> is overloaded for every data type (<span class="mono">int</span>, <span class="mono">boolean</span>, <span class="mono">char</span>, <span class="mono">String</span>, <span class="mono">Object</span>).</div>
  </div>

</div>

</div>

  </template>
</Slide2>
