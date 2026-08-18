---
transition: slide-up
---

<script setup>
const contents = [
  { text: '<b>Problem:</b> Write a Java program that takes a <code>year</code> as input and checks if it is a <b>Leap Year</b> using nested <code>if-else</code> statements.' },
  { text: '<b>Leap Year Rules:</b><br>1. Year must be divisible by 4 (<code>year % 4 == 0</code>)<br>2. If divisible by 100, it must also be divisible by 400 (<code>year % 100 == 0 → check year % 400 == 0</code>)' },
  { text: '<b>Input:</b> <code>2024</code>' },
  {
    text: '<b>Expected Output:</b><br><code>2024 is a Leap Year.</code><br><br><b>More Test Cases:</b><br><code>1900 → 1900 is NOT a Leap Year.</code><br><code>2000 → 2000 is a Leap Year.</code>'
  }
]
</script>

<Slide
  topic="Decision-making statements"
  sub-topic="Practice Problem"
  :contents="contents"
/>
