---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 11 — COMPARISON OF ALL 4 INPUT METHODS
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Java Input Methods">
  <template #content>

<div class="slide-h1" style="margin-bottom:10px;">Comparison of <span class="highlight">All Input Methods</span></div>

<div class="g2" style="gap:14px;align-items:start;">

<div class="flex-col">

  <div style="margin-top:2px;">
    <table class="cmp-table" style="font-size:.66rem;">
      <thead v-click>
        <tr>
          <th>Feature</th>
          <th>Scanner</th>
          <th>BufferedReader</th>
          <th>Console</th>
          <th>CLI Args</th>
        </tr>
      </thead>
      <tbody>
        <tr v-click>
          <td>Package</td>
          <td class="mono">java.util</td>
          <td class="mono">java.io</td>
          <td class="mono">java.io</td>
          <td>Built-in (<span class="mono">main</span>)</td>
        </tr>
        <tr v-click>
          <td>Performance</td>
          <td>Moderate (1KB buffer)</td>
          <td class="yes">Fastest (8KB buffer)</td>
          <td>Fast</td>
          <td class="yes">Instant</td>
        </tr>
        <tr v-click>
          <td>Auto-Parses Primitives?</td>
          <td class="yes">Yes (<span class="mono">nextInt()</span>)</td>
          <td class="no">No (returns <span class="mono">String</span>)</td>
          <td class="no">No (returns <span class="mono">String</span>)</td>
          <td class="no">No (<span class="mono">String[]</span>)</td>
        </tr>
        <tr v-click>
          <td>Masks Passwords?</td>
          <td class="no">No</td>
          <td class="no">No</td>
          <td class="yes">Yes (<span class="mono">readPassword</span>)</td>
          <td class="no">No</td>
        </tr>
        <tr v-click>
          <td>Handles Exceptions?</td>
          <td class="yes">Unchecked runtime</td>
          <td class="no"><span class="mono">throws IOException</span></td>
          <td class="yes">Unchecked</td>
          <td class="yes">Unchecked</td>
        </tr>
        <tr v-click>
          <td>Thread Safe?</td>
          <td class="no">Not synchronized</td>
          <td class="yes">Synchronized</td>
          <td>Synchronized</td>
          <td>N/A</td>
        </tr>
      </tbody>
    </table>
  </div>

</div>

<div class="flex-col">
  <div v-click class="section-label">When Should You Use Each?</div>

  <div style="display:flex;flex-direction:column;gap:6px;">
    <div v-click class="card" style="padding:8px 12px;border-left:4px solid var(--blue);">
      <span class="pill pill-blue">Use Scanner</span>
      <div style="font-size:.68rem;color:var(--slate);margin-top:2px;">Simple console apps, homework assignments, mixed primitive data reading (<span class="mono">int</span> + <span class="mono">double</span>).</div>
    </div>
    <div v-click class="card" style="padding:8px 12px;border-left:4px solid var(--green);">
      <span class="pill pill-green">Use BufferedReader</span>
      <div style="font-size:.68rem;color:var(--slate);margin-top:2px;">Competitive programming (Codeforces, LeetCode), large files, multi-threaded apps.</div>
    </div>
    <div v-click class="card" style="padding:8px 12px;border-left:4px solid var(--purple);">
      <span class="pill pill-purple">Use Console</span>
      <div style="font-size:.68rem;color:var(--slate);margin-top:2px;">CLI tools that require secure password or credential entry without echoing.</div>
    </div>
    <div v-click class="card" style="padding:8px 12px;border-left:4px solid var(--orange);">
      <span class="pill pill-orange">Use CLI Args</span>
      <div style="font-size:.68rem;color:var(--slate);margin-top:2px;">Automation scripts, batch pipelines, configuration flags (<span class="mono">--debug</span>, file paths).</div>
    </div>
  </div>

</div>

</div>

  </template>
</Slide2>
