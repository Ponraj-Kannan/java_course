---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 13 — SUMMARY & BEST PRACTICES
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Java Input Methods">
  <template #content>

<div class="slide-h1" style="margin-bottom:10px;">Module <span class="highlight">Summary</span> &amp; Best Practices</div>

<div class="g2" style="gap:14px;align-items:start;">

<div class="flex-col">

  <div class="section-label" v-click>Key Takeaways</div>

  <div style="display:flex;flex-direction:column;gap:6px;">
    <div v-click class="card" style="padding:8px 12px;border-left:4px solid var(--blue);">
      <div style="font-weight:700;font-size:.72rem;color:var(--navy);">1. Scanner is your default tool</div>
      <div style="font-size:.68rem;color:var(--slate);">Easiest to read primitives (<span class="mono">nextInt()</span>, <span class="mono">nextDouble()</span>) and single tokens (<span class="mono">next()</span>).</div>
    </div>
    <div v-click class="card" style="padding:8px 12px;border-left:4px solid var(--red);">
      <div style="font-weight:700;font-size:.72rem;color:var(--navy);">2. Remember the nextLine() buffer flush</div>
      <div style="font-size:.68rem;color:var(--slate);">Add <span class="mono">sc.nextLine()</span> after <span class="mono">nextInt()</span> before reading text with <span class="mono">nextLine()</span>.</div>
    </div>
    <div v-click class="card" style="padding:8px 12px;border-left:4px solid var(--green);">
      <div style="font-weight:700;font-size:.72rem;color:var(--navy);">3. Use BufferedReader for speed</div>
      <div style="font-size:.68rem;color:var(--slate);">8KB internal buffer minimizes system calls for competitive programming and big data.</div>
    </div>
    <div v-click class="card" style="padding:8px 12px;border-left:4px solid var(--purple);">
      <div style="font-weight:700;font-size:.72rem;color:var(--navy);">4. Use Console for secure passwords</div>
      <div style="font-size:.68rem;color:var(--slate);"><span class="mono">readPassword()</span> disables character echoing and returns a wipeable <span class="mono">char[]</span>.</div>
    </div>
  </div>

</div>

<div class="flex-col">
  <div v-click class="section-label">Decision Flowchart Cheat-Sheet</div>

  <div v-after style="background:#f7f8fc;border:1px solid var(--border);border-radius:10px;padding:12px;font-size:.70rem;line-height:1.8;">
    <div style="font-weight:700;color:var(--navy);margin-bottom:6px;">Which input method should you choose?</div>
    <div>🔹 <strong>Need fast I/O or big input?</strong> → <span class="pill pill-green" style="font-size:.62rem;">BufferedReader</span></div>
    <div>🔹 <strong>Need to hide a password?</strong> → <span class="pill pill-purple" style="font-size:.62rem;">Console.readPassword()</span></div>
    <div>🔹 <strong>Passing flags at program startup?</strong> → <span class="pill pill-orange" style="font-size:.62rem;">String[] args</span></div>
    <div>🔹 <strong>General programming &amp; assignments?</strong> → <span class="pill pill-blue" style="font-size:.62rem;">Scanner</span></div>
  </div>

  <div v-click class="callout callout-success" style="margin-top:8px;">
    <div><strong>Ready for Practice:</strong> Proceed to the test problems on the next slides to test your understanding of Scanner, BufferedReader, buffer flushes, and CLI args!</div>
  </div>

</div>

</div>

  </template>
</Slide2>
