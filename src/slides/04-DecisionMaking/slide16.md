---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 16 — TERNARY CODE EXAMPLES & COMPARISON
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Decision-making statements">
  <template #content>
<div class="slide-h1" style="margin-bottom:12px;">Ternary Operator <span class="highlight">vs if-else</span></div>

<div class="g2" style="gap:14px;">

<div class="flex-col" style="gap:8px;">
  <div class="pill pill-red" style="margin-bottom:4px;">Verbose if-else Approach</div>
  <div v-click style="background:#1a1f36;border-radius:10px;padding:12px 16px;font-family:'Fira Code',monospace;font-size:.72rem;line-height:1.85;">
    <span style="color:#8be9fd;">int</span> <span style="color:#f8f8f2;">a</span> = <span style="color:#bd93f9;">10</span>, <span style="color:#f8f8f2;">b</span> = <span style="color:#bd93f9;">20</span>;<br>
    <span style="color:#8be9fd;">int</span> <span style="color:#f8f8f2;">max</span>;<br><br>
    <span style="color:#ff79c6;">if</span> <span style="color:#f1fa8c;">(</span><span style="color:#f8f8f2;">a &gt; b</span><span style="color:#f1fa8c;">) {</span><br>
    &nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#f8f8f2;">max</span> = <span style="color:#f8f8f2;">a</span>;<br>
    <span style="color:#f1fa8c;">}</span> <span style="color:#ff79c6;">else</span> <span style="color:#f1fa8c;">{</span><br>
    &nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#f8f8f2;">max</span> = <span style="color:#f8f8f2;">b</span>;<br>
    <span style="color:#f1fa8c;">}</span>
  </div>
  <div class="small-text">Requires 6 lines of code.</div>
</div>

<div class="flex-col" style="gap:8px;">
  <div class="pill pill-green" style="margin-bottom:4px;">Concise Ternary Approach</div>
  <div v-click style="background:#1a1f36;border-radius:10px;padding:12px 16px;font-family:'Fira Code',monospace;font-size:.72rem;line-height:1.85;">
    <span style="color:#8be9fd;">int</span> <span style="color:#f8f8f2;">a</span> = <span style="color:#bd93f9;">10</span>, <span style="color:#f8f8f2;">b</span> = <span style="color:#bd93f9;">20</span>;<br><br>
    <span style="color:#8be9fd;">int</span> <span style="color:#f8f8f2;">max</span> = <span style="color:#f1fa8c;">(</span><span style="color:#f8f8f2;">a &gt; b</span><span style="color:#f1fa8c;">)</span> ? <span style="color:#f8f8f2;">a</span> : <span style="color:#f8f8f2;">b</span>;<br><br>
    <span style="color:#8be9fd;">System</span>.<span style="color:#f8f8f2;">out</span>.<span style="color:#50fa7b;">println</span><span style="color:#f1fa8c;">(</span><span style="color:#f1fa8c;">"Max: "</span> + <span style="color:#f8f8f2;">max</span><span style="color:#f1fa8c;">)</span>;
  </div>
  <div class="small-text">Clean, 1-line expression!</div>
</div>

</div>

<div style="margin-top:10px;">
  <div v-click class="card card-purple">
    <div class="slide-h3" style="color:var(--purple);margin-bottom:4px;">Even/Odd String Assignment Example</div>
    <div style="font-family:'Fira Code',monospace;font-size:.72rem;line-height:1.75;background:#ffffff;padding:8px;border-radius:6px;">
      <span style="color:#8be9fd;">String</span> status = (num % 2 == 0) ? <span style="color:#f1fa8c;">"Even Number"</span> : <span style="color:#f1fa8c;">"Odd Number"</span>;
    </div>
  </div>
</div>
  </template>
</Slide2>
