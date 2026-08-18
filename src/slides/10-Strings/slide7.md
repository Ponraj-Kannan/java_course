---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 7 — COMMON STRING METHODS (PART 1)
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Java Strings">
  <template #content>

<div class="slide-h1" style="margin-bottom:10px;">String <span class="highlight">Methods</span> — Search &amp; Extract</div>

<div class="g2" style="gap:14px;align-items:start;">

<div class="flex-col">

  <div v-click class="card-navy" style="border-radius:10px;">
    <div style="font-size:.8rem;line-height:1.6;color:var(--slate);">
      String <strong style="color:var(--red);">methods</strong> are called on a String object using the dot notation: <span class="mono">string.method(args)</span>. Since strings are <strong>immutable</strong>, methods always <strong>return a new String</strong> — they never modify the original.
    </div>
  </div>

  <div style="margin-top:6px;">
    <table class="cmp-table" style="font-size:.7rem;">
      <thead v-click><tr><th>Method</th><th>Description</th><th>Example → Output</th></tr></thead>
      <tbody>
        <tr v-click><td class="mono" style="color:var(--red-dark);font-weight:600;">length()</td><td>Number of characters</td><td class="mono">"hello".length() → 5</td></tr>
        <tr v-click><td class="mono" style="color:var(--red-dark);font-weight:600;">charAt(i)</td><td>Char at index i</td><td class="mono">"Java".charAt(0) → 'J'</td></tr>
        <tr v-click><td class="mono" style="color:var(--red-dark);font-weight:600;">indexOf(s)</td><td>First index of substring</td><td class="mono">"abcabc".indexOf("b") → 1</td></tr>
        <tr v-click><td class="mono" style="color:var(--red-dark);font-weight:600;">lastIndexOf(s)</td><td>Last index of substring</td><td class="mono">"abcabc".lastIndexOf("b") → 4</td></tr>
        <tr v-click><td class="mono" style="color:var(--red-dark);font-weight:600;">contains(s)</td><td>Is substring present?</td><td class="mono">"hello".contains("ell") → true</td></tr>
        <tr v-click><td class="mono" style="color:var(--red-dark);font-weight:600;">startsWith(s)</td><td>Starts with prefix?</td><td class="mono">"Java".startsWith("Ja") → true</td></tr>
        <tr v-click><td class="mono" style="color:var(--red-dark);font-weight:600;">endsWith(s)</td><td>Ends with suffix?</td><td class="mono">"file.java".endsWith(".java") → true</td></tr>
        <tr v-click><td class="mono" style="color:var(--red-dark);font-weight:600;">isEmpty()</td><td>Is string empty?</td><td class="mono">"".isEmpty() → true</td></tr>
        <tr v-click><td class="mono" style="color:var(--red-dark);font-weight:600;">isBlank()</td><td>Empty or only whitespace?</td><td class="mono">"  ".isBlank() → true</td></tr>
      </tbody>
    </table>
  </div>

</div>

<div class="flex-col">
  <div v-click class="section-label">Code Examples</div>

  <div v-after class="code-block" style="font-size:.72rem;line-height:1.9;">
    <span style="color:#ef5050;">String</span> <span style="color:#0e6ead;">s</span> = <span style="color:#2d7a00;">"Hello, World!"</span>;<br>
    <br>
    <span style="color:#0e6ead;">System</span>.<span style="color:#0e6ead;">out</span>.<span style="color:#2d7a00;">println</span>(<span style="color:#0e6ead;">s</span>.<span style="color:#2d7a00;">length</span>());       <span style="color:#6b7280;">// 13</span><br>
    <span style="color:#0e6ead;">System</span>.<span style="color:#0e6ead;">out</span>.<span style="color:#2d7a00;">println</span>(<span style="color:#0e6ead;">s</span>.<span style="color:#2d7a00;">indexOf</span>(<span style="color:#2d7a00;">"World"</span>));<span style="color:#6b7280;">// 7</span><br>
    <span style="color:#0e6ead;">System</span>.<span style="color:#0e6ead;">out</span>.<span style="color:#2d7a00;">println</span>(<span style="color:#0e6ead;">s</span>.<span style="color:#2d7a00;">contains</span>(<span style="color:#2d7a00;">"lo"</span>));   <span style="color:#6b7280;">// true</span><br>
    <span style="color:#0e6ead;">System</span>.<span style="color:#0e6ead;">out</span>.<span style="color:#2d7a00;">println</span>(<span style="color:#0e6ead;">s</span>.<span style="color:#2d7a00;">startsWith</span>(<span style="color:#2d7a00;">"He"</span>));<span style="color:#6b7280;">// true</span><br>
    <span style="color:#0e6ead;">System</span>.<span style="color:#0e6ead;">out</span>.<span style="color:#2d7a00;">println</span>(<span style="color:#0e6ead;">s</span>.<span style="color:#2d7a00;">endsWith</span>(<span style="color:#2d7a00;">"!"</span>));  <span style="color:#6b7280;">// true</span>
  </div>

  <div v-click class="section-label" style="margin-top:8px;">substring() — Extract a Part</div>

  <div v-after class="code-block" style="font-size:.72rem;line-height:1.9;">
    <span style="color:#ef5050;">String</span> <span style="color:#0e6ead;">s</span> = <span style="color:#2d7a00;">"Hello, World!"</span>;<br>
    <span style="color:#6b7280;">// substring(start) — from start to end</span><br>
    <span style="color:#0e6ead;">System</span>.<span style="color:#0e6ead;">out</span>.<span style="color:#2d7a00;">println</span>(<span style="color:#0e6ead;">s</span>.<span style="color:#2d7a00;">substring</span>(<span style="color:#b45309;">7</span>));      <span style="color:#6b7280;">// "World!"</span><br>
    <span style="color:#6b7280;">// substring(start, end) — start inclusive, end exclusive</span><br>
    <span style="color:#0e6ead;">System</span>.<span style="color:#0e6ead;">out</span>.<span style="color:#2d7a00;">println</span>(<span style="color:#0e6ead;">s</span>.<span style="color:#2d7a00;">substring</span>(<span style="color:#b45309;">0</span>, <span style="color:#b45309;">5</span>)); <span style="color:#6b7280;">// "Hello"</span>
  </div>

  <div v-click class="callout callout-info" style="margin-top:4px;margin-bottom:40px;">
    <div><strong>Note:</strong> <span class="mono">substring(start, end)</span> — the <strong>end index is exclusive</strong> (like Python slicing). So <span class="mono">substring(0,5)</span> gives characters at indices 0,1,2,3,4.</div>
  </div>

</div>

</div>

  </template>
</Slide2>
