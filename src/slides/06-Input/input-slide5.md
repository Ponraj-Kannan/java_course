---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 5 — BUFFEREDREADER
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Input Methods">
  <template #content>

<div class="slide-h1" style="margin-bottom:10px;">Reading Input with <span class="highlight">BufferedReader</span></div>

<div class="g2" style="gap:14px;">

<div class="flex-col">

  <div v-click class="card-navy" style="border-radius:10px;">
    <div style="font-size:.8rem;line-height:1.6;color:var(--slate);">
      <strong style="color:var(--red);">Definition:</strong> <span class="mono">BufferedReader</span> (from <span class="mono">java.io</span>) reads text input <strong>faster</strong> than <span class="mono">Scanner</span> by buffering characters, but it only knows how to read <strong>raw text lines</strong> — everything comes back as a <span class="mono">String</span>.
    </div>
  </div>

  <div v-click class="callout callout-warn">
    <div><strong>Checked exception:</strong> <span class="mono">readLine()</span> can throw an <span class="mono">IOException</span>, so it must be wrapped in a <span class="mono">try/catch</span> or declared with <span class="mono">throws IOException</span>.</div>
  </div>

  <div style="display:flex;flex-direction:column;gap:5px;margin-top:2px;">
    <div v-click class="card-purple" style="border-radius:8px;padding:8px 12px;">
      <div style="font-size:.72rem;font-weight:700;color:var(--purple);font-family:'Fira Code',monospace;">Integer.parseInt(str)</div>
      <div style="font-size:.7rem;color:var(--slate);">Converts a String to an int</div>
    </div>
    <div v-click class="card-red" style="border-radius:8px;padding:8px 12px;">
      <div style="font-size:.72rem;font-weight:700;color:var(--red-dark);font-family:'Fira Code',monospace;">Double.parseDouble(str)</div>
      <div style="font-size:.7rem;color:var(--slate);">Converts a String to a double</div>
    </div>
  </div>

</div>

<div class="flex-col">
  <div v-click class="section-label">Code Example</div>

  <div v-after style="background:#f6f8fa;border-radius:10px;border:1px solid #e1e4e8;padding:12px 14px;font-family:'Fira Code',monospace;font-size:.7rem;line-height:1.85;">
    <span style="color:#805ad5;">import</span> <span style="color:#0e6ead;">java.io.*</span>;<br><br>
    <span style="color:#0e6ead;">BufferedReader</span> <span style="color:#0e6ead;">br</span> = <span style="color:#805ad5;">new</span> <span style="color:#0e6ead;">BufferedReader</span>(<br>
    &nbsp;&nbsp;<span style="color:#805ad5;">new</span> <span style="color:#0e6ead;">InputStreamReader</span>(<span style="color:#0e6ead;">System</span>.<span style="color:#0e6ead;">in</span>));<br><br>
    <span style="color:#805ad5;">try</span> {<br>
    &nbsp;&nbsp;<span style="color:#6b7280;">// user types: 42</span><br>
    &nbsp;&nbsp;<span style="color:#0e6ead;">String</span> <span style="color:#0e6ead;">line</span> = <span style="color:#0e6ead;">br</span>.<span style="color:#2d7a00;">readLine</span>();<br>
    &nbsp;&nbsp;<span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">num</span> = <span style="color:#0e6ead;">Integer</span>.<span style="color:#2d7a00;">parseInt</span>(<span style="color:#0e6ead;">line</span>);<br>
    &nbsp;&nbsp;<span style="color:#0e6ead;">System</span>.<span style="color:#0e6ead;">out</span>.<span style="color:#2d7a00;">println</span>(<span style="color:#0e6ead;">num</span> * <span style="color:#b45309;">2</span>); <span style="color:#6b7280;">// 84</span><br>
    } <span style="color:#805ad5;">catch</span> (<span style="color:#0e6ead;">IOException</span> <span style="color:#0e6ead;">e</span>) {<br>
    &nbsp;&nbsp;<span style="color:#0e6ead;">e</span>.<span style="color:#2d7a00;">printStackTrace</span>();<br>
    }
  </div>

  <div v-click class="card card-blue" style="margin-top:6px;">
    <div class="small-text"><strong>No buffer trap here:</strong> Since every call is <span class="mono">readLine()</span>, there's no leftover newline issue like with <span class="mono">Scanner</span>.</div>
  </div>

</div>

</div>

  </template>
</Slide2>
