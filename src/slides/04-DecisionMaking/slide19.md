---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 19 — SWITCH STATEMENT CODE EXAMPLE
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Decision-making statements">
  <template #content>
<div class="slide-h1" style="margin-bottom:12px;"><span class="highlight">switch</span> Statement — Java Example</div>

<div class="g2" style="gap:14px;">

<div class="flex-col" style="gap:10px;">
  <div v-click class="slide-h3">Example: Day Name Selector</div>

  <div v-after style="background:#1a1f36;border-radius:10px;padding:12px 16px;font-family:'Fira Code',monospace;font-size:.72rem;line-height:1.75;">
    <span style="color:#8be9fd;">int</span> <span style="color:#f8f8f2;">dayNumber</span> = <span style="color:#bd93f9;">3</span>;<br><br>
    <span style="color:#ff79c6;">switch</span> <span style="color:#f1fa8c;">(</span><span style="color:#f8f8f2;">dayNumber</span><span style="color:#f1fa8c;">) {</span><br>
    &nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#ff79c6;">case</span> <span style="color:#bd93f9;">1</span>:<br>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#8be9fd;">System</span>.<span style="color:#f8f8f2;">out</span>.<span style="color:#50fa7b;">println</span><span style="color:#f1fa8c;">(</span><span style="color:#f1fa8c;">"Monday"</span><span style="color:#f1fa8c;">)</span>;<br>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#ff79c6;">break</span>;<br>
    &nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#ff79c6;">case</span> <span style="color:#bd93f9;">2</span>:<br>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#8be9fd;">System</span>.<span style="color:#f8f8f2;">out</span>.<span style="color:#50fa7b;">println</span><span style="color:#f1fa8c;">(</span><span style="color:#f1fa8c;">"Tuesday"</span><span style="color:#f1fa8c;">)</span>;<br>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#ff79c6;">break</span>;<br>
    &nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#ff79c6;">case</span> <span style="color:#bd93f9;">3</span>:<br>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#8be9fd;">System</span>.<span style="color:#f8f8f2;">out</span>.<span style="color:#50fa7b;">println</span><span style="color:#f1fa8c;">(</span><span style="color:#f1fa8c;">"Wednesday"</span><span style="color:#f1fa8c;">)</span>;<br>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#ff79c6;">break</span>;<br>
    &nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#ff79c6;">default</span>:<br>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#8be9fd;">System</span>.<span style="color:#f8f8f2;">out</span>.<span style="color:#50fa7b;">println</span><span style="color:#f1fa8c;">(</span><span style="color:#f1fa8c;">"Invalid Day"</span><span style="color:#f1fa8c;">)</span>;<br>
    <span style="color:#f1fa8c;">}</span>
  </div>

  <div v-click class="output-box">
    <span class="prompt">Output (dayNumber = 3):</span><br>
    Wednesday
  </div>
</div>

<div class="flex-col" style="gap:10px;">
  <div v-click class="card card-navy">
    <div class="slide-h3" style="margin-bottom:6px;">How Java Executes Switch</div>
    <div class="flex-col" style="gap:6px;">
      <div class="body-text">1. Java evaluates <code>dayNumber</code> (value 3).</div>
      <div class="body-text">2. Skips <code>case 1:</code> and <code>case 2:</code> directly.</div>
      <div class="body-text">3. Matches <code>case 3:</code>, prints <code>"Wednesday"</code>.</div>
      <div class="body-text">4. Encounters <code>break;</code> statement and immediately exits the switch.</div>
    </div>
  </div>

  <div v-click class="callout callout-success">
    <div><strong>Efficiency Tip:</strong> Switch statements jump directly to the matching case via jump tables/hashcode, making exact match checks faster than long <code>if-else-if</code> chains!</div>
  </div>
</div>

</div>
  </template>
</Slide2>
