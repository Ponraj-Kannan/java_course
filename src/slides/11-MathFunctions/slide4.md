---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 4 — ROUNDING: floor(), ceil(), round(), rint()
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Java Math Functions">
  <template #content>

<div class="slide-h1" style="margin-bottom:10px;">Rounding — <span class="highlight">floor()</span>, <span class="highlight">ceil()</span>, <span class="highlight">round()</span></div>

<div class="g2" style="gap:14px;align-items:start;">

<div class="flex-col">

  <div v-click class="card-navy" style="border-radius:10px;">
    <div style="font-size:.82rem;line-height:1.6;color:var(--slate);">
      Java's Math class provides four rounding strategies: <strong>always-down (floor)</strong>, <strong>always-up (ceiling)</strong>, <strong>nearest integer (round)</strong>, and <strong>nearest even integer (rint)</strong>.
    </div>
  </div>

  <div style="margin-top:6px;">
    <table class="cmp-table" style="font-size:.7rem;">
      <thead v-click><tr><th>Method</th><th>Rule</th><th>Returns</th></tr></thead>
      <tbody>
        <tr v-click><td class="mono" style="color:var(--red-dark);font-weight:600;">Math.floor(x)</td><td>Round down to nearest integer ≤ x</td><td class="mono">double</td></tr>
        <tr v-click><td class="mono" style="color:var(--red-dark);font-weight:600;">Math.ceil(x)</td><td>Round up to nearest integer ≥ x</td><td class="mono">double</td></tr>
        <tr v-click><td class="mono" style="color:var(--red-dark);font-weight:600;">Math.round(x)</td><td>Round to nearest integer (0.5 rounds up)</td><td class="mono">long (if double), int (if float)</td></tr>
        <tr v-click><td class="mono" style="color:var(--red-dark);font-weight:600;">Math.rint(x)</td><td>Round to nearest, ties → nearest even</td><td class="mono">double</td></tr>
      </tbody>
    </table>
  </div>

  <div v-click class="callout callout-info" style="margin-top:6px;">
    <div><strong>floor vs round for negatives:</strong> <span class="mono">Math.floor(-2.3)</span> → <span class="mono">-3.0</span> (goes further from zero); <span class="mono">Math.round(-2.3)</span> → <span class="mono">-2</span> (rounds towards zero).</div>
  </div>

</div>

<div class="flex-col">
  <div v-click class="section-label">Code Examples — Visual Number Line</div>

  <div v-after style="background:#f7f8fc;border:1px solid var(--border);border-radius:8px;padding:10px 12px;font-size:.70rem;margin-bottom:8px;">
    <div style="font-weight:700;color:var(--navy);margin-bottom:6px;">For value: 3.5</div>
    <div style="display:flex;align-items:center;gap:8px;font-family:'Fira Code',monospace;font-size:.64rem;">
      <span style="background:#f0fff4;border:1px solid var(--green);padding:2px 6px;border-radius:4px;">floor → 3.0</span>
      <span style="background:#ebf8ff;border:1px solid var(--blue);padding:2px 6px;border-radius:4px;">ceil → 4.0</span>
      <span style="background:#fdf2f8;border:1px solid #ec4899;padding:2px 6px;border-radius:4px;">round → 4</span>
    </div>
    <div style="font-weight:700;color:var(--navy);margin:8px 0 4px;">For value: -2.7</div>
    <div style="display:flex;align-items:center;gap:8px;font-family:'Fira Code',monospace;font-size:.64rem;">
      <span style="background:#f0fff4;border:1px solid var(--green);padding:2px 6px;border-radius:4px;">floor → -3.0</span>
      <span style="background:#ebf8ff;border:1px solid var(--blue);padding:2px 6px;border-radius:4px;">ceil → -2.0</span>
      <span style="background:#fdf2f8;border:1px solid #ec4899;padding:2px 6px;border-radius:4px;">round → -3</span>
    </div>
  </div>

  <div v-click class="code-block" style="font-size:.70rem;line-height:1.9;">
    <span style="color:#0e6ead;">Math</span>.<span style="color:#2d7a00;">floor</span>(<span style="color:#b45309;">4.9</span>);   <span style="color:#2d7a00;">// 4.0</span><br>
    <span style="color:#0e6ead;">Math</span>.<span style="color:#2d7a00;">ceil</span>(<span style="color:#b45309;">4.1</span>);    <span style="color:#2d7a00;">// 5.0</span><br>
    <span style="color:#0e6ead;">Math</span>.<span style="color:#2d7a00;">round</span>(<span style="color:#b45309;">4.5</span>);   <span style="color:#2d7a00;">// 5 (long)</span><br>
    <span style="color:#0e6ead;">Math</span>.<span style="color:#2d7a00;">round</span>(<span style="color:#b45309;">4.4</span>);   <span style="color:#2d7a00;">// 4 (long)</span><br>
    <span style="color:#0e6ead;">Math</span>.<span style="color:#2d7a00;">rint</span>(<span style="color:#b45309;">2.5</span>);    <span style="color:#2d7a00;">// 2.0 (nearest even: 2 not 3)</span><br>
    <span style="color:#0e6ead;">Math</span>.<span style="color:#2d7a00;">rint</span>(<span style="color:#b45309;">3.5</span>);    <span style="color:#2d7a00;">// 4.0 (nearest even: 4 not 3)</span>
  </div>

</div>

</div>

  </template>
</Slide2>
