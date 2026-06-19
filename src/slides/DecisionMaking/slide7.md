<script setup>
const contents = [
  { text: '<b>Problem:</b> Find the largest among three numbers.' },
  { text: '<b>Input:</b> <code>a = 12, b = 35, c = 27</code>' },
  { text: '<b>Expected Output:</b> <code>Largest = 35</code>' },
  { text: '<b>Note:</b> Do not use any built-in <code>Math</code> methods. Solve using <code>if-else</code> only.' },
  { text: '<b>Hint:</b> Use nested <code>if</code> or an <code>if-else if-else</code> ladder. Check if <code>a</code> is greater than both <code>b</code> and <code>c</code>, then repeat for <code>b</code> and <code>c</code>.', highlight: true },
]
</script>

<Slide
  topic="Decision Making"
  sub-topic="Practice Problem 2 — Largest of Three Numbers"
  :contents="contents"
/>
