---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 13 — SUMMARY & EXAM CHEAT-SHEET
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Java Methods">
  <template #content>

<div class="slide-h1" style="margin-bottom:10px;">Module <span class="highlight">Summary</span> &amp; Exam Checklist</div>

<div class="g2" style="gap:14px;align-items:start;">

<div class="flex-col">

  <div class="section-label" v-click>Core Takeaways</div>

  <div style="display:flex;flex-direction:column;gap:6px;">
    <div v-click class="card" style="padding:8px 12px;border-left:4px solid var(--blue);">
      <div style="font-weight:700;font-size:.72rem;color:var(--navy);">1. Method Anatomy &amp; Signature</div>
      <div style="font-size:.67rem;color:var(--slate);">Signature is <strong>Name + Parameter Types</strong> only. Return type is not part of signature.</div>
    </div>
    <div v-click class="card" style="padding:8px 12px;border-left:4px solid var(--green);">
      <div style="font-weight:700;font-size:.72rem;color:var(--navy);">2. Strict Pass-by-Value</div>
      <div style="font-size:.67rem;color:var(--slate);">Primitives pass copies of values; reference types pass copies of memory addresses.</div>
    </div>
    <div v-click class="card" style="padding:8px 12px;border-left:4px solid var(--orange);">
      <div style="font-weight:700;font-size:.72rem;color:var(--navy);">3. Static vs Instance</div>
      <div style="font-size:.67rem;color:var(--slate);"><span class="mono">static</span> methods belong to class and cannot access instance variables or <span class="mono">this</span>.</div>
    </div>
    <div v-click class="card" style="padding:8px 12px;border-left:4px solid var(--purple);">
      <div style="font-weight:700;font-size:.72rem;color:var(--navy);">4. Method Overloading</div>
      <div style="font-size:.67rem;color:var(--slate);">Same method name, different parameter lists (count, type, or order) resolved at compile time.</div>
    </div>
  </div>

</div>

<div class="flex-col">
  <div v-click class="section-label">Exam / Viva Fast Rules</div>

  <div v-after style="background:#f7f8fc;border:1px solid var(--border);border-radius:10px;padding:12px;font-size:.70rem;line-height:1.8;">
    <div style="font-weight:700;color:var(--navy);margin-bottom:6px;">⚡ Quick Rules to Remember:</div>
    <div>🔹 <strong>Can main() be overloaded?</strong> → <span class="pill pill-green" style="font-size:.62rem;">Yes, but JVM only calls standard main(String[])</span></div>
    <div>🔹 <strong>Is Java pass-by-reference?</strong> → <span class="pill pill-red" style="font-size:.62rem;">No! Strictly pass-by-value</span></div>
    <div>🔹 <strong>Can a void method use return?</strong> → <span class="pill pill-blue" style="font-size:.62rem;">Yes, as "return;" for early exit</span></div>
    <div>🔹 <strong>Where do method calls execute?</strong> → <span class="pill pill-purple" style="font-size:.62rem;">In Call Stack frames (LIFO)</span></div>
  </div>

  <div v-click class="callout callout-success" style="margin-top:8px;">
    <div><strong>Ready for Practice:</strong> Proceed to the coding practice slides to test your method design, overloading, pass-by-value tracing, and recursion skills!</div>
  </div>

</div>

</div>

  </template>
</Slide2>
