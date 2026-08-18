---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 4 — STRING POOL
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Java Strings">
  <template #content>

<div class="slide-h1" style="margin-bottom:10px;">The Java <span class="highlight">String Pool</span></div>

<div class="g2" style="gap:14px;align-items:start;">

<div class="flex-col">

  <div v-click class="card-navy" style="border-radius:10px;">
    <div style="font-size:.82rem;line-height:1.6;color:var(--slate);">
      The <strong style="color:var(--red);">String Pool</strong> (also called String Intern Pool) is a special memory region inside the Java Heap where the JVM stores <strong>unique string literals</strong>. When you create a string literal, Java first checks the pool — if the same value already exists, it <strong>reuses that object</strong> instead of creating a new one.
    </div>
  </div>

  <div v-click class="code-block" style="margin-top:6px;">
    <span style="color:#ef5050;">String</span> <span style="color:#0e6ead;">a</span> = <span style="color:#2d7a00;">"Java"</span>;  <span style="color:#6b7280;">// pool: creates "Java"</span><br>
    <span style="color:#ef5050;">String</span> <span style="color:#0e6ead;">b</span> = <span style="color:#2d7a00;">"Java"</span>;  <span style="color:#6b7280;">// pool: reuses same object</span><br>
    <span style="color:#ef5050;">String</span> <span style="color:#0e6ead;">c</span> = <span style="color:#ef5050;">new</span> <span style="color:#0e6ead;">String</span>(<span style="color:#2d7a00;">"Java"</span>); <span style="color:#6b7280;">// heap: new object (NOT pool)</span><br>
    <br>
    <span style="color:#0e6ead;">System</span>.<span style="color:#0e6ead;">out</span>.<span style="color:#2d7a00;">println</span>(<span style="color:#0e6ead;">a</span> == <span style="color:#0e6ead;">b</span>);  <span style="color:#6b7280;">// true  (same pool object)</span><br>
    <span style="color:#0e6ead;">System</span>.<span style="color:#0e6ead;">out</span>.<span style="color:#2d7a00;">println</span>(<span style="color:#0e6ead;">a</span> == <span style="color:#0e6ead;">c</span>);  <span style="color:#6b7280;">// false (different objects)</span><br>
    <span style="color:#0e6ead;">System</span>.<span style="color:#0e6ead;">out</span>.<span style="color:#2d7a00;">println</span>(<span style="color:#0e6ead;">a</span>.<span style="color:#2d7a00;">equals</span>(<span style="color:#0e6ead;">c</span>)); <span style="color:#6b7280;">// true  (same content)</span>
  </div>

  <div v-click class="callout callout-info" style="margin-top:4px;">
    <div><strong>Manually intern:</strong> You can force a heap string into the pool using <span class="mono">c.intern()</span>. After interning, <span class="mono">a == c.intern()</span> returns <span class="mono">true</span>.</div>
  </div>

</div>

<div class="flex-col">
  <div class="section-label">Pool Diagram — Literal vs new String()</div>

  <div style="background:#f7f8fc;border:1px solid var(--border);border-radius:10px;padding:14px;">
    <div style="display:flex;gap:10px;align-items:flex-start;">
      <div v-click style="flex:1;">
        <div style="font-weight:700;font-size:.65rem;color:var(--slate);text-align:center;margin-bottom:6px;">STACK (variables)</div>
        <div style="display:flex;flex-direction:column;gap:5px;">
          <div style="background:var(--white);border:1px solid var(--border);border-radius:6px;padding:5px 8px;font-family:'Fira Code',monospace;font-size:.68rem;">a → 0x1A</div>
          <div style="background:var(--white);border:1px solid var(--border);border-radius:6px;padding:5px 8px;font-family:'Fira Code',monospace;font-size:.68rem;">b → 0x1A</div>
          <div style="background:var(--white);border:1px solid var(--border);border-radius:6px;padding:5px 8px;font-family:'Fira Code',monospace;font-size:.68rem;">c → 0x2B</div>
        </div>
      </div>
      <div v-click style="display:flex;flex-direction:column;gap:8px;flex:2;">
        <div>
          <div style="font-weight:700;font-size:.65rem;color:var(--slate);text-align:center;margin-bottom:4px;">STRING POOL (Heap)</div>
          <div style="background:#f0fff4;border:2px solid var(--green);border-radius:8px;padding:8px;text-align:center;font-family:'Fira Code',monospace;font-size:.72rem;">
            <div style="color:var(--green);font-weight:700;">"Java" @ 0x1A</div>
            <div style="font-size:.6rem;color:var(--slate);">shared by a &amp; b</div>
          </div>
        </div>
        <div>
          <div style="font-weight:700;font-size:.65rem;color:var(--slate);text-align:center;margin-bottom:4px;">HEAP OBJECT</div>
          <div style="background:#ebf8ff;border:2px dashed var(--blue);border-radius:8px;padding:8px;text-align:center;font-family:'Fira Code',monospace;font-size:.72rem;">
            <div style="color:var(--blue);font-weight:700;">"Java" @ 0x2B</div>
            <div style="font-size:.6rem;color:var(--slate);">used only by c (new String)</div>
          </div>
        </div>
      </div>
    </div>

  </div>

  <div v-click class="callout callout-success" style="margin-top:6px;">
    <div><strong>Memory benefit:</strong> The String Pool avoids duplicating identical string objects — especially important for frequently used strings like <span class="mono">"true"</span>, <span class="mono">"null"</span>, field names in JSON, etc.</div>
  </div>

</div>

</div>

  </template>
</Slide2>
