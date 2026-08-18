---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 5 — THE nextLine() AFTER nextInt() GOTCHA
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Java Input Methods">
  <template #content>

<div class="slide-h1" style="margin-bottom:10px;">The <span class="highlight">nextLine() Gotcha</span> &amp; Fix</div>

<div class="g2" style="gap:14px;align-items:start;">

<div class="flex-col">

  <div v-click class="card-red" style="border-radius:10px;">
    <div style="font-size:.78rem;font-weight:700;color:var(--red-dark);margin-bottom:4px;">The Problem — Skipping nextLine()</div>
    <div style="font-size:.73rem;color:var(--slate);line-height:1.5;">
      When you call <span class="mono">nextInt()</span>, it reads only the number and leaves the trailing newline (<span class="mono">\n</span>) in the input buffer. The next <span class="mono">nextLine()</span> reads that leftover newline and immediately returns an <strong>empty string</strong>!
    </div>
  </div>

  <div v-click class="section-label" style="margin-top:6px;">Input Buffer Visual Diagram</div>

  <div v-after style="background:#f7f8fc;border:1px solid var(--border);border-radius:8px;padding:10px 12px;font-size:.70rem;">
    <div style="font-weight:700;color:var(--navy);margin-bottom:6px;">User types: <span class="mono" style="background:#e2e8f0;padding:1px 6px;border-radius:4px;">25 [Enter]</span></div>
    <div style="display:flex;gap:4px;font-family:'Fira Code',monospace;font-size:.68rem;">
      <div style="background:#f0fff4;border:1px solid var(--green);padding:4px 8px;border-radius:4px;">'2'</div>
      <div style="background:#f0fff4;border:1px solid var(--green);padding:4px 8px;border-radius:4px;">'5'</div>
      <div style="background:#fff5f5;border:2px solid var(--red);padding:4px 8px;border-radius:4px;color:var(--red-dark);font-weight:700;">'\n'</div>
    </div>
    <div style="margin-top:6px;color:var(--slate);font-size:.64rem;">
      1. <span class="mono">nextInt()</span> consumes <span class="mono">'2','5'</span> → returns <span class="mono">25</span>.<br>
      2. <span class="mono">'\n'</span> remains sitting in the buffer!<br>
      3. Next <span class="mono">nextLine()</span> sees <span class="mono">'\n'</span> and consumes it → returns <span class="mono">""</span> (empty)!
    </div>
  </div>

</div>

<div class="flex-col">
  <div v-click class="section-label">Wrong vs Correct Code</div>

  <div v-after class="g2" style="gap:8px;">
    <div class="flex-col">
      <div class="section-label" style="color:var(--red);">❌ WRONG</div>
      <div class="code-block" style="font-size:.66rem;line-height:1.7;">
        <span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">age</span> = <span style="color:#0e6ead;">sc</span>.<span style="color:#2d7a00;">nextInt</span>();<br>
        <span style="color:#6b7280;">// Leftover \n in buffer</span><br>
        <span style="color:#ef5050;">String</span> <span style="color:#0e6ead;">name</span> = <span style="color:#0e6ead;">sc</span>.<span style="color:#2d7a00;">nextLine</span>();<br>
        <span style="color:#6b7280;">// name = "" (SKIPPED!)</span>
      </div>
    </div>
    <div class="flex-col">
      <div class="section-label" style="color:var(--green);">✓ CORRECT FIX</div>
      <div class="code-block" style="font-size:.66rem;line-height:1.7;">
        <span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">age</span> = <span style="color:#0e6ead;">sc</span>.<span style="color:#2d7a00;">nextInt</span>();<br>
        <span style="background:#f0fff4;border-left:2px solid var(--green);padding-left:4px;display:block;"><span style="color:#0e6ead;">sc</span>.<span style="color:#2d7a00;">nextLine</span>(); <span style="color:#6b7280;">// consume \n</span></span>
        <span style="color:#ef5050;">String</span> <span style="color:#0e6ead;">name</span> = <span style="color:#0e6ead;">sc</span>.<span style="color:#2d7a00;">nextLine</span>();<br>
        <span style="color:#6b7280;">// name = "Alice Smith"</span>
      </div>
    </div>
  </div>

  <div v-click class="callout callout-success" style="margin-top:8px;">
    <div><strong>The Universal Fix:</strong> Whenever you read a number with <span class="mono">nextInt()</span>, <span class="mono">nextDouble()</span>, or <span class="mono">next()</span>, always add a dummy <span class="mono">sc.nextLine();</span> before reading the next full string with <span class="mono">nextLine()</span>.</div>
  </div>

</div>

</div>

  </template>
</Slide2>
