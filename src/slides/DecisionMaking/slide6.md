<script setup>
const contents = [
  { text: '<b>Problem:</b> Read a number and print whether it is positive, negative, or zero.' },
  { text: '<b>Input:</b> <code>num = -7</code>' },
  { text: '<b>Expected Output:</b> <code>Negative</code>' },
  { text: '<b>Note:</b> Handle all three cases — positive, negative, and exactly zero.' },
  { text: '<b>Hint:</b> Use an <code>if-else if-else</code> ladder. Check <code>num > 0</code>, then <code>num < 0</code>, and finally the <code>else</code> for zero.', highlight: true },
]
</script>

<Slide
  topic="Decision Making"
  sub-topic="Practice Problem 1 — Positive, Negative, or Zero"
  :contents="contents"
/>
