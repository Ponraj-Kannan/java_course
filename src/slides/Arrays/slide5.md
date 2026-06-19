<script setup>
const contents = [
  { text: '<b>Problem:</b> Find the maximum and minimum elements in a 1D array.' },
  { text: '<b>Input:</b> <code>arr = {3, 7, 1, 9, 4}</code>' },
  { text: '<b>Expected Output:</b> <code>Max = 9, Min = 1</code>' },
  { text: '<b>Note:</b> Do not use <code>Arrays.sort()</code>. Solve using a single loop.' },
  { text: '<b>Hint:</b> Initialize <code>max</code> and <code>min</code> with <code>arr[0]</code>. Loop through the array and update <code>max</code> if <code>arr[i] > max</code> and <code>min</code> if <code>arr[i] < min</code>.', highlight: true },
]
</script>

<Slide
  topic="Arrays"
  sub-topic="Practice Problem 3 — Max and Min"
  :contents="contents"
/>
