---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 21 — NAMING RULE 5: Cannot be a reserved keyword
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Variable Naming Rules">
  <template #content>

<div class="slide-h1" style="margin-bottom:10px;"><span class="highlight">Rule 5</span> — Cannot Be a Reserved Keyword</div>

<div class="g2" style="gap:14px;align-items:start;">

<div class="flex-col">

  <div v-click style="display:flex;gap:10px;align-items:center;margin-bottom:4px;">
    <div style="background:var(--red);color:#fff;border-radius:8px;padding:6px 16px;font-size:.75rem;font-weight:800;">RULE 5</div>
    <div class="body-text" style="font-size:.82rem;">A variable name <strong>cannot be a Java reserved keyword</strong>. These words have special meaning to the compiler and cannot be redefined.</div>
  </div>

  <div v-click class="section-label">✘ Invalid Examples</div>

  <div v-after style="background:var(--red-soft);border-radius:10px;border:1px solid var(--red);padding:12px 14px;font-family:'Fira Code',monospace;font-size:.76rem;line-height:1.9;">
    <span style="color:#ef5050;">int</span> <span style="color:#ef5050;">int</span> = <span style="color:#b45309;">5</span>;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#6b7280;">// ✘ 'int' is a keyword</span><br>
    <span style="color:#ef5050;">String</span> <span style="color:#ef5050;">class</span> = <span style="color:#2d7a00;">"A"</span>;<span style="color:#6b7280;"> // ✘ 'class' is a keyword</span><br>
    <span style="color:#ef5050;">boolean</span> <span style="color:#ef5050;">for</span> = <span style="color:#b45309;">true</span>;<span style="color:#6b7280;">// ✘ 'for' is a keyword</span>
  </div>

  <div v-click class="callout callout-danger" style="margin-top:4px;">
    <div><strong>Compiler error:</strong> <span class="mono">error: illegal start of expression</span> — the compiler expected a variable name but found a keyword it already has a special use for.</div>
  </div>

  <div v-click class="section-label" style="margin-top:6px;">✔ Fix — Use Descriptive Alternatives</div>
  <div v-after style="background:#f6f8fa;border-radius:10px;border:1px solid #e1e4e8;padding:12px 14px;font-family:'Fira Code',monospace;font-size:.76rem;line-height:1.9;">
    <span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">count</span> = <span style="color:#b45309;">5</span>;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#6b7280;">// ✔ instead of 'int'</span><br>
    <span style="color:#ef5050;">String</span> <span style="color:#0e6ead;">className</span> = <span style="color:#2d7a00;">"A"</span>;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#6b7280;">// ✔ instead of 'class'</span><br>
    <span style="color:#ef5050;">boolean</span> <span style="color:#0e6ead;">forLoop</span> = <span style="color:#b45309;">true</span>;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#6b7280;">// ✔ instead of 'for'</span>
  </div>

</div>

