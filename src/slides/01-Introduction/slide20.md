---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 20 — JAVAC & JAVA COMMANDS (CLI Workflow)
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Compiling & Running Java — CLI">
  <template #content>

<div class="slide-h1" style="margin-bottom:12px;">Compiling &amp; Running <span class="highlight">from Terminal</span></div>

<div class="g2" style="gap:16px;align-items:start;">

<div>
  <div class="slide-h3" style="margin-bottom:8px;color:#3182ce;">The Two-Command Workflow</div>

```bash {all}
# Step 1 — Compile (translates .java → .class)
javac Hello.java

# Step 2 — Run (executes the bytecode)
java Hello

# Note: no .class extension when running!
# Output:
# Hello, World!
```

  <div v-click class="callout callout-warn" style="margin-top:8px;">
    <div><strong>Common mistake:</strong> Running <span class="mono">java Hello.class</span> will cause an error — drop the <span class="mono">.class</span> extension!</div>
  </div>

  <div v-click class="callout callout-info" style="margin-top:6px;">
    <div>If there are errors in your code, <span class="mono">javac</span> will <strong>not</strong> create a .class file and will instead print error messages with line numbers.</div>
  </div>
</div>

<div class="flex-col">

  <div v-click class="section-label">Useful javac Flags</div>

  <div style="display:flex;flex-direction:column;gap:6px;">
    <div v-click style="background:#f6f8fa;border-radius:8px;border:1px solid #e1e4e8;padding:10px 14px;font-family:'Fira Code',monospace;font-size:.72rem;">
      <div style="color:#0e6ead;">javac -d out Hello.java</div>
      <div style="color:#6b7280;font-size:.65rem;margin-top:3px;">Outputs .class files into an "out" directory</div>
    </div>
    <div v-click style="background:#f6f8fa;border-radius:8px;border:1px solid #e1e4e8;padding:10px 14px;font-family:'Fira Code',monospace;font-size:.72rem;">
      <div style="color:#0e6ead;">javac -source 21 Hello.java</div>
      <div style="color:#6b7280;font-size:.65rem;margin-top:3px;">Target a specific Java language version</div>
    </div>
    <div v-click style="background:#f6f8fa;border-radius:8px;border:1px solid #e1e4e8;padding:10px 14px;font-family:'Fira Code',monospace;font-size:.72rem;">
      <div style="color:#0e6ead;">java -cp out Hello</div>
      <div style="color:#6b7280;font-size:.65rem;margin-top:3px;">Run with a custom classpath (where .class files live)</div>
    </div>
    <div v-click style="background:#f6f8fa;border-radius:8px;border:1px solid #e1e4e8;padding:10px 14px;font-family:'Fira Code',monospace;font-size:.72rem;">
      <div style="color:#0e6ead;">java Hello Alice Bob</div>
      <div style="color:#6b7280;font-size:.65rem;margin-top:3px;">Pass command-line args → available in String[] args</div>
    </div>

  </div>

  <div v-click class="callout callout-success" style="margin-top:8px;">
    <div><strong>Quick check:</strong> <span class="mono">java --version</span> tells you which JVM is active. <span class="mono">javac --version</span> confirms your compiler.</div>
  </div>

</div>

</div>

  </template>
</Slide2>
