---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 12 — STRING FORMATTING
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Java Strings">
  <template #content>

<div class="slide-h1" style="margin-bottom:10px;">String <span class="highlight">Formatting</span></div>

<div class="g2" style="gap:14px;align-items:start;">

<div class="flex-col">

  <div v-click class="card-navy" style="border-radius:10px;">
    <div style="font-size:.82rem;line-height:1.6;color:var(--slate);">
      <strong style="color:var(--red);">String formatting</strong> lets you embed variable values inside a string cleanly. Java offers <span class="mono">String.format()</span> (printf-style) and, since Java 15, <strong>Text Blocks</strong> (triple-quoted strings for multiline content).
    </div>
  </div>

  <div v-click class="section-label" style="margin-top:8px;">Method 1 — String.format()</div>
  <div v-after class="code-block" style="font-size:.72rem;line-height:1.9;">
    <span style="color:#ef5050;">String</span> <span style="color:#0e6ead;">name</span> = <span style="color:#2d7a00;">"Alice"</span>; <span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">age</span> = <span style="color:#b45309;">25</span>;<br>
    <span style="color:#ef5050;">String</span> <span style="color:#0e6ead;">msg</span> = <span style="color:#0e6ead;">String</span>.<span style="color:#2d7a00;">format</span>(<span style="color:#2d7a00;">"Name: %s, Age: %d"</span>, <span style="color:#0e6ead;">name</span>, <span style="color:#0e6ead;">age</span>);<br>
    <span style="color:#0e6ead;">System</span>.<span style="color:#0e6ead;">out</span>.<span style="color:#2d7a00;">println</span>(<span style="color:#0e6ead;">msg</span>); <span style="color:#6b7280;">// Name: Alice, Age: 25</span><br>
    <br>
    <span style="color:#6b7280;">// Formatting numbers</span><br>
    <span style="color:#0e6ead;">System</span>.<span style="color:#0e6ead;">out</span>.<span style="color:#2d7a00;">printf</span>(<span style="color:#2d7a00;">"Pi = %.2f%n"</span>, <span style="color:#b45309;">3.14159</span>);<br>
    <span style="color:#6b7280;">// Pi = 3.14</span><br>
    <br>
    <span style="color:#6b7280;">// Padding and alignment</span><br>
    <span style="color:#0e6ead;">System</span>.<span style="color:#0e6ead;">out</span>.<span style="color:#2d7a00;">printf</span>(<span style="color:#2d7a00;">"%-10s | %5d%n"</span>, <span style="color:#2d7a00;">"Alice"</span>, <span style="color:#b45309;">25</span>);<br>
    <span style="color:#6b7280;">// Alice      |    25</span>
  </div>

  <div v-click class="section-label" style="margin-top:6px;">Format Specifiers Quick Reference</div>
  <div v-after>
    <table class="cmp-table" style="font-size:.7rem;">
      <thead><tr><th>Specifier</th><th>Type</th><th>Example</th></tr></thead>
      <tbody>
        <tr><td class="mono">%s</td><td>String</td><td class="mono">%s → "hello"</td></tr>
        <tr><td class="mono">%d</td><td>Integer</td><td class="mono">%d → 42</td></tr>
        <tr><td class="mono">%f</td><td>Float/Double</td><td class="mono">%.2f → 3.14</td></tr>
        <tr><td class="mono">%c</td><td>Character</td><td class="mono">%c → 'A'</td></tr>
        <tr><td class="mono">%b</td><td>Boolean</td><td class="mono">%b → true</td></tr>
        <tr><td class="mono">%n</td><td>Newline</td><td class="mono">%n → newline</td></tr>
      </tbody>
    </table>
  </div>

</div>

<div class="flex-col">
  <div v-click class="section-label">Method 2 — Text Blocks (Java 15+)</div>

  <div v-after class="card-navy" style="border-radius:10px;">
    <div style="font-size:.74rem;color:var(--slate);line-height:1.6;margin-bottom:6px;">
      <strong style="color:var(--green);">Text Blocks</strong> use triple double-quotes <span class="mono">"""</span> to write multi-line strings cleanly — no concatenation or <span class="mono">\n</span> needed. Java's equivalent of Python's triple-quoted strings.
    </div>
  </div>

  <div v-click class="code-block" style="font-size:.72rem;line-height:1.9;">
    <span style="color:#6b7280;">// Text Block — triple-quoted string</span><br>
    <span style="color:#ef5050;">String</span> <span style="color:#0e6ead;">json</span> = <span style="color:#2d7a00;">"""</span><br>
    <span style="padding-left:16px;display:block;color:#2d7a00;">{</span><br>
    <span style="padding-left:16px;display:block;color:#2d7a00;">&nbsp;&nbsp;"name": "Alice",</span><br>
    <span style="padding-left:16px;display:block;color:#2d7a00;">&nbsp;&nbsp;"age": 25</span><br>
    <span style="padding-left:16px;display:block;color:#2d7a00;">}</span><br>
    <span style="color:#2d7a00;">"""</span>;<br>
    <span style="color:#0e6ead;">System</span>.<span style="color:#0e6ead;">out</span>.<span style="color:#2d7a00;">println</span>(<span style="color:#0e6ead;">json</span>);
  </div>

  <div v-click style="margin-top:6px;">
    <table class="cmp-table" style="font-size:.7rem;margin-bottom:40px;">
      <thead><tr><th>Method</th><th>Java</th><th>Readability</th></tr></thead>
      <tbody>
        <tr><td class="mono">+</td><td>All versions</td><td>Low for multiline</td></tr>
        <tr><td class="mono">String.format()</td><td>All versions</td><td class="yes">Good for variables</td></tr>
        <tr><td class="mono" style="color:var(--green);font-weight:600;">Text Blocks """</td><td>Java 15+</td><td class="yes">Best for multiline</td></tr>
      </tbody>
    </table>
  </div>

</div>

</div>

  </template>
</Slide2>
