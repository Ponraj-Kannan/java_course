---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 2 — CREATING STRINGS: LITERAL vs new String()
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Java Strings">
  <template #content>

<div class="slide-h1" style="margin-bottom:10px;">Creating <span class="highlight">Strings</span> — Two Ways</div>

<div class="g2" style="gap:14px;align-items:start;">

<div class="flex-col">

  <div v-click class="card-green" style="border-radius:10px;">
    <div style="font-size:.78rem;font-weight:600;color:var(--green);margin-bottom:4px;">Way 1 — String Literal (Recommended)</div>
    <div style="font-size:.74rem;color:var(--slate);line-height:1.6;">Assign a string value directly using double quotes. Java stores this in a special memory area called the <strong>String Pool</strong>.</div>
    <div class="code-block" style="margin-top:8px;font-size:.74rem;">
      <span style="color:#ef5050;">String</span> <span style="color:#0e6ead;">s1</span> = <span style="color:#2d7a00;">"hello"</span>;<br>
      <span style="color:#ef5050;">String</span> <span style="color:#0e6ead;">s2</span> = <span style="color:#2d7a00;">"world"</span>;<br>
      <span style="color:#ef5050;">String</span> <span style="color:#0e6ead;">s3</span> = <span style="color:#2d7a00;">"hello"</span>; <span style="color:#6b7280;">// reuses s1's object from pool</span>
    </div>
  </div>

  <div v-click class="card-blue" style="border-radius:10px;margin-top:6px;">
    <div style="font-size:.78rem;font-weight:600;color:var(--blue);margin-bottom:4px;">Way 2 — new String() Constructor</div>
    <div style="font-size:.74rem;color:var(--slate);line-height:1.6;">Explicitly create a new String object using the constructor. This <strong>always creates a new object</strong> on the heap — even if identical content exists in the pool.</div>
    <div class="code-block" style="margin-top:8px;font-size:.74rem;">
      <span style="color:#ef5050;">String</span> <span style="color:#0e6ead;">s4</span> = <span style="color:#ef5050;">new</span> <span style="color:#0e6ead;">String</span>(<span style="color:#2d7a00;">"hello"</span>); <span style="color:#6b7280;">// heap object — NOT pooled</span>
    </div>
  </div>

  <div v-click class="callout callout-info" style="margin-top:6px;">
    <div><strong>Which to use?</strong> Almost always use <strong>string literals</strong>. The <span class="mono">new String()</span> form is rarely needed and wastes memory by bypassing the pool.</div>
  </div>

</div>

<div class="flex-col">
  <div v-click class="section-label">Memory Diagram — Literal vs new String()</div>

  <div style="background:#f7f8fc;border:1px solid var(--border);border-radius:10px;padding:12px 14px;font-size:.72rem;">
    <div v-click style="font-weight:700;margin-bottom:8px;color:var(--navy);">📦 Heap Memory</div>
    <div style="display:flex;gap:10px;margin-bottom:10px;">
      <div v-click style="flex:1;background:#f0fff4;border:2px solid var(--green);border-radius:8px;padding:8px;text-align:center;">
        <div style="font-size:.65rem;color:var(--slate);margin-bottom:4px;">String Pool (inside Heap)</div>
        <div style="font-family:'Fira Code',monospace;font-weight:700;color:var(--green);">"hello"</div>
        <div style="font-size:.62rem;color:var(--slate);margin-top:4px;">shared by s1 &amp; s3</div>
      </div>
      <div v-click style="flex:1;background:#ebf8ff;border:2px solid var(--blue);border-radius:8px;padding:8px;text-align:center;">
        <div style="font-size:.65rem;color:var(--slate);margin-bottom:4px;">Heap Object (new String)</div>
        <div style="font-family:'Fira Code',monospace;font-weight:700;color:var(--blue);">"hello"</div>
        <div style="font-size:.62rem;color:var(--slate);margin-top:4px;">used only by s4</div>
      </div>
    </div>
    <div style="display:flex;flex-direction:column;gap:4px;font-family:'Fira Code',monospace;font-size:.7rem;">
      <div v-click><span style="color:var(--green);font-weight:600;">s1</span> <span style="color:#6b7280;">→ points to pool "hello"</span></div>
      <div v-click><span style="color:var(--green);font-weight:600;">s3</span> <span style="color:#6b7280;">→ points to pool "hello" (same object!)</span></div>
      <div v-click><span style="color:var(--blue);font-weight:600;">s4</span> <span style="color:#6b7280;">→ points to separate heap object</span></div>
    </div>
  </div>

  <div v-click class="section-label" style="margin-top:8px;">Key Takeaways</div>
  <div style="display:flex;flex-direction:column;gap:5px;">
    <div v-click style="display:flex;gap:8px;align-items:center;">
      <span class="pill pill-green">Literal</span>
      <span style="font-size:.7rem;color:var(--slate);">Stored in String Pool — reused if identical content exists</span>
    </div>
    <div v-click style="display:flex;gap:8px;align-items:center;">
      <span class="pill pill-blue">new String()</span>
      <span style="font-size:.7rem;color:var(--slate);">Always a new heap object — never reused from pool</span>
    </div>
    <div v-click style="display:flex;gap:8px;align-items:center;">
      <span class="pill pill-red">==</span>
      <span style="font-size:.7rem;color:var(--slate);">Compares memory address — different result for s1 vs s4!</span>
    </div>
  </div>

  <div v-click class="callout callout-danger" style="margin-top:6px;">
    <div><strong>Critical Java gotcha:</strong> <span class="mono">s1 == s3</span> is <span class="mono">true</span> (same pool object), but <span class="mono">s1 == s4</span> is <span class="mono">false</span> (different objects). <strong>Always use <span class="mono">.equals()</span> to compare content.</strong></div>
  </div>

</div>

</div>

  </template>
</Slide2>
