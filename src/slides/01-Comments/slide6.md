---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 6 — SUMMARY
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Comments">
  <template #content>

<div class="slide-h1" style="margin-bottom:10px;">Summary — Java <span class="highlight">Comments</span></div>

<div class="g2" style="gap:14px;align-items:start;">

<div class="flex-col">

  <div v-click class="section-label">What We Covered</div>

  <div style="display:flex;flex-direction:column;gap:5px;">
    <div v-click style="display:flex;gap:8px;align-items:center;" class="card">
      <span class="pill pill-green" style="flex-shrink:0;">Single-line</span>
      <span style="font-size:.7rem;color:var(--slate);"><span class="mono">// text</span> — inline notes, quick annotations</span>
    </div>
    <div v-click style="display:flex;gap:8px;align-items:center;" class="card">
      <span class="pill pill-blue" style="flex-shrink:0;">Multi-line</span>
      <span style="font-size:.7rem;color:var(--slate);"><span class="mono">/* text */</span> — longer explanations, must close with <span class="mono">*/</span></span>
    </div>
    <div v-click style="display:flex;gap:8px;align-items:center;" class="card">
      <span class="pill pill-orange" style="flex-shrink:0;">Javadoc</span>
      <span style="font-size:.7rem;color:var(--slate);"><span class="mono">/** text */</span> — API documentation with <span class="mono">@param</span>, <span class="mono">@return</span>, <span class="mono">@author</span></span>
    </div>
    <div v-click style="display:flex;gap:8px;align-items:center;" class="card">
      <span class="pill pill-navy" style="flex-shrink:0;">Best Practice</span>
      <span style="font-size:.7rem;color:var(--slate);">Comment the "why", not the "what" — keep comments concise and current</span>
    </div>
  </div>

</div>

<div class="flex-col">

  <div v-click class="section-label">Key Exam Takeaways</div>

  <div style="display:flex;flex-direction:column;gap:5px;">
    <div v-click class="callout callout-info">
      <div>Comments are <strong>not executed</strong> — they are completely removed by the compiler before generating bytecode.</div>
    </div>
    <div v-click class="callout callout-danger">
      <div>An <strong>unclosed</strong> <span class="mono">/*</span> silently comments out all code below it, causing confusing compile errors.</div>
    </div>
    <div v-click class="callout callout-warn">
      <div>Multi-line comments <strong>cannot be nested</strong> — the first <span class="mono">*/</span> closes the comment regardless of depth.</div>
    </div>
    <div v-click class="callout callout-success">
      <div>Javadoc tags (<span class="mono">@param</span>, <span class="mono">@return</span>, <span class="mono">@author</span>) are only meaningful inside <span class="mono">/** */</span> comments — they are treated as plain text in <span class="mono">/* */</span>.</div>
    </div>
  </div>

  <div v-click class="card-navy" style="margin-top:6px;border-radius:10px;">
    <div style="font-size:.78rem;line-height:1.5;color:var(--slate);">
      <strong style="color:var(--red);">Mastering Java Comments:</strong> Well-commented code is a hallmark of a professional developer. Comments don't make you look unsure — they make your code <em>understandable</em> and <em>maintainable</em>. ☕
    </div>
  </div>

</div>

</div>

  </template>
</Slide2>
