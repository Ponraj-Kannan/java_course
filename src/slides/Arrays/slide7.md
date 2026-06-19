<script setup>
const contents = [
  // {
  //   label: 'Traversal using nested for loop',
  //   text: 'int[][] arr = {{1,2,3},{4,5,6},{7,8,9}};\nfor (int i = 0; i < arr.length; i++) {\n    for (int j = 0; j < arr[i].length; j++) {\n        System.out.print(arr[i][j] + " ");\n    }\n    System.out.println();\n}',
  //   codeEditor: true,
  //   lang: 'java',
  // },
  // {
  //   label: 'Traversal using for-each loop',
  //   text: 'for (int[] row : arr) {\n    for (int val : row) {\n        System.out.print(val + " ");\n    }\n    System.out.println();\n}',
  //   codeEditor: true,
  //   lang: 'java',
  // },
  { text: '<b>Outer loop (i)</b> — iterates over rows' },
  { text: '<b>Inner loop (j)</b> — iterates over columns within each row' },
  { text: '<b>Use nested for loop</b> when you need both row index and column index (e.g., matrix operations)', highlight: true },
]
</script>

<Slide
  topic="Arrays"
  sub-topic="Traversing a 2D Array"
  :contents="contents"
/>
