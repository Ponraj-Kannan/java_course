<script setup>
const contents = [
  { text: '<b>Factorial:</b> The product of all positive integers from 1 to n<br><code>5! = 5 x 4 x 3 x 2 x 1 = 120</code><br><code>0! = 1</code> (by definition)' },
  // {
  //   label: 'Recursive factorial method',
  //   text: 'static int factorial(int n) {\n    if (n == 0) {          // base case\n        return 1;\n    }\n    return n * factorial(n - 1); // recursive case\n}\n\n// factorial(4)\n// = 4 * factorial(3)\n// = 4 * 3 * factorial(2)\n// = 4 * 3 * 2 * factorial(1)\n// = 4 * 3 * 2 * 1 * factorial(0)\n// = 4 * 3 * 2 * 1 * 1  =  24',
  //   codeEditor: true,
  //   lang: 'java',
  // },
  { text: '<b>Base case:</b> <code>n == 0</code>, returns 1' },
  // { text: '<b>Recursive case:</b> <code>n * factorial(n - 1)</code> — problem reduces by 1 each call' },
  { text: '<b>Note:</b> Factorial is only defined for non-negative integers. Always validate input before calling.', highlight: true },
]
</script>

<Slide
  topic="Recursion"
  sub-topic="Factorial"
  :contents="contents"
/>
