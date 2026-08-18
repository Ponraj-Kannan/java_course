---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 19 — LABELED BREAK AND CONTINUE (JAVA SPECIFIC)
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Labeled Statements">
  <template #content>

<div class="slide-h1" style="margin-bottom:10px;"><span class="highlight">Labeled</span> Break &amp; Continue in Java</div>

<div class="g2" style="gap:14px;align-items:start;">

<div class="flex-col">
  <div v-click class="card-navy">
    <div style="font-size:.8rem;line-height:1.6;color:var(--slate);">
      In Java, an unlabeled <span class="mono" style="color:var(--red-dark);">break</span> or <span class="mono" style="color:var(--green);">continue</span> only affects the <strong>innermost</strong> loop. <strong style="color:var(--navy);">Labels</strong> allow breaking or continuing an <strong>outer loop</strong> directly!
    </div>
  </div>

  <div v-click style="background:#f6f8fa;border-radius:10px;border:1px solid #e1e4e8;padding:14px;font-family:'Fira Code',monospace;font-size:.72rem;line-height:1.9;margin-top:8px;">
    <span style="color:#ef5050;font-weight:700;">outerLoop:</span><br>
    <span style="color:#ef5050;">for</span> (<span style="color:#0e6ead;">int</span> i = <span style="color:#b45309;">1</span>; i &lt;= <span style="color:#b45309;">3</span>; i++) {<br>
    <span style="padding-left:20px;display:block;"><span style="color:#ef5050;">for</span> (<span style="color:#0e6ead;">int</span> j = <span style="color:#b45309;">1</span>; j &lt;= <span style="color:#b45309;">3</span>; j++) {</span>
    <span style="padding-left:40px;display:block;"><span style="color:#ef5050;">if</span> (i == <span style="color:#b45309;">2</span> &amp;&amp; j == <span style="color:#b45309;">2</span>) {</span>
    <span style="padding-left:60px;display:block;"><span style="color:#ef5050;">break</span> <span style="color:#ef5050;font-weight:700;">outerLoop</span>; <span style="color:#6b7280;">// Exits BOTH loops!</span></span>
    <span style="padding-left:40px;display:block;">}</span>
    <span style="padding-left:40px;display:block;">System.out.<span style="color:#2d7a00;">println</span>(i + <span style="color:#2d7a00;">","</span> + j);</span>
    <span style="padding-left:20px;display:block;">}</span>
    }
  </div>

</div>

<div class="flex-col">
  <div v-click class="section-label">Execution Trace &amp; Comparison</div>

  <div v-click class="output-box" style="font-size:.72rem;">
    1,1<br>
    1,2<br>
    1,3<br>
    2,1<br>
    <span style="color:#c0392b;">(Loop terminated completely when i=2, j=2)</span>
  </div>

  <div v-click style="margin-top:8px;">
    <table class="cmp-table" style="font-size:.7rem;">
      <thead><tr><th>Statement</th><th>Effect in Nested Loops</th></tr></thead>
      <tbody>
        <tr><td><code>break;</code></td><td>Exits <strong>inner loop only</strong> (outer continues)</td></tr>
        <tr><td><code>break outerLabel;</code></td><td>Exits <strong>outer loop completely</strong></td></tr>
        <tr><td><code>continue outerLabel;</code></td><td>Skips to <strong>next outer loop iteration</strong></td></tr>
      </tbody>
    </table>
  </div>

  <div v-click class="callout callout-info" style="margin-top:6px;">
    <div><strong>Best Practice:</strong> Use labeled breaks primarily for multi-dimensional matrix searches to avoid extra boolean flag variables.</div>
  </div>
</div>

</div>

  </template>
</Slide2>
