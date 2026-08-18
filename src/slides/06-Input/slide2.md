---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 2 — SCANNER CLASS: SETUP & LIFECYCLE
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Java Input Methods">
  <template #content>

<div class="slide-h1" style="margin-bottom:10px;"><span class="highlight">Scanner</span> Class — Setup &amp; Basics</div>

<div class="g2" style="gap:14px;align-items:start;">

<div class="flex-col">

  <div v-click class="card-navy" style="border-radius:10px;">
    <div style="font-size:.82rem;line-height:1.6;color:var(--slate);">
      The <strong style="color:var(--red);">Scanner</strong> class (in package <span class="mono">java.util</span>) is a simple text parser that breaks input into tokens using delimiter patterns and converts them into primitive types and strings.
    </div>
  </div>

  <div v-click class="section-label" style="margin-top:6px;">4-Step Lifecycle of Scanner</div>

  <div style="display:flex;flex-direction:column;gap:6px;">
    <div v-click class="card" style="padding:8px 12px;border-left:4px solid var(--blue);">
      <div style="font-weight:700;font-size:.72rem;color:var(--navy);">1. Import the package</div>
      <div class="mono" style="font-size:.68rem;color:var(--blue);">import java.util.Scanner;</div>
    </div>
    <div v-click class="card" style="padding:8px 12px;border-left:4px solid var(--green);">
      <div style="font-weight:700;font-size:.72rem;color:var(--navy);">2. Create a Scanner object</div>
      <div class="mono" style="font-size:.68rem;color:var(--green);">Scanner sc = new Scanner(System.in);</div>
    </div>
    <div v-click class="card" style="padding:8px 12px;border-left:4px solid var(--orange);">
      <div style="font-weight:700;font-size:.72rem;color:var(--navy);">3. Read values using methods</div>
      <div class="mono" style="font-size:.68rem;color:var(--orange);">int age = sc.nextInt();</div>
    </div>
    <div v-click class="card" style="padding:8px 12px;border-left:4px solid var(--red);">
      <div style="font-weight:700;font-size:.72rem;color:var(--navy);">4. Close the Scanner</div>
      <div class="mono" style="font-size:.68rem;color:var(--red);">sc.close(); <span style="color:var(--slate);font-size:.62rem;">// release underlying stream resources</span></div>
    </div>
  </div>

</div>

<div class="flex-col">
  <div v-click class="section-label">Complete Java Example</div>

  <div v-after class="code-block" style="font-size:.70rem;line-height:1.8;">
    <span style="color:#ef5050;">import</span> <span style="color:#0e6ead;">java.util.Scanner</span>;<br>
    <br>
    <span style="color:#ef5050;">public class</span> <span style="color:#0e6ead;">UserInputDemo</span> {<br>
    <span style="padding-left:16px;display:block;"><span style="color:#ef5050;">public static void</span> <span style="color:#0e6ead;">main</span>(<span style="color:#ef5050;">String</span>[] <span style="color:#0e6ead;">args</span>) {</span>
    <span style="padding-left:32px;display:block;"><span style="color:#6b7280;">// 1. Create scanner attached to keyboard</span></span>
    <span style="padding-left:32px;display:block;"><span style="color:#ef5050;">Scanner</span> <span style="color:#0e6ead;">sc</span> = <span style="color:#ef5050;">new</span> <span style="color:#0e6ead;">Scanner</span>(<span style="color:#0e6ead;">System</span>.<span style="color:#0e6ead;">in</span>);</span>
    <br>
    <span style="padding-left:32px;display:block;"><span style="color:#0e6ead;">System</span>.<span style="color:#0e6ead;">out</span>.<span style="color:#2d7a00;">print</span>(<span style="color:#2d7a00;">"Enter your age: "</span>);</span>
    <span style="padding-left:32px;display:block;"><span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">age</span> = <span style="color:#0e6ead;">sc</span>.<span style="color:#2d7a00;">nextInt</span>();</span>
    <br>
    <span style="padding-left:32px;display:block;"><span style="color:#0e6ead;">System</span>.<span style="color:#0e6ead;">out</span>.<span style="color:#2d7a00;">println</span>(<span style="color:#2d7a00;">"You are "</span> + <span style="color:#0e6ead;">age</span> + <span style="color:#2d7a00;">" years old."</span>);</span>
    <br>
    <span style="padding-left:32px;display:block;"><span style="color:#6b7280;">// 2. Always close when done</span></span>
    <span style="padding-left:32px;display:block;"><span style="color:#0e6ead;">sc</span>.<span style="color:#2d7a00;">close</span>();</span>
    <span style="padding-left:16px;display:block;">}</span>
    }
  </div>

  <div v-click class="callout callout-info" style="margin-top:6px;">
    <div><strong>Prompting Tip:</strong> Use <span class="mono">System.out.print()</span> (without <span class="mono">ln</span>) so the user types their input right next to the prompt text on the same line.</div>
  </div>

</div>

</div>

  </template>
</Slide2>
