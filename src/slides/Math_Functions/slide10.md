<script setup>
const contents = [
  { text: '<b>Problem:</b> Calculate the hypotenuse of a right-angled triangle given the lengths of the two shorter sides.' },
  { text: '<b>Input:</b> <code>a = 3, b = 4</code>' },
  { text: '<b>Expected Output:</b> <code>Hypotenuse = 5.0</code>' },
  { text: '<b>Formula:</b> c = sqrt(a^2 + b^2)  (Pythagorean theorem)' },
  // { text: '<b>Hint:</b> Use <code>Math.pow(a, 2)</code> and <code>Math.pow(b, 2)</code> to square the sides, add them, and pass the result to <code>Math.sqrt()</code>.', highlight: true },
]
</script>

<Slide
  topic="Math Built-in Functions"
  sub-topic="Practice Problem 2 — Hypotenuse"
  :contents="contents"
/>
