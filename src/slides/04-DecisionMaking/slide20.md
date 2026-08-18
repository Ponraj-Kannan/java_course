---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 20 — SWITCH FALL-THROUGH BEHAVIOR
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Decision-making statements">
  <template #content>
<div class="slide-h1" style="margin-bottom:12px;">switch <span class="highlight">Fall-Through Behavior</span></div>

<div class="g2" style="gap:14px;">

<div class="flex-col" style="gap:10px;">
  <div v-click class="callout callout-danger">
    <div style="font-size:.8rem;line-height:1.5;color:var(--slate);">
      <strong>Definition:</strong> <strong style="color:var(--red);">Fall-through behavior</strong> occurs when a <code>break;</code> statement is omitted from a <code>case</code> block. Execution <strong style="color:var(--red);">"falls through"</strong> into subsequent cases, executing their statements regardless of whether their labels match!
    </div>
  </div>

  <div v-click class="card card-red">
    <div class="slide-h3" style="color:var(--red-dark);margin-bottom:6px;">❌ Missing break; Example</div>
    <div style="font-family:'Fira Code',monospace;font-size:.7rem;line-height:1.7;background:#ffffff;padding:8px;border-radius:6px;">
      <span style="color:#8be9fd;">int</span> num = <span style="color:#bd93f9;">1</span>;<br>
      <span style="color:#ff79c6;">switch</span> (num) {<br>
      &nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#ff79c6;">case</span> <span style="color:#bd93f9;">1</span>: System.out.println(<span style="color:#f1fa8c;">"One"</span>); <span style="color:#ef5050;">// NO BREAK!</span><br>
      &nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#ff79c6;">case</span> <span style="color:#bd93f9;">2</span>: System.out.println(<span style="color:#f1fa8c;">"Two"</span>); <span style="color:#ef5050;">// NO BREAK!</span><br>
      &nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#ff79c6;">case</span> <span style="color:#bd93f9;">3</span>: System.out.println(<span style="color:#f1fa8c;">"Three"</span>);<br>
      }
    </div>
    <div class="output-box" style="margin-top:6px;font-size:.7rem;">
      <span class="prompt">Actual Output for num = 1:</span><br>
      One<br>Two<br>Three
    </div>
  </div>
</div>

<div class="flex-col" style="gap:10px;">
  <div v-click class="card card-green">
    <div class="slide-h3" style="color:var(--green);margin-bottom:6px;">Intentional Fall-Through (Grouping Cases)</div>
    <div style="font-family:'Fira Code',monospace;font-size:.7rem;line-height:1.7;background:#ffffff;padding:8px;border-radius:6px;">
      <span style="color:#8be9fd;">char</span> ch = <span style="color:#f1fa8c;">'E'</span>;<br>
      <span style="color:#ff79c6;">switch</span> (ch) {<br>
      &nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#ff79c6;">case</span> <span style="color:#f1fa8c;">'A'</span>: <span style="color:#ff79c6;">case</span> <span style="color:#f1fa8c;">'E'</span>: <span style="color:#ff79c6;">case</span> <span style="color:#f1fa8c;">'I'</span>:<br>
      &nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#ff79c6;">case</span> <span style="color:#f1fa8c;">'O'</span>: <span style="color:#ff79c6;">case</span> <span style="color:#f1fa8c;">'U'</span>:<br>
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;System.out.println(<span style="color:#f1fa8c;">"Vowel"</span>);<br>
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#ff79c6;">break</span>;<br>
      &nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#ff79c6;">default</span>:<br>
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;System.out.println(<span style="color:#f1fa8c;">"Consonant"</span>);<br>
      }
    </div>
  </div>

  <div v-click class="callout callout-warn">
    <div><strong>Gotcha Warning:</strong> 90% of beginner switch bugs are caused by accidentally forgetting <code>break;</code>! Always check your break statements.</div>
  </div>
</div>

</div>
  </template>
</Slide2>
