---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 3 — PARAMETERS VS ARGUMENTS
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Java Methods">
  <template #content>

<div class="slide-h1" style="margin-bottom:10px;">Calling Methods — <span class="highlight">Parameters vs Arguments</span></div>

<div class="g2" style="gap:14px;align-items:start;">

<div class="flex-col">

  <div v-click class="card-navy" style="border-radius:10px;">
    <div style="font-size:.82rem;line-height:1.6;color:var(--slate);">
      <strong style="color:var(--blue);">Parameters</strong> are variables declared in the method definition header; <strong style="color:var(--green);">arguments</strong> are the actual values passed to the method when it is invoked.
    </div>
  </div>

  <div style="margin-top:6px;">
    <table class="cmp-table" style="font-size:.7rem;">
      <thead v-click><tr><th>Feature</th><th>Parameters</th><th>Arguments</th></tr></thead>
      <tbody>
        <tr v-click><td>Location</td><td>In method <strong>definition</strong></td><td>In method <strong>call (caller)</strong></td></tr>
        <tr v-click><td>Nature</td><td>Variable declaration (<span class="mono">int a</span>)</td><td>Actual value / expression (<span class="mono">10</span>, <span class="mono">x + 5</span>)</td></tr>
        <tr v-click><td>Scope</td><td>Local to method body</td><td>Belongs to calling context</td></tr>
        <tr v-click><td>Example</td><td class="mono" style="color:var(--blue);">void printSum(int x, int y)</td><td class="mono" style="color:var(--green);">printSum(10, 20);</td></tr>
      </tbody>
    </table>
  </div>

  <div v-click class="callout callout-warn" style="margin-top:6px;">
    <div><strong>Order &amp; Type Match:</strong> Java maps arguments to parameters <strong>strictly left-to-right by position</strong>. The data types must be compatible, or compilation fails.</div>
  </div>

</div>

<div class="flex-col">
  <div v-click class="section-label">Caller-to-Method Visual Mapping</div>

  <div v-after style="background:#f7f8fc;border:1px solid var(--border);border-radius:10px;padding:12px;font-family:'Fira Code',monospace;font-size:.68rem;line-height:1.8;">
    <div style="color:var(--navy);font-weight:700;margin-bottom:4px;">// 1. Caller in main():</div>
    <div style="background:#f0fff4;border:1px solid var(--green);padding:6px 10px;border-radius:6px;">
      <span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">result</span> = <span style="color:#0e6ead;font-weight:700;">multiply</span>(<span style="color:#22c55e;font-weight:700;">5</span>, <span style="color:#3b82f6;font-weight:700;">8</span>); <span style="color:#64748b;">// Arguments</span>
    </div>
    <div style="text-align:center;color:var(--red);font-weight:700;margin:6px 0;">
      │ &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;│<br>
      ▼ 5 binds to x &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;▼ 8 binds to y
    </div>
    <div style="color:var(--navy);font-weight:700;margin-bottom:4px;">// 2. Method Definition:</div>
    <div style="background:#ebf8ff;border:1px solid var(--blue);padding:6px 10px;border-radius:6px;">
      <span style="color:#ef5050;">public static int</span> <span style="color:#0e6ead;font-weight:700;">multiply</span>(<span style="color:#22c55e;font-weight:700;">int x</span>, <span style="color:#3b82f6;font-weight:700;">int y</span>) {<br>
      &nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#ef5050;">return</span> x * y; <span style="color:#64748b;">// returns 40</span><br>
      }
    </div>
  </div>

  <div v-click class="callout callout-info" style="margin-top:6px;">
    <div><strong>Argument Expressions:</strong> Arguments can be literals (<span class="mono">5</span>), variables (<span class="mono">a</span>), or complex expressions (<span class="mono">Math.sqrt(16) + 1</span>) evaluated before the method call.</div>
  </div>

</div>

</div>

  </template>
</Slide2>
