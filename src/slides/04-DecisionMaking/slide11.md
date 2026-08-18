---
transition: slide-up
---

<script setup>
const contents = [
  { text: '<b>Problem:</b> Write a Java program that takes an integer <code>N</code> as input and classifies it as <b>Positive</b>, <b>Negative</b>, or <b>Zero</b> using an <code>if-else-if</code> ladder.' },
  { text: '<b>Input:</b> <code>-8</code>' },
  {
    text: '<b>Expected Output:</b><br><code>-8 is a Negative number.</code><br><br><b>More Test Cases:</b><br><code>15 &nbsp;→ 15 is a Positive number.</code><br><code>0 &nbsp;&nbsp;→ The number is Zero.</code>'
  }
]
</script>

<Slide
  topic="Decision-making statements"
  sub-topic="Practice Problem"
  :contents="contents"
/>
