---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 13 — COMMON BEGINNER MISTAKES
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Java Strings">
  <template #content>

<div class="slide-h1" style="margin-bottom:10px;">Common <span class="highlight">Mistakes</span> to Avoid</div>

<div class="g2" style="gap:12px;align-items:start;">

<div class="flex-col" style="gap:7px;">

  <div v-click class="card-red" style="border-radius:10px;">
    <div style="font-size:.78rem;font-weight:600;color:var(--red-dark);margin-bottom:4px;">Mistake 1 — Using == Instead of .equals()</div>
    <div style="background:#fff8f8;border-radius:8px;padding:10px 12px;font-family:'Fira Code',monospace;font-size:.68rem;line-height:1.9;">
      <span style="color:#6b7280;">// Wrong — may print false even for same content!</span><br>
      <span style="color:#ef5050;">String</span> <span style="color:#0e6ead;">a</span> = <span style="color:#ef5050;">new</span> <span style="color:#0e6ead;">String</span>(<span style="color:#2d7a00;">"hi"</span>);<br>
      <span style="color:#0e6ead;">System</span>.<span style="color:#0e6ead;">out</span>.<span style="color:#2d7a00;">println</span>(<span style="color:#0e6ead;">a</span> == <span style="color:#2d7a00;">"hi"</span>); <span style="color:#6b7280;">// false!</span><br>
      <span style="color:#6b7280;">// Correct</span><br>
      <span style="color:#0e6ead;">System</span>.<span style="color:#0e6ead;">out</span>.<span style="color:#2d7a00;">println</span>(<span style="color:#0e6ead;">a</span>.<span style="color:#2d7a00;">equals</span>(<span style="color:#2d7a00;">"hi"</span>)); <span style="color:#6b7280;">// true</span>
    </div>
  </div>

  <div v-click class="card-red" style="border-radius:10px;">
    <div style="font-size:.78rem;font-weight:600;color:var(--red-dark);margin-bottom:4px;">Mistake 2 — Ignoring the Return Value of Methods</div>
    <div style="background:#fff8f8;border-radius:8px;padding:10px 12px;font-family:'Fira Code',monospace;font-size:.68rem;line-height:1.9;">
      <span style="color:#ef5050;">String</span> <span style="color:#0e6ead;">s</span> = <span style="color:#2d7a00;">"hello"</span>;<br>
      <span style="color:#6b7280;">// Wrong — s is still "hello"! Methods don't modify in place.</span><br>
      <span style="color:#0e6ead;">s</span>.<span style="color:#2d7a00;">toUpperCase</span>();<br>
      <span style="color:#6b7280;">// Correct — capture the returned String</span><br>
      <span style="color:#0e6ead;">s</span> = <span style="color:#0e6ead;">s</span>.<span style="color:#2d7a00;">toUpperCase</span>(); <span style="color:#6b7280;">// Now s = "HELLO"</span>
    </div>
  </div>

  <div v-click class="card-red" style="border-radius:10px;">
    <div style="font-size:.78rem;font-weight:600;color:var(--red-dark);margin-bottom:4px;">Mistake 3 — Off-By-One with substring()</div>
    <div style="background:#fff8f8;border-radius:8px;padding:10px 12px;font-family:'Fira Code',monospace;font-size:.68rem;line-height:1.9;">
      <span style="color:#ef5050;">String</span> <span style="color:#0e6ead;">s</span> = <span style="color:#2d7a00;">"Hello"</span>;<br>
      <span style="color:#6b7280;">// Wrong — end index is exclusive, so this gives "Hell"</span><br>
      <span style="color:#0e6ead;">System</span>.<span style="color:#0e6ead;">out</span>.<span style="color:#2d7a00;">println</span>(<span style="color:#0e6ead;">s</span>.<span style="color:#2d7a00;">substring</span>(<span style="color:#b45309;">0</span>, <span style="color:#b45309;">4</span>)); <span style="color:#6b7280;">// "Hell" not "Hello"</span><br>
      <span style="color:#6b7280;">// Correct — use s.length() or index 5 for full word</span><br>
      <span style="color:#0e6ead;">System</span>.<span style="color:#0e6ead;">out</span>.<span style="color:#2d7a00;">println</span>(<span style="color:#0e6ead;">s</span>.<span style="color:#2d7a00;">substring</span>(<span style="color:#b45309;">0</span>, <span style="color:#0e6ead;">s</span>.<span style="color:#2d7a00;">length</span>())); <span style="color:#6b7280;">// "Hello"</span>
    </div>
  </div>

