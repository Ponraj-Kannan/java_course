---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 20 — REAL-WORLD JAVA EXAMPLES
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Data Types">
  <template #content>

<div class="slide-h1" style="margin-bottom:10px;">Real-World Java <span class="highlight">Examples</span></div>

<div class="g2" style="gap:14px;">

<div class="flex-col">

  <div v-click class="section-label">Example 1 — String to Integer Parsing</div>
  <div v-after style="background:#f6f8fa;border-radius:10px;border:1px solid #e1e4e8;padding:10px 14px;font-family:'Fira Code',monospace;font-size:.7rem;line-height:1.8;">
    <span style="color:#0e6ead;">String</span> <span style="color:#0e6ead;">input</span> = <span style="color:#2d7a00;">"25"</span>;<br>
    <span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">age</span> = <span style="color:#0e6ead;">Integer</span>.<span style="color:#2d7a00;">parseInt</span>(<span style="color:#0e6ead;">input</span>);<br>
    <span style="color:#0e6ead;">System</span>.<span style="color:#0e6ead;">out</span>.<span style="color:#2d7a00;">println</span>(<span style="color:#2d7a00;">"Next year age: "</span> + (<span style="color:#0e6ead;">age</span> + <span style="color:#b45309;">1</span>)); <span style="color:#6b7280;">// 26</span>
  </div>

  <div v-click class="section-label" style="margin-top:4px;">Example 2 — Large Number Readability</div>
  <div v-after style="background:#f6f8fa;border-radius:10px;border:1px solid #e1e4e8;padding:10px 14px;font-family:'Fira Code',monospace;font-size:.7rem;line-height:1.8;">
    <span style="color:#ef5050;">long</span> <span style="color:#0e6ead;">worldPop</span> = <span style="color:#b45309;">8_000_000_000L</span>;<br>
    <span style="color:#ef5050;">double</span> <span style="color:#0e6ead;">distanceToSun</span> = <span style="color:#b45309;">149_600_000.0</span>; <span style="color:#6b7280;">// km</span><br>
    <span style="color:#0e6ead;">System</span>.<span style="color:#0e6ead;">out</span>.<span style="color:#2d7a00;">println</span>(<span style="color:#0e6ead;">worldPop</span>); <span style="color:#6b7280;">// 8000000000</span>
  </div>

  <div v-click class="section-label" style="margin-top:4px;">Example 3 — Temperature Conversion</div>
  <div v-after style="background:#f6f8fa;border-radius:10px;border:1px solid #e1e4e8;padding:10px 14px;font-family:'Fira Code',monospace;font-size:.7rem;line-height:1.8;">
    <span style="color:#ef5050;">double</span> <span style="color:#0e6ead;">celsius</span> = <span style="color:#b45309;">37.5</span>;<br>
    <span style="color:#ef5050;">double</span> <span style="color:#0e6ead;">fahrenheit</span> = (<span style="color:#0e6ead;">celsius</span> * <span style="color:#b45309;">9.0</span> / <span style="color:#b45309;">5.0</span>) + <span style="color:#b45309;">32.0</span>;<br>
    <span style="color:#0e6ead;">System</span>.<span style="color:#0e6ead;">out</span>.<span style="color:#2d7a00;">println</span>(<span style="color:#2d7a00;">"Fahrenheit: "</span> + <span style="color:#0e6ead;">fahrenheit</span>); <span style="color:#6b7280;">// 99.5</span>
  </div>

</div>

<div class="flex-col">

  <div v-click class="section-label">Example 4 — Unicode Symbol Printing</div>
  <div v-after style="background:#f6f8fa;border-radius:10px;border:1px solid #e1e4e8;padding:10px 14px;font-family:'Fira Code',monospace;font-size:.7rem;line-height:1.8;">
    <span style="color:#ef5050;">char</span> <span style="color:#0e6ead;">rupeeSymbol</span> = <span style="color:#2d7a00;">'\u20B9'</span>;<br>
    <span style="color:#ef5050;">double</span> <span style="color:#0e6ead;">price</span> = <span style="color:#b45309;">499.99</span>;<br>
    <span style="color:#0e6ead;">System</span>.<span style="color:#0e6ead;">out</span>.<span style="color:#2d7a00;">println</span>(<span style="color:#0e6ead;">rupeeSymbol</span> + <span style="color:#2d7a00;">""</span> + <span style="color:#0e6ead;">price</span>); <span style="color:#6b7280;">// ₹499.99</span>
  </div>

  <div v-click class="section-label" style="margin-top:4px;">Example 5 — Clean Code with var</div>
  <div v-after style="background:#f6f8fa;border-radius:10px;border:1px solid #e1e4e8;padding:10px 14px;font-family:'Fira Code',monospace;font-size:.7rem;line-height:1.8;">
    <span style="color:#ef5050;">var</span> <span style="color:#0e6ead;">scores</span> = <span style="color:#ef5050;">new</span> <span style="color:#ef5050;">int</span>[]{ <span style="color:#b45309;">95</span>, <span style="color:#b45309;">88</span>, <span style="color:#b45309;">92</span> };<br>
    <span style="color:#ef5050;">var</span> <span style="color:#0e6ead;">title</span> = <span style="color:#2d7a00;">"Java Data Types"</span>;<br>
    <span style="color:#0e6ead;">System</span>.<span style="color:#0e6ead;">out</span>.<span style="color:#2d7a00;">println</span>(<span style="color:#0e6ead;">title</span> + <span style="color:#2d7a00;">" count: "</span> + <span style="color:#0e6ead;">scores</span>.<span style="color:#0e6ead;">length</span>);
  </div>

  <div v-click class="callout callout-success" style="margin-top:4px;">
    <div>Selecting the proper data type optimizes memory usage, improves readability, and avoids runtime crashes!</div>
  </div>

</div>

</div>

  </template>
</Slide2>
