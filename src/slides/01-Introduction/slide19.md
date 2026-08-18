---
transition: fade
---

<script setup>
const contents = [
  { text: '<b>Problem:</b> Write a Java program that uses all three output methods — <code>print</code>, <code>println</code>, and <code>printf</code> — to display your personal details.' },
  {
    text: '<b>Expected Output:</b><br><code>Name: [Your Name]</code><br><code>Age: [Your Age]</code><br><code>GPA: X.XX</code>'
  },
  {
    text: '<b>Note:</b> Use <code>println</code> for name, <code>print</code> for "Age: " then <code>println</code> for the value, and <code>printf("GPA: %.2f%n", gpa)</code> for the GPA formatted to 2 decimal places.'
  }
]
</script>

<Slide
  topic="Java Output Methods"
  sub-topic="Practice Problem"
  :contents="contents"
/>
