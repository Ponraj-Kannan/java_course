---
transition: fade
---

<script setup>
const contents = [
  { text: '<b>Problem:</b> Declare variables for a student profile: <code>name</code> (String), <code>age</code> (int), <code>gpa</code> (double), <code>isEnrolled</code> (boolean), and <code>grade</code> (char). Print each variable on a separate line.' },
  { text: '<b>Expected Output:</b><br><code>Alice</code><br><code>20</code><br><code>9.2</code><br><code>true</code><br><code>A</code>' },
  { text: '<b>Note:</b> Declare each variable with the correct type. Use <code>System.out.println()</code> for each. Notice that <code>char</code> uses single quotes <code>\'A\'</code> but <code>String</code> uses double quotes <code>"Alice"</code>.' }
]
</script>

<Slide
  topic="Java Data Types"
  sub-topic="Practice Problem"
  :contents="contents"
/>
