---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 9 — HELLO WORLD ANATOMY
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Getting Started with Java">
  <template #content>

<div class="slide-h1" style="margin-bottom:12px;">Anatomy of a <span class="highlight">Hello World</span></div>

<div class="g2" style="gap:14px;align-items:start;">

<div>
  <div class="slide-h3" style="color:#38a169;margin-bottom:6px;">Your First Java Program</div>

```java {all}
// Hello.java
public class Hello {

    public static void main(String[] args) {
        System.out.println("Hello, World!");
    }

}
```

  <div v-click class="output-box" style="margin-top:8px;">Hello, World!</div>

  <!-- <div v-click class="callout callout-info" style="margin-top:8px;">
    <div>Save as <span class="mono">Hello.java</span>, then run: <span class="mono" style="color:var(--green);">javac Hello.java</span> → <span class="mono" style="color:var(--green);">java Hello</span></div>
  </div> -->
</div>

<div class="flex-col">

  <div v-click class="section-label">Breaking It Down</div>

  <div style="display:flex;flex-direction:column;gap:8px;">
    <div v-click style="display:flex;gap:10px;align-items:flex-start;">
      <div style="background:var(--red-soft);border:2px dashed var(--red);border-radius:8px;padding:6px 12px;min-width:70px;text-align:center;">
        <div style="font-family:'Fira Code',monospace;font-weight:800;color:var(--red-dark);font-size:.75rem;">class</div>
      </div>
      <div class="small-text" style="padding-top:4px;">A blueprint for objects. <strong>Filename must match classname</strong> (Hello → Hello.java)</div>
    </div>
    <div v-click style="display:flex;gap:10px;align-items:flex-start;">
      <div style="background:#ebf8ff;border:2px dashed var(--blue);border-radius:8px;padding:6px 12px;min-width:70px;text-align:center;">
        <div style="font-family:'Fira Code',monospace;font-weight:800;color:var(--blue);font-size:.72rem;">main()</div>
      </div>
      <div class="small-text" style="padding-top:4px;">The <strong>entry point</strong> — JVM starts execution here. Must be <span class="mono">public static void</span>.</div>
    </div>
    <div v-click style="display:flex;gap:10px;align-items:flex-start;">
      <div style="background:#f0fff4;border:2px dashed var(--green);border-radius:8px;padding:6px 12px;min-width:70px;text-align:center;">
        <div style="font-family:'Fira Code',monospace;font-weight:800;color:var(--green);font-size:.65rem;">println</div>
      </div>
      <div class="small-text" style="padding-top:4px;"><span class="mono">System.out.println()</span> — Prints text + newline to the console output.</div>
    </div>
    <div v-click style="display:flex;gap:10px;align-items:flex-start;">
      <div style="background:#fffaf0;border:2px dashed var(--orange);border-radius:8px;padding:6px 12px;min-width:70px;text-align:center;">
        <div style="font-family:'Fira Code',monospace;font-weight:800;color:var(--orange);font-size:.65rem;">{ }</div>
      </div>
      <div class="small-text" style="padding-top:4px;">Curly braces define <strong>code blocks</strong>. Every class and method body is wrapped in <span class="mono">{ }</span>.</div>
    </div>

  </div>

  <div v-click class="callout callout-warn" style="margin-top:6px;">
    <div><strong>Semicolons matter!</strong> Every statement in Java <strong>must end with a semicolon</strong> <span class="mono">;</span> — missing one causes a compile error.</div>
  </div>

</div>

</div>

  </template>
</Slide2>
