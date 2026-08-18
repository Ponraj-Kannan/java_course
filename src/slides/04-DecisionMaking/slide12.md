---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 12 — NESTED IF STATEMENTS
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Decision-making statements">
  <template #content>
<div class="slide-h1" style="margin-bottom:12px;">Nested <span class="highlight">if</span> Statements</div>

<div class="g2" style="gap:14px;">

<div class="flex-col" style="gap:10px;">
  <div v-click class="callout callout-info">
    <div style="font-size:.8rem;line-height:1.5;color:var(--slate);">
      <strong>Definition:</strong> A <strong style="color:var(--green);">nested if statement</strong> is an <code>if</code> statement placed inside the body of another <code>if</code> block. The inner <code>if</code> executes <strong style="color:var(--red);">only when the outer condition is true</strong>.
    </div>
  </div>

  <div v-click class="card card-orange">
    <div class="slide-h3" style="margin-bottom:6px;">Visual Nested Structure</div>
    <div style="font-family:'Fira Code',monospace;font-size:.72rem;line-height:1.9;background:#fff8f0;padding:8px;border-radius:6px;">
      <span style="color:#dd6b20;">if</span> (outerCondition) {<br>
      <span style="background:rgba(221,107,32,.15);display:inline-block;width:95%;padding-left:4px;border-left:3px solid #dd6b20;">
        &nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#3182ce;">if</span> (innerCondition) {<br>
        <span style="background:rgba(49,130,206,.15);display:inline-block;width:88%;margin-left:8px;padding-left:4px;border-left:3px solid #3182ce;">
          &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#38a169;">// runs when BOTH are true</span>
        </span><br>
        &nbsp;&nbsp;&nbsp;&nbsp;}
      </span><br>
      }
    </div>
  </div>
</div>

<div class="flex-col" style="gap:10px;">
  <div v-click class="card card-blue">
    <div class="slide-h3" style="color:var(--blue);margin-bottom:6px;">When to use Nested if?</div>
    <div class="body-text">Use nested <code>if</code> when a secondary check is only meaningful after a primary condition passes.</div>
  </div>

  <div v-click class="callout callout-warn">
    <div><strong>Best Practice:</strong> Avoid nesting more than 2–3 levels deep to prevent "spaghetti code". You can often simplify nested ifs using logical AND (<code>&amp;&amp;</code>).</div>
  </div>
</div>

</div>
  </template>
</Slide2>
