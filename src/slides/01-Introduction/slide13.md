---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 13 — JAVA PROGRAM STRUCTURE
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Java Program Structure">
  <template #content>

<div class="slide-h1" style="margin-bottom:12px;">Java <span class="highlight">Program Structure</span></div>

<div class="g2" style="gap:14px;align-items:start;">

<div class="flex-col">

  <div v-click class="card-navy" style="border-radius:10px;">
    <div style="font-size:.82rem;line-height:1.6;color:var(--slate);">
      Every Java program has a <strong style="color:var(--red);">well-defined structure</strong>. Understanding this structure is the foundation of all Java programming.
    </div>
  </div>

  <div v-click class="callout callout-warn">
    <div><strong>Rule:</strong> The filename must <strong>exactly match</strong> the public class name — including capitalisation!</div>
  </div>

  <div v-click style="background:#f6f8fa;border-radius:10px;border:1px solid #e1e4e8;padding:14px;font-family:'Fira Code',monospace;font-size:.75rem;line-height:2;">
    <span style="color:#6b7280;">// File: StudentInfo.java</span><br>
    <span style="color:#ef5050;">public class</span> <span style="color:#0e6ead;">StudentInfo</span> {<br>
    &nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#ef5050;">public static void</span> <span style="color:#2d7a00;">main</span>(<span style="color:#ef5050;">String</span>[] args) {<br>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#2d7a00;">System.out.println</span>(<span style="color:#2d7a00;">"Name: Alice"</span>);<br>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#2d7a00;">System.out.println</span>(<span style="color:#2d7a00;">"Age: 20"</span>);<br>
    &nbsp;&nbsp;&nbsp;&nbsp;}<br>
    }
  </div>

</div>

<div class="flex-col">

  <div v-click class="section-label">Structure Layers (Outer → Inner)</div>

  <div style="display:flex;flex-direction:column;gap:8px;">
    <div v-click style="display:flex;align-items:center;gap:10px;">
      <div style="background:#faf5ff;border:2px dashed var(--purple);border-radius:10px;padding:10px 18px;min-width:100px;text-align:center;">
        <div style="font-size:.62rem;color:var(--muted);font-weight:700;text-transform:uppercase;letter-spacing:1px;margin-bottom:4px;">Layer 1</div>
        <div style="font-family:'Fira Code',monospace;font-weight:800;color:var(--purple);font-size:.82rem;">class</div>
      </div>
      <div class="small-text">The outer wrapper — every Java file needs at least one class.</div>
    </div>
    <div v-click style="display:flex;align-items:center;gap:10px;">
      <div style="background:#ebf8ff;border:2px dashed var(--blue);border-radius:10px;padding:10px 18px;min-width:100px;text-align:center;">
        <div style="font-size:.62rem;color:var(--muted);font-weight:700;text-transform:uppercase;letter-spacing:1px;margin-bottom:4px;">Layer 2</div>
        <div style="font-family:'Fira Code',monospace;font-weight:800;color:var(--blue);font-size:.75rem;">main( )</div>
      </div>
      <div class="small-text">The execution entry point — JVM calls this first.</div>
    </div>
    <div v-click style="display:flex;align-items:center;gap:10px;">
      <div style="background:#f0fff4;border:2px dashed var(--green);border-radius:10px;padding:10px 18px;min-width:100px;text-align:center;">
        <div style="font-size:.62rem;color:var(--muted);font-weight:700;text-transform:uppercase;letter-spacing:1px;margin-bottom:4px;">Layer 3</div>
        <div style="font-family:'Fira Code',monospace;font-weight:800;color:var(--green);font-size:.65rem;">statements;</div>
      </div>
      <div class="small-text">The actual instructions — each must end with a semicolon <span class="mono">;</span></div>
    </div>

  </div>

  <div v-click class="card card-blue" style="margin-top:4px;">
    <div class="small-text"><strong>Java is verbose by design:</strong> More boilerplate = more clarity about what runs, where, and who has access to it.</div>
  </div>

</div>

</div>

  </template>
</Slide2>
