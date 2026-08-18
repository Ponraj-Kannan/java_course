---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 8 — PARSING TYPES WITH BUFFEREDREADER
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Java Input Methods">
  <template #content>

<div class="slide-h1" style="margin-bottom:10px;">BufferedReader — <span class="highlight">Parsing Data</span></div>

<div class="g2" style="gap:14px;align-items:start;">

<div class="flex-col">

  <div v-click class="card-navy" style="border-radius:10px;">
    <div style="font-size:.82rem;line-height:1.6;color:var(--slate);">
      <span class="mono">BufferedReader.readLine()</span> <strong>always returns a String</strong>. To convert it into primitive numbers, use the wrapper class parsing methods like <span class="mono">Integer.parseInt()</span> or <span class="mono">Double.parseDouble()</span>.
    </div>
  </div>

  <div style="margin-top:6px;">
    <table class="cmp-table" style="font-size:.7rem;">
      <thead v-click><tr><th>Target Type</th><th>Parsing Method</th></tr></thead>
      <tbody>
        <tr v-click><td class="mono">int</td><td class="mono">Integer.parseInt(str)</td></tr>
        <tr v-click><td class="mono">double</td><td class="mono">Double.parseDouble(str)</td></tr>
        <tr v-click><td class="mono">long</td><td class="mono">Long.parseLong(str)</td></tr>
        <tr v-click><td class="mono">float</td><td class="mono">Float.parseFloat(str)</td></tr>
        <tr v-click><td class="mono">boolean</td><td class="mono">Boolean.parseBoolean(str)</td></tr>
        <tr v-click><td class="mono">char</td><td class="mono">str.charAt(0)</td></tr>
      </tbody>
    </table>
  </div>

  <div v-click class="callout callout-danger" style="margin-top:6px;">
    <div><strong>NumberFormatException:</strong> If the string cannot be parsed into the target number (e.g. <span class="mono">"abc"</span>), a <span class="mono">NumberFormatException</span> is thrown.</div>
  </div>

</div>

<div class="flex-col">
  <div v-click class="section-label">Reading Multiple Numbers on One Line (Fast I/O)</div>

  <div v-after class="code-block" style="font-size:.68rem;line-height:1.75;">
    <span style="color:#ef5050;">import</span> <span style="color:#0e6ead;">java.io.*</span>;<br>
    <span style="color:#ef5050;">import</span> <span style="color:#0e6ead;">java.util.StringTokenizer</span>;<br>
    <br>
    <span style="color:#6b7280;">// User types: "10 20 30"</span><br>
    <span style="color:#0e6ead;">BufferedReader</span> <span style="color:#0e6ead;">br</span> = <span style="color:#ef5050;">new</span> <span style="color:#0e6ead;">BufferedReader</span>(<br>&nbsp;&nbsp;<span style="color:#ef5050;">new</span> <span style="color:#0e6ead;">InputStreamReader</span>(<span style="color:#0e6ead;">System</span>.<span style="color:#0e6ead;">in</span>));<br>
    <br>
    <span style="color:#ef5050;">String</span> <span style="color:#0e6ead;">line</span> = <span style="color:#0e6ead;">br</span>.<span style="color:#2d7a00;">readLine</span>(); <span style="color:#6b7280;">// reads full line</span><br>
    <span style="color:#0e6ead;">StringTokenizer</span> <span style="color:#0e6ead;">st</span> = <span style="color:#ef5050;">new</span> <span style="color:#0e6ead;">StringTokenizer</span>(<span style="color:#0e6ead;">line</span>);<br>
    <br>
    <span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">a</span> = <span style="color:#0e6ead;">Integer</span>.<span style="color:#2d7a00;">parseInt</span>(<span style="color:#0e6ead;">st</span>.<span style="color:#2d7a00;">nextToken</span>()); <span style="color:#6b7280;">// 10</span><br>
    <span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">b</span> = <span style="color:#0e6ead;">Integer</span>.<span style="color:#2d7a00;">parseInt</span>(<span style="color:#0e6ead;">st</span>.<span style="color:#2d7a00;">nextToken</span>()); <span style="color:#6b7280;">// 20</span><br>
    <span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">c</span> = <span style="color:#0e6ead;">Integer</span>.<span style="color:#2d7a00;">parseInt</span>(<span style="color:#0e6ead;">st</span>.<span style="color:#2d7a00;">nextToken</span>()); <span style="color:#6b7280;">// 30</span><br>
    <br>
    <span style="color:#0e6ead;">System</span>.<span style="color:#0e6ead;">out</span>.<span style="color:#2d7a00;">println</span>(<span style="color:#2d7a00;">"Sum = "</span> + (<span style="color:#0e6ead;">a</span> + <span style="color:#0e6ead;">b</span> + <span style="color:#0e6ead;">c</span>)); <span style="color:#6b7280;">// 60</span>
  </div>

  <div v-click class="callout callout-info" style="margin-top:6px;">
    <div><strong>Competitive Programming:</strong> Combining <span class="mono">BufferedReader</span> with <span class="mono">StringTokenizer</span> is the gold standard for reading 100,000+ numbers within 1 second.</div>
  </div>

</div>

</div>

  </template>
</Slide2>
