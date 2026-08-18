---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 3 — THE nextInt() / nextLine() BUFFER TRAP
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Input Methods">
  <template #content>

<div class="slide-h1" style="margin-bottom:10px;">The <span class="highlight">nextInt() → nextLine()</span> Buffer Trap</div>

<div class="g2" style="gap:14px;">

<div class="flex-col">

  <div v-click class="card-navy" style="border-radius:10px;">
    <div style="font-size:.8rem;line-height:1.6;color:var(--slate);">
      <strong style="color:var(--red);">The Problem:</strong> <span class="mono">nextInt()</span>, <span class="mono">nextDouble()</span>, and similar methods read only the <strong>value</strong> — they leave the trailing <strong>newline character</strong> (<span class="mono">\n</span>) sitting in the input buffer.
    </div>
  </div>

  <div v-click class="callout callout-danger">
    <div><strong>What goes wrong:</strong> A <span class="mono">nextLine()</span> call right after <span class="mono">nextInt()</span> immediately reads that leftover <span class="mono">\n</span> and returns an <strong>empty string</strong> — it never waits for the user!</div>
  </div>

  <div v-click style="background:#f6f8fa;border-radius:10px;border:1px solid #e1e4e8;padding:12px 14px;font-family:'Fira Code',monospace;font-size:.72rem;line-height:1.9;">
    <span style="color:#6b7280;">// BUGGY — skips the name prompt!</span><br>
    <span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">age</span> = <span style="color:#0e6ead;">sc</span>.<span style="color:#2d7a00;">nextInt</span>(); <span style="color:#6b7280;">// user types 20⏎</span><br>
    <span style="color:#0e6ead;">String</span> <span style="color:#0e6ead;">name</span> = <span style="color:#0e6ead;">sc</span>.<span style="color:#2d7a00;">nextLine</span>(); <span style="color:#6b7280;">// grabs leftover ⏎</span><br>
    <span style="color:#0e6ead;">System</span>.<span style="color:#0e6ead;">out</span>.<span style="color:#2d7a00;">println</span>(<span style="color:#2d7a00;">"Name: "</span> + <span style="color:#0e6ead;">name</span>); <span style="color:#6b7280;">// "Name: "</span>
  </div>

</div>

<div class="flex-col">
  <div v-click class="section-label">The Fix</div>

  <div v-after class="callout callout-success" style="margin-bottom:2px;">
    <div>Insert an <strong>extra <span class="mono">sc.nextLine()</span></strong> right after any numeric/boolean read to consume the dangling newline before reading a full line.</div>
  </div>

  <div v-click style="background:#f6f8fa;border-radius:10px;border:1px solid #e1e4e8;padding:12px 14px;font-family:'Fira Code',monospace;font-size:.72rem;line-height:1.9;">
    <span style="color:#6b7280;">// FIXED</span><br>
    <span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">age</span> = <span style="color:#0e6ead;">sc</span>.<span style="color:#2d7a00;">nextInt</span>();<br>
    <span style="color:#0e6ead;">sc</span>.<span style="color:#2d7a00;">nextLine</span>(); <span style="color:#6b7280;">// consume leftover \n</span><br>
    <span style="color:#0e6ead;">String</span> <span style="color:#0e6ead;">name</span> = <span style="color:#0e6ead;">sc</span>.<span style="color:#2d7a00;">nextLine</span>(); <span style="color:#6b7280;">// waits properly</span><br>
    <span style="color:#0e6ead;">System</span>.<span style="color:#0e6ead;">out</span>.<span style="color:#2d7a00;">println</span>(<span style="color:#2d7a00;">"Name: "</span> + <span style="color:#0e6ead;">name</span>); <span style="color:#6b7280;">// "Name: John"</span>
  </div>

  <div v-click class="card card-orange" style="margin-top:2px;">
    <div class="small-text"><strong>Rule of thumb:</strong> Whenever you mix <span class="mono">nextInt()</span>/<span class="mono">nextDouble()</span> with <span class="mono">nextLine()</span>, add a "buffer-clearing" <span class="mono">nextLine()</span> in between.</div>
  </div>

</div>

</div>

  </template>
</Slide2>
