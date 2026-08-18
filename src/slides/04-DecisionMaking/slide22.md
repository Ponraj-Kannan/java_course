---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 22 — ENHANCED SWITCH (JAVA 14+)
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Decision-making statements">
  <template #content>
<div class="slide-h1" style="margin-bottom:12px;">Enhanced <span class="highlight">switch</span> (Java 14+)</div>

<div class="g2" style="gap:14px;">

<div class="flex-col" style="gap:10px;">
  <div v-click class="callout callout-info">
    <div style="font-size:.8rem;line-height:1.5;color:var(--slate);">
      <strong>Definition:</strong> <strong style="color:var(--teal);">Enhanced switch</strong> uses arrow labels (<code>-&gt;</code>) to prevent accidental fall-through, support multiple comma-separated case values, and allow returning results directly as a switch expression.
    </div>
  </div>

  <div v-click class="card card-teal">
    <div class="slide-h3" style="color:var(--teal);margin-bottom:6px;">Arrow Syntax Example</div>
    <div style="font-family:'Fira Code',monospace;font-size:.7rem;line-height:1.75;background:#ffffff;padding:8px;border-radius:6px;">
      <span style="color:#8be9fd;">String</span> day = <span style="color:#f1fa8c;">"Monday"</span>;<br><br>
      <span style="color:#ff79c6;">switch</span> (day) {<br>
      &nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#ff79c6;">case</span> <span style="color:#f1fa8c;">"Monday"</span>, <span style="color:#f1fa8c;">"Friday"</span> -&gt; System.out.println(<span style="color:#f1fa8c;">"Busy day!"</span>);<br>
      &nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#ff79c6;">case</span> <span style="color:#f1fa8c;">"Saturday"</span>, <span style="color:#f1fa8c;">"Sunday"</span> -&gt; System.out.println(<span style="color:#f1fa8c;">"Weekend!"</span>);<br>
      &nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#ff79c6;">default</span> -&gt; System.out.println(<span style="color:#f1fa8c;">"Regular day"</span>);<br>
      }
    </div>
  </div>
</div>

<div class="flex-col" style="gap:10px;">
  <div v-click class="card card-purple">
    <div class="slide-h3" style="color:var(--purple);margin-bottom:6px;">Switch Expression (Returns Value)</div>
    <div style="font-family:'Fira Code',monospace;font-size:.7rem;line-height:1.75;background:#ffffff;padding:8px;border-radius:6px;">
      <span style="color:#8be9fd;">int</span> num = <span style="color:#bd93f9;">2</span>;<br>
      <span style="color:#8be9fd;">String</span> word = <span style="color:#ff79c6;">switch</span> (num) {<br>
      &nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#ff79c6;">case</span> <span style="color:#bd93f9;">1</span> -&gt; <span style="color:#f1fa8c;">"One"</span>;<br>
      &nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#ff79c6;">case</span> <span style="color:#bd93f9;">2</span> -&gt; <span style="color:#f1fa8c;">"Two"</span>;<br>
      &nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#ff79c6;">default</span> -&gt; <span style="color:#f1fa8c;">"Other"</span>;<br>
      };
    </div>
  </div>

  <div v-click class="callout callout-success">
    <div><strong>Key Advantage:</strong> No <code>break;</code> statement required! The arrow syntax automatically stops execution after the matched case expression.</div>
  </div>
</div>

</div>
  </template>
</Slide2>
