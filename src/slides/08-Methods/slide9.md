---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 9 — PASS-BY-VALUE IN JAVA (PRIMITIVE vs OBJECT)
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Java Methods">
  <template #content>

<div class="slide-h1" style="margin-bottom:10px;">Parameter Passing — <span class="highlight">Pass-by-Value</span></div>

<div class="g2" style="gap:14px;align-items:start;">

<div class="flex-col">

  <div v-click class="card-navy" style="border-radius:10px;">
    <div style="font-size:.82rem;line-height:1.6;color:var(--slate);">
      Java is <strong>strictly pass-by-value</strong> at all times. When a method is called, Java makes a <strong>copy of the argument's value</strong> (for primitives) or a <strong>copy of the reference address</strong> (for objects/arrays).
    </div>
  </div>

  <div v-click class="section-label" style="margin-top:6px;">1. Primitive Types (Direct Value Copied)</div>

  <!-- DIAGRAM: PRIMITIVE COPY -->
  <div v-after style="background:#f7f8fc;border:1px solid var(--border);border-radius:8px;padding:10px;font-size:.68rem;">
    <div class="g2" style="gap:8px;">
      <div style="background:#fff;border:1px solid var(--blue);border-radius:6px;padding:6px 8px;">
        <div style="color:var(--blue);font-weight:700;font-family:'Fira Code',monospace;">caller: int x = 10;</div>
        <div style="color:var(--slate);font-size:.62rem;margin-top:2px;">Original variable remains <strong>10</strong></div>
      </div>
      <div style="background:#fff5f5;border:1px solid var(--red);border-radius:6px;padding:6px 8px;">
        <div style="color:var(--red-dark);font-weight:700;font-family:'Fira Code',monospace;">method: n = 99;</div>
        <div style="color:var(--slate);font-size:.62rem;margin-top:2px;">Modifies only local copy <span class="mono">n</span></div>
      </div>
    </div>
  </div>

  <div v-click class="section-label" style="margin-top:6px;">2. Objects &amp; Arrays (Reference Address Copied)</div>

  <!-- DIAGRAM: REFERENCE COPY -->
  <div v-after style="background:#f7f8fc;border:1px solid var(--border);border-radius:8px;padding:10px;font-size:.68rem;">
    <div style="color:var(--navy);font-weight:700;margin-bottom:4px;">📦 Both References Point to Same Heap Array:</div>
    <div style="display:flex;align-items:center;gap:10px;font-family:'Fira Code',monospace;font-size:.68rem;">
      <div style="background:#ebf8ff;border:1px solid var(--blue);padding:4px 8px;border-radius:4px;">caller: arr</div>
      <div style="color:var(--green);font-weight:700;">→ [ 99, 20, 30 ] ←</div>
      <div style="background:#f0fff4;border:1px solid var(--green);padding:4px 8px;border-radius:4px;">method: a</div>
    </div>
    <div style="color:var(--slate);font-size:.62rem;margin-top:4px;">
      Modifying array element <span class="mono">a[0] = 99</span> mutates the underlying heap object!
    </div>
  </div>

</div>

<div class="flex-col">
  <div v-click class="section-label">Code Demonstration</div>

  <div v-after class="code-block" style="font-size:.66rem;line-height:1.75;">
    <span style="color:#ef5050;">public class</span> <span style="color:#0e6ead;">PassByValueDemo</span> {<br>
    <span style="padding-left:16px;display:block;"><span style="color:#6b7280;">// 1. Primitive: cannot change caller's num</span><br><span style="color:#ef5050;">static void</span> <span style="color:#0e6ead;">changePrimitive</span>(<span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">n</span>) { n = <span style="color:#b45309;">99</span>; }</span>
    <br>
    <span style="padding-left:16px;display:block;"><span style="color:#6b7280;">// 2. Array: mutates heap contents!</span><br><span style="color:#ef5050;">static void</span> <span style="color:#0e6ead;">changeArray</span>(<span style="color:#ef5050;">int</span>[] <span style="color:#0e6ead;">arr</span>) { arr[<span style="color:#b45309;">0</span>] = <span style="color:#b45309;">99</span>; }</span>
    <br>
    <span style="padding-left:16px;display:block;"><span style="color:#ef5050;">public static void</span> <span style="color:#0e6ead;">main</span>(<span style="color:#ef5050;">String</span>[] <span style="color:#0e6ead;">args</span>) {</span>
    <span style="padding-left:32px;display:block;"><span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">x</span> = <span style="color:#b45309;">10</span>;</span>
    <span style="padding-left:32px;display:block;"><span style="color:#0e6ead;">changePrimitive</span>(x);</span>
    <span style="padding-left:32px;display:block;"><span style="color:#0e6ead;">System</span>.<span style="color:#0e6ead;">out</span>.<span style="color:#2d7a00;">println</span>(x); <span style="color:#6b7280;">// STILL 10 (unchanged)</span></span>
    <br>
    <span style="padding-left:32px;display:block;"><span style="color:#ef5050;">int</span>[] <span style="color:#0e6ead;">nums</span> = {<span style="color:#b45309;">1</span>, <span style="color:#b45309;">2</span>, <span style="color:#b45309;">3</span>};</span>
    <span style="padding-left:32px;display:block;"><span style="color:#0e6ead;">changeArray</span>(nums);</span>
    <span style="padding-left:32px;display:block;"><span style="color:#0e6ead;">System</span>.<span style="color:#0e6ead;">out</span>.<span style="color:#2d7a00;">println</span>(nums[<span style="color:#b45309;">0</span>]); <span style="color:#2d7a00;">// 99 (MUTATED!)</span></span>
    <span style="padding-left:16px;display:block;">}</span>
    }
  </div>

  <div v-click class="callout callout-warn" style="margin-top:6px;">
    <div><strong>Reassignment Warning:</strong> If a method reassigns the reference itself (<span class="mono">arr = new int[5]</span>), it only changes the local copy; caller's variable still points to original array!</div>
  </div>

</div>

</div>

  </template>
</Slide2>
