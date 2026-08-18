---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 27 — QUICK REFERENCE CHEAT SHEET
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Decision-making statements — Quick Reference">
  <template #content>
<div class="slide-h1" style="margin-bottom:12px;">📋 Java Decision Statements <span class="highlight">Cheat Sheet</span></div>

<div style="margin-top:10px;">
  <table class="cmp-table">
    <thead>
      <tr><th>Statement</th><th>Purpose</th><th>Boolean Condition Required?</th><th>Can stand alone?</th></tr>
    </thead>
    <tbody>
      <tr v-click><td class="mono" style="color:var(--red-dark);">if</td><td>Single conditional execution</td><td class="yes">✅ Yes <code>(cond)</code></td><td class="yes">✅ Yes</td></tr>
      <tr v-click><td class="mono" style="color:#744210;">if-else</td><td>Two-way true/false branching</td><td class="yes">✅ Yes (on <code>if</code>)</td><td class="yes">✅ Yes</td></tr>
      <tr v-click><td class="mono" style="color:#2b6cb0;">if-else-if</td><td>Multi-condition sequential ladder</td><td class="yes">✅ Yes (on each <code>if/else if</code>)</td><td class="no">❌ Needs <code>if</code> first</td></tr>
      <tr v-click><td class="mono" style="color:#553c9a;">switch</td><td>Multi-way discrete constant matching</td><td class="no">❌ Matching expression</td><td class="yes">✅ Yes</td></tr>
      <tr v-click><td class="mono" style="color:#276749;">(?:) Ternary</td><td>Compact 1-line conditional expression</td><td class="yes">✅ Yes</td><td class="no">❌ Returns expression</td></tr>
    </tbody>
  </table>
</div>
  </template>
</Slide2>
