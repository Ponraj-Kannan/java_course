<script setup>
const contents = [
  // {
  //   label: 'Traversal using for loop',
  //   text: 'int[] arr = {10, 20, 30, 40, 50};\nfor (int i = 0; i < arr.length; i++) {\n    System.out.println(arr[i]);\n}',
  //   codeEditor: true,
  //   lang: 'java',
  // },
  // {
  //   label: 'Traversal using for-each loop',
  //   text: 'int[] arr = {10, 20, 30, 40, 50};\nfor (int element : arr) {\n    System.out.println(element);\n}',
  //   codeEditor: true,
  //   lang: 'java',
  // },
  { text: '<b>arr.length</b> — returns the number of elements in the array (not a method, it is a property)' },
  { text: '<b>for loop</b> — use when you need the index (e.g., update elements, compare neighbors)' },
  { text: '<b>for-each loop</b> — use when you only need to read each element (cleaner syntax)' },
  { text: '<b>Note:</b> for-each cannot be used to modify array elements directly.', highlight: true },
]
</script>

<Slide
  topic="Arrays"
  sub-topic="Traversing a 1D Array"
  :contents="contents"
/>
