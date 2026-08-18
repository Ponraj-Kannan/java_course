---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 8 — DO-WHILE LOOP (JAVA SPECIFIC)
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Do-While Loop">
  <template #content>

<div class="slide-h1" style="margin-bottom:10px;"><span class="highlight">Do-While</span> Loop — Java Post-Test Loop</div>

<div class="g2" style="gap:14px;align-items:start;">

<div class="flex-col">

  <div v-click class="section-label">Syntax Diagram</div>
  <div v-after style="background:#f6f8fa;border-radius:10px;border:1px solid #e1e4e8;padding:16px 18px;font-family:'Fira Code',monospace;font-size:.78rem;line-height:2;">
    <span style="color:#0e6ead;">int</span> count = <span style="color:#b45309;">1</span>;<br>
    <span style="color:#ef5050;">do</span> {<br>
    <span style="padding-left:20px;display:block;">System.out.<span style="color:#2d7a00;">println</span>(<span style="color:#2d7a00;">"Count: "</span> + count);</span>
    <span style="padding-left:20px;display:block;">count++;</span>
    } <span style="color:#ef5050;">while</span> (count &lt;= <span style="color:#b45309;">3</span>)<span style="color:#ef5050;">;</span> <span style="color:#6b7280;">// Note ending semicolon!</span>
  </div>

  <div v-click class="callout callout-warn" style="margin-top:8px;">
    <div><strong>Guaranteed Execution:</strong> The <code>do-while</code> loop executes the body <strong>at least once</strong> before evaluating the condition!</div>
  </div>

  <div v-click class="card card-orange" style="margin-top:6px;">
    <div class="slide-h3" style="margin-bottom:4px;">Typical Use Case</div>
    <div class="body-text">Ideal for <strong>menu choices</strong> or <strong>input validation</strong> where prompt logic must run once before checking if input is valid.</div>
  </div>

</div>

<div class="flex-col">
  <div v-click class="section-label">Execution Flowchart</div>

  <div v-after style="display:flex;flex-direction:column;align-items:center;gap:4px;padding:10px 0;border:1px solid #e1e4e8;border-radius:10px;">
    <div class="flow-node flow-start" style="width:140px;">START</div>
    <div class="flow-arrow">&#x25BC;</div>
    <div class="flow-node flow-body" style="width:180px;font-size:.7rem;">Execute Body Block<br>(Runs AT LEAST Once)</div>
    <div class="flow-arrow">&#x25BC;</div>
    <div class="flow-node flow-cond" style="width:180px;">Condition true ?</div>
    <div style="display:flex;align-items:flex-start;gap:16px;width:260px;">
      <div style="display:flex;flex-direction:column;align-items:center;gap:4px;margin-left:10px;">
        <div style="font-size:.6rem;color:var(--green);font-weight:700;">TRUE</div>
        <div class="flow-arrow">&#x21B1;</div>
        <div style="font-size:.6rem;color:var(--muted);font-weight:700;text-align:center;">Repeat<br>Body</div>
      </div>
      <div style="display:flex;flex-direction:column;align-items:center;gap:4px;padding-top:10px;margin-left:40px;">
        <div style="font-size:.6rem;color:var(--red);font-weight:700;">FALSE</div>
        <div class="flow-arrow">&#x25BC;</div>
        <div class="flow-node flow-end" style="width:80px;">END</div>
      </div>
    </div>
  </div>

  <div v-click class="callout callout-danger" style="margin-top:4px;">
    <div><strong>Syntax Warning:</strong> Don't forget the required semicolon <code>;</code> after <code>while(condition);</code> in Java!</div>
  </div>
</div>

</div>

  </template>
</Slide2>
