<script setup>
const contents = [
  { text: '<b>Problem:</b> Search for a given element in a 1D array and print its index.' },
  { text: '<b>Input:</b> <code>arr = {10, 20, 30, 40, 50}</code>, <code>key = 30</code>' },
  { text: '<b>Expected Output:</b> <code>Element 30 found at index 2</code>' },
  { text: '<b>Note:</b> If the element is not found, print <code>Element not found</code>.' },
  { text: '<b>Hint:</b> Use a <code>for</code> loop to compare each element with the key using <code>==</code>. Store the index when a match is found.', highlight: true },
]
</script>

<Slide
  topic="Arrays"
  sub-topic="Practice Problem 1 — Linear Search"
  :contents="contents"
/>
