<script setup>
const contents = [
  { text: '<b>Recursion</b> — a method solves a problem by calling itself with a reduced input' },
  { text: '<b>Iteration</b> — a loop repeats a block of code until a condition is false' },
  // { text: '<b>Recursion</b> — cleaner and more readable for problems that are naturally recursive (trees, divide and conquer). Uses the call stack for each function call.' },
  // { text: '<b>Iteration</b> — more memory efficient. Does not risk StackOverflowError. Preferred when performance matters.' },
  { text: '<b>When to use Recursion:</b> Tree/graph traversal, divide and conquer algorithms (merge sort, binary search), problems defined recursively (factorial, Fibonacci, Tower of Hanoi)', highlight: true },
  { text: '<b>When to use Iteration:</b> Simple counting, array traversal, sum/product calculations where a loop is straightforward', highlight: true },
]
</script>

<Slide
  topic="Recursion"
  sub-topic="Recursion vs Iteration"
  :contents="contents"
/>
