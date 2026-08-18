---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 20 — LOOP SELECTION GUIDE
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Loop Selection Guide">
  <template #content>

<div class="slide-h1" style="margin-bottom:10px;">Which Loop to Use? — <span class="highlight">Decision Matrix</span></div>

<div>
<table class="cmp-table" style="font-size:.68rem;">
  <thead>
    <tr>
      <th>Loop Type</th>
      <th>Check Type</th>
      <th>Min Runs</th>
      <th>Index Access?</th>
      <th>Primary Use Case in Java</th>
    </tr>
  </thead>
  <tbody>
    <tr v-click>
      <td><strong style="color:var(--red);">for loop</strong></td>
      <td>Pre-Test</td>
      <td>0</td>
      <td class="yes">Yes (via <code>i</code>)</td>
      <td>Known iteration count, range counting, indexing</td>
    </tr>
    <tr v-click>
      <td><strong style="color:var(--blue);">while loop</strong></td>
      <td>Pre-Test</td>
      <td>0</td>
      <td class="no">Manual</td>
      <td>Unknown iteration count, condition-based repetition</td>
    </tr>
    <tr v-click>
      <td><strong style="color:var(--orange);">do-while loop</strong></td>
      <td>Post-Test</td>
      <td class="yes"><strong>1 (Guaranteed)</strong></td>
      <td class="no">Manual</td>
      <td>User input validation, menu choice repetition</td>
    </tr>
    <tr v-click>
      <td><strong style="color:var(--purple);">for-each loop</strong></td>
      <td>Implicit</td>
      <td>0</td>
      <td class="no">No (Read-only)</td>
      <td>Traversing arrays &amp; Collections cleanly</td>
    </tr>
  </tbody>
</table>
</div>

<div class="g2" style="gap:10px;margin-top:12px;">

  <div v-click class="card card-green">
    <div class="slide-h3" style="margin-bottom:4px;">Rule of Thumb 1</div>
    <div class="body-text">If iterating through an array without needing to change elements or track indices &rarr; Use <strong>Enhanced For Loop</strong>.</div>
  </div>

  <div v-click class="card card-navy">
    <div class="slide-h3" style="margin-bottom:4px;">Rule of Thumb 2</div>
    <div class="body-text">If code must prompt the user at least once before checking validity &rarr; Use <strong>Do-While Loop</strong>.</div>
  </div>

</div>

  </template>
</Slide2>
