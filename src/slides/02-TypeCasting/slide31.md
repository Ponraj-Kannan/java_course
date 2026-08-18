---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 31 — TYPE CASTING IN JAVA
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Type Casting in Java">
  <template #content>

<div class="slide-h1" style="margin-bottom:10px;">Type <span class="highlight">Casting</span> &amp; Conversion</div>

<div class="g2" style="gap:14px;">

<div class="flex-col">

  <div v-click class="section-label">Widening (Automatic / Implicit)</div>
  <div v-after style="background:#f6f8fa;border-radius:10px;border:1px solid #e1e4e8;padding:12px 14px;font-family:'Fira Code',monospace;font-size:.72rem;line-height:2;">
    <span style="color:#6b7280;">// Smaller → Larger type (safe, automatic)</span><br>
    <span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">num</span> = <span style="color:#b45309;">42</span>;<br>
    <span style="color:#ef5050;">double</span> <span style="color:#0e6ead;">d</span> = <span style="color:#0e6ead;">num</span>; <span style="color:#6b7280;">// int → double</span><br>
    <span style="color:#ef5050;">long</span> <span style="color:#0e6ead;">l</span> = <span style="color:#0e6ead;">num</span>;  <span style="color:#6b7280;">// int → long</span>
  </div>

  <div v-click class="section-label" style="margin-top:6px;">Narrowing (Manual / Explicit Cast)</div>
  <div v-after style="background:#f6f8fa;border-radius:10px;border:1px solid #e1e4e8;padding:12px 14px;font-family:'Fira Code',monospace;font-size:.72rem;line-height:2;">
    <span style="color:#6b7280;">// Larger → Smaller type (may lose data!)</span><br>
    <span style="color:#ef5050;">double</span> <span style="color:#0e6ead;">pi</span> = <span style="color:#b45309;">3.14159</span>;<br>
    <span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">approx</span> = (<span style="color:#ef5050;">int</span>) <span style="color:#0e6ead;">pi</span>; <span style="color:#6b7280;">// → 3 (decimal lost!)</span><br>
    <span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">big</span> = <span style="color:#b45309;">300</span>;<br>
    <span style="color:#ef5050;">byte</span> <span style="color:#0e6ead;">b</span> = (<span style="color:#ef5050;">byte</span>) <span style="color:#0e6ead;">big</span>; <span style="color:#6b7280;">// → 44 (overflow!)</span>
  </div>

  <div v-click class="callout callout-danger" style="margin-top:6px;">
    <div><strong>⚠️ Data loss risk!</strong> Narrowing casts can silently truncate decimals or overflow integer values.</div>
  </div>

</div>

<div class="flex-col">

  <div v-click class="section-label">Conversion Flow Diagram</div>

  <div style="display:flex;flex-direction:column;gap:6px;">
    <div style="display:flex;align-items:center;gap:6px;" v-click>
      <div style="background:var(--red-soft);border:1px solid var(--red);border-radius:6px;padding:5px 12px;font-family:'Fira Code',monospace;font-size:.72rem;font-weight:700;color:var(--red-dark);min-width:60px;text-align:center;">42</div>
      <div style="font-size:.65rem;color:var(--muted);">int</div>
      <div style="color:var(--muted);">→ (double) →</div>
      <div style="background:#f0fff4;border:1px solid var(--green);border-radius:6px;padding:5px 12px;font-family:'Fira Code',monospace;font-size:.72rem;font-weight:700;color:var(--green);">42.0</div>
      <div style="font-size:.65rem;color:var(--muted);">double</div>
    </div>
    <div style="display:flex;align-items:center;gap:6px;" v-click>
      <div style="background:#f0fff4;border:1px solid var(--green);border-radius:6px;padding:5px 12px;font-family:'Fira Code',monospace;font-size:.72rem;font-weight:700;color:var(--green);min-width:60px;text-align:center;">3.14</div>
      <div style="font-size:.65rem;color:var(--muted);">double</div>
      <div style="color:var(--muted);">→ (int) →</div>
      <div style="background:var(--red-soft);border:1px solid var(--red);border-radius:6px;padding:5px 12px;font-family:'Fira Code',monospace;font-size:.72rem;font-weight:700;color:var(--red-dark);">3</div>
      <div style="font-size:.65rem;color:var(--muted);">int ⚠️</div>
    </div>
    <div style="display:flex;align-items:center;gap:6px;" v-click>
      <div style="background:#ebf8ff;border:1px solid var(--blue);border-radius:6px;padding:5px 12px;font-family:'Fira Code',monospace;font-size:.72rem;font-weight:700;color:var(--blue);min-width:60px;text-align:center;">"42"</div>
      <div style="font-size:.65rem;color:var(--muted);">String</div>
      <div style="color:var(--muted);">→ Integer.parseInt() →</div>
      <div style="background:var(--red-soft);border:1px solid var(--red);border-radius:6px;padding:5px 12px;font-family:'Fira Code',monospace;font-size:.72rem;font-weight:700;color:var(--red-dark);">42</div>
      <div style="font-size:.65rem;color:var(--muted);">int</div>
    </div>
  </div>

  <div v-click class="section-label" style="margin-top:6px;">String ↔ Primitive</div>
  <div v-after style="background:#f6f8fa;border-radius:10px;border:1px solid #e1e4e8;padding:12px 14px;font-family:'Fira Code',monospace;font-size:.72rem;line-height:2;">
    <span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">x</span> = <span style="color:#ef5050;">Integer</span>.parseInt(<span style="color:#2d7a00;">"42"</span>); <span style="color:#6b7280;">// str→int</span><br>
    <span style="color:#ef5050;">double</span> <span style="color:#0e6ead;">y</span> = <span style="color:#ef5050;">Double</span>.parseDouble(<span style="color:#2d7a00;">"3.14"</span>);<br>
    <span style="color:#ef5050;">String</span> <span style="color:#0e6ead;">s</span> = <span style="color:#ef5050;">String</span>.valueOf(<span style="color:#b45309;">99</span>); <span style="color:#6b7280;">// int→str</span>
  </div>

  <div v-click class="callout callout-success" style="margin-top:6px;">
    <div><strong>Best practice:</strong> Wrap <span class="mono">Integer.parseInt()</span> in a <span class="mono">try-catch</span> block to handle invalid inputs gracefully.</div>
  </div>

</div>
</div>

  </template>
</Slide2>
