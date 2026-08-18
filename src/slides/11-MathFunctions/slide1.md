<!-- ═══════════════════════════════════════════════════════
     SLIDE 1 — INTRODUCTION TO java.lang.Math
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Java Math Functions">
  <template #content>

<div class="slide-h1" style="margin-bottom:10px;">Introduction to <span class="highlight">java.lang.Math</span></div>

<div class="g2" style="gap:14px;align-items:start;">

<div class="flex-col">

  <div v-click class="card-navy" style="border-radius:10px;">
    <div style="font-size:.82rem;line-height:1.6;color:var(--slate);">
      <span class="mono" style="color:var(--red);font-weight:700;">java.lang.Math</span> is a <strong>final class</strong> in Java's standard library that provides a collection of <strong>static methods</strong> for common mathematical operations such as powers, roots, rounding, logarithms, and trigonometry.
    </div>
  </div>

  <div v-click class="callout callout-success">
    <div><strong>Auto-imported:</strong> The <span class="mono">java.lang</span> package is imported automatically in every Java program. You do <strong>not</strong> need to write <span class="mono">import java.lang.Math;</span> — just use <span class="mono">Math.methodName()</span> directly.</div>
  </div>

  <div v-click class="section-label" style="margin-top:6px;">Two Special Constants</div>

  <div style="display:flex;gap:8px;">
    <div v-click style="flex:1;background:#f0fff4;border:1px solid var(--green);border-radius:8px;padding:10px;text-align:center;">
      <div style="font-family:'Fira Code',monospace;font-weight:700;color:var(--green);font-size:.80rem;">Math.PI</div>
      <div style="font-size:.62rem;color:var(--slate);margin-top:4px;">π ≈ 3.14159265358979</div>
      <div style="font-size:.60rem;color:var(--muted);margin-top:2px;">Ratio of circumference to diameter of a circle</div>
    </div>
    <div v-click style="flex:1;background:#ebf8ff;border:1px solid var(--blue);border-radius:8px;padding:10px;text-align:center;">
      <div style="font-family:'Fira Code',monospace;font-weight:700;color:var(--blue);font-size:.80rem;">Math.E</div>
      <div style="font-size:.62rem;color:var(--slate);margin-top:4px;">e ≈ 2.71828182845905</div>
      <div style="font-size:.60rem;color:var(--muted);margin-top:2px;">Euler's number — base of the natural logarithm</div>
    </div>
  </div>

  <div v-click class="callout callout-info" style="margin-top:6px;">
    <div>Both <span class="mono">Math.PI</span> and <span class="mono">Math.E</span> are declared as <span class="mono">public static final double</span> — they are immutable constants.</div>
  </div>

</div>

<div class="flex-col">
  <div class="section-label" v-click>Why Use Math Methods?</div>

  <div style="display:flex;flex-direction:column;gap:8px;">
    <div v-click class="card" style="display:flex;gap:10px;align-items:flex-start;border:1px solid var(--blue);">
      <div class="icon-circle ic-blue" style="font-size:.9rem;">🧮</div>
      <div>
        <div style="font-size:.75rem;font-weight:600;color:var(--navy);">No Extra Imports Needed</div>
        <div style="font-size:.7rem;color:var(--slate);">All methods available by writing <span class="mono">Math.</span> prefix — zero setup required.</div>
      </div>
    </div>
    <div v-click class="card" style="display:flex;gap:10px;align-items:flex-start;border:1px solid var(--green);">
      <div class="icon-circle ic-green" style="font-size:.9rem;">⚡</div>
      <div>
        <div style="font-size:.75rem;font-weight:600;color:var(--navy);">High Performance</div>
        <div style="font-size:.7rem;color:var(--slate);">Many operations internally delegate to native CPU floating-point instructions.</div>
      </div>
    </div>
    <div v-click class="card" style="display:flex;gap:10px;align-items:flex-start;border:1px solid var(--orange);">
      <div class="icon-circle ic-orange" style="font-size:.9rem;">🔒</div>
      <div>
        <div style="font-size:.75rem;font-weight:600;color:var(--navy);">All Static — No Object Needed</div>
        <div style="font-size:.7rem;color:var(--slate);">You cannot instantiate <span class="mono">Math</span>. Every method is called directly on the class.</div>
      </div>
    </div>
    <div v-click class="card" style="display:flex;gap:10px;align-items:flex-start;border:1px solid var(--purple);">
      <div class="icon-circle ic-purple" style="font-size:.9rem;">📐</div>
      <div>
        <div style="font-size:.75rem;font-weight:600;color:var(--navy);">Covers All Core Math Needs</div>
        <div style="font-size:.7rem;color:var(--slate);">Powers, roots, rounding, extrema, trig, logs, and random numbers — all in one class.</div>
      </div>
    </div>
  </div>

</div>

</div>

  </template>
</Slide2>
