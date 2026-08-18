---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 1 — WHAT IS RECURSION?
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Recursion">
  <template #content>

<div class="slide-h1" style="margin-bottom:12px;">What is <span class="highlight">Recursion?</span></div>

<div class="g2" style="gap:14px;align-items:start;">

<div class="flex-col">

  <div v-click class="card-navy" style="border-radius:10px;">
    <div style="font-size:.82rem;line-height:1.6;color:var(--slate);">
      <strong style="color:var(--red);">Definition:</strong> <strong>Recursion</strong> is a technique where a method <strong style="color:var(--green);">calls itself</strong> to solve a <strong>smaller version</strong> of the same problem — until it reaches a <strong style="color:var(--blue);">stopping condition</strong> called the <em>base case</em>.
    </div>
  </div>

  <div v-click class="callout callout-success">
    <div><strong>Key idea:</strong> Recursion breaks a big problem into a <strong>smaller version of itself</strong>, solves the smallest case (base case), then builds the answer back up.</div>
  </div>

  <div v-click class="section-label" style="margin-top:4px;">Java Syntax Structure</div>

  <div v-after class="code-block" style="font-size:.76rem;line-height:1.9;">
    <span style="color:#ef5050;">returnType</span> <span style="color:#0e6ead;">methodName</span>(<span style="color:#c49a00;">parameters</span>) {<br>
    <span style="padding-left:20px;display:block;color:#6b7280;">// Base Case — stopping condition</span>
    <span style="padding-left:20px;display:block;"><span style="color:#ef5050;">if</span> (<span style="color:#0e6ead;">baseCondition</span>) {</span>
    <span style="padding-left:40px;display:block;"><span style="color:#ef5050;">return</span> <span style="color:#2d7a00;">baseValue</span>;</span>
    <span style="padding-left:20px;display:block;">}</span>
    <span style="padding-left:20px;display:block;color:#6b7280;">// Recursive Case — calls itself</span>
    <span style="padding-left:20px;display:block;"><span style="color:#ef5050;">return</span> <span style="color:#0e6ead;">methodName</span>(<span style="color:#0e6ead;">smallerInput</span>);</span>
    }
  </div>

</div>

<div class="flex-col">

  <div style="margin-top:4px;border:1px solid #e1e4e808;padding:10px;border-radius:10px;">
    <div v-click class="section-label" style="margin-bottom:6px;">Syntax Parts</div>
    <div style="display:flex;flex-direction:column;gap:5px;">
      <div style="display:flex;gap:8px;align-items:center;" v-click>
        <span class="syn-keyword">returnType</span>
        <span class="body-text">Java requires an explicit return type (e.g. <span class="mono">int</span>, <span class="mono">void</span>)</span>
      </div>
      <div style="display:flex;gap:8px;align-items:center;" v-click>
        <span class="syn-varname">baseCondition</span>
        <span class="body-text">When to stop calling itself — mandatory!</span>
      </div>
      <div style="display:flex;gap:8px;align-items:center;" v-click>
        <span class="syn-operator">return baseValue</span>
        <span class="body-text">Return a direct answer at the base case</span>
      </div>
      <div style="display:flex;gap:8px;align-items:center;" v-click>
        <span class="syn-value">methodName(smallerInput)</span>
        <span class="body-text">The recursive call — input must shrink toward base case</span>
      </div>
    </div>
  </div>

  <div v-click class="callout callout-info" style="margin-top:6px;">
    <div>Unlike Python, Java methods must have a <strong>declared return type</strong>. A <span class="mono">static</span> modifier is needed for recursion inside <span class="mono">main()</span> without an object.</div>
  </div>

</div>

</div>

  </template>
</Slide2>
