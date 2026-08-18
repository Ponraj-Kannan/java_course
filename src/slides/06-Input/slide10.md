---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 10 — COMMAND-LINE ARGUMENTS
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Java Input Methods">
  <template #content>

<div class="slide-h1" style="margin-bottom:10px;">Command-Line <span class="highlight">Arguments</span></div>

<div class="g2" style="gap:14px;align-items:start;">

<div class="flex-col">

  <div v-click class="card-navy" style="border-radius:10px;">
    <div style="font-size:.82rem;line-height:1.6;color:var(--slate);">
      <strong style="color:var(--red);">Command-line arguments</strong> are values supplied to a Java program when it is executed from the terminal. Java automatically packages them into the <span class="mono">String[] args</span> parameter in <span class="mono">main(String[] args)</span>.
    </div>
  </div>

  <div v-click class="section-label" style="margin-top:6px;">Terminal Execution Syntax</div>

  <div v-after style="background:#1e293b;border-radius:8px;padding:10px 14px;color:#f8fafc;font-family:'Fira Code',monospace;font-size:.70rem;line-height:1.8;">
    <div style="color:#94a3b8;">$ javac App.java</div>
    <div style="color:#22c55e;">$ java App Alice 25 Chennai</div>
    <div style="color:#cbd5e1;margin-top:4px;">
      args[0] = "Alice"<br>
      args[1] = "25"<br>
      args[2] = "Chennai"<br>
      args.length = 3
    </div>
  </div>

  <div v-click class="callout callout-warn" style="margin-top:6px;">
    <div><strong>ArrayIndexOutOfBoundsException:</strong> Accessing <span class="mono">args[0]</span> when no arguments were supplied will crash your program. Always check <span class="mono">args.length</span> first!</div>
  </div>

</div>

<div class="flex-col">
  <div v-click class="section-label">Code Example — Argument Handling</div>

  <div v-after class="code-block" style="font-size:.68rem;line-height:1.75;">
    <span style="color:#ef5050;">public class</span> <span style="color:#0e6ead;">CmdCalc</span> {<br>
    <span style="padding-left:16px;display:block;"><span style="color:#ef5050;">public static void</span> <span style="color:#0e6ead;">main</span>(<span style="color:#ef5050;">String</span>[] <span style="color:#0e6ead;">args</span>) {</span>
    <span style="padding-left:32px;display:block;"><span style="color:#6b7280;">// 1. Validate argument count</span></span>
    <span style="padding-left:32px;display:block;"><span style="color:#ef5050;">if</span> (<span style="color:#0e6ead;">args</span>.<span style="color:#0e6ead;">length</span> &lt; <span style="color:#b45309;">2</span>) {</span>
    <span style="padding-left:48px;display:block;"><span style="color:#0e6ead;">System</span>.<span style="color:#0e6ead;">out</span>.<span style="color:#2d7a00;">println</span>(<span style="color:#2d7a00;">"Usage: java CmdCalc &lt;num1&gt; &lt;num2&gt;"</span>);</span>
    <span style="padding-left:48px;display:block;"><span style="color:#ef5050;">return</span>;</span>
    <span style="padding-left:32px;display:block;">}</span>
    <br>
    <span style="padding-left:32px;display:block;"><span style="color:#6b7280;">// 2. Parse arguments from String to int</span></span>
    <span style="padding-left:32px;display:block;"><span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">a</span> = <span style="color:#0e6ead;">Integer</span>.<span style="color:#2d7a00;">parseInt</span>(<span style="color:#0e6ead;">args</span>[<span style="color:#b45309;">0</span>]);</span>
    <span style="padding-left:32px;display:block;"><span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">b</span> = <span style="color:#0e6ead;">Integer</span>.<span style="color:#2d7a00;">parseInt</span>(<span style="color:#0e6ead;">args</span>[<span style="color:#b45309;">1</span>]);</span>
    <br>
    <span style="padding-left:32px;display:block;"><span style="color:#0e6ead;">System</span>.<span style="color:#0e6ead;">out</span>.<span style="color:#2d7a00;">println</span>(<span style="color:#2d7a00;">"Sum = "</span> + (<span style="color:#0e6ead;">a</span> + <span style="color:#0e6ead;">b</span>));</span>
    <span style="padding-left:16px;display:block;">}</span>
    }
  </div>

  <div v-click class="callout callout-info" style="margin-top:6px;">
    <div><strong>Key Property:</strong> All command-line arguments are passed as <strong>Strings</strong>, even if they contain numbers like <span class="mono">"25"</span>. You must explicitly parse them.</div>
  </div>

</div>

</div>

  </template>
</Slide2>
