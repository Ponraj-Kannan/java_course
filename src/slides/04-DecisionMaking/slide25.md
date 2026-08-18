---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 25 — COMMON BEGINNER MISTAKES
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Decision-making statements">
  <template #content>
<div class="slide-h1" style="margin-bottom:12px;">Common Beginner <span class="highlight">Mistakes in Java</span></div>

<div class="g2" style="gap:12px;">

<div class="flex-col" style="gap:8px;">
  <div v-click class="card card-red">
    <div class="slide-h3" style="color:var(--red-dark);margin-bottom:4px;">1. Assignment <code>=</code> vs Equality <code>==</code></div>
    <div class="body-text">Using single <code>=</code> inside conditions causes compile errors in Java:</div>
    <div style="font-family:'Fira Code',monospace;font-size:.68rem;background:#fff;padding:6px;border-radius:4px;margin-top:4px;">
      <span style="color:#ef5050;">if (x = 5) // Compiler Error!</span><br>
      <span style="color:#276749;">if (x == 5) // Correct boolean check</span>
    </div>
  </div>

  <div v-click class="card card-red">
    <div class="slide-h3" style="color:var(--red-dark);margin-bottom:4px;">2. Variable Block Scope Leaks</div>
    <div class="body-text">Variables declared inside an <code>if</code> block cannot be accessed outside:</div>
    <div style="font-family:'Fira Code',monospace;font-size:.68rem;background:#fff;padding:6px;border-radius:4px;margin-top:4px;">
      if (flag) { int result = 10; }<br>
      <span style="color:#ef5050;">System.out.println(result); // Error: cannot find symbol</span>
    </div>
  </div>
</div>

<div class="flex-col" style="gap:8px;">
  <div v-click class="card card-orange">
    <div class="slide-h3" style="color:var(--orange);margin-bottom:4px;">3. Dangling else Problem</div>
    <div class="body-text">Without curly braces <code>{ }</code>, an <code>else</code> attaches to the nearest preceding <code>if</code>!</div>
    <div style="font-family:'Fira Code',monospace;font-size:.68rem;background:#fff;padding:6px;border-radius:4px;margin-top:4px;">
      <span style="color:#636e80;">// Always use { } braces to make ownership clear!</span>
    </div>
  </div>

  <div v-click class="card card-orange">
    <div class="slide-h3" style="color:var(--orange);margin-bottom:4px;">4. Missing break in switch</div>
    <div class="body-text">Omitting <code>break;</code> accidentally executes all subsequent case statements!</div>
  </div>
</div>

</div>
  </template>
</Slide2>
