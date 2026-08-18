---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 35 — JAVA NAMING CONVENTIONS (Summary)
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Java Naming Conventions">
  <template #content>

<div class="slide-h1" style="margin-bottom:12px;">Naming <span class="highlight">Conventions</span></div>

<div class="g2" style="gap:14px;align-items:start;">

<div class="flex-col">

  <div v-click class="card-navy" style="border-radius:10px;">
    <div style="font-size:.82rem;line-height:1.6;color:var(--slate);">
      Java has strict naming <strong style="color:var(--red);">conventions</strong> (not rules — the code still compiles without them, but they make your code professional and readable).
    </div>
  </div>

  <div style="display:flex;flex-direction:column;gap:8px;">
    <div v-click style="display:flex;gap:10px;align-items:center;">
      <div style="background:var(--red-soft);border:2px solid var(--red);border-radius:8px;padding:6px 14px;min-width:100px;text-align:center;">
        <div style="font-family:'Fira Code',monospace;font-weight:800;color:var(--red-dark);font-size:.75rem;">PascalCase</div>
      </div>
      <div class="small-text"><strong>Classes &amp; Interfaces</strong><br><span class="mono">StudentRecord</span>, <span class="mono">BankAccount</span>, <span class="mono">Runnable</span></div>
    </div>
    <div v-click style="display:flex;gap:10px;align-items:center;">
      <div style="background:#ebf8ff;border:2px solid var(--blue);border-radius:8px;padding:6px 14px;min-width:100px;text-align:center;">
        <div style="font-family:'Fira Code',monospace;font-weight:800;color:var(--blue);font-size:.75rem;">camelCase</div>
      </div>
      <div class="small-text"><strong>Variables &amp; Methods</strong><br><span class="mono">studentName</span>, <span class="mono">calculateGpa()</span>, <span class="mono">isEnrolled</span></div>
    </div>
    <div v-click style="display:flex;gap:10px;align-items:center;">
      <div style="background:#f0fff4;border:2px solid var(--green);border-radius:8px;padding:6px 14px;min-width:100px;text-align:center;">
        <div style="font-family:'Fira Code',monospace;font-weight:800;color:var(--green);font-size:.75rem;">UPPER_SNAKE</div>
      </div>
      <div class="small-text"><strong>Constants</strong><br><span class="mono">MAX_SIZE</span>, <span class="mono">PI</span>, <span class="mono">DEFAULT_TIMEOUT</span></div>
    </div>
    <div v-click style="display:flex;gap:10px;align-items:center;">
      <div style="background:#fffaf0;border:2px solid var(--orange);border-radius:8px;padding:6px 14px;min-width:100px;text-align:center;">
        <div style="font-family:'Fira Code',monospace;font-weight:800;color:var(--orange);font-size:.75rem;">lowercase</div>
      </div>
      <div class="small-text"><strong>Packages</strong><br><span class="mono">com.example.app</span>, <span class="mono">java.util</span></div>
    </div>

  </div>

</div>

<div class="flex-col">

  <div v-click class="section-label">Good vs Bad Naming</div>

  <div class="g2" style="gap:8px;">
    <div>
      <div class="slide-h3" style="color:#c73c3c;margin-bottom:4px;">❌ Bad</div>
      <div v-click style="background:#f6f8fa;border-radius:8px;border:1px solid #e1e4e8;padding:10px 14px;font-family:'Fira Code',monospace;font-size:.72rem;line-height:2;">
        <span style="color:#ef5050;">int</span> X = <span style="color:#b45309;">20</span>;<br>
        <span style="color:#ef5050;">String</span> mystring;<br>
        <span style="color:#ef5050;">class</span> bankaccount { }
      </div>
    </div>
    <div>
      <div class="slide-h3" style="color:#38a169;margin-bottom:4px;">✅ Good</div>
      <div v-click style="background:#f6f8fa;border-radius:8px;border:1px solid #e1e4e8;padding:10px 14px;font-family:'Fira Code',monospace;font-size:.72rem;line-height:2;">
        <span style="color:#ef5050;">int</span> age = <span style="color:#b45309;">20</span>;<br>
        <span style="color:#ef5050;">String</span> studentName;<br>
        <span style="color:#ef5050;">class</span> BankAccount { }
      </div>
    </div>
  </div>

  <div v-click class="callout callout-info" style="margin-top:8px;">
    <div><strong>Variables must start with</strong> a letter, <span class="mono">$</span>, or <span class="mono">_</span>. They cannot start with a digit and cannot be a reserved keyword.</div>
  </div>

  <div v-click class="callout callout-success" style="margin-top:6px;">
    <div><strong>Self-documenting code:</strong> Choose names like <span class="mono">totalMarks</span> instead of <span class="mono">tm</span> — your future self will thank you!</div>
  </div>

</div>

</div>

  </template>
</Slide2>
