<script setup>
const contents = [
  { text: '<b>Problem:</b> Write a method that takes an integer array and returns the sum of all its elements.' },
  { text: '<b>Method signature:</b> <code>static int sumArray(int[] arr)</code>' },
  { text: '<b>Input:</b> <code>arr = {1, 2, 3, 4, 5}</code> → <b>Output:</b> <code>15</code>' },
  { text: '<b>Note:</b> The method should work for any size array.' },
  // { text: '<b>Hint:</b> Initialize a variable <code>sum = 0</code>. Use a <code>for</code> loop (or for-each) to add each element to <code>sum</code>. Return <code>sum</code> after the loop.', highlight: true },
]
</script>

<Slide
  topic="Methods"
  sub-topic="Practice Problem 2 — sumArray"
  :contents="contents"
/>
