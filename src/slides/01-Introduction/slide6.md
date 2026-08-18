---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 6 — HOW JAVA WORKS (Compile → Run Pipeline)
═══════════════════════════════════════════════════════ -->

<Slide2 topic="How Java Works">
  <template #content>

<div class="slide-h1" style="margin-bottom:12px;">How Java <span class="highlight">Works</span></div>

<div class="g2" style="gap:16px;align-items:start;">

<div>
  <div class="slide-h3" style="margin-bottom:8px;color:#3182ce;">The Compile → Run Pipeline</div>
  <div style="background:#fff;border:1px solid var(--border);border-radius:10px;padding:14px;">
    <div class="step-flow" style="flex-direction:column;align-items:flex-start;gap:8px;">
      <div v-click class="step-box" style="width:100%;text-align:left;"><strong>1.</strong> Write source code → <span class="mono">Hello.java</span></div>
      <div v-click class="step-box" style="width:100%;text-align:left;"><strong>2.</strong> Compile with <span class="mono">javac Hello.java</span></div>
      <div v-click class="step-box" style="width:100%;text-align:left;"><strong>3.</strong> Compiler creates → <span class="mono">Hello.class</span> (bytecode)</div>
      <div v-click class="step-box" style="width:100%;text-align:left;"><strong>4.</strong> JVM loads and runs bytecode</div>
      <div v-click class="step-box active" style="width:100%;text-align:left;"><strong>5.</strong> JIT compiles to native machine code → output!</div>
    </div>
    <div class="small-text" style="margin-top:8px;">⏱ Compile once, run anywhere (WORA)</div>
  </div>
</div>

<div>
  <div v-click class="slide-h3" style="margin-bottom:8px;color:#38a169;">What is Bytecode?</div>

  <div v-click class="card-navy" style="border-radius:10px;margin-bottom:10px;">
    <div style="font-size:.82rem;line-height:1.6;color:var(--slate);">
      Bytecode is an <strong style="color:var(--red);">intermediate representation</strong> — not raw machine code, not human-readable source. The JVM on any platform reads and executes it.
    </div>
  </div>

  <div v-click class="section-label" style="margin-bottom:6px;">File Extension Summary</div>

  <div style="display:flex;flex-direction:column;gap:6px;">
    <div style="display:flex;align-items:center;gap:8px;" v-click>
      <div style="background:#ebf8ff;border:1px solid var(--blue);border-radius:6px;padding:5px 14px;font-family:'Fira Code',monospace;font-size:.75rem;font-weight:700;color:#2b6cb0;min-width:90px;text-align:center;">.java</div>
      <div style="color:var(--muted);">→</div>
      <div class="small-text">Your source code file — human-readable</div>
    </div>
    <div style="display:flex;align-items:center;gap:8px;" v-click>
      <div style="background:var(--red-soft);border:1px solid var(--red);border-radius:6px;padding:5px 14px;font-family:'Fira Code',monospace;font-size:.75rem;font-weight:700;color:var(--red-dark);min-width:90px;text-align:center;">.class</div>
      <div style="color:var(--muted);">→</div>
      <div class="small-text">Compiled bytecode — created by <span class="mono">javac</span></div>
    </div>
    <div style="display:flex;align-items:center;gap:8px;" v-click>
      <div style="background:#f0fff4;border:1px solid var(--green);border-radius:6px;padding:5px 14px;font-family:'Fira Code',monospace;font-size:.75rem;font-weight:700;color:var(--green);min-width:90px;text-align:center;">.jar</div>
      <div style="color:var(--muted);">→</div>
      <div class="small-text">Packaged app archive — multiple .class files zipped</div>
    </div>
  </div>

</div>

</div>

  </template>
</Slide2>
