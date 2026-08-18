---
transition: slide-up
---

<script setup>
const contents = [
  { text: '<b>Problem:</b> Write a Java program that takes a person\'s <code>age</code> as input and checks if they are eligible to vote. (Rule: <code>age &gt;= 18</code> → "Eligible to Vote", otherwise → "Not Eligible to Vote").' },
  { text: '<b>Input:</b> <code>20</code>' },
  {
    text: '<b>Expected Output:</b><br><code>Eligible to Vote</code><br><br><b>More Test Cases:</b><br><code>18 &nbsp;→ Eligible to Vote</code><br><code>15 &nbsp;→ Not Eligible to Vote</code>'
  }
]
</script>

<Slide
  topic="Decision-making statements"
  sub-topic="Practice Problem"
  :contents="contents"
/>
