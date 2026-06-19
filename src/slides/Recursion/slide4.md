<script setup>
const contents = [
  { text: '<b>Sum of Natural Numbers:</b> Add all integers from 1 up to n<br><code>sum(4) = 4 + 3 + 2 + 1 = 10</code>' },
  // {
  //   label: 'Recursive sum method',
  //   text: 'static int sum(int n) {\n    if (n == 0) {       // base case\n        return 0;\n    }\n    return n + sum(n - 1); // recursive case\n}\n\n// sum(4)\n// = 4 + sum(3)\n// = 4 + 3 + sum(2)\n// = 4 + 3 + 2 + sum(1)\n// = 4 + 3 + 2 + 1 + sum(0)\n// = 4 + 3 + 2 + 1 + 0  =  10',
  //   codeEditor: true,
  //   lang: 'java',
  // },
  { text: '<b>Base case:</b> <code>n == 0</code>, returns 0 (adding nothing)' },
  // { text: '<b>Recursive case:</b> <code>n + sum(n - 1)</code> — adds current n to the sum of all smaller numbers' },
  { text: '<b>Compare with loop:</b> Recursion and loops can solve the same problems. Recursion is elegant but uses more memory (call stack) than a simple loop.', highlight: true },
]
</script>

<Slide
  topic="Recursion"
  sub-topic="Sum of Natural Numbers"
  :contents="contents"
/>
