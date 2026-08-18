---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 8 — COMMON STRING METHODS (PART 2)
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Java Strings">
  <template #content>

<div class="slide-h1" style="margin-bottom:10px;">String <span class="highlight">Methods</span> — Modify &amp; Transform</div>

<div class="g2" style="gap:14px;align-items:start;">

<div class="flex-col">

  <div style="margin-top:2px;">
    <table class="cmp-table" style="font-size:.7rem;">
      <thead v-click><tr><th>Method</th><th>Description</th><th>Example → Output</th></tr></thead>
      <tbody>
        <tr v-click><td class="mono" style="color:var(--red-dark);font-weight:600;">toUpperCase()</td><td>ALL UPPERCASE</td><td class="mono">"hello".toUpperCase() → "HELLO"</td></tr>
        <tr v-click><td class="mono" style="color:var(--red-dark);font-weight:600;">toLowerCase()</td><td>all lowercase</td><td class="mono">"HELLO".toLowerCase() → "hello"</td></tr>
        <tr v-click><td class="mono" style="color:var(--red-dark);font-weight:600;">trim()</td><td>Remove leading/trailing spaces</td><td class="mono">"  hi  ".trim() → "hi"</td></tr>
        <tr v-click><td class="mono" style="color:var(--red-dark);font-weight:600;">strip()</td><td>Like trim() but Unicode-aware</td><td class="mono">"  hi  ".strip() → "hi"</td></tr>
        <tr v-click><td class="mono" style="color:var(--red-dark);font-weight:600;">replace(a,b)</td><td>Replace all occurrences of a with b</td><td class="mono">"aabbcc".replace("a","x") → "xxbbcc"</td></tr>
        <tr v-click><td class="mono" style="color:var(--red-dark);font-weight:600;">split(delim)</td><td>Split into String array</td><td class="mono">"a,b,c".split(",") → ["a","b","c"]</td></tr>
        <tr v-click><td class="mono" style="color:var(--red-dark);font-weight:600;">concat(s)</td><td>Append string (same as +)</td><td class="mono">"Hi".concat("!") → "Hi!"</td></tr>
        <tr v-click><td class="mono" style="color:var(--red-dark);font-weight:600;">repeat(n)</td><td>Repeat string n times (Java 11+)</td><td class="mono">"ab".repeat(3) → "ababab"</td></tr>
        <tr v-click><td class="mono" style="color:var(--red-dark);font-weight:600;">valueOf(x)</td><td>Convert other types to String</td><td class="mono">String.valueOf(42) → "42"</td></tr>
      </tbody>
    </table>
  </div>

</div>

<div class="flex-col">
  <div v-click class="section-label">Code Examples</div>

  <div v-after class="code-block" style="font-size:.72rem;line-height:1.9;">
    <span style="color:#ef5050;">String</span> <span style="color:#0e6ead;">s</span> = <span style="color:#2d7a00;">"  Hello, World!  "</span>;<br>
    <span style="color:#0e6ead;">System</span>.<span style="color:#0e6ead;">out</span>.<span style="color:#2d7a00;">println</span>(<span style="color:#0e6ead;">s</span>.<span style="color:#2d7a00;">toUpperCase</span>()); <span style="color:#6b7280;">// "  HELLO, WORLD!  "</span><br>
    <span style="color:#0e6ead;">System</span>.<span style="color:#0e6ead;">out</span>.<span style="color:#2d7a00;">println</span>(<span style="color:#0e6ead;">s</span>.<span style="color:#2d7a00;">strip</span>());      <span style="color:#6b7280;">// "Hello, World!"</span><br>
    <span style="color:#0e6ead;">System</span>.<span style="color:#0e6ead;">out</span>.<span style="color:#2d7a00;">println</span>(<span style="color:#0e6ead;">s</span>.<span style="color:#2d7a00;">replace</span>(<span style="color:#2d7a00;">"World"</span>, <span style="color:#2d7a00;">"Java"</span>));<br>
    <span style="color:#6b7280;">// "  Hello, Java!  "</span>
  </div>

  <div v-click class="section-label" style="margin-top:8px;">Chaining Methods</div>

  <div v-after class="code-block" style="font-size:.72rem;line-height:1.9;">
    <span style="color:#6b7280;">// Clean user input: strip + lowercase</span><br>
    <span style="color:#ef5050;">String</span> <span style="color:#0e6ead;">input</span> = <span style="color:#2d7a00;">"  ALICE  "</span>;<br>
    <span style="color:#ef5050;">String</span> <span style="color:#0e6ead;">clean</span> = <span style="color:#0e6ead;">input</span>.<span style="color:#2d7a00;">strip</span>().<span style="color:#2d7a00;">toLowerCase</span>();<br>
    <span style="color:#0e6ead;">System</span>.<span style="color:#0e6ead;">out</span>.<span style="color:#2d7a00;">println</span>(<span style="color:#0e6ead;">clean</span>); <span style="color:#6b7280;">// "alice"</span><br>
    <br>
    <span style="color:#6b7280;">// split() with loop</span><br>
    <span style="color:#ef5050;">String</span>[] <span style="color:#0e6ead;">parts</span> = <span style="color:#2d7a00;">"a,b,c"</span>.<span style="color:#2d7a00;">split</span>(<span style="color:#2d7a00;">","</span>);<br>
    <span style="color:#ef5050;">for</span> (<span style="color:#ef5050;">String</span> <span style="color:#0e6ead;">p</span> : <span style="color:#0e6ead;">parts</span>) <span style="color:#0e6ead;">System</span>.<span style="color:#0e6ead;">out</span>.<span style="color:#2d7a00;">print</span>(<span style="color:#0e6ead;">p</span> + <span style="color:#2d7a00;">" "</span>);
    <span style="color:#6b7280;">// a b c</span>
  </div>

  <div v-click class="callout callout-info" style="margin-top:4px;margin-bottom:40px;">
    <div><strong>Real-world:</strong> Use <span class="mono">.strip().toLowerCase()</span> when comparing user input to avoid mismatches from accidental spaces or case differences.</div>
  </div>

</div>

</div>

  </template>
</Slide2>
