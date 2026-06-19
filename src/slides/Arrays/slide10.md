<script setup>
const contents = [
  {
    label: 'Import required before use',
    text: 'import java.util.Arrays;',
    codeEditor: true,
    lang: 'java',
  },
  { text: '<b>Arrays.sort(arr)</b> — sorts elements in ascending order<br><code>Arrays.sort(arr)</code> modifies the original array' },
  // { text: '<b>Arrays.binarySearch(arr, key)</b> — returns index of key in a sorted array (-1 if not found)' },
  { text: '<b>Arrays.fill(arr, val)</b> — fills all elements with the given value<br><code>Arrays.fill(arr, 0)</code> → all elements become 0' },
  { text: '<b>Arrays.copyOf(arr, len)</b> — returns a new array of given length copied from arr' },
]
</script>

<Slide
  topic="Arrays"
  sub-topic="Built-in Methods — java.util.Arrays"
  :contents="contents"
/>
