---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 11 — RECURSION & THE RECURSIVE CALL STACK
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Java Methods">
  <template #content>

<div class="slide-h1" style="margin-bottom:10px;"><span class="highlight">Recursion</span> &amp; The Recursive Call Stack</div>

<div class="g2" style="gap:14px;align-items:start;">

<div class="flex-col">

  <div v-click class="card-navy" style="border-radius:10px;">
    <div style="font-size:.82rem;line-height:1.6;color:var(--slate);">
      <strong style="color:var(--red);">Recursion</strong> is a programming technique where a method <strong>calls itself</strong> to break a problem into smaller sub-problems until reaching a terminating <strong>base case</strong>.
    </div>
  </div>

  <div v-click class="section-label" style="margin-top:6px;">Two Essential Parts of Every Recursive Method</div>

  <div style="display:flex;flex-direction:column;gap:6px;">
    <div v-click class="card" style="padding:8px 12px;border-left:4px solid var(--green);">
      <div style="font-weight:700;font-size:.72rem;color:var(--navy);">1. Base Case (Stopping Condition)</div>
      <div style="font-size:.67rem;color:var(--slate);">Condition that returns directly without making further recursive calls.</div>
    </div>
    <div v-click class="card" style="padding:8px 12px;border-left:4px solid var(--blue);">
      <div style="font-weight:700;font-size:.72rem;color:var(--navy);">2. Recursive Case (Self Call)</div>
      <div style="font-size:.67rem;color:var(--slate);">Calls the method with smaller/modified input progressing toward the base case.</div>
    </div>
  </div>

  <div v-click class="callout callout-danger" style="margin-top:6px;">
    <div><strong>StackOverflowError:</strong> If the base case is missing or never reached, recursive calls push infinite frames onto the call stack until memory is exhausted!</div>
  </div>

</div>

<div class="flex-col">
  <div v-click class="section-label">Recursive Unwinding Diagram — factorial(3)</div>

  <!-- DIAGRAM: RECURSIVE CALL STACK UNWINDING -->
  <div v-after style="background:#f7f8fc;border:1px solid var(--border);border-radius:10px;padding:12px;font-size:.68rem;">
    <div style="font-weight:700;color:var(--navy);margin-bottom:6px;">🔄 Stack Growth (Descent) ➔ Resolution (Unwind):</div>
    <div style="display:flex;flex-direction:column;gap:5px;font-family:'Fira Code',monospace;">
      <!-- Base Case Frame -->
      <div style="background:#f0fff4;border:2px solid var(--green);border-radius:6px;padding:5px 8px;">
        <div style="color:var(--green);font-weight:700;">factorial(1) → hits base case! Returns 1</div>
      </div>
      <!-- Frame 2 -->
      <div style="background:#ebf8ff;border:1px solid var(--blue);border-radius:6px;padding:5px 8px;">
        <div style="color:var(--blue);font-weight:700;">factorial(2) = 2 * factorial(1) = 2 * 1 = 2</div>
      </div>
      <!-- Frame 3 -->
      <div style="background:#fdf2f8;border:1px solid #ec4899;border-radius:6px;padding:5px 8px;">
        <div style="color:#be185d;font-weight:700;">factorial(3) = 3 * factorial(2) = 3 * 2 = 6</div>
      </div>
    </div>
    <div style="margin-top:8px;font-size:.64rem;color:var(--slate);line-height:1.5;">
      1. <strong>Winding:</strong> <span class="mono">fact(3) → fact(2) → fact(1)</span> pushes 3 stack frames.<br>
      2. <strong>Unwinding:</strong> <span class="mono">1 → 2 → 6</span> resolves values back up and pops frames.
    </div>
  </div>

  <div v-click class="code-block" style="margin-top:6px;font-size:.66rem;">
    <span style="color:#ef5050;">public static int</span> <span style="color:#0e6ead;">factorial</span>(<span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">n</span>) {<br>
    &nbsp;&nbsp;<span style="color:#ef5050;">if</span> (n &lt;= <span style="color:#b45309;">1</span>) <span style="color:#ef5050;">return</span> <span style="color:#b45309;">1</span>; <span style="color:#64748b;">// Base case</span><br>
    &nbsp;&nbsp;<span style="color:#ef5050;">return</span> n * <span style="color:#0e6ead;">factorial</span>(n - <span style="color:#b45309;">1</span>); <span style="color:#64748b;">// Recursive case</span><br>
    }
  </div>

</div>

</div>

  </template>
</Slide2>
