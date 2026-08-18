---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 5 — == vs .equals() (DEDICATED SLIDE)
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Java Strings">
  <template #content>

<div class="slide-h1" style="margin-bottom:10px;"><span class="highlight">==</span> vs <span class="highlight">.equals()</span> — A Critical Difference</div>

<div class="g2" style="gap:14px;align-items:start;">

<div class="flex-col">

  <div v-click class="card-navy" style="border-radius:10px;">
    <div style="font-size:.82rem;line-height:1.6;color:var(--slate);">
      <strong style="color:var(--red);">==</strong> compares <strong>memory addresses</strong> (reference equality) — are two variables pointing to the exact same object?<br>
      <strong style="color:var(--green);">.equals()</strong> compares <strong>content</strong> (value equality) — do two strings have the same characters?
    </div>
  </div>

  <div v-click class="code-block" style="margin-top:6px;">
    <span style="color:#ef5050;">String</span> <span style="color:#0e6ead;">s1</span> = <span style="color:#2d7a00;">"hello"</span>;          <span style="color:#6b7280;">// pool</span><br>
    <span style="color:#ef5050;">String</span> <span style="color:#0e6ead;">s2</span> = <span style="color:#2d7a00;">"hello"</span>;          <span style="color:#6b7280;">// same pool object</span><br>
    <span style="color:#ef5050;">String</span> <span style="color:#0e6ead;">s3</span> = <span style="color:#ef5050;">new</span> <span style="color:#0e6ead;">String</span>(<span style="color:#2d7a00;">"hello"</span>); <span style="color:#6b7280;">// new heap object</span><br>
    <br>
    <span style="color:#0e6ead;">System</span>.<span style="color:#0e6ead;">out</span>.<span style="color:#2d7a00;">println</span>(<span style="color:#0e6ead;">s1</span> == <span style="color:#0e6ead;">s2</span>);          <span style="color:#6b7280;">// true  (same address)</span><br>
    <span style="color:#0e6ead;">System</span>.<span style="color:#0e6ead;">out</span>.<span style="color:#2d7a00;">println</span>(<span style="color:#0e6ead;">s1</span> == <span style="color:#0e6ead;">s3</span>);          <span style="color:#6b7280;">// false (different address!)</span><br>
    <span style="color:#0e6ead;">System</span>.<span style="color:#0e6ead;">out</span>.<span style="color:#2d7a00;">println</span>(<span style="color:#0e6ead;">s1</span>.<span style="color:#2d7a00;">equals</span>(<span style="color:#0e6ead;">s3</span>));      <span style="color:#6b7280;">// true  (same content)</span><br>
    <span style="color:#0e6ead;">System</span>.<span style="color:#0e6ead;">out</span>.<span style="color:#2d7a00;">println</span>(<span style="color:#0e6ead;">s1</span>.<span style="color:#2d7a00;">equalsIgnoreCase</span>(<span style="color:#2d7a00;">"HELLO"</span>)); <span style="color:#6b7280;">// true</span>
  </div>

  <div v-click class="callout callout-danger" style="margin-top:4px;">
    <div><strong>Rule: NEVER use == to compare String content.</strong> Always use <span class="mono">.equals()</span> or <span class="mono">.equalsIgnoreCase()</span>. Using <span class="mono">==</span> produces <strong>unpredictable bugs</strong> depending on whether strings come from the pool or the heap.</div>
  </div>

</div>

<div class="flex-col">
  <div v-click class="section-label">Reference vs Content — Diagram</div>

  <div style="background:#f7f8fc;border:1px solid var(--border);border-radius:10px;padding:14px;font-size:.72rem;">
    <div v-click style="font-weight:700;font-size:.65rem;color:var(--slate);margin-bottom:8px;">MEMORY VIEW</div>
    <div style="display:flex;gap:12px;align-items:flex-start;margin-bottom:10px;">
      <div v-click style="flex:1;">
        <div style="font-size:.62rem;color:var(--slate);margin-bottom:4px;">STACK</div>
        <div style="display:flex;flex-direction:column;gap:4px;font-family:'Fira Code',monospace;">
          <div style="background:var(--white);border:1px solid var(--green);border-radius:5px;padding:4px 8px;font-size:.68rem;">s1 → @100</div>
          <div style="background:var(--white);border:1px solid var(--green);border-radius:5px;padding:4px 8px;font-size:.68rem;">s2 → @100</div>
          <div style="background:var(--white);border:1px solid var(--blue);border-radius:5px;padding:4px 8px;font-size:.68rem;">s3 → @200</div>
        </div>
      </div>
      <div v-click style="flex:1.5;">
        <div style="font-size:.62rem;color:var(--slate);margin-bottom:4px;">HEAP</div>
        <div style="display:flex;flex-direction:column;gap:6px;">
          <div style="background:#f0fff4;border:2px solid var(--green);border-radius:7px;padding:6px 10px;text-align:center;font-family:'Fira Code',monospace;">
            <div style="font-size:.65rem;color:var(--slate);">Pool @100</div>
            <div style="color:var(--green);font-weight:700;">"hello"</div>
          </div>
          <div style="background:#ebf8ff;border:2px dashed var(--blue);border-radius:7px;padding:6px 10px;text-align:center;font-family:'Fira Code',monospace;">
            <div style="font-size:.65rem;color:var(--slate);">Heap @200</div>
            <div style="color:var(--blue);font-weight:700;">"hello"</div>
          </div>
        </div>
      </div>
    </div>
    <div v-click style="background:#fff5f5;border:1px solid #fecaca;border-radius:6px;padding:6px 10px;font-size:.65rem;color:var(--red-dark);">
      <strong>s1 == s2</strong> → true (both @100) &nbsp;|&nbsp; <strong>s1 == s3</strong> → false (@100 ≠ @200)
    </div>
    <div v-click style="background:#f0fff4;border:1px solid #a7f3d0;border-radius:6px;padding:6px 10px;font-size:.65rem;color:var(--green);margin-top:4px;">
      <strong>s1.equals(s3)</strong> → true (both "hello" — content matches!)
    </div>

  </div>

  <div v-click class="section-label" style="margin-top:8px;">Comparison Quick Reference</div>
  <div >
    <table class="cmp-table" style="font-size:.7rem;">
      <thead v-click><tr><th>Method</th><th>Compares</th><th>Case Sensitive?</th></tr></thead>
      <tbody>
        <tr v-click><td class="mono">==</td><td class="no">References (addresses)</td><td>N/A</td></tr>
        <tr v-click><td class="mono">.equals()</td><td class="yes">Content (characters)</td><td class="yes">Yes</td></tr>
        <tr v-click><td class="mono">.equalsIgnoreCase()</td><td class="yes">Content (characters)</td><td class="no">No</td></tr>
        <tr v-click><td class="mono">.compareTo()</td><td>Lexicographic order</td><td class="yes">Yes</td></tr>
      </tbody>
    </table>
  </div>

</div>

</div>

  </template>
</Slide2>
