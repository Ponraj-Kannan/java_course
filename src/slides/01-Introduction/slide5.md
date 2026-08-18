---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 5 — JDK, JRE, JVM
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Java Platform — JDK, JRE, JVM">
  <template #content>

<div class="slide-h1" style="margin-bottom:12px;">JDK, JRE &amp; <span class="highlight">JVM</span></div>

<div class="g2" style="gap:16px;align-items:start;">

<div class="flex-col">

<div v-click class="section-label">The Layered Relationship</div>

  <div v-after style="display:flex;flex-direction:column;gap:6px;align-items:center;">
    <div style="background:#faf5ff;border:2px dashed var(--purple);border-radius:10px;padding:10px 30px;width:90%;text-align:center;">
      <div style="font-size:.62rem;color:var(--muted);font-weight:700;text-transform:uppercase;letter-spacing:1px;margin-bottom:2px;">Outermost</div>
      <div style="font-family:'Fira Code',monospace;font-weight:800;color:var(--purple);font-size:.9rem;">JDK</div>
      <div class="small-text">javac · jdb · javadoc · tools</div>
    </div>
    <div style="color:var(--muted);font-size:1.2rem;">⬇</div>
    <div style="background:#ebf8ff;border:2px dashed var(--blue);border-radius:10px;padding:10px 24px;width:76%;text-align:center;">
      <div style="font-size:.62rem;color:var(--muted);font-weight:700;text-transform:uppercase;letter-spacing:1px;margin-bottom:2px;">Inside JDK</div>
      <div style="font-family:'Fira Code',monospace;font-weight:800;color:var(--blue);font-size:.9rem;">JRE</div>
      <div class="small-text">Core libraries · java.lang · java.util</div>
    </div>
    <div style="color:var(--muted);font-size:1.2rem;">⬇</div>
    <div style="background:var(--red-soft);border:2px dashed var(--red);border-radius:10px;padding:10px 18px;width:60%;text-align:center;">
      <div style="font-size:.62rem;color:var(--muted);font-weight:700;text-transform:uppercase;letter-spacing:1px;margin-bottom:2px;">Inside JRE</div>
      <div style="font-family:'Fira Code',monospace;font-weight:800;color:var(--red-dark);font-size:.9rem;">JVM</div>
      <div class="small-text">Bytecode interpreter · JIT</div>
    </div>
  </div>
</div>

<div class="flex-col">
<div style="display:flex;flex-direction:column;gap:8px;">
    <div v-click style="background:#faf5ff;border:2px solid var(--purple);border-radius:10px;padding:12px 16px;">
      <div style="display:flex;align-items:center;gap:8px;margin-bottom:4px;">
        <span class="slide-h3">Java Development Kit</span>
      </div>
      <div class="small-text">The <strong>complete toolkit</strong> for developers. Includes the compiler (<span class="mono">javac</span>), debugger, and the JRE. <strong>Install this to write Java programs.</strong></div>
    </div>
    <div v-click style="background:#ebf8ff;border:2px solid var(--blue);border-radius:10px;padding:12px 16px;">
      <div style="display:flex;align-items:center;gap:8px;margin-bottom:4px;">
        <span class="slide-h3">Java Runtime Environment</span>
      </div>
      <div class="small-text">Everything needed to <strong>run</strong> a Java program. Includes the JVM and core libraries. No compiler included.</div>
    </div>
    <div v-click style="background:var(--red-soft);border:2px solid var(--red);border-radius:10px;padding:12px 16px;">
      <div style="display:flex;align-items:center;gap:8px;margin-bottom:4px;">
        <span class="slide-h3">Java Virtual Machine</span>
      </div>
      <div class="small-text">The engine that <strong>executes bytecode</strong>. Translates .class files into machine instructions for your OS.</div>
    </div>

  </div>
  
</div>

</div>

  </template>
</Slide2>
