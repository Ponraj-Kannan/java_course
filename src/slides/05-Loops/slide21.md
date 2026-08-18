---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 21 — COMMON BEGINNER MISTAKES IN JAVA LOOPS
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Beginner Mistakes">
  <template #content>

<div class="slide-h1" style="margin-bottom:10px;">Common Beginner <span class="highlight">Loop Pitfalls</span></div>

<div class="g2" style="gap:14px;align-items:start;">

<div class="flex-col">

  <div v-click class="card card-red" style="margin-bottom:8px;">
    <div class="slide-h3" style="color:var(--red-dark);margin-bottom:4px;">1. The Semicolon Trap</div>
    <div style="font-family:'Fira Code',monospace;font-size:.7rem;color:#6b7280;background:#fff;padding:6px;border-radius:6px;border:1px solid #feb2b2;">
      <span style="color:#ef5050;">while</span> (i &lt; <span style="color:#b45309;">5</span>)<span style="color:#ef5050;font-weight:700;">;</span> { <span style="color:#6b7280;">// Empty loop!</span><br>
      &nbsp;&nbsp;i++;<br>
      }
    </div>
    <div class="small-text" style="margin-top:4px;">Placing <code>;</code> right after <code>while()</code> makes the loop repeat an empty statement infinitely!</div>
  </div>

  <div v-click class="card card-orange">
    <div class="slide-h3" style="color:var(--orange);margin-bottom:4px;">2. Off-By-One Error (OBOE)</div>
    <div style="font-family:'Fira Code',monospace;font-size:.7rem;color:#6b7280;background:#fff;padding:6px;border-radius:6px;border:1px solid #fbd38d;">
      <span style="color:#ef5050;">for</span> (<span style="color:#0e6ead;">int</span> i = <span style="color:#b45309;">0</span>; i <span style="color:#ef5050;font-weight:700;">&lt;=</span> arr.length; i++) { ... }
    </div>
    <div class="small-text" style="margin-top:4px;">Causes <code>ArrayIndexOutOfBoundsException</code>! Arrays are 0-indexed; last index is <code>arr.length - 1</code>. Use <code>i &lt; arr.length</code>.</div>
  </div>

</div>

<div class="flex-col">

  <div v-click class="card card-navy" style="margin-bottom:8px;">
    <div class="slide-h3" style="color:var(--navy);margin-bottom:4px;">3. Counter Variable Scope</div>
    <div style="font-family:'Fira Code',monospace;font-size:.7rem;color:#6b7280;background:#fff;padding:6px;border-radius:6px;border:1px solid #cbd5e0;">
      <span style="color:#ef5050;">for</span> (<span style="color:#0e6ead;">int</span> i = <span style="color:#b45309;">0</span>; i &lt; <span style="color:#b45309;">5</span>; i++) { ... }<br>
      System.out.println(i); <span style="color:#ef5050;">// Compiler Error!</span>
    </div>
    <div class="small-text" style="margin-top:4px;">Variable <code>i</code> declared inside <code>for(...)</code> header doesn't exist outside the loop.</div>
  </div>

  <div v-click class="card card-green">
    <div class="slide-h3" style="color:var(--green);margin-bottom:4px;">4. Forgetting Update in While Loops</div>
    <div style="font-family:'Fira Code',monospace;font-size:.7rem;color:#6b7280;background:#fff;padding:6px;border-radius:6px;border:1px solid #9ae6b4;">
      <span style="color:#ef5050;">while</span> (i &lt; <span style="color:#b45309;">5</span>) {<br>
      &nbsp;&nbsp;System.out.println(i);<br>
      &nbsp;&nbsp;<span style="color:#ef5050;">// missing i++ !!</span><br>
      }
    </div>
    <div class="small-text" style="margin-top:4px;">Without updating state, <code>i &lt; 5</code> remains true forever.</div>
  </div>

</div>

</div>

  </template>
</Slide2>
