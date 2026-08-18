---
transition: fade
---

<script setup>
const contents = [
  { text: '<b>Problem:</b> Write a Java program using an <b>enhanced switch expression</b> that takes a <code>month</code> String as input (e.g. "December", "March") and returns the corresponding <b>Season</b>.' },
  { text: '<b>Season Mapping:</b><br>• "December", "January", "February" → <code>"Winter"</code><br>• "March", "April", "May" → <code>"Spring"</code><br>• "June", "July", "August" → <code>"Summer"</code><br>• "September", "October", "November" → <code>"Autumn"</code>' },
  { text: '<b>Input:</b> <code>"July"</code>' },
  {
    text: '<b>Expected Output:</b><br><code>Summer</code><br><br><b>More Test Cases:</b><br><code>"January" → Winter</code><br><code>"Unknown" → Invalid Month</code>'
  }
]
</script>

<Slide
  topic="Enhanced Switch"
  sub-topic="Practice Problem"
  :contents="contents"
/>
