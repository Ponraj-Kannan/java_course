---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 16 — INFINITE LOOPS IN JAVA
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Infinite Loops">
  <template #content>

<div class="slide-h1" style="margin-bottom:10px;"><span class="highlight">Infinite</span> Loops — Causes &amp; Safe Usage</div>

<div class="g2" style="gap:14px;align-items:start;">

<div class="flex-col">
  <div v-click class="section-label">Syntax &amp; Unintentional Causes</div>

  <div v-after style="background:#f6f8fa;border-radius:10px;border:1px solid #e1e4e8;padding:14px;font-family:'Fira Code',monospace;font-size:.72rem;line-height:1.9;">
    <span style="color:#6b7280;">// Standard infinite while loop</span><br>
    <span style="color:#ef5050;">while</span> (<span style="color:#ef5050;">true</span>) {<br>
    <span style="padding-left:20px;display:block;">System.out.<span style="color:#2d7a00;">println</span>(<span style="color:#2d7a00;">"Running forever..."</span>);</span>
    }<br><br>
    <span style="color:#6b7280;">// Standard infinite for loop</span><br>
    <span style="color:#ef5050;">for</span> (;;) {<br>
    <span style="padding-left:20px;display:block;">System.out.<span style="color:#2d7a00;">println</span>(<span style="color:#2d7a00;">"Running forever..."</span>);</span>
    }
  </div>

  <div v-click class="callout callout-danger" style="margin-top:6px;">
    <div><strong>Bug Warning:</strong> Common cause is forgetting to update the loop counter (e.g. missing <code>i++</code>) or setting a condition that is always true.</div>
  </div>
</div>

<div class="flex-col">
  <div v-click class="section-label">Intentional Use Cases</div>

  <div v-click class="card card-navy" style="margin-bottom:6px;">
    <div class="slide-h3" style="margin-bottom:4px;">🌐 Server &amp; Socket Polling</div>
    <div class="body-text">Web servers use infinite loops to continuously listen for incoming HTTP requests on a port.</div>
  </div>

  <div v-click class="card card-green" style="margin-bottom:6px;">
    <div class="slide-h3" style="margin-bottom:4px;">🎮 Game Loops</div>
    <div class="body-text">Game engines execute a <code>while (running)</code> loop 60 times per second to update positions and re-render frames.</div>
  </div>

  <div v-click class="card card-orange">
    <div class="slide-h3" style="margin-bottom:4px;">🚪 Safe Exit Pattern</div>
    <div class="body-text">Pair an infinite loop with an <code>if (exitCondition) break;</code> check inside the loop body to exit cleanly on command.</div>
  </div>
</div>

</div>

  </template>
</Slide2>
