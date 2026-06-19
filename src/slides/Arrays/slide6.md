<script setup>
const contents = [
  {
    label: 'Declaration with size',
    text: '// Declaration\nint[][] arr = new int[3][3];',
    codeEditor: true,
    lang: 'java',
  },
  // {
  //   label: 'Declaration with values',
  //   text: '// Initialization at declaration\nint[][] arr = {\n    {1, 2, 3},\n    {4, 5, 6},\n    {7, 8, 9}\n};',
  //   codeEditor: true,
  //   lang: 'java',
  // },
  { text: '<b>int[][]</b> — declares a 2D array (array of arrays)' },
  { text: '<b>new int[3][3]</b> — creates a matrix with 3 rows and 3 columns (9 elements total)' },
  { text: '<b>Access:</b> arr[row][col] — reads element at given row and column' },
  { text: '<b>Update:</b> arr[1][2] = 99 — sets the element at row 1, column 2' },
  { text: '<b>arr.length</b> → number of rows<br><b>arr[0].length</b> → number of columns'},
]
</script>

<Slide
  topic="Arrays"
  sub-topic="Two-Dimensional Arrays"
  :contents="contents"
/>
