---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 10 — STRINGBUILDER
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Java Strings">
  <template #content>

<div class="slide-h1" style="margin-bottom:10px;"><span class="highlight">StringBuilder</span> — Mutable Strings</div>

<div class="g2" style="gap:14px;align-items:start;">

<div class="flex-col">

  <div v-click class="card-navy" style="border-radius:10px;">
    <div style="font-size:.82rem;line-height:1.6;color:var(--slate);">
      <strong style="color:var(--red);">StringBuilder</strong> is a <strong>mutable sequence of characters</strong>. Unlike <span class="mono">String</span>, a <span class="mono">StringBuilder</span> can be <strong>modified in place</strong> — characters can be appended, inserted, deleted, or reversed without creating new objects. Use it when building strings inside loops or through repeated modifications.
    </div>
  </div>

  <div v-click class="section-label" style="margin-top:6px;">Creating &amp; Using StringBuilder</div>

  <div v-after class="code-block" style="font-size:.72rem;line-height:1.9;">
    <span style="color:#0e6ead;">StringBuilder</span> <span style="color:#0e6ead;">sb</span> = <span style="color:#ef5050;">new</span> <span style="color:#0e6ead;">StringBuilder</span>();<br>
    <br>
    <span style="color:#6b7280;">// append() — add to the end</span><br>
    <span style="color:#0e6ead;">sb</span>.<span style="color:#2d7a00;">append</span>(<span style="color:#2d7a00;">"Hello"</span>).<span style="color:#2d7a00;">append</span>(<span style="color:#2d7a00;">"World"</span>);<br>
    <span style="color:#0e6ead;">System</span>.<span style="color:#0e6ead;">out</span>.<span style="color:#2d7a00;">println</span>(<span style="color:#0e6ead;">sb</span>); <span style="color:#6b7280;">// HelloWorld</span><br>
    <br>
    <span style="color:#6b7280;">// insert() — add at a position</span><br>
    <span style="color:#0e6ead;">sb</span>.<span style="color:#2d7a00;">insert</span>(<span style="color:#b45309;">5</span>, <span style="color:#2d7a00;">", "</span>);<br>
    <span style="color:#0e6ead;">System</span>.<span style="color:#0e6ead;">out</span>.<span style="color:#2d7a00;">println</span>(<span style="color:#0e6ead;">sb</span>); <span style="color:#6b7280;">// Hello, World</span><br>
    <br>
    <span style="color:#6b7280;">// reverse() — reverse the content</span><br>
    <span style="color:#0e6ead;">StringBuilder</span> <span style="color:#0e6ead;">r</span> = <span style="color:#ef5050;">new</span> <span style="color:#0e6ead;">StringBuilder</span>(<span style="color:#2d7a00;">"Java"</span>).<span style="color:#2d7a00;">reverse</span>();<br>
    <span style="color:#0e6ead;">System</span>.<span style="color:#0e6ead;">out</span>.<span style="color:#2d7a00;">println</span>(<span style="color:#0e6ead;">r</span>); <span style="color:#6b7280;">// avaJ</span>
  </div>

</div>

<div class="flex-col">
  <div v-click class="section-label">StringBuilder Method Reference</div>

  <div>
    <table class="cmp-table" style="font-size:.7rem;">
      <thead v-click><tr><th>Method</th><th>Description</th></tr></thead>
      <tbody>
        <tr v-click><td class="mono" style="color:var(--red-dark);font-weight:600;">append(x)</td><td>Add x to the end (any type)</td></tr>
        <tr v-click><td class="mono" style="color:var(--red-dark);font-weight:600;">insert(i, x)</td><td>Insert x at index i</td></tr>
        <tr v-click><td class="mono" style="color:var(--red-dark);font-weight:600;">delete(s, e)</td><td>Delete chars from s to e (exclusive)</td></tr>
        <tr v-click><td class="mono" style="color:var(--red-dark);font-weight:600;">reverse()</td><td>Reverse the content in place</td></tr>
        <tr v-click><td class="mono" style="color:var(--red-dark);font-weight:600;">replace(s,e,str)</td><td>Replace chars s–e with str</td></tr>
        <tr v-click><td class="mono" style="color:var(--red-dark);font-weight:600;">toString()</td><td>Convert back to an immutable String</td></tr>
        <tr v-click><td class="mono" style="color:var(--red-dark);font-weight:600;">length()</td><td>Current number of characters</td></tr>
      </tbody>
    </table>
  </div>

  <div v-click class="section-label" style="margin-top:6px;">Efficient Loop Building — The Right Way</div>

  <div v-after class="code-block" style="font-size:.70rem;line-height:1.9;">
    <span style="color:#6b7280;">// GOOD — one object, modified in place</span><br>
    <span style="color:#0e6ead;">StringBuilder</span> <span style="color:#0e6ead;">sb</span> = <span style="color:#ef5050;">new</span> <span style="color:#0e6ead;">StringBuilder</span>();<br>
    <span style="color:#ef5050;">for</span> (<span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">i</span> = <span style="color:#b45309;">1</span>; <span style="color:#0e6ead;">i</span> &lt;= <span style="color:#b45309;">5</span>; <span style="color:#0e6ead;">i</span>++) {<br>
    <span style="padding-left:20px;display:block;background:#f0fff4;border-left:2px solid var(--green);"><span style="color:#0e6ead;">sb</span>.<span style="color:#2d7a00;">append</span>(<span style="color:#0e6ead;">i</span>).<span style="color:#2d7a00;">append</span>(<span style="color:#2d7a00;">" "</span>);</span>
    }<br>
    <span style="color:#0e6ead;">System</span>.<span style="color:#0e6ead;">out</span>.<span style="color:#2d7a00;">println</span>(<span style="color:#0e6ead;">sb</span>.<span style="color:#2d7a00;">toString</span>()); <span style="color:#6b7280;">// 1 2 3 4 5</span>
  </div>

</div>

</div>

  </template>
</Slide2>
