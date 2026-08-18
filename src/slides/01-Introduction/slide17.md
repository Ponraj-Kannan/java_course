---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 17 — PRINT VARIATIONS IN JAVA
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Java Output — print vs println vs printf">
  <template #content>

<div class="slide-h1" style="margin-bottom:12px;">Output <span class="highlight">Methods</span></div>

<div class="g2" style="gap:14px;align-items:start;">

<div>
  <div class="slide-h3" style="margin-bottom:8px;color:#3182ce;">Three Ways to Print</div>

```java {all}
// println — prints and moves to next line
System.out.println("Hello, World!");
System.out.println("Line 2");

// print — no newline at end
System.out.print("Hello ");
System.out.print("World");  // same line!

// printf — formatted output (like C)
System.out.printf("Name: %s, Age: %d%n", "Alice", 20);
```

  <div v-click class="output-box" style="margin-top:8px;">
    Hello, World!<br>
    Line 2<br>
    Hello World<br>
    Name: Alice, Age: 20
  </div>
</div>

<div class="flex-col">

  <div v-click class="section-label">When to Use Each</div>

  <div style="display:flex;flex-direction:column;gap:8px;">
    <div v-click style="background:#ebf8ff;border:1px solid var(--blue);border-radius:8px;padding:10px 14px;">
      <span class="pill pill-blue" style="margin-left:-13px">println</span>
      <div class="small-text">Use when each output is on its own line — most common choice.</div>
    </div>
    <div v-click style="background:var(--red-soft);border:1px solid var(--red);border-radius:8px;padding:10px 14px;">
      <span class="pill pill-red" style="margin-left:-13px">print</span>
      <div class="small-text">Use when building output across multiple calls without line breaks.</div>
    </div>
    <div v-click style="background:#faf5ff;border:1px solid var(--purple);border-radius:8px;padding:10px 14px;">
      <span class="pill pill-purple" style="margin-left:-13px">printf</span>
      <div class="small-text">Use for precise formatting — numbers, padding, decimal places. Supports <span class="mono">%s %d %f %.2f %n</span>.</div>
    </div>

  </div>

  <div v-click class="callout callout-info" style="margin-top:8px;">
    <div><strong>Tip:</strong> <span class="mono">%n</span> in printf is the platform-safe newline. Prefer it over <span class="mono">\n</span> for portability.</div>
  </div>

</div>

</div>

  </template>
</Slide2>
