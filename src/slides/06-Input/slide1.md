<!-- ═══════════════════════════════════════════════════════
     SLIDE 1 — INTRODUCTION TO JAVA INPUT METHODS
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Java Input Methods">
  <template #content>

<div class="slide-h1" style="margin-bottom:10px;">Introduction to <span class="highlight">User Input</span></div>

<div class="g2" style="gap:14px;align-items:start;">

<div class="flex-col">

  <div v-click class="card-navy" style="border-radius:10px;">
    <div style="font-size:.82rem;line-height:1.6;color:var(--slate);">
      <strong style="color:var(--red);">User input</strong> is data supplied by a user or external source to a program at runtime. In Java, input is read from the standard input stream (<span class="mono">System.in</span>) using specialized I/O classes.
    </div>
  </div>

  <div v-click class="callout callout-warn">
    <div><strong>Java vs Python:</strong> Python has a built-in <span class="mono">input()</span> function. Java has <strong>no single input keyword</strong> — you must use I/O utility classes like <span class="mono">Scanner</span>, <span class="mono">BufferedReader</span>, or <span class="mono">Console</span>.</div>
  </div>

  <div v-click class="section-label" style="margin-top:6px;">How Input Streams Work</div>

  <div v-after style="background:#f6f8fa;border-radius:10px;border:1px solid #e1e4e8;padding:12px;font-family:'Fira Code',monospace;font-size:.7rem;line-height:1.9;">
    <div style="color:var(--navy);font-weight:700;margin-bottom:4px;">⌨️ Keyboard → System.in (Bytes) → Parser → Variables</div>
    <span style="color:#6b7280;">// System.in reads raw bytes from keyboard</span><br>
    <span style="color:#ef5050;">Scanner</span> <span style="color:#0e6ead;">sc</span> = <span style="color:#ef5050;">new</span> <span style="color:#0e6ead;">Scanner</span>(<span style="color:#0e6ead;">System</span>.<span style="color:#0e6ead;">in</span>);<br>
    <span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">age</span> = <span style="color:#0e6ead;">sc</span>.<span style="color:#2d7a00;">nextInt</span>(); <span style="color:#6b7280;">// parses byte stream into an int</span>
  </div>

  <div v-click class="callout callout-info" style="margin-top:4px;">
    <div><span class="mono">System.in</span> is an instance of <span class="mono">java.io.InputStream</span> that reads raw bytes from the standard input stream.</div>
  </div>

</div>

<div class="flex-col">
  <div class="section-label" v-click>4 Ways to Take Input in Java</div>

  <div style="display:flex;flex-direction:column;gap:8px;">
    <div v-click class="card" style="display:flex;gap:10px;align-items:flex-start;border:1px solid var(--blue);">
      <span class="pill pill-blue" style="flex-shrink:0;min-width:90px;text-align:center;">Scanner</span>
      <div>
        <div style="font-size:.75rem;font-weight:700;color:var(--navy);">java.util.Scanner</div>
        <div style="font-size:.68rem;color:var(--slate);">Easiest to use — automatically parses primitives (<span class="mono">int</span>, <span class="mono">double</span>) and strings. Best for beginners.</div>
      </div>
    </div>
    <div v-click class="card" style="display:flex;gap:10px;align-items:flex-start;border:1px solid var(--green);">
      <span class="pill pill-green" style="flex-shrink:0;min-width:90px;text-align:center;">BufferedReader</span>
      <div>
        <div style="font-size:.75rem;font-weight:700;color:var(--navy);">java.io.BufferedReader</div>
        <div style="font-size:.68rem;color:var(--slate);">High-performance buffered reader. Fast I/O, preferred for competitive programming and large datasets.</div>
      </div>
    </div>
    <div v-click class="card" style="display:flex;gap:10px;align-items:flex-start;border:1px solid var(--purple);">
      <span class="pill pill-purple" style="flex-shrink:0;min-width:90px;text-align:center;">Console</span>
      <div>
        <div style="font-size:.75rem;font-weight:700;color:var(--navy);">java.io.Console</div>
        <div style="font-size:.68rem;color:var(--slate);">Reads passwords securely without echoing characters to screen (<span class="mono">readPassword()</span>).</div>
      </div>
    </div>
    <div v-click class="card" style="display:flex;gap:10px;align-items:flex-start;border:1px solid var(--orange);">
      <span class="pill pill-orange" style="flex-shrink:0;min-width:90px;text-align:center;">CLI Args</span>
      <div>
        <div style="font-size:.75rem;font-weight:700;color:var(--navy);">String[] args in main()</div>
        <div style="font-size:.68rem;color:var(--slate);">Values passed via command line at program launch (<span class="mono">java App 10 20</span>).</div>
      </div>
    </div>
  </div>

</div>

</div>

  </template>
</Slide2>
