---
transition: slide-up
---

<script setup>
const contents = [
  { text: '<b>Problem:</b> Write a Java program that takes an integer <code>num</code> as input and checks if it is a <b>Positive Number</b> using an <code>if</code> statement.' },
  { text: '<b>Input:</b> <code>12</code>' },
  {
    text: '<b>Expected Output:</b><br><code>12 is a positive number.</code><br><br><b>More Test Cases:</b><br><code>25 &nbsp;→ 25 is a positive number.</code><br><code>-5 &nbsp;→ (No output printed from if block)</code>'
  }
]
</script>

<Slide
  topic="Decision-making statements"
  sub-topic="Practice Problem"
  :contents="contents"
/>
