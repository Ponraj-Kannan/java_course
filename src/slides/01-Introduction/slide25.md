---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 25 — STRING CONCATENATION
═══════════════════════════════════════════════════════ -->

<Slide2 topic="String Concatenation in Java">
  <template #content>

<div class="slide-h1" style="margin-bottom:12px;">String <span class="highlight">Concatenation</span></div>

<div class="g2" style="gap:14px;align-items:start;">

<div class="flex-col">

  <div v-click class="card-navy" style="border-radius:10px;">
    <div style="font-size:.82rem;line-height:1.6;color:var(--slate);">
      In Java, the <strong style="color:var(--red);">+ operator</strong> joins (concatenates) strings together. You can also combine strings with numbers.
    </div>
  </div>

  <div v-click style="background:#f6f8fa;border-radius:10px;border:1px solid #e1e4e8;padding:14px;font-family:'Fira Code',monospace;font-size:.74rem;line-height:2;">
    <span style="color:#6b7280;">// Joining strings</span><br>
    <span style="color:#ef5050;">String</span> <span style="color:#0e6ead;">first</span> = <span style="color:#2d7a00;">"Hello"</span>;<br>
    <span style="color:#ef5050;">String</span> <span style="color:#0e6ead;">last</span> = <span style="color:#2d7a00;">"World"</span>;<br>
    <span style="color:#2d7a00;">System.out.println</span>(<span style="color:#0e6ead;">first</span> + <span style="color:#2d7a00;">" "</span> + <span style="color:#0e6ead;">last</span>);<br><br>
    <span style="color:#6b7280;">// Mixing strings with numbers</span><br>
    <span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">age</span> = <span style="color:#b45309;">20</span>;<br>
    <span style="color:#2d7a00;">System.out.println</span>(<span style="color:#2d7a00;">"Age: "</span> + <span style="color:#0e6ead;">age</span>);
  </div>

  <div v-click class="output-box">
    Hello World<br>
    Age: 20
  </div>

  <div v-click class="card card-green">
    <div class="small-text"><strong>Key idea:</strong> When <span class="mono">+</span> involves a String, Java converts the other value to String automatically.</div>
  </div>

</div>

<div class="flex-col">

  <div v-click class="section-label">Watch Out for This Trap!</div>

  <div v-after style="background:#f6f8fa;border-radius:10px;border:1px solid #e1e4e8;padding:14px;font-family:'Fira Code',monospace;font-size:.74rem;line-height:2;">
    <span style="color:#6b7280;">// Mixing numbers and strings</span><br>
    <span style="color:#2d7a00;">System.out.println</span>(<span style="color:#2d7a00;">"Sum: "</span> + <span style="color:#b45309;">5</span> + <span style="color:#b45309;">3</span>);<br>
    <span style="color:#6b7280;">// Output: Sum: 53  (not 8!)</span><br><br>
    <span style="color:#6b7280;">// Fix — use parentheses:</span><br>
    <span style="color:#2d7a00;">System.out.println</span>(<span style="color:#2d7a00;">"Sum: "</span> + (<span style="color:#b45309;">5</span> + <span style="color:#b45309;">3</span>));<br>
    <span style="color:#6b7280;">// Output: Sum: 8  ✓</span>
  </div>

  <div v-click class="callout callout-danger">
    <div><strong>Order matters!</strong> <span class="mono">"Sum: " + 5 + 3</span> → concatenates left-to-right → <strong>"Sum: 53"</strong></div>
  </div>

  <div v-click class="card card-blue" style="margin-top:6px;">
    <div class="slide-h3" style="margin-bottom:4px;">Text Blocks (Java 15+)</div>
    <div class="small-text">Use triple quotes <span class="mono">"""</span> for multi-line strings without escape sequences. Great for JSON, SQL, HTML inside Java.</div>
  </div>

</div>

</div>

  </template>
</Slide2>
