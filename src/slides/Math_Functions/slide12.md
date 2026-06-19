<script setup>
const contents = [
  { text: '<b>Problem:</b> Calculate the distance between two points on a 2D plane.' },
  { text: '<b>Input:</b> <code>x1 = 1, y1 = 2, x2 = 4, y2 = 6</code>' },
  { text: '<b>Expected Output:</b> <code>Distance = 5.0</code>' },
  { text: '<b>Formula:</b> distance = sqrt( (x2 - x1)^2 + (y2 - y1)^2 )' },
  // { text: '<b>Hint:</b> Use <code>Math.pow(x2 - x1, 2)</code> and <code>Math.pow(y2 - y1, 2)</code>, add the results, then pass to <code>Math.sqrt()</code>.', highlight: true },
]
</script>

<Slide
  topic="Math Built-in Functions"
  sub-topic="Practice Problem 4 — Distance Between Points"
  :contents="contents"
/>
