<script setup>
const contents = [
  { text: '<b>Problem:</b> Find and print the transpose of a given 3x3 matrix.' },
  { text: '<b>Input:</b><br><code>1 2 3</code><br><code>4 5 6</code><br><code>7 8 9</code>' },
  { text: '<b>Expected Output:</b><br><code>1 4 7</code><br><code>2 5 8</code><br><code>3 6 9</code>' },
  { text: '<b>Note:</b> In a transpose, rows become columns and columns become rows. Element at <code>[i][j]</code> moves to <code>[j][i]</code>.' },
  // { text: '<b>Hint:</b> Create a new matrix <code>transpose[j][i] = original[i][j]</code> inside a nested loop, then print the transpose matrix.', highlight: true },
]
</script>

<Slide
  topic="Arrays"
  sub-topic="Practice Problem 5 — Matrix Transpose"
  :contents="contents"
/>
