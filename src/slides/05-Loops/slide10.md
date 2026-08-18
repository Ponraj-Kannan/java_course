---
transition: slide-up
---

<script setup>
const contents = [
  { text: '<b>Problem:</b> Write a Java program using a <code>do-while</code> loop to keep asking the user to enter a positive integer until a valid number (greater than 0) is entered.' },
  { text: '<b>Input Simulation:</b><br><code>-5<br>0<br>12</code>' },
  {
    text: '<b>Expected Output:</b><br><code>Invalid! Enter positive number: -5</code><br><code>Invalid! Enter positive number: 0</code><br><code>Valid number accepted: 12</code>'
  }
]
</script>

<Slide
  topic="Do-While Loop"
  sub-topic="Practice Problem"
  :contents="contents"
/>
