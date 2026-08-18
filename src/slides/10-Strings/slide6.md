---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 6 — STRING INDEXING & charAt()
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Java Strings">
  <template #content>

<div class="slide-h1" style="margin-bottom:10px;">String <span class="highlight">Indexing</span> &amp; charAt()</div>

<div class="g2" style="gap:14px;align-items:start;">

<div class="flex-col">

  <div v-click class="card-navy" style="border-radius:10px;">
    <div style="font-size:.82rem;line-height:1.6;color:var(--slate);">
      Java assigns an <strong>index number</strong> to every character in a String, starting at <strong>0</strong>. Use <span class="mono">charAt(index)</span> to retrieve a single character. Unlike Python, Java strings do not support negative indexing.
    </div>
  </div>

  <div v-click style="background:#f6f8fa;border-radius:10px;border:1px solid #e1e4e8;padding:12px;font-family:'Fira Code',monospace;font-size:.68rem;margin-top:6px;">
    <div style="margin-bottom:6px;color:var(--slate);text-align:center;font-weight:600;">"J a v a"</div>
    <div style="display:grid;grid-template-columns:repeat(4,1fr);gap:4px;text-align:center;">
      <div v-click style="background:var(--white);border:1px solid var(--green);border-radius:5px;padding:5px 2px;font-weight:600;color:var(--navy);">J</div>
      <div v-after style="background:var(--white);border:1px solid var(--green);border-radius:5px;padding:5px 2px;font-weight:600;color:var(--navy);">a</div>
      <div v-after style="background:var(--white);border:1px solid var(--green);border-radius:5px;padding:5px 2px;font-weight:600;color:var(--navy);">v</div>
      <div v-after style="background:var(--white);border:1px solid var(--green);border-radius:5px;padding:5px 2px;font-weight:600;color:var(--navy);">a</div>
      <div style="font-size:.6rem;color:var(--blue);font-weight:600;">0</div>
      <div style="font-size:.6rem;color:var(--blue);font-weight:600;">1</div>
      <div style="font-size:.6rem;color:var(--blue);font-weight:600;">2</div>
      <div style="font-size:.6rem;color:var(--blue);font-weight:600;">3</div>
    </div>
    <div style="color:var(--blue);font-size:.62rem;text-align:center;margin-top:4px;">← Indices (0 to length-1) →</div>
  </div>

  <div v-click class="code-block" style="margin-top:6px;">
    <span style="color:#ef5050;">String</span> <span style="color:#0e6ead;">s</span> = <span style="color:#2d7a00;">"Java"</span>;<br>
    <span style="color:#0e6ead;">System</span>.<span style="color:#0e6ead;">out</span>.<span style="color:#2d7a00;">println</span>(<span style="color:#0e6ead;">s</span>.<span style="color:#2d7a00;">charAt</span>(<span style="color:#b45309;">0</span>));  <span style="color:#6b7280;">// J</span><br>
    <span style="color:#0e6ead;">System</span>.<span style="color:#0e6ead;">out</span>.<span style="color:#2d7a00;">println</span>(<span style="color:#0e6ead;">s</span>.<span style="color:#2d7a00;">charAt</span>(<span style="color:#b45309;">3</span>));  <span style="color:#6b7280;">// a</span><br>
    <span style="color:#6b7280;">// Last character — Java way (no negative index)</span><br>
    <span style="color:#ef5050;">char</span> <span style="color:#0e6ead;">last</span> = <span style="color:#0e6ead;">s</span>.<span style="color:#2d7a00;">charAt</span>(<span style="color:#0e6ead;">s</span>.<span style="color:#2d7a00;">length</span>() - <span style="color:#b45309;">1</span>);<br>
    <span style="color:#0e6ead;">System</span>.<span style="color:#0e6ead;">out</span>.<span style="color:#2d7a00;">println</span>(<span style="color:#0e6ead;">last</span>); <span style="color:#6b7280;">// a</span>
  </div>

  <div v-click class="callout callout-warn">
    <div><strong>Key rule:</strong> For a string of length <span class="mono">n</span>, valid indices are <span class="mono">0</span> to <span class="mono">n-1</span>. Accessing index <span class="mono">n</span> or beyond throws <span class="mono">StringIndexOutOfBoundsException</span>.</div>
  </div>

</div>

<div class="flex-col">
  <div v-click class="section-label">Iterating Over Characters</div>

  <div v-after class="code-block">
    <span style="color:#ef5050;">String</span> <span style="color:#0e6ead;">word</span> = <span style="color:#2d7a00;">"Hello"</span>;<br>
    <br>
    <span style="color:#6b7280;">// Method 1 — using index loop</span><br>
    <span style="color:#ef5050;">for</span> (<span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">i</span> = <span style="color:#b45309;">0</span>; <span style="color:#0e6ead;">i</span> &lt; <span style="color:#0e6ead;">word</span>.<span style="color:#2d7a00;">length</span>(); <span style="color:#0e6ead;">i</span>++) {<br>
    <span style="padding-left:20px;display:block;"><span style="color:#0e6ead;">System</span>.<span style="color:#0e6ead;">out</span>.<span style="color:#2d7a00;">print</span>(<span style="color:#0e6ead;">word</span>.<span style="color:#2d7a00;">charAt</span>(<span style="color:#0e6ead;">i</span>) + <span style="color:#2d7a00;">" "</span>);</span>
    }<br>
    <span style="color:#6b7280;">// H e l l o</span><br>
    <br>
    <span style="color:#6b7280;">// Method 2 — enhanced for loop (via toCharArray)</span><br>
    <span style="color:#ef5050;">for</span> (<span style="color:#ef5050;">char</span> <span style="color:#0e6ead;">ch</span> : <span style="color:#0e6ead;">word</span>.<span style="color:#2d7a00;">toCharArray</span>()) {<br>
    <span style="padding-left:20px;display:block;"><span style="color:#0e6ead;">System</span>.<span style="color:#0e6ead;">out</span>.<span style="color:#2d7a00;">print</span>(<span style="color:#0e6ead;">ch</span> + <span style="color:#2d7a00;">" "</span>);</span>
    }
  </div>

  <div v-click class="section-label" style="margin-top:6px;">length() vs charAt()</div>
  <div v-after>
    <table class="cmp-table" style="font-size:.7rem;margin-bottom:40px;">
      <thead><tr><th>Method</th><th>Returns</th><th>Example</th></tr></thead>
      <tbody>
        <tr><td class="mono">length()</td><td class="yes">int — number of chars</td><td class="mono">"Java".length() → 4</td></tr>
        <tr><td class="mono">charAt(i)</td><td class="yes">char at index i</td><td class="mono">"Java".charAt(1) → 'a'</td></tr>
      </tbody>
    </table>
  </div>

</div>

</div>

  </template>
</Slide2>
