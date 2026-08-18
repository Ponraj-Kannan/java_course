<script setup>
const contents = [
  { text: '<b>Problem:</b> Trace the following recursive method by hand and predict its output for <code>printFun(3)</code>.' },
  { text: '<b>Expected Output:</b> <code>3 2 1 1 2 3</code>' },
  { text: '<b>Explanation:</b> Prints before the recursive call (winding phase: 3 2 1), then prints after returning from the call (unwinding phase: 1 2 3).' },
]
</script>

<Slide
  topic="Recursion"
  sub-topic="Practice Problem 4 — Trace & Predict Output"
  :contents="contents"
/>
