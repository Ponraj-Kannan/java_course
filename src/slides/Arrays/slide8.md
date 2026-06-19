<script setup>
const contents = [
  { text: '<b>Problem:</b> Add two matrices of the same dimensions and print the resulting matrix.' },
  { text: '<b>Input Matrix A:</b><br><code>1 2 3</code><br><code>4 5 6</code><br><code>7 8 9</code>' },
  { text: '<b>Input Matrix B:</b><br><code>1 2 3</code><br><code>4 5 6</code><br><code>7 8 9</code>' },
  { text: '<b>Expected Output:</b><br><code>2  4  6</code><br><code>8  10 12</code><br><code>14 16 18</code>' },
  // { text: '<b>Hint:</b> Use nested <code>for</code> loops. For each position <code>[i][j]</code>, compute <code>result[i][j] = a[i][j] + b[i][j]</code>. Then print the result matrix using another nested loop.', highlight: true },
]
</script>

<Slide
  topic="Arrays"
  sub-topic="Practice Problem 4 — Matrix Addition"
  :contents="contents"
/>
