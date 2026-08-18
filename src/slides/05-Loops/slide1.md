---
theme: default
title: Java Looping Statements
titleTemplate: '%s — Java Fundamentals'
highlighter: shiki
lineNumbers: true
drawings:
  persist: false
transition: slide-left
mdc: true
colorSchema: light
fonts:
  sans: 'Nunito'
  mono: 'Fira Code'
---

<Slide2 topic="Introduction to Loops">
  <template #content>

<div class="slide-h1" style="margin-bottom:12px;">What is a <span class="highlight">Loop ?</span></div>

<div class="g2" style="gap:14px;align-items:start;">

<div class="flex-col">

  <div v-click class="card-navy" style="border-radius:10px;">
    <div style="font-size:.82rem;line-height:1.6;color:var(--slate);">
      A <strong style="color:var(--red);">loop</strong> is a control structure that <strong style="color:var(--green);">repeats a block of code</strong> multiple times — until a specified boolean condition evaluates to <span class="mono" style="color:var(--red-dark);">false</span>.
    </div>
  </div>

  <div v-click class="callout callout-warn">
    <div><strong>Without a loop:</strong> Printing 1 to 100 requires 100 <code>System.out.println()</code> statements. With a loop — just 3 lines of Java!</div>
  </div>

  <div v-click class="card card-red" style="margin-top:4px;">
    <div class="slide-h3" style="margin-bottom:6px;">Real-World Analogy</div>
    <div class="body-text">A traffic signal cycle runs <strong>repeatedly</strong> throughout the day based on a timer and sensor state. That is exactly how a loop operates in Java.</div>
  </div>

  <div v-click class="card-navy">
    <div class="small-text"><strong>Key benefit:</strong> Write code <strong>once</strong>, execute it <strong>N</strong> times — eliminates code duplication and simplifies maintenance.</div>
  </div>

</div>

<div class="flex-col">
  <div v-click class="slide-h3" style="margin-bottom:8px;">Without Loop vs With Loop in Java</div>

  <div v-after style="background:#f6f8fa;border-radius:10px;border:1px solid #e1e4e8;padding:14px;font-family:'Fira Code',monospace;font-size:.7rem;line-height:1.8;">
    <div style="color:#6b7280;margin-bottom:4px;">// Without loop — repetitive & error-prone!</div>
    <div>System.out.<span style="color:#2d7a00;">println</span>(<span style="color:#b45309;">1</span>);</div>
    <div>System.out.<span style="color:#2d7a00;">println</span>(<span style="color:#b45309;">2</span>);</div>
    <div>System.out.<span style="color:#2d7a00;">println</span>(<span style="color:#b45309;">3</span>);</div>
    <div style="color:#6b7280;">// ... 97 more lines ...</div>
    <br>
    <div style="color:#6b7280;">// With loop — clean, dynamic & robust!</div>
    <div><span style="color:#ef5050;">for</span> (<span style="color:#0e6ead;">int</span> i = <span style="color:#b45309;">1</span>; i &lt;= <span style="color:#b45309;">100</span>; i++) {</div>
    <div style="padding-left:20px;">System.out.<span style="color:#2d7a00;">println</span>(i);</div>
    <div>}</div>
  </div>
</div>

</div>

  </template>
</Slide2>
