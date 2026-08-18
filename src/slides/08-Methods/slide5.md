---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 5 — THE main() METHOD DECONSTRUCTED
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Java Methods">
  <template #content>

<div class="slide-h1" style="margin-bottom:10px;">The <span class="highlight">main()</span> Method Deconstructed</div>

<div class="g2" style="gap:14px;align-items:start;">

<div class="flex-col">

  <div v-click class="card-navy" style="border-radius:10px;">
    <div style="font-size:.82rem;line-height:1.6;color:var(--slate);">
      The <span class="mono" style="color:var(--red);font-weight:700;">public static void main(String[] args)</span> signature is the <strong>standard entry point</strong> predefined by the JVM specification to begin program execution.
    </div>
  </div>

  <div v-click class="section-label" style="margin-top:6px;">Keyword-by-Keyword Breakdown</div>

  <div style="display:flex;flex-direction:column;gap:5px;">
    <div v-click class="card" style="padding:6px 10px;border-left:4px solid #38bdf8;">
      <span class="pill pill-blue" style="font-size:.62rem;">public</span>
      <span style="font-size:.68rem;color:var(--slate);margin-left:6px;">Must be globally visible so JVM can invoke it from outside the package.</span>
    </div>
    <div v-click class="card" style="padding:6px 10px;border-left:4px solid #f59e0b;">
      <span class="pill pill-orange" style="font-size:.62rem;">static</span>
      <span style="font-size:.68rem;color:var(--slate);margin-left:6px;">Allows JVM to call <span class="mono">main()</span> without first creating an instance of the class.</span>
    </div>
    <div v-click class="card" style="padding:6px 10px;border-left:4px solid #a855f7;">
      <span class="pill pill-purple" style="font-size:.62rem;">void</span>
      <span style="font-size:.68rem;color:var(--slate);margin-left:6px;">Returns nothing to the JVM upon termination.</span>
    </div>
    <div v-click class="card" style="padding:6px 10px;border-left:4px solid #22c55e;">
      <span class="pill pill-green" style="font-size:.62rem;">main</span>
      <span style="font-size:.68rem;color:var(--slate);margin-left:6px;">The exact identifier name the JVM runtime searches for as the entry hook.</span>
    </div>
    <div v-click class="card" style="padding:6px 10px;border-left:4px solid #ef5050;">
      <span class="pill pill-red" style="font-size:.62rem;">String[] args</span>
      <span style="font-size:.68rem;color:var(--slate);margin-left:6px;">Array parameter receiving command-line arguments passed at startup.</span>
    </div>
  </div>

</div>

<div class="flex-col">
  <div v-click class="section-label">Execution Flow by JVM</div>

  <div v-after style="background:#f7f8fc;border:1px solid var(--border);border-radius:10px;padding:12px;font-size:.68rem;line-height:1.8;">
    <div style="font-weight:700;color:var(--navy);margin-bottom:6px;">How JVM Launches Your Java App:</div>
    <div style="display:flex;flex-direction:column;gap:4px;font-family:'Fira Code',monospace;">
      <div style="background:#fff;border:1px solid var(--border);padding:4px 8px;border-radius:4px;">1. $ java MyApp arg1 arg2</div>
      <div style="text-align:center;color:var(--blue);font-weight:700;">↓</div>
      <div style="background:#ebf8ff;border:1px solid var(--blue);padding:4px 8px;border-radius:4px;">2. JVM loads MyApp.class into memory</div>
      <div style="text-align:center;color:var(--blue);font-weight:700;">↓</div>
      <div style="background:#f0fff4;border:1px solid var(--green);padding:4px 8px;border-radius:4px;">3. JVM locates exact signature: public static void main(...)</div>
      <div style="text-align:center;color:var(--blue);font-weight:700;">↓</div>
      <div style="background:#fdf2f8;border:1px solid #ec4899;padding:4px 8px;border-radius:4px;">4. Packages ["arg1", "arg2"] into args array &amp; starts execution</div>
    </div>
  </div>

  <div v-click class="callout callout-warn" style="margin-top:8px;">
    <div><strong>Exam / Viva Question:</strong> Can we change <span class="mono">String[] args</span> to <span class="mono">String args[]</span> or <span class="mono">String... args</span>? <strong>Yes!</strong> All three are valid signatures recognized by the JVM.</div>
  </div>

</div>

</div>

  </template>
</Slide2>
