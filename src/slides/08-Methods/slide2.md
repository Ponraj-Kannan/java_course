---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 2 — METHOD DECLARATION & ANATOMY
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Java Methods">
  <template #content>

<div class="slide-h1" style="margin-bottom:10px;">Method <span class="highlight">Declaration &amp; Anatomy</span></div>

<div class="g2" style="gap:14px;align-items:start;">

<div class="flex-col">

  <div v-click class="card-navy" style="border-radius:10px;">
    <div style="font-size:.82rem;line-height:1.6;color:var(--slate);">
      A <strong style="color:var(--red);">method declaration</strong> defines the method's header (access level, return type, name, parameters) and its enclosed execution body block (<span class="mono">{ ... }</span>).
    </div>
  </div>

  <div v-click class="section-label" style="margin-top:6px;">Visual Anatomy of a Method</div>

  <!-- DIAGRAM: METHOD ANATOMY -->
  <div v-after style="background:#1e293b;border-radius:10px;padding:14px;color:#f8fafc;font-family:'Fira Code',monospace;font-size:.70rem;line-height:1.8;">
    <div style="color:#94a3b8;font-size:.62rem;margin-bottom:6px;">// Method Signature &amp; Header Breakdown:</div>
    <div style="font-size:.80rem;letter-spacing:0.5px;padding-bottom:6px;border-bottom:1px dashed #475569;">
      <span style="color:#38bdf8;font-weight:700;">public</span>
      <span style="color:#f59e0b;font-weight:700;"> static</span>
      <span style="color:#a855f7;font-weight:700;"> int</span>
      <span style="color:#22c55e;font-weight:700;"> addNumbers</span>(<span style="color:#f43f5e;font-weight:700;">int a, int b</span>) {
    </div>
    <div style="display:flex;flex-direction:column;gap:3px;margin-top:8px;font-size:.64rem;">
      <div><span style="color:#38bdf8;font-weight:700;">▲ public</span> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;→ <strong>Access Modifier</strong> (accessible from anywhere)</div>
      <div><span style="color:#f59e0b;font-weight:700;">▲ static</span> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;→ <strong>Modifier</strong> (belongs to class, no object needed)</div>
      <div><span style="color:#a855f7;font-weight:700;">▲ int</span> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;→ <strong>Return Type</strong> (sends back an integer result)</div>
      <div><span style="color:#22c55e;font-weight:700;">▲ addNumbers</span> &nbsp;&nbsp;→ <strong>Method Name</strong> (camelCase identifier)</div>
      <div><span style="color:#f43f5e;font-weight:700;">▲ (int a, b)</span> &nbsp;&nbsp;→ <strong>Parameter List</strong> (inputs accepted)</div>
    </div>
    <div style="margin-top:6px;padding-top:6px;border-top:1px dashed #475569;color:#cbd5e1;">
      &nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#ef5050;">return</span> a + b; <span style="color:#64748b;">// Method Body</span><br>
      }
    </div>
  </div>

</div>

<div class="flex-col">
  <div v-click class="section-label">Component Explanations</div>

  <div style="display:flex;flex-direction:column;gap:6px;">
    <div v-click class="card" style="padding:8px 12px;border-left:4px solid #38bdf8;">
      <div style="font-weight:700;font-size:.72rem;color:var(--navy);">1. Access Modifier (<span class="mono" style="color:#38bdf8;">public / private / protected</span>)</div>
      <div style="font-size:.67rem;color:var(--slate);">Controls visibility and accessibility from other classes.</div>
    </div>
    <div v-click class="card" style="padding:8px 12px;border-left:4px solid #a855f7;">
      <div style="font-weight:700;font-size:.72rem;color:var(--navy);">2. Return Type (<span class="mono" style="color:#a855f7;">int, double, String, void</span>)</div>
      <div style="font-size:.67rem;color:var(--slate);">Data type of value returned. Use <span class="mono">void</span> if method returns nothing.</div>
    </div>
    <div v-click class="card" style="padding:8px 12px;border-left:4px solid #22c55e;">
      <div style="font-weight:700;font-size:.72rem;color:var(--navy);">3. Method Name (Identifier)</div>
      <div style="font-size:.67rem;color:var(--slate);">Follows <span class="mono">camelCase</span> convention starting with a lowercase verb (e.g. <span class="mono">calculateTax</span>).</div>
    </div>
    <div v-click class="card" style="padding:8px 12px;border-left:4px solid #f43f5e;">
      <div style="font-weight:700;font-size:.72rem;color:var(--navy);">4. Parameter List (<span class="mono" style="color:#f43f5e;">type name, ...</span>)</div>
      <div style="font-size:.67rem;color:var(--slate);">Comma-separated input variables enclosed in mandatory parentheses <span class="mono">()</span>.</div>
    </div>
  </div>

  <div v-click class="callout callout-info" style="margin-top:4px;">
    <div><strong>Method Signature:</strong> Consists only of the <strong>Method Name + Parameter Types</strong> (e.g. <span class="mono">addNumbers(int, int)</span>). Return type and access modifier are NOT part of the signature!</div>
  </div>

</div>

</div>

  </template>
</Slide2>
