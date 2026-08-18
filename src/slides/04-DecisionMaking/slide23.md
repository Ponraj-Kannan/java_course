---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 23 — IF-ELSE-IF VS SWITCH COMPARISON
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Decision-making statements">
  <template #content>
<div class="slide-h1" style="margin-bottom:14px;">if-else-if  <span class="highlight">vs</span>  switch Statement</div>

<div style="margin-top:10px;">
  <table class="cmp-table">
    <thead>
      <tr v-click>
        <th>Feature</th>
        <th>if-else-if Ladder</th>
        <th>switch Statement</th>
      </tr>
    </thead>
    <tbody>
      <tr v-click>
        <td>Condition Evaluation</td>
        <td>Evaluates <strong>boolean expressions</strong> (ranges, logical AND/OR)</td>
        <td>Evaluates <strong>equality matching</strong> against single constant value</td>
      </tr>
      <tr v-click>
        <td>Supported Types</td>
        <td>All types &amp; expressions returning <code>boolean</code></td>
        <td><code>byte</code>, <code>short</code>, <code>char</code>, <code>int</code>, <code>String</code>, <code>enum</code></td>
      </tr>
      <tr v-click>
        <td>Range Checks (<code>&gt;</code>, <code>&lt;</code>)</td>
        <td class="yes">✅ Supported natively</td>
        <td class="no">❌ Not directly supported</td>
      </tr>
      <tr v-click>
        <td>Multiple Values</td>
        <td>Requires <code>||</code> or multiple <code>else if</code> blocks</td>
        <td class="yes">✅ Comma-separated or fall-through cases</td>
      </tr>
      <tr v-click>
        <td>Default Handler</td>
        <td>Final <code>else { }</code> block</td>
        <td class="yes"><code>default:</code> label</td>
      </tr>
      <tr v-click>
        <td>Best Used For</td>
        <td>Complex range checks, floating-point comparisons</td>
        <td class="yes">Discrete menu choices, discrete integer/string codes</td>
      </tr>
    </tbody>
  </table>
</div>
  </template>
</Slide2>
