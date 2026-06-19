<script setup>
const contents = [
  { text: '<b>Problem:</b> Simulate rolling two six-sided dice and print the result of each die and their total.' },
  { text: '<b>Expected Output (sample):</b><br><code>Die 1: 4</code><br><code>Die 2: 6</code><br><code>Total: 10</code>' },
  { text: '<b>Note:</b> Each die produces a random integer between 1 and 6 (inclusive). Output will differ each run.' },
  // { text: '<b>Hint:</b> Use the formula <code>(int)(Math.random() * 6) + 1</code> to generate a random number between 1 and 6. Call it twice — once for each die.', highlight: true },
]
</script>

<Slide
  topic="Math Built-in Functions"
  sub-topic="Practice Problem 3 — Dice Roll Simulation"
  :contents="contents"
/>
