---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 9 — LOGICAL OPERATORS & SHORT-CIRCUIT
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Operators">
  <template #content>

<div class="slide-h1" style="margin-bottom:10px;">Logical Operators &amp; <span class="highlight">Short-Circuiting</span></div>

<div class="g2" style="gap:14px;">

<div class="flex-col">

  <div v-click class="card-navy" style="border-radius:10px;">
    <div style="font-size:.8rem;line-height:1.6;color:var(--slate);">
      <strong style="color:var(--red);">Definition:</strong> <strong>Logical operators</strong> evaluate and combine multiple boolean conditions to make decision-making expressions in Java.
    </div>
  </div>

  <div style="display:flex;flex-direction:column;gap:6px;margin-top:2px;">
    <div v-click class="card-green" style="border-radius:8px;padding:8px 12px;">
      <div style="font-size:.72rem;font-weight:700;color:var(--green);margin-bottom:2px;font-family:'Fira Code',monospace;">&amp;&amp; (Logical AND)</div>
      <div style="font-size:.7rem;color:var(--slate);">Returns <span class="mono" style="color:var(--green);">true</span> only if <strong>both</strong> conditions are true</div>
    </div>
    <div v-click class="card-blue" style="border-radius:8px;padding:8px 12px;">
      <div style="font-size:.72rem;font-weight:700;color:var(--blue);margin-bottom:2px;font-family:'Fira Code',monospace;">|| (Logical OR)</div>
      <div style="font-size:.7rem;color:var(--slate);">Returns <span class="mono" style="color:var(--green);">true</span> if <strong>at least one</strong> condition is true</div>
    </div>
    <div v-click class="card-red" style="border-radius:8px;padding:8px 12px;">
      <div style="font-size:.72rem;font-weight:700;color:var(--red-dark);margin-bottom:2px;font-family:'Fira Code',monospace;">! (Logical NOT)</div>
      <div style="font-size:.7rem;color:var(--slate);">Inverts the boolean value (<span class="mono">true</span> → <span class="mono">false</span>, <span class="mono">false</span> → <span class="mono">true</span>)</div>
    </div>
  </div>

  <div v-click class="callout callout-warn" style="margin-top:4px;">
    <div><strong>Short-Circuit Evaluation:</strong><br>
    • <span class="mono">&amp;&amp;</span> skips condition 2 if condition 1 is <span class="mono">false</span>.<br>
    • <span class="mono">||</span> skips condition 2 if condition 1 is <span class="mono">true</span>.<br>
    Prevents runtime crashes (e.g. dividing by zero or <span class="mono">NullPointerException</span>)!</div>
  </div>

</div>

<div class="flex-col">
  <div v-click class="section-label">Truth Table</div>

  <div>
    <table class="cmp-table" style="font-size:.68rem;">
      <thead v-click><tr><th>A</th><th>B</th><th>A &amp;&amp; B</th><th>A || B</th><th>!A</th></tr></thead>
      <tbody>
        <tr v-click><td class="yes">true</td><td class="yes">true</td><td class="yes">true</td><td class="yes">true</td><td class="no">false</td></tr>
        <tr v-click><td class="yes">true</td><td class="no">false</td><td class="no">false</td><td class="yes">true</td><td class="no">false</td></tr>
        <tr v-click><td class="no">false</td><td class="yes">true</td><td class="no">false</td><td class="yes">true</td><td class="yes">true</td></tr>
        <tr v-click><td class="no">false</td><td class="no">false</td><td class="no">false</td><td class="no">false</td><td class="yes">true</td></tr>
      </tbody>
    </table>
  </div>

  <div v-click class="section-label" style="margin-top:6px;">Java Code Example</div>
  <div v-after style="background:#f6f8fa;border-radius:10px;border:1px solid #e1e4e8;padding:10px 14px;font-family:'Fira Code',monospace;font-size:.72rem;line-height:1.9;">
    <span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">age</span> = <span style="color:#b45309;">20</span>;<br>
    <span style="color:#ef5050;">boolean</span> <span style="color:#0e6ead;">hasLicense</span> = <span style="color:#ef5050;">true</span>;<br>
    <span style="color:#ef5050;">boolean</span> <span style="color:#0e6ead;">canDrive</span> = (<span style="color:#0e6ead;">age</span> &gt;= <span style="color:#b45309;">18</span>) &amp;&amp; <span style="color:#0e6ead;">hasLicense</span>;<br>
    <span style="color:#0e6ead;">System</span>.<span style="color:#0e6ead;">out</span>.<span style="color:#2d7a00;">println</span>(<span style="color:#0e6ead;">canDrive</span>); <span style="color:#6b7280;">// true</span>
  </div>

</div>

</div>

  </template>
</Slide2>
