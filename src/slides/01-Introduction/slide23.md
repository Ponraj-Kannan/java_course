---
transition: fade
---

<script setup>
const contents = [
  { text: '<b>Problem:</b> Write a Java program that prints a simple welcome banner for a student. Display the student\'s name, roll number, and department — each on a separate line.' },
  {
    text: '<b>Expected Output:</b><br><code>===========================</code><br><code>Name       : [Your Name]</code><br><code>Roll No    : [Your Roll No]</code><br><code>Department : CSE</code><br><code>===========================</code>'
  },
  {
    text: '<b>Note:</b> Use multiple <code>System.out.println()</code> statements. Replace the placeholders with your own details. The dashes are just strings — print them as-is.'
  }
]
</script>

<Slide
  topic="Compiling & Running Java"
  sub-topic="Practice Problem"
  :contents="contents"
/>
