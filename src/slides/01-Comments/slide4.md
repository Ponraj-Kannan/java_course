---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 4 — GOOD vs BAD COMMENTING (Before/After)
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Comments">
  <template #content>

<div class="slide-h1" style="margin-bottom:10px;">Good Commenting <span class="highlight">Practices</span></div>

<div class="g2" style="gap:14px;align-items:start;">

<div class="flex-col">

  <div v-click class="card-navy" style="border-radius:10px;">
    <div style="font-size:.82rem;line-height:1.6;color:var(--slate);">
      <strong style="color:var(--red);">Golden Rule:</strong> Comment the <strong>"Why"</strong>, not the <strong>"What"</strong>. Code already shows <em>what</em> it does — a good comment explains <em>why</em> that decision was made, or warns about a non-obvious behaviour.
    </div>
  </div>

  <div v-click class="section-label">❌ Bad Comment — States the Obvious</div>
  <div v-after style="background:var(--red-soft);border-radius:10px;border:1px solid var(--red);padding:14px;font-family:'Fira Code',monospace;font-size:.74rem;line-height:2;">
    <span style="color:#6b7280;">// Add 1 to count</span><br>
    <span style="color:#0e6ead;">count</span>++;<br>
    <br>
    <span style="color:#6b7280;">// Check if age is greater than 18</span><br>
    <span style="color:#ef5050;">if</span> (<span style="color:#0e6ead;">age</span> &gt; <span style="color:#b45309;">18</span>) { ... }
  </div>

</div>

<div class="flex-col">

  <div v-click class="section-label">✔ Good Comment — Explains Why</div>
  <div v-after style="background:#f0fff4;border-radius:10px;border:1px solid var(--green);padding:14px;font-family:'Fira Code',monospace;font-size:.74rem;line-height:2;">
    <span style="color:#6b7280;">// Start from index 1 to skip the header row</span><br>
    <span style="color:#ef5050;">for</span> (<span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">i</span> = <span style="color:#b45309;">1</span>; <span style="color:#0e6ead;">i</span> &lt; <span style="color:#0e6ead;">data</span>.<span style="color:#0e6ead;">length</span>; <span style="color:#0e6ead;">i</span>++) { ... }<br>
    <br>
    <span style="color:#6b7280;">// Using 18 as the legal voting age threshold (India)</span><br>
    <span style="color:#ef5050;">if</span> (<span style="color:#0e6ead;">age</span> &gt;= <span style="color:#b45309;">18</span>) { ... }
  </div>

  <div style="display:flex;flex-direction:column;gap:5px;margin-top:6px;">
    <div v-click class="section-label">Best Practices Summary</div>
    <div v-click class="card" style="padding:8px 14px;">
      <div class="body-text">✔ &nbsp;Explain <strong>intent and reasoning</strong>, not the syntax</div>
    </div>
    <div v-click class="card" style="padding:8px 14px;">
      <div class="body-text">✔ &nbsp;Keep comments <strong>updated</strong> when code changes — stale comments mislead</div>
    </div>
    <div v-click class="card" style="padding:8px 14px;">
      <div class="body-text">✔ &nbsp;Prefer <strong>clear, self-documenting variable/method names</strong> over excessive comments</div>
    </div>
  </div>

</div>

</div>

  </template>
</Slide2>
