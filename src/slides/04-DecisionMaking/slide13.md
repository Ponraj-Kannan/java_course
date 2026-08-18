---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 13 — NESTED IF CODE EXAMPLE
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Decision-making statements">
  <template #content>
<div class="slide-h1" style="margin-bottom:12px;">Nested <span class="highlight">if</span> — Java Example</div>

<div class="g2" style="gap:14px;">

<div class="flex-col" style="gap:10px;">
  <div v-click class="slide-h3">Example: Loan Approval Check</div>

  <div v-after style="background:#1a1f36;border-radius:10px;padding:12px 16px;font-family:'Fira Code',monospace;font-size:.72rem;line-height:1.75;">
    <span style="color:#8be9fd;">int</span> <span style="color:#f8f8f2;">age</span> = <span style="color:#bd93f9;">25</span>;<br>
    <span style="color:#8be9fd;">double</span> <span style="color:#f8f8f2;">salary</span> = <span style="color:#bd93f9;">45000.0</span>;<br><br>
    <span style="color:#ff79c6;">if</span> <span style="color:#f1fa8c;">(</span><span style="color:#f8f8f2;">age &gt;= 21</span><span style="color:#f1fa8c;">) {</span><br>
    &nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#ff79c6;">if</span> <span style="color:#f1fa8c;">(</span><span style="color:#f8f8f2;">salary &gt;= 30000</span><span style="color:#f1fa8c;">) {</span><br>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#8be9fd;">System</span>.<span style="color:#f8f8f2;">out</span>.<span style="color:#50fa7b;">println</span><span style="color:#f1fa8c;">(</span><span style="color:#f1fa8c;">"Loan Approved!"</span><span style="color:#f1fa8c;">)</span>;<br>
    &nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#f1fa8c;">}</span> <span style="color:#ff79c6;">else</span> <span style="color:#f1fa8c;">{</span><br>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#8be9fd;">System</span>.<span style="color:#f8f8f2;">out</span>.<span style="color:#50fa7b;">println</span><span style="color:#f1fa8c;">(</span><span style="color:#f1fa8c;">"Loan Denied: Salary too low."</span><span style="color:#f1fa8c;">)</span>;<br>
    &nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#f1fa8c;">}</span><br>
    <span style="color:#f1fa8c;">}</span> <span style="color:#ff79c6;">else</span> <span style="color:#f1fa8c;">{</span><br>
    &nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#8be9fd;">System</span>.<span style="color:#f8f8f2;">out</span>.<span style="color:#50fa7b;">println</span><span style="color:#f1fa8c;">(</span><span style="color:#f1fa8c;">"Loan Denied: Underage."</span><span style="color:#f1fa8c;">)</span>;<br>
    <span style="color:#f1fa8c;">}</span>
  </div>

  <div v-click class="output-box">
    <span class="prompt">Output (age=25, salary=45000):</span><br>
    Loan Approved!
  </div>
</div>

<div class="flex-col" style="gap:10px;">
  <div v-click class="card card-navy">
    <div class="slide-h3" style="margin-bottom:6px;">Simplified Alternative with &&</div>
    <div style="font-family:'Fira Code',monospace;font-size:.72rem;line-height:1.75;background:#ffffff;padding:8px;border-radius:6px;">
      <span style="color:#ff79c6;">if</span> (age &gt;= 21 &amp;&amp; salary &gt;= 30000) {<br>
      &nbsp;&nbsp;&nbsp;&nbsp;System.out.println("Loan Approved!");<br>
      } <span style="color:#ff79c6;">else</span> {<br>
      &nbsp;&nbsp;&nbsp;&nbsp;System.out.println("Loan Denied.");<br>
      }
    </div>
    <div class="small-text" style="margin-top:6px;">Use logical AND when specific rejection reasons are not needed.</div>
  </div>
</div>

</div>
  </template>
</Slide2>
