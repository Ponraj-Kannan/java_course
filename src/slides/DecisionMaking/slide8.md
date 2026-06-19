<script setup>
const contents = [
  { text: '<b>Problem:</b> Given a day number (1–7), print the corresponding day name using a <code>switch</code> statement.' },
  { text: '<b>Input:</b> <code>day = 5</code>' },
  { text: '<b>Expected Output:</b> <code>Friday</code>' },
  { text: '<b>Note:</b> If the input is outside 1–7, print <code>Invalid day</code>.' },
  { text: '<b>Hint:</b> Use a <code>switch</code> with cases 1 through 7. Add a <code>default</code> case for invalid input. Remember to include <code>break</code> after each case.', highlight: true },
]
</script>

<Slide
  topic="Decision Making"
  sub-topic="Practice Problem 3 — Day Name using switch"
  :contents="contents"
/>
