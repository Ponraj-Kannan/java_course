---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 15 — ACCESS MODIFIERS (public, static, void)
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Java Keywords — public · static · void">
  <template #content>

<div class="slide-h1" style="margin-bottom:10px;"><span class="highlight">public · static · void</span> Explained</div>

<div class="g2" style="gap:14px;align-items:start;">

<div class="flex-col">

  <div v-click class="card-navy" style="border-radius:10px;">
    <div style="font-size:.82rem;line-height:1.6;color:var(--slate);">
      The <span class="mono" style="color:var(--red);">main</span> method signature looks complex — but each keyword has a specific role.
    </div>
  </div>

  <div v-click style="background:#f6f8fa;border-radius:10px;border:1px solid #e1e4e8;padding:14px;font-family:'Fira Code',monospace;font-size:.78rem;line-height:2.2;">
    <span style="color:#ef5050;">public</span> <span style="color:#805ad5;">static</span> <span style="color:#38a169;">void</span> <span style="color:#0e6ead;">main</span>(<span style="color:#ef5050;">String</span>[] args) { }
  </div>

</div>

<div class="flex-col">

  <div style="display:flex;flex-direction:column;gap:8px;">
    <div v-click style="display:flex;gap:10px;align-items:flex-start;">
      <div style="background:var(--red-soft);border:2px solid var(--red);border-radius:8px;padding:6px 14px;min-width:80px;text-align:center;">
        <div style="font-family:'Fira Code',monospace;font-weight:800;color:var(--red-dark);font-size:.8rem;">public</div>
      </div>
      <div class="small-text" style="padding-top:4px;"><strong>Access modifier</strong> — anyone (including the JVM) can call this method. No restrictions.</div>
    </div>
    <div v-click style="display:flex;gap:10px;align-items:flex-start;">
      <div style="background:#faf5ff;border:2px solid var(--purple);border-radius:8px;padding:6px 14px;min-width:80px;text-align:center;">
        <div style="font-family:'Fira Code',monospace;font-weight:800;color:var(--purple);font-size:.8rem;">static</div>
      </div>
      <div class="small-text" style="padding-top:4px;"><strong>No object needed</strong> — JVM can call <span class="mono">main()</span> directly without creating a class instance.</div>
    </div>
    <div v-click style="display:flex;gap:10px;align-items:flex-start;">
      <div style="background:#f0fff4;border:2px solid var(--green);border-radius:8px;padding:6px 14px;min-width:80px;text-align:center;">
        <div style="font-family:'Fira Code',monospace;font-weight:800;color:var(--green);font-size:.8rem;">void</div>
      </div>
      <div class="small-text" style="padding-top:4px;"><strong>Return type</strong> — this method does not return any value to the caller.</div>
    </div>
    <div v-click style="display:flex;gap:10px;align-items:flex-start;">
      <div style="background:#ebf8ff;border:2px solid var(--blue);border-radius:8px;padding:6px 14px;min-width:80px;text-align:center;">
        <div style="font-family:'Fira Code',monospace;font-weight:800;color:var(--blue);font-size:.75rem;">String[]</div>
      </div>
      <div class="small-text" style="padding-top:4px;"><strong>Command-line args</strong> — an array of strings passed when running the program from terminal.</div>
    </div>

  </div>

  <div v-click class="callout callout-warn" style="margin-top:6px;">
    <div><strong>Memorise this signature:</strong> <span class="mono">public static void main(String[] args)</span> — Java requires this exact signature to find the entry point.</div>
  </div>

</div>

</div>

  </template>
</Slide2>
