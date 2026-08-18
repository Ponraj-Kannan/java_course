---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 8 — CODING PRACTICE
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Comments">
  <template #content>

<div class="slide-h1" style="margin-bottom:10px;">Coding <span class="highlight">Practice</span></div>

<div class="g2" style="gap:14px;align-items:start;">

<div class="flex-col">

  <div class="activity-box">
    <div class="act-title">🖥 Java Comments Exercises</div>

    <div class="act-task" v-click>
      <div style="font-size:.7rem;font-weight:700;color:var(--navy);margin-bottom:4px;">Exercise 1 — Add Appropriate Comments</div>
      <div style="font-size:.72rem;color:var(--slate);">The code below has no comments. Add meaningful single-line comments explaining the <em>why</em> behind each step — not just what the line does.</div>
      <div style="font-family:'Fira Code',monospace;font-size:.66rem;background:#f6f8fa;border:1px solid var(--border);border-radius:6px;padding:8px;margin-top:6px;line-height:1.8;">
        <span style="color:#ef5050;">double</span> principal = <span style="color:#b45309;">10000</span>;<br>
        <span style="color:#ef5050;">double</span> rate = <span style="color:#b45309;">0.07</span>;<br>
        <span style="color:#ef5050;">int</span> years = <span style="color:#b45309;">5</span>;<br>
        <span style="color:#ef5050;">double</span> interest = principal * rate * years;<br>
        System.out.<span style="color:#2d7a00;">println</span>(<span style="color:#2d7a00;">"Interest: ₹"</span> + interest);
      </div>
      <div class="hint">💡 Think: why is rate 0.07? why multiply by years?</div>
    </div>

    <div class="act-task" v-click>
      <div style="font-size:.7rem;font-weight:700;color:var(--navy);margin-bottom:4px;">Exercise 2 — Fix the Broken Comment</div>
      <div style="font-size:.72rem;color:var(--slate);">The following program fails to compile. Find and fix the error — then explain why it caused a problem.</div>
      <div style="font-family:'Fira Code',monospace;font-size:.66rem;background:var(--red-soft);border:1px solid var(--red);border-radius:6px;padding:8px;margin-top:6px;line-height:1.8;">
        <span style="color:#ef5050;">/*</span><br>
        <span style="color:#ef5050;">&nbsp; Greet the user by name</span><br>
        String name = <span style="color:#2d7a00;">"Alice"</span>;<br>
        System.out.<span style="color:#2d7a00;">println</span>(<span style="color:#2d7a00;">"Hello, "</span> + name);
      </div>
      <div class="hint">💡 Hint: count the comment delimiters carefully</div>
    </div>

  </div>

</div>

<div class="flex-col">

  <div class="activity-box">

    <div class="act-task" v-click>
      <div style="font-size:.7rem;font-weight:700;color:var(--navy);margin-bottom:4px;">Exercise 3 — Good vs Bad Practice</div>
      <div style="font-size:.72rem;color:var(--slate);">Look at these two code snippets and decide: which one uses comments well, and which one misuses them? Rewrite the bad snippet with improved commenting.</div>
      <div style="display:flex;gap:8px;margin-top:6px;">
        <div style="flex:1;font-family:'Fira Code',monospace;font-size:.64rem;background:var(--red-soft);border:1px solid var(--red);border-radius:6px;padding:8px;line-height:1.8;">
          <span style="color:#6b7280;">// Add a to b</span><br>
          <span style="color:#0e6ead;">int</span> c = a + b;<br>
          <span style="color:#6b7280;">// print c</span><br>
          System.out.<span style="color:#2d7a00;">println</span>(c);
        </div>
        <div style="flex:1;font-family:'Fira Code',monospace;font-size:.64rem;background:#f0fff4;border:1px solid var(--green);border-radius:6px;padding:8px;line-height:1.8;">
          <span style="color:#6b7280;">// Combine base and bonus</span><br>
          <span style="color:#6b7280;">// salary before tax deductions</span><br>
          <span style="color:#0e6ead;">int</span> gross = base + bonus;<br>
          System.out.<span style="color:#2d7a00;">println</span>(gross);
        </div>
      </div>
      <div class="hint">💡 Left: bad (states the obvious). Right: good (explains why)</div>
    </div>

    <div class="act-task" v-click>
      <div style="font-size:.7rem;font-weight:700;color:var(--navy);margin-bottom:4px;">Exercise 4 — Write a Javadoc Comment</div>
      <div style="font-size:.72rem;color:var(--slate);">Write a proper <span class="mono">/** */</span> Javadoc comment for this method. Include <span class="mono">@param</span>, <span class="mono">@return</span>, and a one-line description.</div>
      <div style="font-family:'Fira Code',monospace;font-size:.66rem;background:#f6f8fa;border:1px solid var(--border);border-radius:6px;padding:8px;margin-top:6px;line-height:1.8;">
        <span style="color:#ef5050;">int</span> <span style="color:#2d7a00;">power</span>(<span style="color:#ef5050;">int</span> base, <span style="color:#ef5050;">int</span> exponent) {<br>
        &nbsp;&nbsp;<span style="color:#ef5050;">return</span> (<span style="color:#ef5050;">int</span>) Math.<span style="color:#2d7a00;">pow</span>(base, exponent);<br>
        }
      </div>
      <div class="hint">💡 Place the /** */ block directly above the method signature</div>
    </div>

    <div v-click class="callout callout-success" style="margin-top:6px;">
      <div><strong>Bonus:</strong> Take any program you wrote in a previous module and add appropriate comments throughout — using all three comment types where suitable.</div>
    </div>

  </div>

</div>

</div>

  </template>
</Slide2>
