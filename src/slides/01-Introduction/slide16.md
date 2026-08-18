---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 16 — JAVA KEYWORDS
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Java Reserved Keywords">
  <template #content>

<div class="slide-h1" style="margin-bottom:10px;"><span class="highlight">Reserved Keywords</span></div>

<div class="g2" style="gap:14px;">

<div class="flex-col">

  <div v-click class="card-navy" style="border-radius:10px;">
    <div style="font-size:.82rem;line-height:1.6;color:var(--slate);">
      Java is <strong style="color:var(--red);">case-sensitive</strong>. <span class="mono">Class</span>, <span class="mono">class</span>, and <span class="mono">CLASS</span> are <strong>three different things</strong> — only <span class="mono">class</span> is a valid keyword.
    </div>
  </div>

  <div v-click class="section-label">Java Reserved Keywords</div>
  <div v-click class="small-text" style="margin-bottom:6px;">These cannot be used as variable or class names</div>

  <div style="display:flex;gap:4px;flex-wrap:wrap;">
    <span v-click style="background:var(--red-soft);color:var(--red-dark);border:1px solid var(--red);border-radius:6px;padding:3px 10px;font-family:'Fira Code',monospace;font-size:.68rem;font-weight:700;">class</span>
    <span v-after style="background:var(--red-soft);color:var(--red-dark);border:1px solid var(--red);border-radius:6px;padding:3px 10px;font-family:'Fira Code',monospace;font-size:.68rem;font-weight:700;">public</span>
    <span v-after style="background:var(--red-soft);color:var(--red-dark);border:1px solid var(--red);border-radius:6px;padding:3px 10px;font-family:'Fira Code',monospace;font-size:.68rem;font-weight:700;">static</span>
    <span v-after style="background:var(--red-soft);color:var(--red-dark);border:1px solid var(--red);border-radius:6px;padding:3px 10px;font-family:'Fira Code',monospace;font-size:.68rem;font-weight:700;">void</span>
    <span v-after style="background:var(--red-soft);color:var(--red-dark);border:1px solid var(--red);border-radius:6px;padding:3px 10px;font-family:'Fira Code',monospace;font-size:.68rem;font-weight:700;">int</span>
    <span v-after style="background:var(--red-soft);color:var(--red-dark);border:1px solid var(--red);border-radius:6px;padding:3px 10px;font-family:'Fira Code',monospace;font-size:.68rem;font-weight:700;">double</span>
    <span v-after style="background:var(--red-soft);color:var(--red-dark);border:1px solid var(--red);border-radius:6px;padding:3px 10px;font-family:'Fira Code',monospace;font-size:.68rem;font-weight:700;">boolean</span>
    <span v-after style="background:var(--red-soft);color:var(--red-dark);border:1px solid var(--red);border-radius:6px;padding:3px 10px;font-family:'Fira Code',monospace;font-size:.68rem;font-weight:700;">char</span>
    <span v-after style="background:var(--red-soft);color:var(--red-dark);border:1px solid var(--red);border-radius:6px;padding:3px 10px;font-family:'Fira Code',monospace;font-size:.68rem;font-weight:700;">String</span>
    <span v-after style="background:var(--red-soft);color:var(--red-dark);border:1px solid var(--red);border-radius:6px;padding:3px 10px;font-family:'Fira Code',monospace;font-size:.68rem;font-weight:700;">if</span>
    <span v-after style="background:var(--red-soft);color:var(--red-dark);border:1px solid var(--red);border-radius:6px;padding:3px 10px;font-family:'Fira Code',monospace;font-size:.68rem;font-weight:700;">else</span>
    <span v-after style="background:var(--red-soft);color:var(--red-dark);border:1px solid var(--red);border-radius:6px;padding:3px 10px;font-family:'Fira Code',monospace;font-size:.68rem;font-weight:700;">for</span>
    <span v-after style="background:var(--red-soft);color:var(--red-dark);border:1px solid var(--red);border-radius:6px;padding:3px 10px;font-family:'Fira Code',monospace;font-size:.68rem;font-weight:700;">while</span>
    <span v-after style="background:var(--red-soft);color:var(--red-dark);border:1px solid var(--red);border-radius:6px;padding:3px 10px;font-family:'Fira Code',monospace;font-size:.68rem;font-weight:700;">do</span>
    <span v-after style="background:var(--red-soft);color:var(--red-dark);border:1px solid var(--red);border-radius:6px;padding:3px 10px;font-family:'Fira Code',monospace;font-size:.68rem;font-weight:700;">return</span>
    <span v-after style="background:var(--red-soft);color:var(--red-dark);border:1px solid var(--red);border-radius:6px;padding:3px 10px;font-family:'Fira Code',monospace;font-size:.68rem;font-weight:700;">new</span>
    <span v-after style="background:var(--red-soft);color:var(--red-dark);border:1px solid var(--red);border-radius:6px;padding:3px 10px;font-family:'Fira Code',monospace;font-size:.68rem;font-weight:700;">import</span>
    <span v-after style="background:var(--red-soft);color:var(--red-dark);border:1px solid var(--red);border-radius:6px;padding:3px 10px;font-family:'Fira Code',monospace;font-size:.68rem;font-weight:700;">package</span>
    <span v-after style="background:var(--red-soft);color:var(--red-dark);border:1px solid var(--red);border-radius:6px;padding:3px 10px;font-family:'Fira Code',monospace;font-size:.68rem;font-weight:700;">try</span>
    <span v-after style="background:var(--red-soft);color:var(--red-dark);border:1px solid var(--red);border-radius:6px;padding:3px 10px;font-family:'Fira Code',monospace;font-size:.68rem;font-weight:700;">catch</span>
    <span v-after style="background:var(--red-soft);color:var(--red-dark);border:1px solid var(--red);border-radius:6px;padding:3px 10px;font-family:'Fira Code',monospace;font-size:.68rem;font-weight:700;">finally</span>
    <span v-after style="background:var(--red-soft);color:var(--red-dark);border:1px solid var(--red);border-radius:6px;padding:3px 10px;font-family:'Fira Code',monospace;font-size:.68rem;font-weight:700;">throw</span>
    <span v-after style="background:var(--red-soft);color:var(--red-dark);border:1px solid var(--red);border-radius:6px;padding:3px 10px;font-family:'Fira Code',monospace;font-size:.68rem;font-weight:700;">extends</span>
    <span v-after style="background:var(--red-soft);color:var(--red-dark);border:1px solid var(--red);border-radius:6px;padding:3px 10px;font-family:'Fira Code',monospace;font-size:.68rem;font-weight:700;">implements</span>
    <span v-after style="background:var(--red-soft);color:var(--red-dark);border:1px solid var(--red);border-radius:6px;padding:3px 10px;font-family:'Fira Code',monospace;font-size:.68rem;font-weight:700;">interface</span>
    <span v-after style="background:var(--red-soft);color:var(--red-dark);border:1px solid var(--red);border-radius:6px;padding:3px 10px;font-family:'Fira Code',monospace;font-size:.68rem;font-weight:700;">abstract</span>
    <span v-after style="background:var(--red-soft);color:var(--red-dark);border:1px solid var(--red);border-radius:6px;padding:3px 10px;font-family:'Fira Code',monospace;font-size:.68rem;font-weight:700;">final</span>
    <span v-after style="background:var(--red-soft);color:var(--red-dark);border:1px solid var(--red);border-radius:6px;padding:3px 10px;font-family:'Fira Code',monospace;font-size:.68rem;font-weight:700;">this</span>
    <span v-after style="background:var(--red-soft);color:var(--red-dark);border:1px solid var(--red);border-radius:6px;padding:3px 10px;font-family:'Fira Code',monospace;font-size:.68rem;font-weight:700;">super</span>
    <span v-after style="background:var(--red-soft);color:var(--red-dark);border:1px solid var(--red);border-radius:6px;padding:3px 10px;font-family:'Fira Code',monospace;font-size:.68rem;font-weight:700;">null</span>
    <span v-after style="background:var(--red-soft);color:var(--red-dark);border:1px solid var(--red);border-radius:6px;padding:3px 10px;font-family:'Fira Code',monospace;font-size:.68rem;font-weight:700;">true</span>
    <span v-after style="background:var(--red-soft);color:var(--red-dark);border:1px solid var(--red);border-radius:6px;padding:3px 10px;font-family:'Fira Code',monospace;font-size:.68rem;font-weight:700;">false</span>
  </div>

  <div v-click class="callout callout-info" style="margin-top:8px;">
    <div>Java has <strong>50+ reserved keywords</strong>. Your IDE will highlight them in a different colour to help you avoid using them as names.</div>
  </div>

