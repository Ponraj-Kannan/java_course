---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 7 — INSTALLING JAVA (Setup)
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Setting Up Java">
  <template #content>

<div class="slide-h1" style="margin-bottom:12px;">Installing <span class="highlight">Java</span></div>

<div class="g2" style="gap:16px;align-items:start;">

<div class="flex-col">

  <div v-click class="section-label">Step 1 — Download the JDK</div>

  <div v-after class="card card-blue" style="margin-bottom:6px;">
    <div class="small-text"><strong>Recommended:</strong> Download <strong>Java 21 LTS</strong> (Long-Term Support) from <span class="mono" style="color:var(--blue);">adoptium.net</span> or <span class="mono" style="color:var(--blue);">oracle.com/java</span></div>
  </div>

  <div v-click class="section-label" style="margin-top:4px;">Step 2 — Install &amp; Set PATH</div>

  <div v-after style="background:#f6f8fa;border-radius:10px;border:1px solid #e1e4e8;padding:12px 14px;font-family:'Fira Code',monospace;font-size:.72rem;line-height:2;">
    <span style="color:#6b7280;"># Windows — add to System Environment Variables</span><br>
    <span style="color:#0e6ead;">JAVA_HOME</span> = <span style="color:#2d7a00;">C:\Program Files\Java\jdk-21</span><br>
    <span style="color:#0e6ead;">PATH</span> += <span style="color:#2d7a00;">%JAVA_HOME%\bin</span>
  </div>

  <div v-click class="section-label" style="margin-top:4px;">Step 3 — Verify Installation</div>

  <div v-after style="background:#f6f8fa;border-radius:10px;border:1px solid #e1e4e8;padding:12px 14px;font-family:'Fira Code',monospace;font-size:.72rem;line-height:2;">
    <span style="color:#6b7280;"># Open terminal and type:</span><br>
    <span style="color:#ef5050;">$</span> <span style="color:#0e6ead;">java</span> <span style="color:#2d7a00;">--version</span><br>
    <span style="color:#6b7280;">openjdk 21.0.x 2024-xx-xx</span><br><br>
    <span style="color:#ef5050;">$</span> <span style="color:#0e6ead;">javac</span> <span style="color:#2d7a00;">--version</span><br>
    <span style="color:#6b7280;">javac 21.0.x</span>
  </div>

</div>

<div class="flex-col">

  <div v-click class="section-label">Recommended IDE</div>

  <div v-after style="display:flex;flex-direction:column;gap:8px;">
    <div class="card" style="display:flex;gap:10px;align-items:center;border:1px solid var(--blue);">
      <div class="icon-circle ic-blue">💡</div>
      <div>
        <div class="slide-h3">IntelliJ IDEA (Recommended)</div>
        <div class="small-text">Best-in-class Java IDE. Community edition is free. Smart autocomplete, debugger, refactoring.</div>
      </div>
    </div>
    <div class="card" style="display:flex;gap:10px;align-items:center;border:1px solid var(--orange);">
      <div class="icon-circle ic-orange">🌙</div>
      <div>
        <div class="slide-h3">VS Code + Extension Pack</div>
        <div class="small-text">Lightweight option. Install "Extension Pack for Java" from Microsoft.</div>
      </div>
    </div>
    <div class="card" style="display:flex;gap:10px;align-items:center;border:1px solid var(--purple);">
      <div class="icon-circle ic-purple">🌑</div>
      <div>
        <div class="slide-h3">Eclipse IDE</div>
        <div class="small-text">Widely used in academia & enterprise. Free and open-source.</div>
      </div>
    </div>

  </div>

  <div v-click class="callout callout-warn" style="margin-top:8px;">
    <div><strong>Quick Start:</strong> For this course, any text editor + terminal will work. We focus on core concepts, not IDE features.</div>
  </div>

</div>

</div>

  </template>
</Slide2>
