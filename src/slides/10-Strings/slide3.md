---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 3 — STRING IMMUTABILITY
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Java Strings">
  <template #content>

<div class="slide-h1" style="margin-bottom:10px;">String <span class="highlight">Immutability</span></div>

<div class="g2" style="gap:14px;align-items:start;">

<div class="flex-col">

  <div v-click class="card-red" style="border-radius:10px;">
    <div style="font-size:.78rem;font-weight:600;color:var(--red-dark);margin-bottom:6px;">Definition — Immutable</div>
    <div style="font-size:.74rem;color:var(--slate);line-height:1.6;">Once a String object is created, its <strong>content cannot be changed</strong>. Any operation that appears to "modify" a string actually creates a <strong>brand-new String object</strong> — the original is untouched.</div>
  </div>

  <div v-click class="code-block" style="margin-top:6px;">
    <span style="color:#0e6ead;">String</span> <span style="color:#0e6ead;">s</span> = <span style="color:#2d7a00;">"hello"</span>;<br>
    <span style="color:#6b7280;">// s.charAt(0) = 'H';  ← compile error! Cannot modify</span><br>
    <br>
    <span style="color:#0e6ead;">String</span> <span style="color:#0e6ead;">upper</span> = <span style="color:#0e6ead;">s</span>.<span style="color:#2d7a00;">toUpperCase</span>(); <span style="color:#6b7280;">// new object "HELLO"</span><br>
    <span style="color:#0e6ead;">System</span>.<span style="color:#0e6ead;">out</span>.<span style="color:#2d7a00;">println</span>(<span style="color:#0e6ead;">s</span>);     <span style="color:#6b7280;">// still "hello" — unchanged!</span><br>
    <span style="color:#0e6ead;">System</span>.<span style="color:#0e6ead;">out</span>.<span style="color:#2d7a00;">println</span>(<span style="color:#0e6ead;">upper</span>); <span style="color:#6b7280;">// "HELLO"</span>
  </div>

  <div v-click class="callout callout-warn" style="margin-top:4px;">
    <div><strong>Common mistake:</strong> Calling <span class="mono">s.toUpperCase()</span> and then using <span class="mono">s</span> — thinking it changed. <strong>Always capture the returned string!</strong></div>
  </div>

  <div v-click class="section-label" style="margin-top:4px;">Why Java Made Strings Immutable</div>
  <div style="display:flex;flex-direction:column;gap:5px;">
    <div v-click style="display:flex;gap:8px;align-items:flex-start;">
      <span class="pill pill-green" style="flex-shrink:0;">Security</span>
      <span style="font-size:.7rem;color:var(--slate);">Prevents malicious code from changing credentials or file paths after validation</span>
    </div>
    <div v-click style="display:flex;gap:8px;align-items:flex-start;">
      <span class="pill pill-blue" style="flex-shrink:0;">Thread Safety</span>
      <span style="font-size:.7rem;color:var(--slate);">Immutable objects can be shared across threads without synchronisation</span>
    </div>
    <div v-click style="display:flex;gap:8px;align-items:flex-start;">
      <span class="pill pill-purple" style="flex-shrink:0;">String Pool</span>
      <span style="font-size:.7rem;color:var(--slate);">Safe to share pool objects because no one can secretly change the content</span>
    </div>
  </div>

</div>

<div class="flex-col">
  <div v-click class="section-label">Memory Diagram — What Actually Happens</div>

  <div style="background:#f7f8fc;border:1px solid var(--border);border-radius:10px;padding:12px 14px;font-size:.72rem;">
    <div v-click style="margin-bottom:8px;font-weight:700;color:var(--navy);">String Pool / Heap</div>
    <div v-click style="display:flex;align-items:center;gap:8px;margin-bottom:8px;">
      <div style="background:#f0fff4;border:2px solid var(--green);border-radius:8px;padding:8px 14px;font-family:'Fira Code',monospace;font-weight:700;color:var(--green);">"hello"</div>
      <div style="font-size:.65rem;color:var(--slate);">← s points here</div>
    </div>
    <div v-click style="font-size:.65rem;color:var(--slate);margin-bottom:6px;">After calling <span style="font-family:'Fira Code',monospace;">s.toUpperCase()</span>:</div>
    <div v-click style="display:flex;align-items:center;gap:8px;margin-bottom:8px;">
      <div style="background:#f0fff4;border:2px solid var(--green);border-radius:8px;padding:8px 14px;font-family:'Fira Code',monospace;font-weight:700;color:var(--green);">"hello"</div>
      <div style="font-size:.65rem;color:var(--slate);">← s still here (unchanged!)</div>
    </div>
    <div v-click style="display:flex;align-items:center;gap:8px;">
      <div style="background:#ebf8ff;border:2px dashed var(--blue);border-radius:8px;padding:8px 14px;font-family:'Fira Code',monospace;font-weight:700;color:var(--blue);">"HELLO"</div>
      <div style="font-size:.65rem;color:var(--slate);">← NEW object returned by toUpperCase()</div>
    </div>
    <div style="margin-top:10px;padding:6px 10px;background:#fff5f5;border-radius:6px;border:1px solid #fecaca;font-size:.65rem;color:var(--red-dark);" v-click>
      ⚠ String <span style="font-family:'Fira Code',monospace;">"hello"</span> was never touched. A completely new object was created.
    </div>

  </div>

  <div v-click class="callout callout-success" style="margin-top:8px;">
    <div><strong>Golden Rule:</strong> Always <strong>capture the result</strong> of a string method into a variable — <span class="mono">s = s.toUpperCase();</span> — otherwise the transformation is lost.</div>
  </div>

</div>

</div>

  </template>
</Slide2>
