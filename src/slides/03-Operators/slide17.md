---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 17 — REAL-WORLD JAVA EXAMPLES
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Operators">
  <template #content>

<div class="slide-h1" style="margin-bottom:10px;">Real-World Java <span class="highlight">Examples</span></div>

<div class="g2" style="gap:14px;">

<div class="flex-col">

  <div v-click class="section-label">Example 1 — Simple Interest Calculator</div>
  <div v-after style="background:#f6f8fa;border-radius:10px;border:1px solid #e1e4e8;padding:10px 14px;font-family:'Fira Code',monospace;font-size:.7rem;line-height:1.8;">
    <span style="color:#ef5050;">double</span> <span style="color:#0e6ead;">principal</span> = <span style="color:#b45309;">10000</span>, <span style="color:#0e6ead;">rate</span> = <span style="color:#b45309;">8.5</span>, <span style="color:#0e6ead;">time</span> = <span style="color:#b45309;">3</span>;<br>
    <span style="color:#ef5050;">double</span> <span style="color:#0e6ead;">si</span> = (<span style="color:#0e6ead;">principal</span> * <span style="color:#0e6ead;">rate</span> * <span style="color:#0e6ead;">time</span>) / <span style="color:#b45309;">100.0</span>;<br>
    <span style="color:#0e6ead;">System</span>.<span style="color:#0e6ead;">out</span>.<span style="color:#2d7a00;">println</span>(<span style="color:#2d7a00;">"Interest: ₹"</span> + <span style="color:#0e6ead;">si</span>); <span style="color:#6b7280;">// ₹2550.0</span>
  </div>

  <div v-click class="section-label" style="margin-top:4px;">Example 2 — Even or Odd Checker</div>
  <div v-after style="background:#f6f8fa;border-radius:10px;border:1px solid #e1e4e8;padding:10px 14px;font-family:'Fira Code',monospace;font-size:.7rem;line-height:1.8;">
    <span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">num</span> = <span style="color:#b45309;">27</span>;<br>
    <span style="color:#ef5050;">boolean</span> <span style="color:#0e6ead;">isEven</span> = (<span style="color:#0e6ead;">num</span> % <span style="color:#b45309;">2</span> == <span style="color:#b45309;">0</span>);<br>
    <span style="color:#0e6ead;">System</span>.<span style="color:#0e6ead;">out</span>.<span style="color:#2d7a00;">println</span>(<span style="color:#0e6ead;">num</span> + <span style="color:#2d7a00;">" is even? "</span> + <span style="color:#0e6ead;">isEven</span>); <span style="color:#6b7280;">// false</span>
  </div>

  <div v-click class="section-label" style="margin-top:4px;">Example 3 — BMI Calculator</div>
  <div v-after style="background:#f6f8fa;border-radius:10px;border:1px solid #e1e4e8;padding:10px 14px;font-family:'Fira Code',monospace;font-size:.7rem;line-height:1.8;">
    <span style="color:#ef5050;">double</span> <span style="color:#0e6ead;">weight</span> = <span style="color:#b45309;">70.0</span>, <span style="color:#0e6ead;">height</span> = <span style="color:#b45309;">1.75</span>;<br>
    <span style="color:#ef5050;">double</span> <span style="color:#0e6ead;">bmi</span> = <span style="color:#0e6ead;">weight</span> / <span style="color:#0e6ead;">Math</span>.<span style="color:#0e6ead;">pow</span>(<span style="color:#0e6ead;">height</span>, <span style="color:#b45309;">2</span>);<br>
    <span style="color:#0e6ead;">System</span>.<span style="color:#0e6ead;">out</span>.<span style="color:#2d7a00;">println</span>(<span style="color:#2d7a00;">"BMI: "</span> + <span style="color:#0e6ead;">bmi</span>); <span style="color:#6b7280;">// 22.857...</span>
  </div>

</div>

<div class="flex-col">

  <div v-click class="section-label">Example 4 — Login Validator</div>
  <div v-after style="background:#f6f8fa;border-radius:10px;border:1px solid #e1e4e8;padding:10px 14px;font-family:'Fira Code',monospace;font-size:.7rem;line-height:1.8;">
    <span style="color:#0e6ead;">String</span> <span style="color:#0e6ead;">user</span> = <span style="color:#2d7a00;">"admin"</span>, <span style="color:#0e6ead;">pass</span> = <span style="color:#2d7a00;">"pass123"</span>;<br>
    <span style="color:#ef5050;">boolean</span> <span style="color:#0e6ead;">isValid</span> = <span style="color:#0e6ead;">user</span>.<span style="color:#2d7a00;">equals</span>(<span style="color:#2d7a00;">"admin"</span>) &amp;&amp; <span style="color:#0e6ead;">pass</span>.<span style="color:#2d7a00;">equals</span>(<span style="color:#2d7a00;">"pass123"</span>);<br>
    <span style="color:#0e6ead;">System</span>.<span style="color:#0e6ead;">out</span>.<span style="color:#2d7a00;">println</span>(<span style="color:#2d7a00;">"Access: "</span> + <span style="color:#0e6ead;">isValid</span>); <span style="color:#6b7280;">// true</span>
  </div>

  <div v-click class="section-label" style="margin-top:4px;">Example 5 — Leap Year Logic</div>
  <div v-after style="background:#f6f8fa;border-radius:10px;border:1px solid #e1e4e8;padding:10px 14px;font-family:'Fira Code',monospace;font-size:.7rem;line-height:1.8;">
    <span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">year</span> = <span style="color:#b45309;">2024</span>;<br>
    <span style="color:#ef5050;">boolean</span> <span style="color:#0e6ead;">isLeap</span> = (<span style="color:#0e6ead;">year</span> % <span style="color:#b45309;">4</span> == <span style="color:#b45309;">0</span> &amp;&amp; <span style="color:#0e6ead;">year</span> % <span style="color:#b45309;">100</span> != <span style="color:#b45309;">0</span>) || (<span style="color:#0e6ead;">year</span> % <span style="color:#b45309;">400</span> == <span style="color:#b45309;">0</span>);<br>
    <span style="color:#0e6ead;">System</span>.<span style="color:#0e6ead;">out</span>.<span style="color:#2d7a00;">println</span>(<span style="color:#2d7a00;">"Leap year? "</span> + <span style="color:#0e6ead;">isLeap</span>); <span style="color:#6b7280;">// true</span>
  </div>

  <div v-click class="callout callout-success" style="margin-top:4px;">
    <div>Operators form the backbone of practical Java software — from financial calculations to authorization security!</div>
  </div>

</div>

</div>

  </template>
</Slide2>
