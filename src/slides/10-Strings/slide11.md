---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 11 — STRING vs STRINGBUILDER COMPARISON
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Java Strings">
  <template #content>

<div class="slide-h1" style="margin-bottom:10px;"><span class="highlight">String</span> vs <span class="highlight">StringBuilder</span></div>

<div class="g2" style="gap:14px;align-items:start;">

<div class="flex-col">

  <div v-click class="g2" style="gap:8px;">
    <div class="card-red" style="text-align:center;">
      <div class="slide-h2" style="color:var(--red);">String</div>
      <div class="small-text" style="margin-top:4px;"><strong>Immutable</strong> — every modification creates a new object in memory.</div>
    </div>
    <div class="card-green" style="text-align:center;">
      <div class="slide-h2" style="color:var(--green);">StringBuilder</div>
      <div class="small-text" style="margin-top:4px;"><strong>Mutable</strong> — modifications happen in place on the same object.</div>
    </div>
  </div>

  <div style="margin-top:8px;">
    <table class="cmp-table" style="font-size:.7rem;">
      <thead v-click><tr><th>Feature</th><th>String</th><th>StringBuilder</th></tr></thead>
      <tbody>
        <tr v-click><td>Mutability</td><td class="no">Immutable</td><td class="yes">Mutable</td></tr>
        <tr v-click><td>Performance (loop)</td><td class="no">Slow — new object each time</td><td class="yes">Fast — modifies in place</td></tr>
        <tr v-click><td>Thread safety</td><td class="yes">Safe (immutable)</td><td class="no">Not thread-safe</td></tr>
        <tr v-click><td>Memory (loop)</td><td class="no">Many throwaway objects</td><td class="yes">Single object grows</td></tr>
        <tr v-click><td>Use for</td><td>Fixed/known strings</td><td>Dynamic string building</td></tr>
        <tr v-click><td>Common methods</td><td><span class="mono">.equals()</span>, <span class="mono">.substring()</span></td><td><span class="mono">.append()</span>, <span class="mono">.reverse()</span></td></tr>
        <tr v-click><td>Convert to other</td><td>—</td><td class="mono">.toString()</td></tr>
      </tbody>
    </table>
  </div>

</div>

<div class="flex-col">
  <div v-click class="section-label">Side-by-Side — Building a String in a Loop</div>

  <div v-after class="g2" style="gap:8px;">
    <div class="flex-col">
      <div class="section-label" style="color:var(--red);">Using String (Slow)</div>
      <div class="code-block" style="font-size:.66rem;line-height:1.8;">
        <span style="color:#ef5050;">String</span> <span style="color:#0e6ead;">r</span> = <span style="color:#2d7a00;">""</span>;<br>
        <span style="color:#ef5050;">for</span> (<span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">i</span>=<span style="color:#b45309;">1</span>; <span style="color:#0e6ead;">i</span>&lt;=<span style="color:#b45309;">5</span>; <span style="color:#0e6ead;">i</span>++)<br>
        <span style="padding-left:12px;display:block;background:#fff5f5;border-left:2px solid var(--red);"><span style="color:#0e6ead;">r</span> += <span style="color:#0e6ead;">i</span> + <span style="color:#2d7a00;">" "</span>;</span>
        <span style="color:#6b7280;">// 5 new String objects!</span>
      </div>
    </div>
    <div class="flex-col">
      <div class="section-label" style="color:var(--green);">Using StringBuilder (Fast)</div>
      <div class="code-block" style="font-size:.66rem;line-height:1.8;">
        <span style="color:#0e6ead;">StringBuilder</span> <span style="color:#0e6ead;">sb</span> =<br>
        <span style="padding-left:12px;display:block;"><span style="color:#ef5050;">new</span> <span style="color:#0e6ead;">StringBuilder</span>();</span>
        <span style="color:#ef5050;">for</span> (<span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">i</span>=<span style="color:#b45309;">1</span>; <span style="color:#0e6ead;">i</span>&lt;=<span style="color:#b45309;">5</span>; <span style="color:#0e6ead;">i</span>++)<br>
        <span style="padding-left:12px;display:block;background:#f0fff4;border-left:2px solid var(--green);"><span style="color:#0e6ead;">sb</span>.<span style="color:#2d7a00;">append</span>(<span style="color:#0e6ead;">i</span>+<span style="color:#2d7a00;">" "</span>);</span>
        <span style="color:#0e6ead;">sb</span>.<span style="color:#2d7a00;">toString</span>();
      </div>
    </div>
  </div>

  <div v-click class="callout callout-info" style="margin-top:8px;">
    <div><strong>When to use StringBuilder:</strong>
      <ul style="margin:4px 0 0 16px;font-size:.7rem;">
        <li>Building strings inside a loop</li>
        <li>Repeated append/insert/delete operations</li>
        <li>Reversing a string efficiently</li>
      </ul>
    </div>
  </div>

  <div v-click class="callout callout-warn" style="margin-top:4px;">
    <div><strong>Note:</strong> Java also has <span class="mono">StringBuffer</span> — it's thread-safe but slower. Prefer <span class="mono">StringBuilder</span> for single-threaded code.</div>
  </div>

</div>

</div>

  </template>
</Slide2>
