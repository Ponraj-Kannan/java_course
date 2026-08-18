---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 13 — SPECIAL JAVA OPERATORS (INSTANCEOF & TERNARY)
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Operators">
  <template #content>

<div class="slide-h1" style="margin-bottom:10px;">Special Java Operators — <span class="highlight">instanceof &amp; Ternary</span></div>

<div class="g2" style="gap:14px;">

<div class="flex-col">

  <div v-click class="card-navy" style="border-radius:10px;">
    <div style="font-size:.78rem;line-height:1.5;color:var(--slate);">
      <strong style="color:var(--red);">1. instanceof Definition:</strong> Tests whether an object reference variable is an instance of a specific <strong>Class, Subclass, or Interface</strong> type (returns <span class="mono" style="color:var(--green);">true</span> or <span class="mono" style="color:var(--red-dark);">false</span>).
    </div>
  </div>

  <div v-click class="section-label" style="margin-top:2px;">instanceof Code Example</div>
  <div v-after style="background:#f6f8fa;border-radius:10px;border:1px solid #e1e4e8;padding:10px 14px;font-family:'Fira Code',monospace;font-size:.72rem;line-height:1.9;">
    <span style="color:#0e6ead;">String</span> <span style="color:#0e6ead;">name</span> = <span style="color:#2d7a00;">"Java Programming"</span>;<br>
    <span style="color:#ef5050;">boolean</span> <span style="color:#0e6ead;">isStr</span> = <span style="color:#0e6ead;">name</span> <span style="color:#ef5050;">instanceof</span> <span style="color:#0e6ead;">String</span>;<br>
    <span style="color:#0e6ead;">System</span>.<span style="color:#0e6ead;">out</span>.<span style="color:#2d7a00;">println</span>(<span style="color:#0e6ead;">isStr</span>); <span style="color:#6b7280;">// true</span>
  </div>

  <div v-click class="callout callout-info" style="margin-top:4px;">
    <div><strong>Java Use Case:</strong> <span class="mono">instanceof</span> prevents invalid object casting (downcasting) errors at runtime.</div>
  </div>

</div>

<div class="flex-col">

  <div v-click class="card-navy" style="border-radius:10px;">
    <div style="font-size:.78rem;line-height:1.5;color:var(--slate);">
      <strong style="color:var(--red);">2. Ternary Operator Definition:</strong> A compact, three-operand conditional operator (<span class="mono">? :</span>) that evaluates a boolean condition and returns one of two values.
    </div>
  </div>

  <div v-click class="section-label" style="margin-top:2px;">Syntax &amp; Code Example</div>
  <div v-after style="background:#f6f8fa;border-radius:10px;border:1px solid #e1e4e8;padding:10px 14px;font-family:'Fira Code',monospace;font-size:.72rem;line-height:1.9;">
    <span style="color:#6b7280;">// Syntax: variable = (condition) ? valueIfTrue : valueIfFalse;</span><br>
    <span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">marks</span> = <span style="color:#b45309;">75</span>;<br>
    <span style="color:#0e6ead;">String</span> <span style="color:#0e6ead;">status</span> = (<span style="color:#0e6ead;">marks</span> &gt;= <span style="color:#b45309;">50</span>) ? <span style="color:#2d7a00;">"Pass"</span> : <span style="color:#2d7a00;">"Fail"</span>;<br>
    <span style="color:#0e6ead;">System</span>.<span style="color:#0e6ead;">out</span>.<span style="color:#2d7a00;">println</span>(<span style="color:#0e6ead;">status</span>); <span style="color:#6b7280;">// "Pass"</span>
  </div>

  <div v-click class="card card-green" style="margin-top:4px;">
    <div class="small-text"><strong>Why use Ternary?</strong> It replaces simple 4-line <span class="mono">if-else</span> statements with a single clean, readable line!</div>
  </div>

</div>

</div>

  </template>
</Slide2>
