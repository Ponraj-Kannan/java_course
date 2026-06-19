<script setup>
const contents = [
  { text: '<b>Problem:</b> Calculate and print the area and circumference of a circle given its radius.' },
  { text: '<b>Input:</b> <code>radius = 7</code>' },
  { text: '<b>Expected Output:</b><br><code>Area = 153.94</code><br><code>Circumference = 43.98</code>' },
  { text: '<b>Formulas:</b> Area = pi x r^2 <br>Circumference = 2 x pi x r' },
  // { text: '<b>Hint:</b> Use <code>Math.PI</code> for pi and <code>Math.pow(radius, 2)</code> for r squared. Round results to 2 decimal places using <code>Math.round(value * 100.0) / 100.0</code>.', highlight: true },
]
</script>

<Slide
  topic="Math Built-in Functions"
  sub-topic="Practice Problem 1 — Circle Geometry"
  :contents="contents"
/>
