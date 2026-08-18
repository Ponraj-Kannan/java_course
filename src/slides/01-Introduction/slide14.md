---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 14 — COMMENTS IN JAVA
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Java Comments">
  <template #content>

<div class="slide-h1" style="margin-bottom:12px;"><span class="highlight">Comments</span></div>

<div class="body-text" style="margin-bottom:12px;">Comments are notes for humans — Java completely ignores them during compilation and execution.</div>

<div class="g2" style="gap:14px;align-items:start;">

<div>
  <div class="slide-h3" style="margin-bottom:6px;">Single-line Comment <span class="mono" style="color:#ef5050;">//</span></div>

```java {1,2,4|all}
// This is a single-line comment
// Use // for any short explanation

int age = 20;   // inline comment too!
String name = "Alice";  // student name
```

  <div v-click class="callout callout-info" style="margin-top:8px;">
    <div>Use <span class="mono">//</span> for quick notes on a single line.</div>
  </div>
</div>

<div>
  <div class="slide-h3" style="margin-bottom:6px;">Multi-line Comment <span class="mono" style="color:#ef5050;">/* ... */</span></div>

```java {1,2,3,4,5|all}
/*
 * This is a multi-line comment.
 * It can span several lines.
 * Often used for longer explanations.
 */

/** Javadoc comment — generates API docs */
public class Hello { }
```

  <div v-click class="callout callout-warn" style="margin-top:8px;">
    <div><span class="mono">/** ... */</span> is a <strong>Javadoc comment</strong> — used to auto-generate HTML documentation with <span class="mono">javadoc</span>.</div>
  </div>
</div>

</div>

<div v-click class="callout callout-success" style="margin-top:10px;">
  <div><strong>Best practice:</strong> Write comments that explain <em>WHY</em> you wrote the code, not just <em>WHAT</em> it does. Good code is self-explanatory!</div>
</div>

  </template>
</Slide2>
