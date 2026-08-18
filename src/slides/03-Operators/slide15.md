---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 15 — OPERATOR PRECEDENCE AND ASSOCIATIVITY
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Operators">
  <template #content>

<div class="slide-h1" style="margin-bottom:10px;">Operator <span class="highlight">Precedence</span> &amp; Associativity</div>

<div class="g2" style="gap:14px;">

<div class="flex-col">

  <div v-click class="card-navy" style="border-radius:10px;">
    <div style="font-size:.8rem;line-height:1.6;color:var(--slate);">
      <strong style="color:var(--red);">Definition:</strong> <strong>Precedence</strong> rules dictate which operator is evaluated first in an expression. <strong>Associativity</strong> defines evaluation direction (Left-to-Right or Right-to-Left) when operators share equal priority.
    </div>
  </div>

  <div>
    <table class="cmp-table" style="font-size:.65rem;margin-top:4px;">
      <thead v-click><tr><th>Priority</th><th>Operators</th><th>Category</th></tr></thead>
      <tbody>
        <tr v-click><td style="color:var(--red-dark);font-weight:700;">1 (Highest)</td><td class="mono">() [] .</td><td>Parentheses / Access</td></tr>
        <tr v-click><td style="color:var(--orange);font-weight:700;">2</td><td class="mono">expr++ expr--</td><td>Postfix</td></tr>
        <tr v-click><td style="color:var(--orange);font-weight:700;">3</td><td class="mono">++expr --expr + - ! ~</td><td>Prefix &amp; Unary</td></tr>
        <tr v-click><td style="color:#d69e2e;font-weight:700;">4</td><td class="mono">* / %</td><td>Multiplicative</td></tr>
        <tr v-click><td style="color:var(--green);font-weight:700;">5</td><td class="mono">+ -</td><td>Additive</td></tr>
        <tr v-click><td style="color:var(--green);font-weight:700;">6</td><td class="mono">&lt;&lt; &gt;&gt; &gt;&gt;&gt;</td><td>Bitwise Shift</td></tr>
        <tr v-click><td style="color:var(--blue);font-weight:700;">7</td><td class="mono">&lt; &gt; &lt;= &gt;= instanceof</td><td>Relational</td></tr>
        <tr v-click><td style="color:var(--blue);font-weight:700;">8</td><td class="mono">== !=</td><td>Equality</td></tr>
        <tr v-click><td style="color:var(--purple);font-weight:700;">9</td><td class="mono">&amp; ^ |</td><td>Bitwise</td></tr>
        <tr v-click><td style="color:var(--navy-mid);font-weight:700;">10</td><td class="mono">&amp;&amp; ||</td><td>Logical</td></tr>
        <tr v-click><td style="color:var(--slate);font-weight:700;">11</td><td class="mono">? :</td><td>Ternary</td></tr>
        <tr v-click><td style="color:var(--slate);font-weight:700;">12 (Lowest)</td><td class="mono">= += -= *= /= %=</td><td>Assignment</td></tr>
      </tbody>
    </table>
  </div>

</div>

<div class="flex-col">
  <div v-click class="section-label">Precedence in Action</div>

  <div v-after style="background:#f6f8fa;border-radius:10px;border:1px solid #e1e4e8;padding:10px 14px;font-family:'Fira Code',monospace;font-size:.72rem;line-height:1.9;">
    <span style="color:#6b7280;">// Example 1: Multiplicative before Additive</span><br>
    <span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">res1</span> = <span style="color:#b45309;">2</span> + <span style="color:#b45309;">3</span> * <span style="color:#b45309;">4</span>; &nbsp;&nbsp;<span style="color:#6b7280;">// 14 (* first)</span><br>
    <span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">res2</span> = (<span style="color:#b45309;">2</span> + <span style="color:#b45309;">3</span>) * <span style="color:#b45309;">4</span>; <span style="color:#6b7280;">// 20 (() forces + first)</span><br><br>
    <span style="color:#6b7280;">// Example 2: Relational before Logical</span><br>
    <span style="color:#ef5050;">boolean</span> <span style="color:#0e6ead;">check</span> = <span style="color:#b45309;">5</span> &gt; <span style="color:#b45309;">3</span> &amp;&amp; <span style="color:#b45309;">2</span> &lt; <span style="color:#b45309;">4</span>; <span style="color:#6b7280;">// true</span>
  </div>

  <div v-click class="section-label" style="margin-top:6px;">Associativity Directions</div>
  <div v-after style="display:flex;flex-direction:column;gap:4px;">
    <div class="card" style="padding:6px 12px;">
      <div style="font-size:.7rem;"><strong style="color:var(--green);">Left-to-Right:</strong> Most operators (<span class="mono">+ - * / % &amp;&amp; ||</span>) evaluate left to right.</div>
    </div>
    <div class="card" style="padding:6px 12px;">
      <div style="font-size:.7rem;"><strong style="color:var(--orange);">Right-to-Left:</strong> Unary (<span class="mono">++ -- !</span>), Ternary (<span class="mono">?:</span>), and Assignment (<span class="mono">= +=</span>) evaluate right to left.</div>
    </div>
  </div>

  <div v-click class="callout callout-success" style="margin-top:4px;">
    <div><strong>Golden Rule:</strong> Use <span class="mono">()</span> parentheses whenever an expression combines multiple operators to ensure clarity!</div>
  </div>

</div>

</div>

  </template>
</Slide2>
