---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 12 — COMMON MISTAKES & EXCEPTIONS
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Java Input Methods">
  <template #content>

<div class="slide-h1" style="margin-bottom:10px;">Common <span class="highlight">Mistakes</span> to Avoid</div>

<div class="g2" style="gap:12px;align-items:start;">

<div class="flex-col" style="gap:7px;">

  <div v-click class="card-red" style="border-radius:10px;">
    <div style="font-size:.78rem;font-weight:600;color:var(--red-dark);margin-bottom:4px;">Mistake 1 — Missing \n Flush Before nextLine()</div>
    <div style="background:#fff8f8;border-radius:8px;padding:8px 12px;font-family:'Fira Code',monospace;font-size:.66rem;line-height:1.8;">
      <span style="color:#6b7280;">// Wrong — nextLine() reads leftover newline and is skipped!</span><br>
      <span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">id</span> = <span style="color:#0e6ead;">sc</span>.<span style="color:#2d7a00;">nextInt</span>();<br>
      <span style="color:#ef5050;">String</span> <span style="color:#0e6ead;">name</span> = <span style="color:#0e6ead;">sc</span>.<span style="color:#2d7a00;">nextLine</span>();<br>
      <span style="color:#6b7280;">// Correct — consume the newline first</span><br>
      <span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">id</span> = <span style="color:#0e6ead;">sc</span>.<span style="color:#2d7a00;">nextInt</span>();<br>
      <span style="color:#0e6ead;">sc</span>.<span style="color:#2d7a00;">nextLine</span>(); <span style="color:#6b7280;">// flush</span><br>
      <span style="color:#ef5050;">String</span> <span style="color:#0e6ead;">name</span> = <span style="color:#0e6ead;">sc</span>.<span style="color:#2d7a00;">nextLine</span>();
    </div>
  </div>

  <div v-click class="card-red" style="border-radius:10px;">
    <div style="font-size:.78rem;font-weight:600;color:var(--red-dark);margin-bottom:4px;">Mistake 2 — InputMismatchException on Mismatched Types</div>
    <div style="background:#fff8f8;border-radius:8px;padding:8px 12px;font-family:'Fira Code',monospace;font-size:.66rem;line-height:1.8;">
      <span style="color:#6b7280;">// Wrong — crashes if user enters "twenty"</span><br>
      <span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">age</span> = <span style="color:#0e6ead;">sc</span>.<span style="color:#2d7a00;">nextInt</span>();<br>
      <span style="color:#6b7280;">// Correct — validate with hasNextInt()</span><br>
      <span style="color:#ef5050;">if</span> (<span style="color:#0e6ead;">sc</span>.<span style="color:#2d7a00;">hasNextInt</span>()) {<br>
      <span style="padding-left:16px;display:block;"><span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">age</span> = <span style="color:#0e6ead;">sc</span>.<span style="color:#2d7a00;">nextInt</span>();</span>
      }
    </div>
  </div>

</div>

<div class="flex-col" style="gap:7px;">

  <div v-click class="card-red" style="border-radius:10px;">
    <div style="font-size:.78rem;font-weight:600;color:var(--red-dark);margin-bottom:4px;">Mistake 3 — Forgetting throws IOException on BufferedReader</div>
    <div style="background:#fff8f8;border-radius:8px;padding:8px 12px;font-family:'Fira Code',monospace;font-size:.66rem;line-height:1.8;">
      <span style="color:#6b7280;">// Wrong — does not compile!</span><br>
      <span style="color:#ef5050;">public static void</span> <span style="color:#0e6ead;">main</span>(<span style="color:#ef5050;">String</span>[] <span style="color:#0e6ead;">args</span>) {<br>
      <span style="padding-left:16px;display:block;"><span style="color:#ef5050;">String</span> <span style="color:#0e6ead;">s</span> = <span style="color:#0e6ead;">br</span>.<span style="color:#2d7a00;">readLine</span>(); <span style="color:#6b7280;">// unhandled IOException</span></span>
      }<br>
      <span style="color:#6b7280;">// Correct — declare throws IOException on main()</span><br>
      <span style="color:#ef5050;">public static void</span> <span style="color:#0e6ead;">main</span>(<span style="color:#ef5050;">String</span>[] <span style="color:#0e6ead;">args</span>) <span style="color:#ef5050;font-weight:700;">throws IOException</span>
    </div>
  </div>

  <div v-click class="card-red" style="border-radius:10px;">
    <div style="font-size:.78rem;font-weight:600;color:var(--red-dark);margin-bottom:4px;">Mistake 4 — Array Index Out of Bounds on CLI Args</div>
    <div style="background:#fff8f8;border-radius:8px;padding:8px 12px;font-family:'Fira Code',monospace;font-size:.66rem;line-height:1.8;">
      <span style="color:#6b7280;">// Wrong — crashes if no args passed</span><br>
      <span style="color:#ef5050;">String</span> <span style="color:#0e6ead;">file</span> = <span style="color:#0e6ead;">args</span>[<span style="color:#b45309;">0</span>];<br>
      <span style="color:#6b7280;">// Correct — always check args.length first</span><br>
      <span style="color:#ef5050;">if</span> (<span style="color:#0e6ead;">args</span>.<span style="color:#0e6ead;">length</span> &gt; <span style="color:#b45309;">0</span>) { <span style="color:#ef5050;">String</span> <span style="color:#0e6ead;">file</span> = <span style="color:#0e6ead;">args</span>[<span style="color:#b45309;">0</span>]; }
    </div>
  </div>

  <div v-click class="callout callout-warn" style="margin-top:2px;">
    <div><strong>Resource Leak:</strong> Always call <span class="mono">sc.close()</span> or <span class="mono">br.close()</span> when input processing finishes to release OS file and keyboard handles.</div>
  </div>

</div>

</div>

  </template>
</Slide2>
