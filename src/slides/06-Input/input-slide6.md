---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 6 — SCANNER vs BUFFEREDREADER
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Input Methods">
  <template #content>

<div class="slide-h1" style="margin-bottom:10px;"><span class="highlight">Scanner</span> vs <span class="highlight">BufferedReader</span></div>

<div class="g2" style="gap:14px;">

<div class="flex-col">

  <div v-click class="card-navy" style="border-radius:10px;">
    <div style="font-size:.8rem;line-height:1.6;color:var(--slate);">
      <strong style="color:var(--red);">Definition:</strong> Both classes read input, but they trade off <strong>convenience</strong> against <strong>performance</strong> and <strong>type-safety</strong> against <strong>flexibility</strong>.
    </div>
  </div>

  <div>
    <table class="cmp-table" style="font-size:.7rem;margin-top:6px;">
      <thead v-click><tr><th>Feature</th><th>Scanner</th><th>BufferedReader</th></tr></thead>
      <tbody>
        <tr v-click><td>Package</td><td class="mono">java.util</td><td class="mono">java.io</td></tr>
        <tr v-click><td>Return types</td><td>int, double, String, …</td><td><span class="mono">String</span> only</td></tr>
        <tr v-click><td>Speed</td><td class="no">Slower</td><td class="yes">Faster</td></tr>
        <tr v-click><td>Parsing needed</td><td class="yes">Built-in</td><td class="no">Manual</td></tr>
        <tr v-click><td>Exception handling</td><td>Unchecked</td><td class="mono">throws IOException</td></tr>
        <tr v-click><td>Best for</td><td>Small programs, learning</td><td>Large / competitive input</td></tr>
      </tbody>
    </table>
  </div>

</div>

<div class="flex-col">
  <div v-click class="section-label">Which Should You Use?</div>

  <div v-after class="callout callout-info" style="margin-bottom:2px;">
    <div><strong>Use <span class="mono">Scanner</span></strong> when you want simple, readable code and need to read mixed types (ints, doubles, words) without manual conversion.</div>
  </div>

  <div v-click class="callout callout-success">
    <div><strong>Use <span class="mono">BufferedReader</span></strong> when performance matters — e.g. reading thousands of lines, or in competitive programming with tight time limits.</div>
  </div>

  <div v-click class="card card-orange" style="margin-top:6px;">
    <div class="small-text"><strong>Remember:</strong> <span class="mono">Scanner</span>'s parsing convenience comes at the cost of speed — internally it does more work per token than <span class="mono">BufferedReader</span>'s raw line reads.</div>
  </div>

</div>

</div>

  </template>
</Slide2>
