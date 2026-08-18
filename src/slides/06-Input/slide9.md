---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 9 — CONSOLE CLASS (SECURE PASSWORD INPUT)
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Java Input Methods">
  <template #content>

<div class="slide-h1" style="margin-bottom:10px;"><span class="highlight">Console</span> Class — Secure Passwords</div>

<div class="g2" style="gap:14px;align-items:start;">

<div class="flex-col">

  <div v-click class="card-navy" style="border-radius:10px;">
    <div style="font-size:.82rem;line-height:1.6;color:var(--slate);">
      The <strong style="color:var(--red);">Console</strong> class (in package <span class="mono">java.io</span>) provides methods to read text and <strong>passwords without echoing</strong> characters to the terminal, enhancing security.
    </div>
  </div>

  <div v-click class="section-label" style="margin-top:6px;">Key Methods of Console</div>

  <div style="display:flex;flex-direction:column;gap:6px;">
    <div v-click class="card" style="padding:8px 12px;border-left:4px solid var(--blue);">
      <div style="font-weight:700;font-size:.72rem;color:var(--navy);">System.console()</div>
      <div style="font-size:.68rem;color:var(--slate);">Returns the unique <span class="mono">Console</span> object associated with the current JVM terminal.</div>
    </div>
    <div v-click class="card" style="padding:8px 12px;border-left:4px solid var(--green);">
      <div style="font-weight:700;font-size:.72rem;color:var(--navy);">c.readLine(prompt)</div>
      <div style="font-size:.68rem;color:var(--slate);">Displays prompt and reads a full line as a <span class="mono">String</span>.</div>
    </div>
    <div v-click class="card" style="padding:8px 12px;border-left:4px solid var(--purple);">
      <div style="font-weight:700;font-size:.72rem;color:var(--navy);">c.readPassword(prompt)</div>
      <div style="font-size:.68rem;color:var(--slate);">Reads password as a <span class="mono">char[]</span> with <strong>character echoing disabled</strong>.</div>
    </div>
  </div>

  <div v-click class="callout callout-warn" style="margin-top:6px;">
    <div><strong>Security Note:</strong> <span class="mono">readPassword()</span> returns <span class="mono">char[]</span> (not <span class="mono">String</span>) so you can wipe it from memory with <span class="mono">Arrays.fill(pwd, ' ')</span> immediately after verification.</div>
  </div>

</div>

<div class="flex-col">
  <div v-click class="section-label">Code Example — Login Authentication</div>

  <div v-after class="code-block" style="font-size:.68rem;line-height:1.75;">
    <span style="color:#ef5050;">import</span> <span style="color:#0e6ead;">java.io.Console</span>;<br>
    <br>
    <span style="color:#ef5050;">public class</span> <span style="color:#0e6ead;">LoginApp</span> {<br>
    <span style="padding-left:16px;display:block;"><span style="color:#ef5050;">public static void</span> <span style="color:#0e6ead;">main</span>(<span style="color:#ef5050;">String</span>[] <span style="color:#0e6ead;">args</span>) {</span>
    <span style="padding-left:32px;display:block;"><span style="color:#ef5050;">Console</span> <span style="color:#0e6ead;">c</span> = <span style="color:#0e6ead;">System</span>.<span style="color:#2d7a00;">console</span>();</span>
    <br>
    <span style="padding-left:32px;display:block;"><span style="color:#6b7280;">// Check if terminal is available</span></span>
    <span style="padding-left:32px;display:block;"><span style="color:#ef5050;">if</span> (<span style="color:#0e6ead;">c</span> == <span style="color:#b45309;">null</span>) {</span>
    <span style="padding-left:48px;display:block;"><span style="color:#0e6ead;">System</span>.<span style="color:#0e6ead;">out</span>.<span style="color:#2d7a00;">println</span>(<span style="color:#2d7a00;">"No console attached! Run from terminal."</span>);</span>
    <span style="padding-left:48px;display:block;"><span style="color:#ef5050;">return</span>;</span>
    <span style="padding-left:32px;display:block;">}</span>
    <br>
    <span style="padding-left:32px;display:block;"><span style="color:#ef5050;">String</span> <span style="color:#0e6ead;">user</span> = <span style="color:#0e6ead;">c</span>.<span style="color:#2d7a00;">readLine</span>(<span style="color:#2d7a00;">"Username: "</span>);</span>
    <span style="padding-left:32px;display:block;"><span style="color:#ef5050;">char</span>[] <span style="color:#0e6ead;">pass</span> = <span style="color:#0e6ead;">c</span>.<span style="color:#2d7a00;">readPassword</span>(<span style="color:#2d7a00;">"Password: "</span>); <span style="color:#6b7280;">// hidden!</span></span>
    <br>
    <span style="padding-left:32px;display:block;"><span style="color:#0e6ead;">System</span>.<span style="color:#0e6ead;">out</span>.<span style="color:#2d7a00;">println</span>(<span style="color:#2d7a00;">"Welcome back, "</span> + <span style="color:#0e6ead;">user</span>);</span>
    <span style="padding-left:16px;display:block;">}</span>
    }
  </div>

  <div v-click class="callout callout-danger" style="margin-top:6px;">
    <div><strong>IDE Gotcha:</strong> <span class="mono">System.console()</span> returns <span class="mono">null</span> inside some IDEs (Eclipse/VS Code output pane). It must be run in a real operating system terminal!</div>
  </div>

</div>

</div>

  </template>
</Slide2>