</div>

<div class="flex-col" style="gap:7px;">

  <div v-click class="card-red" style="border-radius:10px;">
    <div style="font-size:.78rem;font-weight:600;color:var(--red-dark);margin-bottom:4px;">Mistake 4 — Concatenation in a Loop (Performance)</div>
    <div style="background:#fff8f8;border-radius:8px;padding:10px 12px;font-family:'Fira Code',monospace;font-size:.68rem;line-height:1.9;">
      <span style="color:#6b7280;">// Wrong — creates N new String objects!</span><br>
      <span style="color:#ef5050;">String</span> <span style="color:#0e6ead;">r</span> = <span style="color:#2d7a00;">""</span>;<br>
      <span style="color:#ef5050;">for</span>(<span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">i</span>=<span style="color:#b45309;">0</span>; <span style="color:#0e6ead;">i</span>&lt;<span style="color:#b45309;">1000</span>; <span style="color:#0e6ead;">i</span>++) <span style="color:#0e6ead;">r</span> += <span style="color:#0e6ead;">i</span>;<br>
      <span style="color:#6b7280;">// Correct — use StringBuilder</span><br>
      <span style="color:#0e6ead;">StringBuilder</span> <span style="color:#0e6ead;">sb</span> = <span style="color:#ef5050;">new</span> <span style="color:#0e6ead;">StringBuilder</span>();<br>
      <span style="color:#ef5050;">for</span>(<span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">i</span>=<span style="color:#b45309;">0</span>; <span style="color:#0e6ead;">i</span>&lt;<span style="color:#b45309;">1000</span>; <span style="color:#0e6ead;">i</span>++) <span style="color:#0e6ead;">sb</span>.<span style="color:#2d7a00;">append</span>(<span style="color:#0e6ead;">i</span>);
    </div>
  </div>

  <div v-click class="card-red" style="border-radius:10px;">
    <div style="font-size:.78rem;font-weight:600;color:var(--red-dark);margin-bottom:4px;">Mistake 5 — NullPointerException on String Methods</div>
    <div style="background:#fff8f8;border-radius:8px;padding:10px 12px;font-family:'Fira Code',monospace;font-size:.68rem;line-height:1.9;">
      <span style="color:#ef5050;">String</span> <span style="color:#0e6ead;">s</span> = <span style="color:#b45309;">null</span>;<br>
      <span style="color:#6b7280;">// Wrong — NullPointerException!</span><br>
      <span style="color:#0e6ead;">s</span>.<span style="color:#2d7a00;">length</span>();<br>
      <span style="color:#6b7280;">// Correct — check for null first</span><br>
      <span style="color:#ef5050;">if</span> (<span style="color:#0e6ead;">s</span> != <span style="color:#b45309;">null</span>) <span style="color:#0e6ead;">System</span>.<span style="color:#0e6ead;">out</span>.<span style="color:#2d7a00;">println</span>(<span style="color:#0e6ead;">s</span>.<span style="color:#2d7a00;">length</span>());<br>
      <span style="color:#6b7280;">// Or use Objects.requireNonNullElse(s, "")</span>
    </div>
  </div>

  <div v-click class="callout callout-warn" style="margin-top:2px;">
    <div><strong>Golden Rule:</strong> Always <strong>capture</strong> the result of a string method — strings are immutable, so methods never change the original. And always use <span class="mono">.equals()</span>, never <span class="mono">==</span>.</div>
  </div>

</div>

</div>

  </template>
</Slide2>
