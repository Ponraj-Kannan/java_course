<script setup>
const contents = [
  { text: '<b>Power:</b> Multiply a base by itself n times<br><code>power(2, 4) = 2 x 2 x 2 x 2 = 16</code><br><code>power(x, 0) = 1</code> (any number to the power 0 is 1)' },
  // {
  //   label: 'Recursive power method',
  //   text: 'static int power(int base, int exp) {\n    if (exp == 0) {              // base case\n        return 1;\n    }\n    return base * power(base, exp - 1); // recursive case\n}\n\n// power(3, 3)\n// = 3 * power(3, 2)\n// = 3 * 3 * power(3, 1)\n// = 3 * 3 * 3 * power(3, 0)\n// = 3 * 3 * 3 * 1  =  27',
  //   codeEditor: true,
  //   lang: 'java',
  // },
  { text: '<b>Base case:</b> <code>exp == 0</code>, returns 1' },
  // { text: '<b>Recursive case:</b> multiply <code>base</code> by the result of <code>power(base, exp - 1)</code>' },
  { text: '<b>Note:</b> This handles only non-negative integer exponents. Use <code>Math.pow()</code> for decimal or negative exponents.', highlight: true },
]
</script>

<Slide
  topic="Recursion"
  sub-topic="Power of a Number"
  :contents="contents"
/>