<div class="flex-col">

  <div v-click class="section-label">Java Reserved Keywords</div>
  <div v-click class="small-text" style="margin-bottom:6px;">These 50+ words cannot be used as variable names:</div>

  <div style="display:flex;gap:4px;flex-wrap:wrap;">
    <span v-click style="background:var(--red-soft);color:var(--red-dark);border:1px solid var(--red);border-radius:6px;padding:3px 9px;font-family:'Fira Code',monospace;font-size:.65rem;font-weight:700;">abstract</span>
    <span v-after style="background:var(--red-soft);color:var(--red-dark);border:1px solid var(--red);border-radius:6px;padding:3px 9px;font-family:'Fira Code',monospace;font-size:.65rem;font-weight:700;">assert</span>
    <span v-after style="background:var(--red-soft);color:var(--red-dark);border:1px solid var(--red);border-radius:6px;padding:3px 9px;font-family:'Fira Code',monospace;font-size:.65rem;font-weight:700;">boolean</span>
    <span v-after style="background:var(--red-soft);color:var(--red-dark);border:1px solid var(--red);border-radius:6px;padding:3px 9px;font-family:'Fira Code',monospace;font-size:.65rem;font-weight:700;">break</span>
    <span v-after style="background:var(--red-soft);color:var(--red-dark);border:1px solid var(--red);border-radius:6px;padding:3px 9px;font-family:'Fira Code',monospace;font-size:.65rem;font-weight:700;">byte</span>
    <span v-after style="background:var(--red-soft);color:var(--red-dark);border:1px solid var(--red);border-radius:6px;padding:3px 9px;font-family:'Fira Code',monospace;font-size:.65rem;font-weight:700;">case</span>
    <span v-after style="background:var(--red-soft);color:var(--red-dark);border:1px solid var(--red);border-radius:6px;padding:3px 9px;font-family:'Fira Code',monospace;font-size:.65rem;font-weight:700;">catch</span>
    <span v-after style="background:var(--red-soft);color:var(--red-dark);border:1px solid var(--red);border-radius:6px;padding:3px 9px;font-family:'Fira Code',monospace;font-size:.65rem;font-weight:700;">char</span>
    <span v-after style="background:var(--red-soft);color:var(--red-dark);border:1px solid var(--red);border-radius:6px;padding:3px 9px;font-family:'Fira Code',monospace;font-size:.65rem;font-weight:700;">class</span>
    <span v-after style="background:var(--red-soft);color:var(--red-dark);border:1px solid var(--red);border-radius:6px;padding:3px 9px;font-family:'Fira Code',monospace;font-size:.65rem;font-weight:700;">const</span>
    <span v-after style="background:var(--red-soft);color:var(--red-dark);border:1px solid var(--red);border-radius:6px;padding:3px 9px;font-family:'Fira Code',monospace;font-size:.65rem;font-weight:700;">continue</span>
    <span v-after style="background:var(--red-soft);color:var(--red-dark);border:1px solid var(--red);border-radius:6px;padding:3px 9px;font-family:'Fira Code',monospace;font-size:.65rem;font-weight:700;">default</span>
    <span v-after style="background:var(--red-soft);color:var(--red-dark);border:1px solid var(--red);border-radius:6px;padding:3px 9px;font-family:'Fira Code',monospace;font-size:.65rem;font-weight:700;">do</span>
    <span v-after style="background:var(--red-soft);color:var(--red-dark);border:1px solid var(--red);border-radius:6px;padding:3px 9px;font-family:'Fira Code',monospace;font-size:.65rem;font-weight:700;">double</span>
    <span v-after style="background:var(--red-soft);color:var(--red-dark);border:1px solid var(--red);border-radius:6px;padding:3px 9px;font-family:'Fira Code',monospace;font-size:.65rem;font-weight:700;">else</span>
    <span v-after style="background:var(--red-soft);color:var(--red-dark);border:1px solid var(--red);border-radius:6px;padding:3px 9px;font-family:'Fira Code',monospace;font-size:.65rem;font-weight:700;">enum</span>
    <span v-after style="background:var(--red-soft);color:var(--red-dark);border:1px solid var(--red);border-radius:6px;padding:3px 9px;font-family:'Fira Code',monospace;font-size:.65rem;font-weight:700;">extends</span>
    <span v-after style="background:var(--red-soft);color:var(--red-dark);border:1px solid var(--red);border-radius:6px;padding:3px 9px;font-family:'Fira Code',monospace;font-size:.65rem;font-weight:700;">final</span>
    <span v-after style="background:var(--red-soft);color:var(--red-dark);border:1px solid var(--red);border-radius:6px;padding:3px 9px;font-family:'Fira Code',monospace;font-size:.65rem;font-weight:700;">finally</span>
    <span v-after style="background:var(--red-soft);color:var(--red-dark);border:1px solid var(--red);border-radius:6px;padding:3px 9px;font-family:'Fira Code',monospace;font-size:.65rem;font-weight:700;">float</span>
    <span v-after style="background:var(--red-soft);color:var(--red-dark);border:1px solid var(--red);border-radius:6px;padding:3px 9px;font-family:'Fira Code',monospace;font-size:.65rem;font-weight:700;">for</span>
    <span v-after style="background:var(--red-soft);color:var(--red-dark);border:1px solid var(--red);border-radius:6px;padding:3px 9px;font-family:'Fira Code',monospace;font-size:.65rem;font-weight:700;">goto</span>
    <span v-after style="background:var(--red-soft);color:var(--red-dark);border:1px solid var(--red);border-radius:6px;padding:3px 9px;font-family:'Fira Code',monospace;font-size:.65rem;font-weight:700;">if</span>
    <span v-after style="background:var(--red-soft);color:var(--red-dark);border:1px solid var(--red);border-radius:6px;padding:3px 9px;font-family:'Fira Code',monospace;font-size:.65rem;font-weight:700;">implements</span>
    <span v-after style="background:var(--red-soft);color:var(--red-dark);border:1px solid var(--red);border-radius:6px;padding:3px 9px;font-family:'Fira Code',monospace;font-size:.65rem;font-weight:700;">import</span>
    <span v-after style="background:var(--red-soft);color:var(--red-dark);border:1px solid var(--red);border-radius:6px;padding:3px 9px;font-family:'Fira Code',monospace;font-size:.65rem;font-weight:700;">instanceof</span>
    <span v-after style="background:var(--red-soft);color:var(--red-dark);border:1px solid var(--red);border-radius:6px;padding:3px 9px;font-family:'Fira Code',monospace;font-size:.65rem;font-weight:700;">int</span>
    <span v-after style="background:var(--red-soft);color:var(--red-dark);border:1px solid var(--red);border-radius:6px;padding:3px 9px;font-family:'Fira Code',monospace;font-size:.65rem;font-weight:700;">interface</span>
    <span v-after style="background:var(--red-soft);color:var(--red-dark);border:1px solid var(--red);border-radius:6px;padding:3px 9px;font-family:'Fira Code',monospace;font-size:.65rem;font-weight:700;">long</span>
    <span v-after style="background:var(--red-soft);color:var(--red-dark);border:1px solid var(--red);border-radius:6px;padding:3px 9px;font-family:'Fira Code',monospace;font-size:.65rem;font-weight:700;">native</span>
    <span v-after style="background:var(--red-soft);color:var(--red-dark);border:1px solid var(--red);border-radius:6px;padding:3px 9px;font-family:'Fira Code',monospace;font-size:.65rem;font-weight:700;">new</span>
    <span v-after style="background:var(--red-soft);color:var(--red-dark);border:1px solid var(--red);border-radius:6px;padding:3px 9px;font-family:'Fira Code',monospace;font-size:.65rem;font-weight:700;">package</span>
    <span v-after style="background:var(--red-soft);color:var(--red-dark);border:1px solid var(--red);border-radius:6px;padding:3px 9px;font-family:'Fira Code',monospace;font-size:.65rem;font-weight:700;">private</span>
    <span v-after style="background:var(--red-soft);color:var(--red-dark);border:1px solid var(--red);border-radius:6px;padding:3px 9px;font-family:'Fira Code',monospace;font-size:.65rem;font-weight:700;">protected</span>
    <span v-after style="background:var(--red-soft);color:var(--red-dark);border:1px solid var(--red);border-radius:6px;padding:3px 9px;font-family:'Fira Code',monospace;font-size:.65rem;font-weight:700;">public</span>
    <span v-after style="background:var(--red-soft);color:var(--red-dark);border:1px solid var(--red);border-radius:6px;padding:3px 9px;font-family:'Fira Code',monospace;font-size:.65rem;font-weight:700;">return</span>
    <span v-after style="background:var(--red-soft);color:var(--red-dark);border:1px solid var(--red);border-radius:6px;padding:3px 9px;font-family:'Fira Code',monospace;font-size:.65rem;font-weight:700;">short</span>
    <span v-after style="background:var(--red-soft);color:var(--red-dark);border:1px solid var(--red);border-radius:6px;padding:3px 9px;font-family:'Fira Code',monospace;font-size:.65rem;font-weight:700;">static</span>
    <span v-after style="background:var(--red-soft);color:var(--red-dark);border:1px solid var(--red);border-radius:6px;padding:3px 9px;font-family:'Fira Code',monospace;font-size:.65rem;font-weight:700;">strictfp</span>
    <span v-after style="background:var(--red-soft);color:var(--red-dark);border:1px solid var(--red);border-radius:6px;padding:3px 9px;font-family:'Fira Code',monospace;font-size:.65rem;font-weight:700;">super</span>
    <span v-after style="background:var(--red-soft);color:var(--red-dark);border:1px solid var(--red);border-radius:6px;padding:3px 9px;font-family:'Fira Code',monospace;font-size:.65rem;font-weight:700;">switch</span>
    <span v-after style="background:var(--red-soft);color:var(--red-dark);border:1px solid var(--red);border-radius:6px;padding:3px 9px;font-family:'Fira Code',monospace;font-size:.65rem;font-weight:700;">synchronized</span>
    <span v-after style="background:var(--red-soft);color:var(--red-dark);border:1px solid var(--red);border-radius:6px;padding:3px 9px;font-family:'Fira Code',monospace;font-size:.65rem;font-weight:700;">this</span>
    <span v-after style="background:var(--red-soft);color:var(--red-dark);border:1px solid var(--red);border-radius:6px;padding:3px 9px;font-family:'Fira Code',monospace;font-size:.65rem;font-weight:700;">throw</span>
    <span v-after style="background:var(--red-soft);color:var(--red-dark);border:1px solid var(--red);border-radius:6px;padding:3px 9px;font-family:'Fira Code',monospace;font-size:.65rem;font-weight:700;">throws</span>
    <span v-after style="background:var(--red-soft);color:var(--red-dark);border:1px solid var(--red);border-radius:6px;padding:3px 9px;font-family:'Fira Code',monospace;font-size:.65rem;font-weight:700;">transient</span>
    <span v-after style="background:var(--red-soft);color:var(--red-dark);border:1px solid var(--red);border-radius:6px;padding:3px 9px;font-family:'Fira Code',monospace;font-size:.65rem;font-weight:700;">try</span>
    <span v-after style="background:var(--red-soft);color:var(--red-dark);border:1px solid var(--red);border-radius:6px;padding:3px 9px;font-family:'Fira Code',monospace;font-size:.65rem;font-weight:700;">void</span>
    <span v-after style="background:var(--red-soft);color:var(--red-dark);border:1px solid var(--red);border-radius:6px;padding:3px 9px;font-family:'Fira Code',monospace;font-size:.65rem;font-weight:700;">volatile</span>
    <span v-after style="background:var(--red-soft);color:var(--red-dark);border:1px solid var(--red);border-radius:6px;padding:3px 9px;font-family:'Fira Code',monospace;font-size:.65rem;font-weight:700;">while</span>
  </div>

</div>

</div>

  </template>
</Slide2>
