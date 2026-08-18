---
transition: fade
---

<script setup>
const contents = [
  { text: '<b>Problem:</b> Declare a <code>double</code> variable for a student\'s percentage (e.g., <code>87.65</code>). Cast it to an <code>int</code> to get the whole number and print both values. Also parse the string <code>"2024"</code> into an <code>int</code> and print it.' },
  { text: '<b>Expected Output:</b><br><code>Percentage : 87.65</code><br><code>Truncated  : 87</code><br><code>Year       : 2024</code>' },
  { text: '<b>Note:</b> Use <code>(int) percentage</code> for casting. Use <code>Integer.parseInt("2024")</code> for parsing the string. Use <code>System.out.printf</code> or <code>println</code> to format the output.' }
]
</script>

<Slide
  topic="Type Casting in Java"
  sub-topic="Practice Problem"
  :contents="contents"
/>
