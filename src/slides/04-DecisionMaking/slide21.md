---
transition: slide-up
---

<script setup>
const contents = [
  { text: '<b>Problem:</b> Write a Java program using a <code>switch</code> statement that takes an integer <code>day</code> (1 to 7) as input and prints whether it is a <b>"Weekday"</b> (1-5) or a <b>"Weekend"</b> (6-7). Handle invalid inputs with a <code>default</code> block.' },
  { text: '<b>Input:</b> <code>6</code>' },
  {
    text: '<b>Expected Output:</b><br><code>Weekend</code><br><br><b>More Test Cases:</b><br><code>3 → Weekday</code><br><code>9 → Invalid day number!</code>'
  }
]
</script>

<Slide
  topic="Decision-making statements"
  sub-topic="Practice Problem"
  :contents="contents"
/>
