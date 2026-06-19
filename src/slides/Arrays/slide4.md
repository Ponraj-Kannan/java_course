<script setup>
const contents = [
  { text: '<b>Problem:</b> Reverse the elements of a 1D array and print the result.' },
  { text: '<b>Input:</b> <code>arr = {1, 2, 3, 4, 5}</code>' },
  { text: '<b>Expected Output:</b> <code>{5, 4, 3, 2, 1}</code>' },
  { text: '<b>Note:</b> Reverse the array in-place (without using a second array).' },
  { text: '<b>Hint:</b> Use two pointers — one starting at index <code>0</code> and one at <code>arr.length - 1</code>. Swap elements and move both pointers inward until they meet.', highlight: true },
]
</script>

<Slide
  topic="Arrays"
  sub-topic="Practice Problem 2 — Reverse Array"
  :contents="contents"
/>
