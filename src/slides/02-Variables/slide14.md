---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 14 — DEFAULT VALUES
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Java Variables">
  <template #content>

<div class="slide-h1" style="margin-bottom:10px;"><span class="highlight">Default Values</span> of Variables</div>

<div class="g2" style="gap:14px;align-items:start;">

<div class="flex-col">

  <div v-click class="card-navy" style="border-radius:10px;">
    <div style="font-size:.82rem;line-height:1.6;color:var(--slate);">
      <strong style="color:var(--red);">Definition:</strong> <strong>Instance</strong> and <strong>static</strong> variables automatically receive a default value when declared. <strong>Local variables do NOT</strong> — you must assign a value explicitly before using them.
    </div>
  </div>

  <div v-click class="section-label">Default Values — Instance &amp; Static</div>

  <div>
    <table class="cmp-table">
      <thead v-click>
        <tr><th>Type</th><th>Default Value</th></tr>
      </thead>
      <tbody>
        <tr v-click><td class="mono">byte, short, int</td><td class="mono yes">0</td></tr>
        <tr v-click><td class="mono">long</td><td class="mono yes">0L</td></tr>
        <tr v-click><td class="mono">float</td><td class="mono yes">0.0f</td></tr>
        <tr v-click><td class="mono">double</td><td class="mono yes">0.0</td></tr>
        <tr v-click><td class="mono">char</td><td class="mono yes">'\u0000' (null char)</td></tr>
        <tr v-click><td class="mono">boolean</td><td class="mono yes">false</td></tr>
        <tr v-click><td class="mono">Object / String / any ref</td><td class="mono no">null</td></tr>
      </tbody>
    </table>
  </div>

</div>

<div class="flex-col">

  <div v-click class="section-label">Code Illustration</div>

  <div v-after style="background:#f6f8fa;border-radius:10px;border:1px solid #e1e4e8;padding:14px;font-family:'Fira Code',monospace;font-size:.72rem;line-height:1.9;">
    <span style="color:#ef5050;">class</span> <span style="color:#0e6ead;">Demo</span> {<br>
    &nbsp;&nbsp;<span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">count</span>; &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#6b7280;">// instance → 0</span><br>
    &nbsp;&nbsp;<span style="color:#ef5050;">String</span> <span style="color:#0e6ead;">text</span>; &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#6b7280;">// instance → null</span><br>
    &nbsp;&nbsp;<span style="color:#ef5050;">static</span> <span style="color:#ef5050;">boolean</span> <span style="color:#0e6ead;">flag</span>; <span style="color:#6b7280;">// static → false</span><br><br>
    &nbsp;&nbsp;<span style="color:#ef5050;">void</span> <span style="color:#2d7a00;">show</span>() {<br>
    &nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#0e6ead;">System</span>.<span style="color:#0e6ead;">out</span>.<span style="color:#2d7a00;">println</span>(<span style="color:#0e6ead;">count</span>);<span style="color:#6b7280;"> // 0</span><br>
    &nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#0e6ead;">System</span>.<span style="color:#0e6ead;">out</span>.<span style="color:#2d7a00;">println</span>(<span style="color:#0e6ead;">text</span>);&nbsp;<span style="color:#6b7280;"> // null</span><br>
    &nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#0e6ead;">System</span>.<span style="color:#0e6ead;">out</span>.<span style="color:#2d7a00;">println</span>(<span style="color:#0e6ead;">flag</span>);&nbsp;<span style="color:#6b7280;"> // false</span><br>
    &nbsp;&nbsp;}<br>
    }
  </div>

  <div v-click class="callout callout-danger" style="margin-top:6px;">
    <div><strong>⚠ Local variable gotcha:</strong></div>
    <div style="margin-top:4px;background:#f6f8fa;border-radius:6px;padding:8px;font-family:'Fira Code',monospace;font-size:.7rem;line-height:1.8;">
      <span style="color:#ef5050;">void</span> <span style="color:#2d7a00;">compute</span>() {<br>
      &nbsp;&nbsp;<span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">x</span>; <span style="color:#6b7280;">// no default!</span><br>
      &nbsp;&nbsp;<span style="color:#0e6ead;">System</span>.<span style="color:#0e6ead;">out</span>.<span style="color:#2d7a00;">println</span>(<span style="color:#0e6ead;">x</span>); <span style="color:#ef5050;">// COMPILE ERROR</span><br>
      }
    </div>
  </div>

  <div v-click class="callout callout-success" style="margin-top:4px;">
    <div><strong>Rule to remember:</strong> Only <strong>local variables</strong> require explicit initialization. Instance and static variables are safe to use without explicit assignment (they have defaults).</div>
  </div>

</div>

</div>

  </template>
</Slide2>
