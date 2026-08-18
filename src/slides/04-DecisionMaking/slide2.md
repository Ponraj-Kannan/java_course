---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 2 — OPERATORS RECAP FOR CONDITIONS
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Decision-making statements">
  <template #content>
<div class="slide-h1" style="margin-bottom:12px;">Conditions: <span class="highlight">Relational & Logical Operators</span></div>

<div class="g2" style="gap:14px;">

<div class="flex-col" style="gap:8px;">
  <div v-click class="slide-h3">Relational Operators (Compare Values)</div>
  <table class="cmp-table" style="font-size:.7rem;">
    <thead>
      <tr><th>Operator</th><th>Name</th><th>Example (`a=10, b=20`)</th><th>Result</th></tr>
    </thead>
    <tbody>
      <tr v-click><td><code>==</code></td><td>Equal to</td><td><code>a == b</code></td><td class="no">false</td></tr>
      <tr v-click><td><code>!=</code></td><td>Not equal to</td><td><code>a != b</code></td><td class="yes">true</td></tr>
      <tr v-click><td><code>&gt;</code></td><td>Greater than</td><td><code>a &gt; b</code></td><td class="no">false</td></tr>
      <tr v-click><td><code>&lt;</code></td><td>Less than</td><td><code>a &lt; b</code></td><td class="yes">true</td></tr>
      <tr v-click><td><code>&gt;=</code></td><td>Greater or equal</td><td><code>a &gt;= 10</code></td><td class="yes">true</td></tr>
      <tr v-click><td><code>&lt;=</code></td><td>Less or equal</td><td><code>b &lt;= 15</code></td><td class="no">false</td></tr>
    </tbody>
  </table>
</div>

<div class="flex-col" style="gap:8px;">
  <div v-click class="slide-h3">Logical Operators (Combine Conditions)</div>
  <table class="cmp-table" style="font-size:.7rem;">
    <thead>
      <tr><th>Operator</th><th>Name</th><th>Rule</th><th>Example</th></tr>
    </thead>
    <tbody>
      <tr v-click>
        <td><code>&amp;&amp;</code></td>
        <td>AND</td>
        <td><code>true</code> only if <strong>both</strong> operands are true</td>
        <td><code>(x &gt; 0 &amp;&amp; x &lt; 10)</code></td>
      </tr>
      <tr v-click>
        <td><code>||</code></td>
        <td>OR</td>
        <td><code>true</code> if <strong>at least one</strong> operand is true</td>
        <td><code>(age &lt; 18 || age &gt; 60)</code></td>
      </tr>
      <tr v-click>
        <td><code>!</code></td>
        <td>NOT</td>
        <td>Inverts boolean value (true ↔ false)</td>
        <td><code>!(isLoggedIn)</code></td>
      </tr>
    </tbody>
  </table>

  <div v-click class="callout callout-warn" style="margin-top:4px;">
    <div><strong>Java Gotcha:</strong> Never use a single <code>=</code> in a condition! <code>if (x = 5)</code> will cause a <strong>compiler error</strong> in Java because <code>5</code> is an <code>int</code>, not a <code>boolean</code>.</div>
  </div>
</div>

</div>
  </template>
</Slide2>
