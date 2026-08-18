---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 3 — DOCUMENTATION COMMENTS (JAVADOC)
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Comments">
  <template #content>

<div class="slide-h1" style="margin-bottom:10px;"><span class="highlight">Documentation</span> Comments — Javadoc</div>

<div class="g2" style="gap:14px;">

<div class="flex-col">

  <div v-click class="card-navy" style="border-radius:10px;">
    <div style="font-size:.82rem;line-height:1.6;color:var(--slate);">
      <strong style="color:var(--red);">Definition:</strong> A <strong>documentation comment</strong> starts with <span class="mono" style="color:var(--orange);">/**</span> and ends with <span class="mono" style="color:var(--orange);">*/</span>. The <span class="mono">javadoc</span> tool reads these comments and generates professional <strong>HTML API documentation</strong> automatically.
    </div>
  </div>

  <div v-click class="section-label">Common Javadoc Tags</div>

  <div style="display:flex;flex-direction:column;gap:5px;">
    <div v-click class="card" style="padding:8px 14px;">
      <div style="display:flex;gap:8px;align-items:center;">
        <span class="pill pill-orange" style="font-family:'Fira Code',monospace;">@param</span>
        <div class="body-text">Describes a method <strong>parameter</strong> — its name and meaning</div>
      </div>
    </div>
    <div v-click class="card" style="padding:8px 14px;">
      <div style="display:flex;gap:8px;align-items:center;">
        <span class="pill pill-green" style="font-family:'Fira Code',monospace;">@return</span>
        <div class="body-text">Describes the <strong>return value</strong> of a method</div>
      </div>
    </div>
    <div v-click class="card" style="padding:8px 14px;">
      <div style="display:flex;gap:8px;align-items:center;">
        <span class="pill pill-blue" style="font-family:'Fira Code',monospace;">@author</span>
        <div class="body-text">Names the <strong>author</strong> of the class or method</div>
      </div>
    </div>
    <div v-click class="card" style="padding:8px 14px;">
      <div style="display:flex;gap:8px;align-items:center;">
        <span class="pill pill-navy" style="font-family:'Fira Code',monospace;">@throws</span>
        <div class="body-text">Documents exceptions the method may <strong>throw</strong></div>
      </div>
    </div>
  </div>

</div>

<div class="flex-col">

  <div v-click class="section-label">Javadoc — Full Example</div>

  <div v-after style="background:#f6f8fa;border-radius:10px;border:1px solid #e1e4e8;padding:14px;font-family:'Fira Code',monospace;font-size:.72rem;line-height:1.9;">
    <span style="color:#6b7280;">/**</span><br>
    <span style="color:#6b7280;">&nbsp; * Calculates the area of a rectangle.</span><br>
    <span style="color:#6b7280;">&nbsp; *</span><br>
    <span style="color:#6b7280;">&nbsp; * <span style="color:var(--orange);">@author</span> Priya Sharma</span><br>
    <span style="color:#6b7280;">&nbsp; * <span style="color:var(--orange);">@param</span>  length the length of the rectangle</span><br>
    <span style="color:#6b7280;">&nbsp; * <span style="color:var(--orange);">@param</span>  width  the width of the rectangle</span><br>
    <span style="color:#6b7280;">&nbsp; * <span style="color:var(--orange);">@return</span> the calculated area (length × width)</span><br>
    <span style="color:#6b7280;">&nbsp; */</span><br>
    <span style="color:#ef5050;">double</span> <span style="color:#2d7a00;">calculateArea</span>(<span style="color:#ef5050;">double</span> <span style="color:#0e6ead;">length</span>, <span style="color:#ef5050;">double</span> <span style="color:#0e6ead;">width</span>) {<br>
    &nbsp;&nbsp;<span style="color:#ef5050;">return</span> <span style="color:#0e6ead;">length</span> * <span style="color:#0e6ead;">width</span>;<br>
    }
  </div>

</div>

</div>

  </template>
</Slide2>
