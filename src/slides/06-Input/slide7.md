---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 7 — BUFFEREDREADER & INPUTSTREAMREADER
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Java Input Methods">
  <template #content>

<div class="slide-h1" style="margin-bottom:10px;"><span class="highlight">BufferedReader</span> — Fast I/O</div>

<div class="g2" style="gap:14px;align-items:start;">

<div class="flex-col">

  <div v-click class="card-navy" style="border-radius:10px;">
    <div style="font-size:.82rem;line-height:1.6;color:var(--slate);">
      <strong style="color:var(--red);">BufferedReader</strong> (in package <span class="mono">java.io</span>) reads text from a character-input stream, <strong>buffering characters</strong> (default 8 KB buffer) to provide efficient, high-speed reading of lines and arrays.
    </div>
  </div>

  <div v-click class="section-label" style="margin-top:6px;">How the Pipeline Works</div>

  <div v-after style="display:flex;flex-direction:column;gap:6px;font-family:'Fira Code',monospace;font-size:.68rem;">
    <div style="background:#f0f4ff;border:1px solid #c5cde8;border-radius:6px;padding:6px 10px;">
      <span style="color:var(--navy);font-weight:700;">1. System.in</span> <span style="color:var(--slate);">(Byte Stream from keyboard)</span>
    </div>
    <div style="text-align:center;color:var(--blue);font-weight:700;">↓ wrapped inside</div>
    <div style="background:#ebf8ff;border:1px solid var(--blue);border-radius:6px;padding:6px 10px;">
      <span style="color:var(--blue);font-weight:700;">2. InputStreamReader</span> <span style="color:var(--slate);">(Converts bytes to characters)</span>
    </div>
    <div style="text-align:center;color:var(--green);font-weight:700;">↓ wrapped inside</div>
    <div style="background:#f0fff4;border:1px solid var(--green);border-radius:6px;padding:6px 10px;">
      <span style="color:var(--green);font-weight:700;">3. BufferedReader</span> <span style="color:var(--slate);">(Stores in 8KB buffer &amp; reads whole lines)</span>
    </div>
  </div>

  <div v-click class="callout callout-warn" style="margin-top:6px;">
    <div><strong>Throws IOException:</strong> <span class="mono">BufferedReader</span> methods can throw checked <span class="mono">IOException</span>. You must declare <span class="mono">throws IOException</span> on <span class="mono">main()</span> or use a <span class="mono">try-catch</span> block.</div>
  </div>

</div>

<div class="flex-col">
  <div v-click class="section-label">Complete Code Example</div>

  <div v-after class="code-block" style="font-size:.70rem;line-height:1.8;">
    <span style="color:#ef5050;">import</span> <span style="color:#0e6ead;">java.io.BufferedReader</span>;<br>
    <span style="color:#ef5050;">import</span> <span style="color:#0e6ead;">java.io.InputStreamReader</span>;<br>
    <span style="color:#ef5050;">import</span> <span style="color:#0e6ead;">java.io.IOException</span>;<br>
    <br>
    <span style="color:#ef5050;">public class</span> <span style="color:#0e6ead;">FastInputDemo</span> {<br>
    <span style="padding-left:16px;display:block;"><span style="color:#ef5050;">public static void</span> <span style="color:#0e6ead;">main</span>(<span style="color:#ef5050;">String</span>[] <span style="color:#0e6ead;">args</span>) <span style="color:#ef5050;font-weight:700;">throws IOException</span> {</span>
    <span style="padding-left:32px;display:block;background:#f0fff4;border-left:2px solid var(--green);"><span style="color:#0e6ead;">BufferedReader</span> <span style="color:#0e6ead;">br</span> = <span style="color:#ef5050;">new</span> <span style="color:#0e6ead;">BufferedReader</span>(<br>&nbsp;&nbsp;<span style="color:#ef5050;">new</span> <span style="color:#0e6ead;">InputStreamReader</span>(<span style="color:#0e6ead;">System</span>.<span style="color:#0e6ead;">in</span>));</span>
    <br>
    <span style="padding-left:32px;display:block;"><span style="color:#0e6ead;">System</span>.<span style="color:#2d7a00;">print</span>(<span style="color:#2d7a00;">"Enter your name: "</span>);</span>
    <span style="padding-left:32px;display:block;"><span style="color:#ef5050;">String</span> <span style="color:#0e6ead;">name</span> = <span style="color:#0e6ead;">br</span>.<span style="color:#2d7a00;">readLine</span>();</span>
    <br>
    <span style="padding-left:32px;display:block;"><span style="color:#0e6ead;">System</span>.<span style="color:#0e6ead;">out</span>.<span style="color:#2d7a00;">println</span>(<span style="color:#2d7a00;">"Hello, "</span> + <span style="color:#0e6ead;">name</span>);</span>
    <span style="padding-left:32px;display:block;"><span style="color:#0e6ead;">br</span>.<span style="color:#2d7a00;">close</span>();</span>
    <span style="padding-left:16px;display:block;">}</span>
    }
  </div>

  <div v-click class="callout callout-info" style="margin-top:6px;">
    <div><strong>Why it is fast:</strong> <span class="mono">BufferedReader</span> reads large 8KB chunks into memory at once, minimizing expensive disk/keyboard OS system calls.</div>
  </div>

</div>

</div>

  </template>
</Slide2>
