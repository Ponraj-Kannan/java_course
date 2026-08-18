---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 24 — ESCAPE SEQUENCES & STRING LITERALS
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Escape Sequences in Java">
  <template #content>

<div class="slide-h1" style="margin-bottom:12px;"><span class="highlight">Escape Sequences</span></div>

<div class="g2" style="gap:14px;align-items:start;">

<div>
  <div class="slide-h3" style="margin-bottom:8px;color:#3182ce;">Common Escape Sequences</div>

<table class="cmp-table">
  <thead>
    <tr>
      <th>Sequence</th>
      <th>Meaning</th>
      <th>Example Output</th>
    </tr>
  </thead>
  <tbody>
    <tr v-click>
      <td><span class="mono">\n</span></td>
      <td>New line</td>
      <td><span class="small-text">Moves to next line</span></td>
    </tr>
    <tr v-click>
      <td><span class="mono">\t</span></td>
      <td>Tab</td>
      <td><span class="small-text">Horizontal tab space</span></td>
    </tr>
    <tr v-click>
      <td><span class="mono">\\</span></td>
      <td>Backslash</td>
      <td><span class="mono">\</span></td>
    </tr>
    <tr v-click>
      <td><span class="mono">\"</span></td>
      <td>Double quote</td>
      <td><span class="mono">"</span></td>
    </tr>
    <tr v-click>
      <td><span class="mono">\'</span></td>
      <td>Single quote</td>
      <td><span class="mono">'</span></td>
    </tr>
    <tr v-click>
      <td><span class="mono">\r</span></td>
      <td>Carriage return</td>
      <td><span class="small-text">Returns to line start</span></td>
    </tr>
  </tbody>
</table>
</div>

<div>
  <div class="slide-h3" style="margin-bottom:8px;color:#38a169;">Examples in Action</div>

```java {all}
// Tab and newline
System.out.println("Name:\tAlice");
System.out.println("Age:\t20");

// Quote inside a string
System.out.println("He said \"Hello!\"");

// Backslash in file paths
System.out.println("C:\\Users\\Alice\\file.txt");

// Multiple lines in one println
System.out.println("Line 1\nLine 2\nLine 3");
```

  <div v-click class="output-box" style="margin-top:8px;">
    Name:&nbsp;&nbsp;&nbsp;&nbsp;Alice<br>
    Age:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;20<br>
    He said "Hello!"<br>
    C:\Users\Alice\file.txt<br>
    Line 1<br>Line 2<br>Line 3
  </div>
</div>

</div>

  </template>
</Slide2>
