---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 1 — INTRODUCTION TO JAVA INPUT
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Input Methods">
  <template #content>

<div class="slide-h1" style="margin-bottom:10px;">Introduction to Java <span class="highlight">Input Methods</span></div>

<div class="g2" style="gap:14px;align-items:start;">

<div class="flex-col">

  <div v-click class="card-navy" style="border-radius:10px;">
    <div style="font-size:.82rem;line-height:1.6;color:var(--slate);">
      <strong style="color:var(--red);">Definition:</strong> Getting <strong>input</strong> means reading data typed by the user while the program is running, so the program can react to it instead of using only hard-coded values.
    </div>
  </div>

  <div v-click class="callout callout-warn">
    <div><strong>The Scanner class:</strong> Java's most common way to read keyboard input is the <span class="mono">Scanner</span> class, found in the <span class="mono">java.util</span> package.</div>
  </div>

  <div v-click style="background:#f6f8fa;border-radius:10px;border:1px solid #e1e4e8;padding:14px;font-family:'Fira Code',monospace;font-size:.74rem;line-height:2;">
    <span style="color:#805ad5;">import</span> <span style="color:#0e6ead;">java.util.Scanner</span>;<br><br>
    <span style="color:#ef5050;">public</span> <span style="color:#ef5050;">class</span> <span style="color:#0e6ead;">Main</span> {<br>
    &nbsp;&nbsp;<span style="color:#ef5050;">public</span> <span style="color:#ef5050;">static</span> <span style="color:#ef5050;">void</span> <span style="color:#2d7a00;">main</span>(<span style="color:#0e6ead;">String</span>[] <span style="color:#0e6ead;">args</span>) {<br>
    &nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#0e6ead;">Scanner</span> <span style="color:#0e6ead;">sc</span> = <span style="color:#805ad5;">new</span> <span style="color:#0e6ead;">Scanner</span>(<span style="color:#0e6ead;">System</span>.<span style="color:#0e6ead;">in</span>); <span style="color:#6b7280;">// create scanner</span><br>
    &nbsp;&nbsp;}<br>
    }
  </div>

</div>

<div class="flex-col">
  <div class="section-label" v-click>Three Steps to Read Input</div>

  <div v-click class="step-flow">
    <div class="step-box active">1. Import</div>
    <span class="step-arrow">→</span>
    <div class="step-box active">2. Create</div>
    <span class="step-arrow">→</span>
    <div class="step-box active">3. Read</div>
  </div>

  <div style="display:flex;flex-direction:column;gap:5px;margin-top:6px;">
    <div style="display:flex;gap:6px;flex-wrap:wrap;" v-click>
      <span class="pill pill-blue">Numbers</span>
      <span class="small-text" style="align-self:center;">— nextInt(), nextDouble(), nextLong()</span>
    </div>
    <div style="display:flex;gap:6px;flex-wrap:wrap;" v-click>
      <span class="pill pill-green">Text</span>
      <span class="small-text" style="align-self:center;">— next(), nextLine()</span>
    </div>
    <div style="display:flex;gap:6px;flex-wrap:wrap;" v-click>
      <span class="pill pill-purple">Boolean</span>
      <span class="small-text" style="align-self:center;">— nextBoolean()</span>
    </div>
  </div>

  <div v-click class="callout callout-info" style="margin-top:6px;">
    <div><strong>Why <span class="mono">System.in</span>?</strong> It represents the <strong>standard input stream</strong> — by default, the keyboard. Wrapping it in a <span class="mono">Scanner</span> lets Java parse the raw text into usable types.</div>
  </div>

</div>

</div>

  </template>
</Slide2>
