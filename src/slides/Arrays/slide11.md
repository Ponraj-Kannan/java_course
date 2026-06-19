<script setup>
const contents = [
  { text: '<b>Arrays.copyOfRange(arr, from, to)</b> — copies elements from index <code>from</code> to <code>to-1</code>' },
  { text: '<b>Arrays.equals(a, b)</b> — returns true if both arrays have same length and elements' },
  { text: '<b>Arrays.toString(arr)</b> — converts 1D array to a readable string<br><code>[10, 20, 30]</code>' },
  { text: '<b>Note:</b> Always call <code>Arrays.sort(arr)</code> before using <code>Arrays.binarySearch()</code>, otherwise the result is unpredictable.', highlight: true },
]
</script>

<Slide
  topic="Arrays"
  sub-topic="Built-in Methods — java.util.Arrays"
  :contents="contents"
/>