</div>

<div class="flex-col">

  <div v-click class="section-label">Case Sensitivity Examples</div>

  <div v-after style="background:#f6f8fa;border-radius:10px;border:1px solid #e1e4e8;padding:14px;font-family:'Fira Code',monospace;font-size:.74rem;line-height:2;margin-top:4px;">
    <span style="color:#0e6ead;">student</span> = <span style="color:#2d7a00;">"Alice"</span>;<br>
    <span style="color:#c49a00;">Student</span> = <span style="color:#2d7a00;">"Bob"</span>;<span style="color:#6b7280;"> // different name!</span><br>
    <span style="color:#ef5050;">STUDENT</span> = <span style="color:#2d7a00;">"Charlie"</span>;<span style="color:#6b7280;"> // yet another!</span>
  </div>

  <div v-click class="callout callout-danger" style="margin-top:8px;">
    <div><strong>Common Mistake:</strong> Writing <span class="mono">System.Out.Println()</span> instead of <span class="mono" style="color:var(--green);">System.out.println()</span> causes a compile error!</div>
  </div>

  <div v-click class="card card-green" style="margin-top:6px;">
    <div class="small-text"><strong>Naming convention:</strong> Use <span class="mono">camelCase</span> for variables (<span class="mono">studentName</span>) and <span class="mono">PascalCase</span> for classes (<span class="mono">StudentInfo</span>).</div>
  </div>

</div>

</div>

  </template>
</Slide2>
