---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 5 — Math.random() & GENERATING RANGES
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Java Math Functions">
  <template #content>

<div class="slide-h1" style="margin-bottom:10px;"><span class="highlight">Math.random()</span> &amp; Random Ranges</div>

<div class="g2" style="gap:14px;align-items:start;">

<div class="flex-col">

  <div v-click class="card-navy" style="border-radius:10px;">
    <div style="font-size:.82rem;line-height:1.6;color:var(--slate);">
      <span class="mono" style="color:var(--red);font-weight:700;">Math.random()</span> returns a <strong>pseudo-random <span class="mono">double</span></strong> in the range <strong>[0.0, 1.0)</strong> — inclusive of <span class="mono">0.0</span> but exclusive of <span class="mono">1.0</span>.
    </div>
  </div>

  <div v-click class="section-label" style="margin-top:6px;">Range Formula Derivation</div>

  <div style="display:flex;flex-direction:column;gap:6px;">
    <div v-click style="background:#f7f8fc;border:1px solid var(--border);border-radius:8px;padding:10px 12px;font-size:.70rem;">
      <div style="font-weight:700;color:var(--navy);margin-bottom:4px;">Random integer in range [min, max] inclusive:</div>
      <div style="font-family:'Fira Code',monospace;font-size:.76rem;background:#1e293b;color:#f8fafc;padding:8px 10px;border-radius:6px;">
        <span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">rand</span> = (<span style="color:#ef5050;">int</span>)(<span style="color:#0e6ead;">Math</span>.<span style="color:#2d7a00;">random</span>() * (max - min + <span style="color:#b45309;">1</span>)) + min;
      </div>
      <div style="font-size:.62rem;color:var(--slate);margin-top:6px;line-height:1.6;">
        Step 1: <span class="mono">Math.random()</span> gives [0.0, 1.0)<br>
        Step 2: Multiply by <span class="mono">(max - min + 1)</span> to scale to <span class="mono">(max - min + 1)</span> possible values<br>
        Step 3: Cast to <span class="mono">int</span> truncates to [0, max−min]<br>
        Step 4: Add <span class="mono">min</span> to shift into [min, max]
      </div>
    </div>
  </div>

  <div v-click class="callout callout-info" style="margin-top:6px;">
    <div><strong>For better control:</strong> Prefer <span class="mono">java.util.Random</span> or <span class="mono">java.util.concurrent.ThreadLocalRandom</span> when generating many random numbers in production code.</div>
  </div>

</div>

<div class="flex-col">
  <div v-click class="section-label">Practical Random Examples</div>

  <div v-after class="code-block" style="font-size:.70rem;line-height:1.9;">
    <span style="color:#6b7280;">// 1. Raw random double</span><br>
    <span style="color:#ef5050;">double</span> <span style="color:#0e6ead;">d</span> = <span style="color:#0e6ead;">Math</span>.<span style="color:#2d7a00;">random</span>();    <span style="color:#2d7a00;">// e.g. 0.7381...</span><br>
    <br>
    <span style="color:#6b7280;">// 2. Random 0 or 1 (coin flip)</span><br>
    <span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">coin</span> = (<span style="color:#ef5050;">int</span>)(<span style="color:#0e6ead;">Math</span>.<span style="color:#2d7a00;">random</span>() * <span style="color:#b45309;">2</span>); <span style="color:#2d7a00;">// 0 or 1</span><br>
    <br>
    <span style="color:#6b7280;">// 3. Random int in [1, 6] — dice roll</span><br>
    <span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">dice</span> = (<span style="color:#ef5050;">int</span>)(<span style="color:#0e6ead;">Math</span>.<span style="color:#2d7a00;">random</span>() * <span style="color:#b45309;">6</span>) + <span style="color:#b45309;">1</span>;<br>
    <br>
    <span style="color:#6b7280;">// 4. Random int in [50, 100]</span><br>
    <span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">score</span> = (<span style="color:#ef5050;">int</span>)(<span style="color:#0e6ead;">Math</span>.<span style="color:#2d7a00;">random</span>() * <span style="color:#b45309;">51</span>) + <span style="color:#b45309;">50</span>;<br>
    <br>
    <span style="color:#6b7280;">// 5. Random double in [0.0, 5.0)</span><br>
    <span style="color:#ef5050;">double</span> <span style="color:#0e6ead;">r</span> = <span style="color:#0e6ead;">Math</span>.<span style="color:#2d7a00;">random</span>() * <span style="color:#b45309;">5.0</span>;
  </div>

  <div v-click class="callout callout-warn" style="margin-top:6px;">
    <div><strong>Not truly random:</strong> <span class="mono">Math.random()</span> is pseudo-random (deterministic sequence). Do not use for cryptographic or security-sensitive purposes.</div>
  </div>

</div>

</div>

  </template>
</Slide2>
