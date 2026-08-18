---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 15 — TERNARY OPERATOR DEFINITION & SYNTAX
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Decision-making statements">
  <template #content>
<div class="slide-h1" style="margin-bottom:12px;">Ternary Operator <span class="highlight">(?:)</span></div>

<div class="g2" style="gap:14px;">

<div class="flex-col" style="gap:10px;">
  <div v-click class="callout callout-info">
    <div style="font-size:.8rem;line-height:1.5;color:var(--slate);">
      <strong>Definition:</strong> The <strong style="color:var(--purple);">ternary operator (?:)</strong> is a shorthand conditional operator that evaluates a condition and returns <strong style="color:var(--green);">one of two values</strong> in a single expression line.
    </div>
  </div>

  <div v-click class="card" style="border:1px solid var(--purple);">
    <div class="slide-h3" style="margin-bottom:8px;">Syntax Pattern</div>
    <div class="syntax-row" style="flex-wrap:wrap;gap:6px;">
      <div>
        <div class="syn-varname">variable</div>
        <div class="syn-label">stores result</div>
      </div>
      <div>
        <div class="syn-operator">=</div>
        <div class="syn-label">assign</div>
      </div>
      <div>
        <div class="syn-keyword" style="background:#fffaf0;color:#c05621;">( condition )</div>
        <div class="syn-label">boolean test</div>
      </div>
      <div>
        <div class="syn-operator">?</div>
        <div class="syn-label">if true</div>
      </div>
      <div>
        <div class="syn-value">value_if_true</div>
        <div class="syn-label">return when true</div>
      </div>
      <div>
        <div class="syn-operator">:</div>
        <div class="syn-label">else</div>
      </div>
      <div>
        <div class="syn-value" style="background:#fde8e8;color:#c73c3c;">value_if_false</div>
        <div class="syn-label">return when false</div>
      </div>
    </div>
  </div>
</div>

<div class="flex-col" style="gap:10px;">
  <div v-click class="card card-purple">
    <div class="slide-h3" style="color:var(--purple);margin-bottom:6px;">Why is it called Ternary?</div>
    <div class="body-text">Because it is the only operator in Java that takes <strong>three operands</strong>: (1) Condition, (2) Value if True, and (3) Value if False.</div>
  </div>

  <div v-click class="callout callout-warn">
    <div><strong>Type Rule:</strong> Both <code>value_if_true</code> and <code>value_if_false</code> must evaluate to compatible types that match the target variable!</div>
  </div>
</div>

</div>
  </template>
</Slide2>
