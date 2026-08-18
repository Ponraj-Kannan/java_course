---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 28 — JAVA DATA TYPES (Primitive overview)
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Java Primitive Data Types">
  <template #content>

<div class="slide-h1" style="margin-bottom:12px;">Java <span class="highlight">Data Types</span> Overview</div>

<div class="g2" style="gap:14px;align-items:start;">

<div class="flex-col">

  <div v-click class="card-navy" style="border-radius:10px;">
    <div style="font-size:.82rem;line-height:1.6;color:var(--slate);">
      Java has <strong style="color:var(--red);">8 primitive types</strong> — they store simple values directly in memory, not objects. You must declare the type before using a variable.
    </div>
  </div>

<table class="cmp-table" style="margin-top:8px;">
  <thead>
    <tr>
      <th>Type</th>
      <th>Size</th>
      <th>Example Value</th>
    </tr>
  </thead>
  <tbody>
    <tr v-click>
      <td><span class="mono" style="color:var(--red-dark);">byte</span></td>
      <td>8 bits</td>
      <td><span class="mono">127</span></td>
    </tr>
    <tr v-click>
      <td><span class="mono" style="color:var(--red-dark);">short</span></td>
      <td>16 bits</td>
      <td><span class="mono">32767</span></td>
    </tr>
    <tr v-click>
      <td><span class="mono" style="color:var(--red-dark);">int</span></td>
      <td>32 bits</td>
      <td><span class="mono">2,147,483,647</span></td>
    </tr>
    <tr v-click>
      <td><span class="mono" style="color:var(--red-dark);">long</span></td>
      <td>64 bits</td>
      <td><span class="mono">100L</span></td>
    </tr>
    <tr v-click>
      <td><span class="mono" style="color:var(--blue);">float</span></td>
      <td>32 bits</td>
      <td><span class="mono">3.14f</span></td>
    </tr>
    <tr v-click>
      <td><span class="mono" style="color:var(--blue);">double</span></td>
      <td>64 bits</td>
      <td><span class="mono">3.14159</span></td>
    </tr>
    <tr v-click>
      <td><span class="mono" style="color:var(--green);">char</span></td>
      <td>16 bits</td>
      <td><span class="mono">'A'</span></td>
    </tr>
    <tr v-click>
      <td><span class="mono" style="color:var(--orange);">boolean</span></td>
      <td>1 bit</td>
      <td><span class="mono">true / false</span></td>
    </tr>
  </tbody>
</table>

</div>

<div class="flex-col">

  <div v-click class="section-label">Declaring Variables</div>

  <div v-after style="background:#f6f8fa;border-radius:10px;border:1px solid #e1e4e8;padding:14px;font-family:'Fira Code',monospace;font-size:.74rem;line-height:2;">
    <span style="color:#6b7280;">// type variableName = value;</span><br>
    <span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">age</span> = <span style="color:#b45309;">20</span>;<br>
    <span style="color:#ef5050;">double</span> <span style="color:#0e6ead;">gpa</span> = <span style="color:#b45309;">9.2</span>;<br>
    <span style="color:#ef5050;">char</span> <span style="color:#0e6ead;">grade</span> = <span style="color:#2d7a00;">'A'</span>;<br>
    <span style="color:#ef5050;">boolean</span> <span style="color:#0e6ead;">passed</span> = <span style="color:#b45309;">true</span>;<br>
    <span style="color:#ef5050;">String</span> <span style="color:#0e6ead;">name</span> = <span style="color:#2d7a00;">"Alice"</span>;<span style="color:#6b7280;"> // not a primitive!</span>
  </div>

  <div v-click class="callout callout-warn" style="margin-top:8px;">
    <div><strong>Note:</strong> <span class="mono">String</span> is <strong>not</strong> a primitive type — it's a class. But it's used so frequently that Java gives it special support.</div>
  </div>

  <div v-click class="card card-green" style="margin-top:6px;">
    <div class="small-text"><strong>Java 10+ tip:</strong> Use <span class="mono">var</span> for local variables — the compiler infers the type: <span class="mono">var age = 20;</span> → type is <span class="mono">int</span>.</div>
  </div>

</div>

</div>

  </template>
</Slide2>
