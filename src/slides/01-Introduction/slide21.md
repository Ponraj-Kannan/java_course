---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 21 — COMMON JAVA ERRORS (Beginner Traps)
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Common Java Errors">
  <template #content>

<div class="slide-h1" style="margin-bottom:10px;"><span class="highlight">Common Errors</span> &amp; How to Fix Them</div>

<div class="g2" style="gap:14px;align-items:start;">

<div class="flex-col">

  <div v-click style="background:#fff;border:1px solid var(--border);border-radius:10px;padding:14px;">
    <div class="slide-h3" style="color:#c73c3c;margin-bottom:6px;">❌ Missing Semicolon</div>

```java
// Error! Missing ;
System.out.println("Hello")  // ← crash!
```

  <div class="card card-red" style="margin-top:6px;">
    error: ';' expected<br>
    System.out.println("Hello")
  </div>
  </div>

  <div v-click style="background:#fff;border:1px solid var(--border);border-radius:10px;padding:14px;margin-top:8px;">
    <div class="slide-h3" style="color:#c73c3c;margin-bottom:6px;">❌ Wrong Class Name</div>

```java
// File is saved as "hello.java" (lowercase h)
// but class is named "Hello"
public class Hello { }  // ← mismatch!
```

  <div class="card card-red" style="margin-top:6px;">
    error: class Hello is public, should be declared in a file named Hello.java
  </div>
  </div>

</div>

<div class="flex-col">

  <div v-click style="background:#fff;border:1px solid var(--border);border-radius:10px;padding:14px;">
    <div class="slide-h3" style="color:#38a169;margin-bottom:6px;">✅ Fixed: Semicolon</div>

```java {all}
// Correct — semicolon at end!
System.out.println("Hello");
```

  <div class="card card-green" style="margin-top:6px;">
    Hello
  </div>
  </div>

  <div v-click class="callout callout-warn" style="margin-top:8px;">
    <div><strong>Missing braces</strong> are also common — every <span class="mono">{</span> must have a matching <span class="mono">}</span>. Your IDE can highlight mismatches.</div>
  </div>

  <div v-click class="card card-blue" style="margin-top:8px;">
    <div class="slide-h3" style="margin-bottom:4px;">Reading Error Messages</div>
    <div class="small-text">Java error messages always include a <strong>file name</strong>, <strong>line number</strong>, and a <strong>description</strong>. Always read the <em>first</em> error — fixing it often resolves subsequent ones.</div>
  </div>

  <div v-click class="callout callout-success" style="margin-top:6px;">
    <div><strong>Pro tip:</strong> Compile often! Fix errors one at a time, starting from the top of the error list.</div>
  </div>

</div>

</div>

  </template>
</Slide2>
