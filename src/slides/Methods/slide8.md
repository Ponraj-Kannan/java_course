<script setup>
const contents = [
  // {
  //   label: 'Factorial using recursion',
  //   text: 'static int factorial(int n) {\n    if (n == 0) return 1;   // base case\n    return n * factorial(n - 1); // recursive call\n}\n\nSystem.out.println(factorial(5)); // 120',
  //   codeEditor: true,
  //   lang: 'java',
  // },
  // {
  //   label: 'How the call stack unfolds',
  //   text: '// factorial(5)\n//   → 5 * factorial(4)\n//        → 4 * factorial(3)\n//             → 3 * factorial(2)\n//                  → 2 * factorial(1)\n//                       → 1 * factorial(0) = 1\n// Result: 5*4*3*2*1 = 120',
  //   codeEditor: true,
  //   lang: 'java',
  // },
  { text: '<b>Recursion</b> — a method that calls itself to solve a smaller version of the same problem' },
  { text: '<b>Base case</b> — the condition that stops the recursion (e.g., <code>n == 0</code>); without it the method runs forever' },
  { text: '<b>Recursive case</b> — the step that breaks the problem into a smaller sub-problem' },
  { text: '<b>Warning:</b> If the base case is missing or never reached, a StackOverflowError occurs at runtime.', highlight: true },
]
</script>

<Slide
  topic="Methods"
  sub-topic="Recursion"
  :contents="contents"
/>
