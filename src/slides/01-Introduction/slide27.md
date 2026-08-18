---
transition: fade
---

<script setup>
const contents = [
  { text: '<b>Problem:</b> Declare variables for a student — <code>name</code> (String), <code>rollNo</code> (int), <code>cgpa</code> (double), <code>isActive</code> (boolean). Print each variable and its type using formatted output.' },
  { text: '<b>Expected Output:</b><br><code>Alice &lt;String&gt;</code><br><code>101 &lt;int&gt;</code><br><code>9.20 &lt;double&gt;</code><br><code>true &lt;boolean&gt;</code>' },
  { text: '<b>Note:</b> Use <code>System.out.printf("%s &lt;String&gt;%n", name)</code> for the string. For CGPA use <code>%.2f</code> format specifier. There is no built-in <code>type()</code> in Java — just hardcode the type name in the format string.' }
]
</script>

<Slide
  topic="String Concatenation"
  sub-topic="Practice Problem"
  :contents="contents"
/>
