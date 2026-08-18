---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 6 — PRIMITIVE TYPES: char & boolean
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Data Types">
  <template #content>

<div class="slide-h1" style="margin-bottom:10px;">Character &amp; Logical — <span class="highlight">char &amp; boolean</span></div>

<div class="g2" style="gap:14px;">

<div class="flex-col">

  <div v-click class="card-navy" style="border-radius:10px;">
    <div style="font-size:.78rem;line-height:1.5;color:var(--slate);">
      <strong style="color:var(--red);">1. char Definition:</strong> A 2-byte (16-bit) unsigned integer type that stores a single <strong>16-bit Unicode character</strong> enclosed in single quotes (e.g. <span class="mono">'A'</span>), ranging from <span class="mono">0</span> to <span class="mono">65,535</span> (<span class="mono">'\u0000'</span> to <span class="mono">'\uffff'</span>).
    </div>
  </div>

  <div v-click class="card-navy" style="border-radius:10px;margin-top:4px;">
    <div style="font-size:.78rem;line-height:1.5;color:var(--slate);">
      <strong style="color:var(--red);">2. boolean Definition:</strong> A 1-bit logical data type that holds only one of two state values: <span class="mono" style="color:var(--green);">true</span> or <span class="mono" style="color:var(--red-dark);">false</span> (default: <span class="mono">false</span>).
    </div>
  </div>

  <div v-click class="section-label" style="margin-top:4px;">Code Examples</div>
  <div v-after style="background:#f6f8fa;border-radius:10px;border:1px solid #e1e4e8;padding:10px 14px;font-family:'Fira Code',monospace;font-size:.72rem;line-height:1.9;">
    <span style="color:#6b7280;">// char: single quotes only</span><br>
    <span style="color:#ef5050;">char</span> <span style="color:#0e6ead;">grade</span> = <span style="color:#2d7a00;">'A'</span>;<br>
    <span style="color:#ef5050;">char</span> <span style="color:#0e6ead;">symbol</span> = <span style="color:#2d7a00;">'\u20B9'</span>; <span style="color:#6b7280;">// ₹ (Rupee Unicode)</span><br>
    <span style="color:#ef5050;">int</span> <span style="color:#0e6ead;">asciiVal</span> = <span style="color:#2d7a00;">'A'</span>;   <span style="color:#6b7280;">// 65 (Implicit ASCII cast)</span><br><br>
    <span style="color:#6b7280;">// boolean: logical state flag</span><br>
    <span style="color:#ef5050;">boolean</span> <span style="color:#0e6ead;">isPassed</span> = <span style="color:#ef5050;">true</span>;<br>
    <span style="color:#ef5050;">boolean</span> <span style="color:#0e6ead;">isOver18</span> = (<span style="color:#0e6ead;">age</span> &gt;= <span style="color:#b45309;">18</span>);
  </div>

</div>

<div class="flex-col">

  <div v-click class="card-purple" style="border-radius:10px;padding:10px 14px;">
    <div style="font-size:.78rem;font-weight:700;color:var(--purple);margin-bottom:2px;">Unicode Support in Java</div>
    <div style="font-size:.7rem;color:var(--slate);">
      Unlike C/C++ which use 8-bit ASCII, Java <span class="mono">char</span> is <strong>16-bit Unicode</strong>! It supports English, Hindi (Devanagari), Tamil, Chinese, Japanese, and special math/currency symbols.
    </div>
  </div>

  <div v-click class="mem-box" style="margin-top:6px;">
    <div class="mem-header">char vs boolean Specification</div>
    <div class="mem-row">
      <div class="mem-name">char</div>
      <div class="mem-val">2 bytes (16-bit Unicode)</div>
      <div class="mem-type">Default: '\u0000'</div>
    </div>
    <div class="mem-row">
      <div class="mem-name">boolean</div>
      <div class="mem-val">1 bit (logical)</div>
      <div class="mem-type">Default: false</div>
    </div>
  </div>

  <div v-click class="callout callout-warn" style="margin-top:6px;">
    <div><strong>Boolean Rule:</strong> In Java, <span class="mono">boolean</span> values cannot be converted to integers (no <span class="mono">0</span> or <span class="mono">1</span> interchanging like C++ or Python)!</div>
  </div>

</div>

</div>

  </template>
</Slide2>
