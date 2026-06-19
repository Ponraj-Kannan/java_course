<script setup>
const contents = [
  { text: '<b>Problem:</b> Write a recursive method to compute the n-th Fibonacci number.' },
  { text: '<b>Method signature:</b> <code>static int fibonacci(int n)</code>' },
  { text: '<b>Definition:</b> fib(0) = 0, fib(1) = 1, fib(n) = fib(n-1) + fib(n-2) for n > 1' },
  { text: '<b>Input:</b> <code>n = 6</code> → <b>Output:</b> <code>8</code><br>(Sequence: 0, 1, 1, 2, 3, 5, 8, ...)' },
  { text: '<b>Hint:</b> Use two base cases — return <code>0</code> when <code>n == 0</code> and return <code>1</code> when <code>n == 1</code>. For all other values, return <code>fibonacci(n-1) + fibonacci(n-2)</code>.', highlight: true },
]
</script>

<Slide
  topic="Methods"
  sub-topic="Practice Problem 3 — Fibonacci"
  :contents="contents"
/>
