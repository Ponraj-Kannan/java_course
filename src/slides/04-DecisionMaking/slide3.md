---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 3 — IF STATEMENT SYNTAX & DEFINITION
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Decision-making statements">
  <template #content>
<div class="slide-h1" style="margin-bottom:14px;"><span class="highlight">if</span> Statement Syntax</div>

<div class="g2" style="gap:16px;">

<div class="flex-col" style="gap:10px;">
  <div v-click class="callout callout-info">
    <div style="font-size:.8rem;line-height:1.5;color:var(--slate);">
      <strong>Definition:</strong> The <strong style="color:var(--red);">if statement</strong> evaluates a boolean condition and executes its enclosed block of statements <strong style="color:var(--green);">if and only if</strong> the condition evaluates to <span style="color:var(--blue);">true</span>.
    </div>
  </div>

  <div class="slide-h3" v-click>Syntax Breakdown</div>

  <div v-after style="background:#1a1f36;border-radius:10px;padding:14px 18px;font-family:'Fira Code',monospace;font-size:.82rem;line-height:2;">
    <span style="color:#ff79c6;">if</span> <span style="color:#f1fa8c;">(</span><span style="color:#61dafb;">condition</span><span style="color:#f1fa8c;">)</span> <span style="color:#f1fa8c;">{</span><br>
    <span style="color:#636e80;">&nbsp;&nbsp;&nbsp;&nbsp;// code executed if condition is true</span><br>
    <span style="color:#a8ff78;">&nbsp;&nbsp;&nbsp;&nbsp;statement_1;</span><br>
    <span style="color:#a8ff78;">&nbsp;&nbsp;&nbsp;&nbsp;statement_2;</span><br>
    <span style="color:#f1fa8c;">}</span>
  </div>

  <div v-click style="display:flex;flex-direction:column;gap:8px;">
    <div class="syntax-row">
      <div>
        <div class="syn-keyword">if</div>
        <div class="syn-label">keyword</div>
      </div>
      <div>
        <div class="syn-varname">( condition )</div>
        <div class="syn-label">must be in () &amp; boolean</div>
      </div>
      <div>
        <div class="syn-operator">{ }</div>
        <div class="syn-label">block braces</div>
      </div>
    </div>
  </div>

  <div v-click class="callout callout-danger">
    <div><strong>Java Syntax Rules:</strong> The condition <strong>MUST</strong> be enclosed in parentheses <code>( )</code> and must resolve strictly to a <code>boolean</code>!</div>
  </div>
</div>

<div class="flex-col" style="gap:10px;">
  <div class="slide-h3" v-click style="margin-bottom:4px;">Execution Diagram</div>

  <div v-after style="display:flex;flex-direction:column;align-items:center;gap:4px;">
    <div class="flow-v-box" style="background:#ebf8ff;border:1px solid #3182ce;color:#2b6cb0;">▶ Reaches if statement</div>
    <div class="flow-v-arrow">▼</div>
    <div class="flow-v-box" style="background:var(--red-soft);border:2px solid var(--red);color:var(--red-dark);">🔎 Evaluate (condition)</div>
    <div style="display:flex;gap:20px;align-items:flex-start;margin-top:4px;">
      <div class="flex-col" style="align-items:center;gap:4px;">
        <div style="font-size:.7rem;font-weight:800;color:var(--green);">true</div>
        <div class="flow-v-arrow" style="color:var(--green);">▼</div>
        <div class="flow-v-box" style="background:#f0fff4;border:1px solid var(--green);color:var(--green);min-width:100px;">Run block inside { }</div>
      </div>
      <div class="flex-col" style="align-items:center;gap:4px;">
        <div style="font-size:.7rem;font-weight:800;color:var(--red);">false</div>
        <div class="flow-v-arrow" style="color:var(--red);">▼</div>
        <div class="flow-v-box" style="background:var(--red-soft);border:1px solid var(--red);color:var(--red-dark);min-width:100px;">Skip block inside { }</div>
      </div>
    </div>
    <div class="flow-v-arrow" style="margin-top:4px;">▼</div>
    <div class="flow-v-box" style="background:#fffff0;border:1px solid var(--yellow);color:#744210;">Continue next statements</div>
  </div>
</div>

</div>
  </template>
</Slide2>
