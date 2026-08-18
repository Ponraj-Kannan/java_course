---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 11 — ENHANCED FOR LOOP (FOR-EACH)
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Enhanced For Loop">
  <template #content>

<div class="slide-h1" style="margin-bottom:10px;"><span class="highlight">Enhanced For</span> Loop (For-Each)</div>

<div class="g2" style="gap:14px;align-items:start;">

<div class="flex-col">

  <div v-click class="section-label">Syntax Structure</div>
  <div v-after style="background:#f6f8fa;border-radius:10px;border:1px solid #e1e4e8;padding:16px;font-family:'Fira Code',monospace;font-size:.78rem;line-height:2;">
    <span style="color:#ef5050;">for</span> (<span style="color:#0e6ead;">DataType</span> item <span style="color:#ef5050;">:</span> collection) {<br>
    <span style="padding-left:20px;display:block;">System.out.<span style="color:#2d7a00;">println</span>(item);</span>
    }
  </div>

  <div v-click style="margin-top:6px;display:flex;flex-direction:column;gap:5px;border:1px solid #e1e4e8;padding:10px;border-radius:10px;">
    <div style="display:flex;gap:8px;align-items:center;">
      <span class="syn-keyword">DataType</span>
      <span class="body-text">Matches element type in array (e.g. <code>int</code>, <code>String</code>)</span>
    </div>
    <div style="display:flex;gap:8px;align-items:center;">
      <span class="syn-varname">item</span>
      <span class="body-text">Variable holding current element during iteration</span>
    </div>
    <div style="display:flex;gap:8px;align-items:center;">
      <span class="syn-operator">:</span>
      <span class="body-text">Separator meaning <em>"in"</em> or <em>"for each element of"</em></span>
    </div>
    <div style="display:flex;gap:8px;align-items:center;">
      <span class="syn-value">collection</span>
      <span class="body-text">Array or iterable collection object</span>
    </div>
  </div>

  <div v-click class="callout callout-success" style="margin-top:6px;">
    <div>Eliminates array index tracking and prevents <code>ArrayIndexOutOfBoundsException</code>!</div>
  </div>

</div>

<div class="flex-col">
  <div v-click class="section-label">Traditional vs Enhanced For Loop</div>

  <div v-after style="background:#f6f8fa;border-radius:10px;border:1px solid #e1e4e8;padding:14px;font-family:'Fira Code',monospace;font-size:.72rem;line-height:1.9;">
    <span style="color:#0e6ead;">String</span>[] colors = {<span style="color:#2d7a00;">"Red"</span>, <span style="color:#2d7a00;">"Green"</span>, <span style="color:#2d7a00;">"Blue"</span>};<br><br>
    <span style="color:#6b7280;">// Traditional for loop (uses index)</span><br>
    <span style="color:#ef5050;">for</span> (<span style="color:#0e6ead;">int</span> i = <span style="color:#b45309;">0</span>; i &lt; colors.length; i++) {<br>
    <span style="padding-left:20px;display:block;">System.out.<span style="color:#2d7a00;">println</span>(colors[i]);</span>
    }<br><br>
    <span style="color:#6b7280;">// Enhanced for loop (cleaner!)</span><br>
    <span style="color:#ef5050;">for</span> (<span style="color:#0e6ead;">String</span> c : colors) {<br>
    <span style="padding-left:20px;display:block;">System.out.<span style="color:#2d7a00;">println</span>(c);</span>
    }
  </div>

  <div v-click class="card card-purple" style="margin-top:8px;">
    <div class="small-text"><strong>Limitation:</strong> Enhanced for loop is <strong>read-only</strong>. You cannot modify original array values or access loop index <code>i</code> directly.</div>
  </div>

</div>

</div>

  </template>
</Slide2>
