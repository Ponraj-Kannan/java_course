<script setup>
const contents = [
  { text: '<b>Fibonacci Series:</b> Each number is the sum of the two preceding numbers<br><code>0, 1, 1, 2, 3, 5, 8, 13, 21 ...</code><br>Formula: <code>F(n) = F(n-1) + F(n-2)</code>' },
  // {
  //   label: 'Recursive Fibonacci method',
  //   text: 'static int fibonacci(int n) {\n    if (n == 0) return 0; // base case 1\n    if (n == 1) return 1; // base case 2\n    return fibonacci(n - 1) + fibonacci(n - 2); // recursive case\n}\n\n// fibonacci(5)\n// = fibonacci(4) + fibonacci(3)\n// = (fibonacci(3) + fibonacci(2)) + ...\n// = 5',
  //   codeEditor: true,
  //   lang: 'java',
  // },
  { text: '<b>Two base cases:</b> <code>F(0) = 0</code> and <code>F(1) = 1</code>' },
  // { text: '<b>Recursive case:</b> <code>F(n-1) + F(n-2)</code> — branches into two recursive calls each time' },
  { text: '<b>Note:</b> Recursive Fibonacci is simple to understand but inefficient for large n — it recalculates the same values many times. Iterative approach is preferred for performance.', highlight: true },
]
</script>

<Slide
  topic="Recursion"
  sub-topic="Fibonacci Series"
  :contents="contents"
/>
