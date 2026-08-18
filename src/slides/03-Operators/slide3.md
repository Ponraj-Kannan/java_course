---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 3 — UNARY OPERATORS (PREFIX VS POSTFIX)
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Operators">
  <template #content>

<div class="slide-h1" style="margin-bottom:10px;">Unary Operators &amp; <span class="highlight">Increment / Decrement</span></div>

<div class="g2" style="gap:14px;">

<div class="flex-col">

  <div v-click class="card-navy" style="border-radius:10px;">
    <div style="font-size:.8rem;line-height:1.6;color:var(--slate);">
      <strong style="color:var(--red);">Definition:</strong> <strong>Unary operators</strong> operate on a single operand to invert its sign, negate a boolean value, or increment/decrement a variable by 1.
    </div>
  </div>

  <div style="display:flex;flex-direction:column;gap:5px;margin-top:4px;">
    <div v-click class="card-purple" style="border-radius:8px;padding:8px 12px;">
      <div style="font-size:.72rem;font-weight:700;color:var(--purple);font-family:'Fira Code',monospace;">++ (Increment)</div>
      <div style="font-size:.7rem;color:var(--slate);">Increases an integer variable's value by 1</div>
    </div>
    <div v-click class="card-red" style="border-radius:8px;padding:8px 12px;">
      <div style="font-size:.72rem;font-weight:700;color:var(--red-dark);font-family:'Fira Code',monospace;">-- (Decrement)</div>
      <div style="font-size:.7rem;color:var(--slate);">Decreases an integer variable's value by 1</div>
    </div>
  </div>

  <div v-click class="callout callout-info" style="margin-top:4px;">
    <div><strong>Prefix vs Postfix Rule:</strong><br>
    • <strong>Prefix (<span class="mono">++x</span>):</strong> <em>Change first</em>, then use the new value.<br>
    • <strong>Postfix (<span class="mono">x++</span>):</strong> <em>Use current value first</em>, then change.</div>
  </div>

</div>

<div class="flex-col">
  <div v-click class="section-label">Prefix vs Postfix Comparison</div>

  <div v-after style="background:#f6f8fa;border-radius:10px;border:1px solid #e1e4e8;padding:12px 14px;font-family:'Fira Code',monospace;font-size:.72rem;line-height:1.9;">
    <span style="color:#6b7280;">// Case 1: Postfix (x++)</span><br>
    <span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">a</span> = <span style="color:#b45309;">5</span>;<br>
    <span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">b</span> = <span style="color:#0e6ead;">a</span>++; &nbsp;<span style="color:#6b7280;">// b gets 5, THEN a becomes 6</span><br>
    <span style="color:#0e6ead;">System</span>.<span style="color:#0e6ead;">out</span>.<span style="color:#2d7a00;">println</span>(<span style="color:#2d7a00;">"a="</span> + <span style="color:#0e6ead;">a</span> + <span style="color:#2d7a00;">", b="</span> + <span style="color:#0e6ead;">b</span>); <span style="color:#6b7280;">// a=6, b=5</span><br><br>
    <span style="color:#6b7280;">// Case 2: Prefix (++x)</span><br>
    <span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">x</span> = <span style="color:#b45309;">5</span>;<br>
    <span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">y</span> = ++<span style="color:#0e6ead;">x</span>; &nbsp;<span style="color:#6b7280;">// x becomes 6 FIRST, THEN y gets 6</span><br>
    <span style="color:#0e6ead;">System</span>.<span style="color:#0e6ead;">out</span>.<span style="color:#2d7a00;">println</span>(<span style="color:#2d7a00;">"x="</span> + <span style="color:#0e6ead;">x</span> + <span style="color:#2d7a00;">", y="</span> + <span style="color:#0e6ead;">y</span>); <span style="color:#6b7280;">// x=6, y=6</span>
  </div>

</div>

</div>

  </template>
</Slide2>
