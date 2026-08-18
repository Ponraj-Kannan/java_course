---
transition: slide-up
---

<script setup>
const contents = [
  { text: '<b>Problem:</b> Write a Java program that takes two integer numbers <code>num1</code> and <code>num2</code> as input and uses the <b>ternary operator (?:)</b> to find and print the minimum value between them.' },
  { text: '<b>Input:</b> <code>num1 = 45, num2 = 18</code>' },
  {
    text: '<b>Expected Output:</b><br><code>Minimum value is: 18</code><br><br><b>More Test Cases:</b><br><code>num1 = 7, num2 = 12 → Minimum value is: 7</code><br><code>num1 = 15, num2 = 15 → Minimum value is: 15</code>'
  }
]
</script>

<Slide
  topic="Decision-making statements"
  sub-topic="Practice Problem"
  :contents="contents"
/>
