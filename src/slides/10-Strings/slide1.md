<!-- ═══════════════════════════════════════════════════════
     SLIDE 1 — INTRODUCTION TO STRINGS IN JAVA
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Java Strings">
  <template #content>

<div class="slide-h1" style="margin-bottom:10px;">Introduction to <span class="highlight">Strings</span></div>

<div class="g2" style="gap:14px;align-items:start;">

<div class="flex-col">

  <div v-click class="card-navy" style="border-radius:10px;">
    <div style="font-size:.82rem;line-height:1.6;color:var(--slate);">
      A <strong style="color:var(--red);">String</strong> in Java is a <strong>sequence of characters</strong> represented as an object of the <span class="mono">String</span> class — <strong>not a primitive type</strong>. Strings are enclosed in double quotes (<span class="mono">"&nbsp;"</span>) and can hold letters, digits, spaces, and symbols.
    </div>
  </div>

  <div v-click class="callout callout-warn">
    <div><strong>Java vs Python:</strong> In Python strings can use <span class="mono">'single'</span> or <span class="mono">"double"</span> quotes. In Java, <strong>only double quotes</strong> are used for strings — single quotes (<span class="mono">'A'</span>) denote a <span class="mono">char</span> primitive, not a String.</div>
  </div>

  <div v-click class="code-block" style="font-size:.76rem;line-height:1.9;">
    <span style="color:#6b7280;">// All of these are String objects</span><br>
    <span style="color:#ef5050;">String</span> <span style="color:#0e6ead;">name</span>    = <span style="color:#2d7a00;">"Alice"</span>;<br>
    <span style="color:#ef5050;">String</span> <span style="color:#0e6ead;">city</span>    = <span style="color:#2d7a00;">"Chennai"</span>;<br>
    <span style="color:#ef5050;">String</span> <span style="color:#0e6ead;">digit</span>   = <span style="color:#2d7a00;">"42"</span>;   <span style="color:#6b7280;">// "42" is a String, not a number</span><br>
    <span style="color:#ef5050;">String</span> <span style="color:#0e6ead;">empty</span>   = <span style="color:#2d7a00;">""</span>;    <span style="color:#6b7280;">// empty String is valid</span><br>
    <span style="color:#ef5050;">String</span> <span style="color:#0e6ead;">message</span> = <span style="color:#2d7a00;">"Hello, World!"</span>;
  </div>

  <div v-click class="callout callout-success">
    <div>In Java, <span class="mono">String</span> is a class in <span class="mono">java.lang</span> — automatically imported. Use <span class="mono">s.getClass().getName()</span> to verify: prints <span class="mono" style="color:var(--green);">java.lang.String</span></div>
  </div>

</div>

<div class="flex-col">
  <div class="section-label" v-click>Why Strings Matter</div>

  <div style="display:flex;flex-direction:column;gap:8px;">
    <div v-click class="card" style="display:flex;gap:10px;align-items:flex-start;">
      <div class="icon-circle ic-red" style="font-size:.9rem;">💬</div>
      <div>
        <div style="font-size:.75rem;font-weight:600;color:var(--navy);">User Interaction</div>
        <div style="font-size:.7rem;color:var(--slate);">Names, messages, prompts, and responses are all strings</div>
      </div>
    </div>
    <div v-click class="card" style="display:flex;gap:10px;align-items:flex-start;">
      <div class="icon-circle ic-blue" style="font-size:.9rem;">📂</div>
      <div>
        <div style="font-size:.75rem;font-weight:600;color:var(--navy);">File &amp; Data Handling</div>
        <div style="font-size:.7rem;color:var(--slate);">File paths, CSV fields, and database records use strings</div>
      </div>
    </div>
    <div v-click class="card" style="display:flex;gap:10px;align-items:flex-start;">
      <div class="icon-circle ic-green" style="font-size:.9rem;">🌐</div>
      <div>
        <div style="font-size:.75rem;font-weight:600;color:var(--navy);">Web &amp; APIs</div>
        <div style="font-size:.7rem;color:var(--slate);">URLs, JSON keys, HTTP headers — all strings</div>
      </div>
    </div>
    <div v-click class="card" style="display:flex;gap:10px;align-items:flex-start;">
      <div class="icon-circle ic-orange" style="font-size:.9rem;">🔐</div>
      <div>
        <div style="font-size:.75rem;font-weight:600;color:var(--navy);">Security</div>
        <div style="font-size:.7rem;color:var(--slate);">Passwords, tokens, and validation rely on strings</div>
      </div>
    </div>
  </div>

  <div v-click class="callout callout-info" style="margin-top:6px;">
    <div>Strings are the most-used non-primitive type in Java — mastering them unlocks real-world programming power!</div>
  </div>

</div>

</div>

  </template>
</Slide2>
