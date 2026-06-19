<script setup>
const contents = [
  { text: '<b>Problem:</b> Declare variables for the length and width of a rectangle, then calculate and print the area and perimeter.' },
  { text: '<b>Input (hardcoded):</b> <code>length = 12, width = 7</code>' },
  { text: '<b>Expected Output:</b><br><code>Area = 84</code><br><code>Perimeter = 38</code>' },
  { text: '<b>Formulas:</b> Area = length x width | Perimeter = 2 x (length + width)' },
  { text: '<b>Hint:</b> Declare <code>int length = 12</code> and <code>int width = 7</code>. Then declare two more variables <code>area</code> and <code>perimeter</code>, compute using the formulas, and print both.', highlight: true },
]
</script>

<Slide
  topic="Variables"
  sub-topic="Practice Problem 2 — Area and Perimeter"
  :contents="contents"
/>
