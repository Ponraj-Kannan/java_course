---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 7 — IF-ELSE CODE EXAMPLE
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Decision-making statements">
  <template #content>
<div class="slide-h1" style="margin-bottom:12px;"><span class="highlight">if-else</span> Statement — Java Example</div>

<div class="g2" style="gap:14px;">

<div class="flex-col" style="gap:10px;">
  <div v-click class="slide-h3">Example: Even or Odd Number</div>

  <div v-after style="background:#1a1f36;border-radius:10px;padding:12px 16px;font-family:'Fira Code',monospace;font-size:.74rem;line-height:1.8;">
    <span style="color:#ff79c6;">public class</span> <span style="color:#50fa7b;">EvenOdd</span> <span style="color:#f1fa8c;">{</span><br>
    &nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#ff79c6;">public static void</span> <span style="color:#50fa7b;">main</span><span style="color:#f1fa8c;">(</span><span style="color:#8be9fd;">String</span><span style="color:#ff79c6;">[]</span> <span style="color:#ffb86c;">args</span><span style="color:#f1fa8c;">) {</span><br>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#8be9fd;">int</span> <span style="color:#f8f8f2;">number</span> = <span style="color:#bd93f9;">17</span>;<br><br>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#ff79c6;">if</span> <span style="color:#f1fa8c;">(</span><span style="color:#f8f8f2;">number % 2 == 0</span><span style="color:#f1fa8c;">) {</span><br>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#8be9fd;">System</span>.<span style="color:#f8f8f2;">out</span>.<span style="color:#50fa7b;">println</span><span style="color:#f1fa8c;">(</span><span style="color:#f8f8f2;">number</span> + <span style="color:#f1fa8c;">" is Even."</span><span style="color:#f1fa8c;">)</span>;<br>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#f1fa8c;">}</span> <span style="color:#ff79c6;">else</span> <span style="color:#f1fa8c;">{</span><br>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#8be9fd;">System</span>.<span style="color:#f8f8f2;">out</span>.<span style="color:#50fa7b;">println</span><span style="color:#f1fa8c;">(</span><span style="color:#f8f8f2;">number</span> + <span style="color:#f1fa8c;">" is Odd."</span><span style="color:#f1fa8c;">)</span>;<br>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#f1fa8c;">}</span><br>
    &nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#f1fa8c;">}</span><br>
    <span style="color:#f1fa8c;">}</span>
  </div>

  <div v-click class="output-box">
    <span class="prompt">Output (number = 17):</span><br>
    17 is Odd.
  </div>
</div>

<div class="flex-col" style="gap:10px;">
  <div v-click class="card card-green">
    <div class="slide-h3" style="color:var(--green);margin-bottom:6px;">Line-by-Line Execution</div>
    <div class="flex-col" style="gap:6px;">
      <div class="body-text">1. <code>number</code> holds value <code>17</code>.</div>
      <div class="body-text">2. <code>17 % 2</code> equals <code>1</code>.</div>
      <div class="body-text">3. <code>1 == 0</code> evaluates to <span style="color:var(--red);font-weight:700;">false</span>.</div>
      <div class="body-text">4. The <code>if</code> block is skipped completely.</div>
      <div class="body-text">5. Control jumps directly to <code>else</code> block and prints <code>17 is Odd.</code></div>
    </div>
  </div>

  <div v-click class="callout callout-warn">
    <div><strong>Modulus Operator (<code>%</code>):</strong> <code>number % 2</code> yields the remainder when divided by 2. If remainder is 0, number is even!</div>
  </div>
</div>

</div>
  </template>
</Slide2>
