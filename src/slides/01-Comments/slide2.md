---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 2 — SINGLE-LINE & MULTI-LINE COMMENTS
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Comments">
  <template #content>

<div class="slide-h1" style="margin-bottom:10px;"><span class="highlight">Single-Line</span> &amp; <span class="highlight">Multi-Line</span> Comments</div>

<div class="g2" style="gap:14px;">

<div class="flex-col">

  <div v-click class="card-navy" style="border-radius:10px;">
    <div style="font-size:.82rem;line-height:1.6;color:var(--slate);">
      <strong style="color:var(--red);">Single-line comment:</strong> Starts with <span class="mono" style="color:var(--green);">//</span> — everything after <span class="mono">//</span> on that line is ignored by the compiler. Used for short, inline notes.
    </div>
  </div>

  <div v-click class="section-label">Single-Line — Examples</div>
  <div v-after style="background:#f6f8fa;border-radius:10px;border:1px solid #e1e4e8;padding:14px;font-family:'Fira Code',monospace;font-size:.74rem;line-height:2;">
    <span style="color:#6b7280;">// Calculate the area of a circle</span><br>
    <span style="color:#ef5050;">double</span> <span style="color:#0e6ead;">area</span> = <span style="color:#b45309;">3.14159</span> * <span style="color:#0e6ead;">radius</span> * <span style="color:#0e6ead;">radius</span>;<br>
    <br>
    <span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">age</span> = <span style="color:#b45309;">20</span>; <span style="color:#6b7280;">// user's current age</span><br>
    <br>
    <span style="color:#6b7280;">// TODO: validate input before processing</span><br>
    <span style="color:#0e6ead;">System</span>.<span style="color:#0e6ead;">out</span>.<span style="color:#2d7a00;">println</span>(<span style="color:#0e6ead;">age</span>);
  </div>

  <div v-click class="callout callout-info" style="margin-top:4px;">
    <div><span class="mono">//</span> can appear at the start of a line (standalone comment) or after code on the same line (inline comment). Both are valid and widely used.</div>
  </div>

</div>

<div class="flex-col">

  <div v-click class="card-navy" style="border-radius:10px;">
    <div style="font-size:.82rem;line-height:1.6;color:var(--slate);">
      <strong style="color:var(--red);">Multi-line comment:</strong> Starts with <span class="mono" style="color:var(--blue);">/*</span> and ends with <span class="mono" style="color:var(--blue);">*/</span>. Everything between these markers is ignored. Used for longer explanations spanning multiple lines.
    </div>
  </div>

  <div v-click class="section-label">Multi-Line — Example</div>
  <div v-after style="background:#f6f8fa;border-radius:10px;border:1px solid #e1e4e8;padding:14px;font-family:'Fira Code',monospace;font-size:.74rem;line-height:2;">
    <span style="color:#6b7280;">/*</span><br>
    <span style="color:#6b7280;">&nbsp; This method calculates the final grade</span><br>
    <span style="color:#6b7280;">&nbsp; of a student based on their total marks.</span><br>
    <span style="color:#6b7280;">&nbsp; Formula: marks / totalMarks * 100</span><br>
    <span style="color:#6b7280;">*/</span><br>
    <span style="color:#ef5050;">double</span> <span style="color:#0e6ead;">grade</span> = (<span style="color:#0e6ead;">marks</span> / <span style="color:#0e6ead;">totalMarks</span>) * <span style="color:#b45309;">100</span>;
  </div>

  <div v-click class="callout callout-danger" style="margin-top:4px;">
    <div><strong>Must close the comment!</strong> Forgetting the closing <span class="mono">*/</span> causes the compiler to treat everything after <span class="mono">/*</span> as a comment — resulting in a compile error.</div>
  </div>

</div>

</div>

  </template>
</Slide2>
