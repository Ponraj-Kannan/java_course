---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 4 — IF STATEMENT CODE EXAMPLE
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Decision-making statements">
  <template #content>
<div class="slide-h1" style="margin-bottom:12px;"><span class="highlight">if</span> Statement — Java Example</div>

<div class="g2" style="gap:14px;">

<div class="flex-col" style="gap:10px;">
  <div v-click class="slide-h3">Example: Checking Pass Marks</div>

  <div v-after style="background:#1a1f36;border-radius:10px;padding:12px 16px;font-family:'Fira Code',monospace;font-size:.74rem;line-height:1.8;">
    <span style="color:#ff79c6;">public class</span> <span style="color:#50fa7b;">PassCheck</span> <span style="color:#f1fa8c;">{</span><br>
    &nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#ff79c6;">public static void</span> <span style="color:#50fa7b;">main</span><span style="color:#f1fa8c;">(</span><span style="color:#8be9fd;">String</span><span style="color:#ff79c6;">[]</span> <span style="color:#ffb86c;">args</span><span style="color:#f1fa8c;">) {</span><br>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#8be9fd;">int</span> <span style="color:#f8f8f2;">marks</span> = <span style="color:#bd93f9;">75</span>;<br><br>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#ff79c6;">if</span> <span style="color:#f1fa8c;">(</span><span style="color:#f8f8f2;">marks &gt;= 50</span><span style="color:#f1fa8c;">) {</span><br>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#8be9fd;">System</span>.<span style="color:#f8f8f2;">out</span>.<span style="color:#50fa7b;">println</span><span style="color:#f1fa8c;">(</span><span style="color:#f1fa8c;">"Congratulations! You passed."</span><span style="color:#f1fa8c;">)</span>;<br>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#f1fa8c;">}</span><br><br>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#8be9fd;">System</span>.<span style="color:#f8f8f2;">out</span>.<span style="color:#50fa7b;">println</span><span style="color:#f1fa8c;">(</span><span style="color:#f1fa8c;">"End of Program."</span><span style="color:#f1fa8c;">)</span>;<br>
    &nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#f1fa8c;">}</span><br>
    <span style="color:#f1fa8c;">}</span>
  </div>

  <div v-click class="output-box">
    <span class="prompt">Output (marks = 75):</span><br>
    Congratulations! You passed.<br>
    End of Program.
  </div>
</div>

<div class="flex-col" style="gap:10px;">
  <div v-click class="card card-navy">
    <div class="slide-h3" style="margin-bottom:6px;">Execution Trace</div>
    <div class="flex-col" style="gap:6px;">
      <div class="body-text">1. Variable <code>marks</code> initialized to <code>75</code>.</div>
      <div class="body-text">2. Condition <code>75 &gt;= 50</code> evaluates to <span style="color:var(--green);font-weight:700;">true</span>.</div>
      <div class="body-text">3. Statements inside <code>{ }</code> are executed.</div>
      <div class="body-text">4. Control moves to the line after <code>}</code> and prints <code>"End of Program."</code>.</div>
    </div>
  </div>

  <div v-click class="card card-red">
    <div class="slide-h3" style="color:var(--red-dark);margin-bottom:4px;">What if marks = 30?</div>
    <div class="body-text">Condition <code>30 &gt;= 50</code> evaluates to <span style="color:var(--red);font-weight:700;">false</span>.</div>
    <div class="output-box" style="margin-top:6px;">
      <span class="prompt">Output (marks = 30):</span><br>
      End of Program.
    </div>
  </div>
</div>

</div>
  </template>
</Slide2>
