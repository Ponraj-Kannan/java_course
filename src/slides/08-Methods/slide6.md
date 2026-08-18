---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 6 — THE CALL STACK & STACK FRAMES
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Java Methods">
  <template #content>

<div class="slide-h1" style="margin-bottom:10px;">The <span class="highlight">Call Stack</span> &amp; Stack Frames</div>

<div class="g2" style="gap:14px;align-items:start;">

<div class="flex-col">

  <div v-click class="card-navy" style="border-radius:10px;">
    <div style="font-size:.82rem;line-height:1.6;color:var(--slate);">
      The <strong style="color:var(--red);">Call Stack</strong> is a Last-In, First-Out (LIFO) runtime memory structure where the JVM creates a new <strong>stack frame</strong> for each active method call to store its parameters and local variables.
    </div>
  </div>

  <div v-click class="section-label" style="margin-top:6px;">Call Stack Lifecycle</div>

  <div style="display:flex;flex-direction:column;gap:6px;">
    <div v-click class="card" style="padding:8px 12px;border-left:4px solid var(--blue);">
      <div style="font-weight:700;font-size:.72rem;color:var(--navy);">1. Method Call → PUSH Frame</div>
      <div style="font-size:.67rem;color:var(--slate);">A new frame with method arguments and local variables is pushed onto the top of the stack.</div>
    </div>
    <div v-click class="card" style="padding:8px 12px;border-left:4px solid var(--orange);">
      <div style="font-weight:700;font-size:.72rem;color:var(--navy);">2. Topmost Frame Executes</div>
      <div style="font-size:.67rem;color:var(--slate);">The CPU only executes the method at the very top of the stack (active frame).</div>
    </div>
    <div v-click class="card" style="padding:8px 12px;border-left:4px solid var(--green);">
      <div style="font-weight:700;font-size:.72rem;color:var(--navy);">3. Return → POP Frame</div>
      <div style="font-size:.67rem;color:var(--slate);">When the method returns, its frame is popped and destroyed; control resumes in caller.</div>
    </div>
  </div>

</div>

<div class="flex-col">
  <div v-click class="section-label">Call Stack Visual Diagram</div>

  <!-- DIAGRAM: CALL STACK -->
  <div v-after style="background:#f7f8fc;border:1px solid var(--border);border-radius:10px;padding:12px;font-size:.68rem;">
    <div style="font-weight:700;color:var(--navy);margin-bottom:6px;">📚 Stack Memory Growth (Bottom to Top):</div>
    <div style="display:flex;flex-direction:column;gap:6px;">
      <!-- Active Top Frame -->
      <div style="background:#fff0f0;border:2px solid var(--red);border-radius:6px;padding:6px 10px;">
        <div style="display:flex;justify-content:space-between;font-weight:700;color:var(--red-dark);font-family:'Fira Code',monospace;">
          <span>applyTax(double amount)</span>
          <span class="pill pill-red" style="font-size:.58rem;padding:2px 6px;">Active (Top)</span>
        </div>
        <div style="font-size:.62rem;color:var(--slate);margin-top:2px;">locals: amount = 100.0, rate = 0.05 → returns 105.0</div>
      </div>
      <!-- Caller Frame -->
      <div style="background:#ebf8ff;border:2px solid var(--blue);border-radius:6px;padding:6px 10px;">
        <div style="display:flex;justify-content:space-between;font-weight:700;color:var(--blue);font-family:'Fira Code',monospace;">
          <span>calcTotal()</span>
          <span class="pill pill-blue" style="font-size:.58rem;padding:2px 6px;">Waiting for applyTax</span>
        </div>
        <div style="font-size:.62rem;color:var(--slate);margin-top:2px;">locals: price = 100.0, total = waiting...</div>
      </div>
      <!-- Base Frame -->
      <div style="background:#f0fff4;border:2px solid var(--green);border-radius:6px;padding:6px 10px;">
        <div style="display:flex;justify-content:space-between;font-weight:700;color:var(--green);font-family:'Fira Code',monospace;">
          <span>main(String[] args)</span>
          <span class="pill pill-green" style="font-size:.58rem;padding:2px 6px;">Base Frame</span>
        </div>
        <div style="font-size:.62rem;color:var(--slate);margin-top:2px;">locals: args = [], started program execution</div>
      </div>
    </div>
  </div>

  <div v-click class="callout callout-info" style="margin-top:6px;">
    <div>Each stack frame has its own private set of variables. Variables in <span class="mono">applyTax()</span> cannot conflict with or access variables in <span class="mono">calcTotal()</span>.</div>
  </div>

</div>

</div>

  </template>
</Slide2>
