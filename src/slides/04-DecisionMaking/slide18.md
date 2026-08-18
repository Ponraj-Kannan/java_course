---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 18 — SWITCH STATEMENT SYNTAX & DEFINITION
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Decision-making statements">
  <template #content>
<div class="slide-h1" style="margin-bottom:12px;">The <span class="highlight">switch</span> Statement</div>

<div class="g2" style="gap:14px;">

<div class="flex-col" style="gap:10px;">
  <div v-click class="callout callout-info">
    <div style="font-size:.8rem;line-height:1.5;color:var(--slate);">
      <strong>Definition:</strong> The <strong style="color:var(--purple);">switch statement</strong> evaluates a single variable or expression against multiple constant values (<strong style="color:var(--green);">case labels</strong>) and executes the matching code block.
    </div>
  </div>

  <div v-click class="card-navy">
    <div style="font-size:.7rem;text-transform:uppercase;letter-spacing:1px;color:var(--muted);margin-bottom:4px;">Java Traditional Switch Syntax</div>
    <div style="font-family:'Fira Code',monospace;font-size:.74rem;line-height:1.8;margin-top:4px;background:#1a1f36;padding:10px 14px;border-radius:6px;color:#f8f8f2;">
      <span style="color:#ff79c6;">switch</span> <span style="color:#f1fa8c;">(</span><span style="color:#61dafb;">expression</span><span style="color:#f1fa8c;">) {</span><br>
      &nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#ff79c6;">case</span> <span style="color:#bd93f9;">value1</span>:<br>
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#a8ff78;">// statements</span><br>
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#ff79c6;">break</span>;<br>
      &nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#ff79c6;">case</span> <span style="color:#bd93f9;">value2</span>:<br>
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#a8ff78;">// statements</span><br>
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#ff79c6;">break</span>;<br>
      &nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#ff79c6;">default</span>:<br>
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#636e80;">// fallback if no match</span><br>
      <span style="color:#f1fa8c;">}</span>
    </div>
  </div>
</div>

<div class="flex-col" style="gap:10px;">
  <div v-click class="card card-purple">
    <div class="slide-h3" style="color:var(--purple);margin-bottom:6px;">Supported Switch Expression Types</div>
    <div class="flex-col" style="gap:6px;">
      <div class="body-text">• Primitive integers: <code>byte</code>, <code>short</code>, <code>char</code>, <code>int</code></div>
      <div class="body-text">• Wrapper types: <code>Byte</code>, <code>Short</code>, <code>Character</code>, <code>Integer</code></div>
      <div class="body-text">• <code>String</code> (Java 7+)</div>
      <div class="body-text">• Enumerations (<code>enum</code>)</div>
      <div class="small-text" style="color:var(--red);">❌ <code>boolean</code>, <code>long</code>, <code>float</code>, <code>double</code> are NOT allowed in switch!</div>
    </div>
  </div>

  <div v-click class="callout callout-warn">
    <div><strong>Key Keywords:</strong><br>• <code>case</code>: Constant matching label.<br>• <code>break</code>: Terminates switch execution.<br>• <code>default</code>: Catches all unhandled cases.</div>
  </div>
</div>

</div>
  </template>
</Slide2>
