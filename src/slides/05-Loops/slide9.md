---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 9 — WHILE vs DO-WHILE COMPARISON
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Comparison">
  <template #content>

<div class="slide-h1" style="margin-bottom:10px;"><span class="highlight">while</span> vs <span class="highlight">do-while</span> Loop</div>

<div>
<table class="cmp-table">
  <thead>
    <tr>
      <th>Feature</th>
      <th>while Loop (Pre-Test)</th>
      <th>do-while Loop (Post-Test)</th>
    </tr>
  </thead>
  <tbody>
    <tr v-click>
      <td><strong>Condition Check</strong></td>
      <td>Evaluated <strong>before</strong> entering body</td>
      <td>Evaluated <strong>after</strong> executing body</td>
    </tr>
    <tr v-click>
      <td><strong>Minimum Runs</strong></td>
      <td class="no"><strong>0 times</strong> (if initial condition false)</td>
      <td class="yes"><strong>At least 1 time</strong> (guaranteed)</td>
    </tr>
    <tr v-click>
      <td><strong>Ending Semicolon</strong></td>
      <td>No semicolon after <code>while(cond)</code></td>
      <td class="no">Mandatory semicolon after <code>while(cond);</code></td>
    </tr>
    <tr v-click>
      <td><strong>Best Used For</strong></td>
      <td>General looping when entry is conditional</td>
      <td>User input menus, retry prompts, validation</td>
    </tr>
  </tbody>
</table>
</div>

<div class="g2" style="gap:10px;margin-top:12px;">

  <div v-click style="background:#f6f8fa;border-radius:10px;border:1px solid #e1e4e8;padding:12px;font-family:'Fira Code',monospace;font-size:.7rem;line-height:1.9;">
    <div style="color:#ef5050;font-weight:700;margin-bottom:6px;">while Loop (0 executions)</div>
    <span style="color:#0e6ead;">int</span> x = <span style="color:#b45309;">10</span>;<br>
    <span style="color:#ef5050;">while</span> (x &lt; <span style="color:#b45309;">5</span>) {<br>
    <span style="padding-left:20px;display:block;">System.out.<span style="color:#2d7a00;">println</span>(<span style="color:#2d7a00;">"Inside while"</span>);</span>
    }<br>
    <span style="color:#6b7280;">// Output: (Nothing printed)</span>
  </div>

  <div v-click style="background:#f6f8fa;border-radius:10px;border:1px solid #e1e4e8;padding:12px;font-family:'Fira Code',monospace;font-size:.7rem;line-height:1.9;">
    <div style="color:#2d7a00;font-weight:700;margin-bottom:6px;">do-while Loop (1 execution)</div>
    <span style="color:#0e6ead;">int</span> x = <span style="color:#b45309;">10</span>;<br>
    <span style="color:#ef5050;">do</span> {<br>
    <span style="padding-left:20px;display:block;">System.out.<span style="color:#2d7a00;">println</span>(<span style="color:#2d7a00;">"Inside do-while"</span>);</span>
    } <span style="color:#ef5050;">while</span> (x &lt; <span style="color:#b45309;">5</span>);<br>
    <span style="color:#2d7a00;">// Output: Inside do-while</span>
  </div>

</div>

  </template>
</Slide2>
