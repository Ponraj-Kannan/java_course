<script setup>
const contents = [
  { text: '<b>Math.min(a, b)</b> — returns the smaller of two values. Works with <code>int</code>, <code>long</code>, <code>float</code>, and <code>double</code>.' },
  { text: '<b>Math.max(a, b)</b> — returns the larger of two values. Works with the same types as <code>min()</code>.' },
  { text: '<b>Math.abs(n)</b> — returns the absolute value (removes the negative sign). Works with all numeric types.' },
  // {
  //   label: 'Examples',
  //   text: 'System.out.println(Math.min(10, 20));    // 10\nSystem.out.println(Math.min(-5, -3));   // -5\n\nSystem.out.println(Math.max(10, 20));    // 20\nSystem.out.println(Math.max(-5, -3));   // -3\n\nSystem.out.println(Math.abs(-99));      // 99\nSystem.out.println(Math.abs(45));       // 45\nSystem.out.println(Math.abs(-3.14));    // 3.14',
  //   codeEditor: true,
  //   lang: 'java',
  // },
  // { text: '<b>Common use of abs():</b> calculating the difference between two values regardless of order<br><code>Math.abs(a - b)</code> gives the distance between a and b', highlight: true },
]
</script>

<Slide
  topic="Math Built-in Functions"
  sub-topic="Min, Max, and Abs Methods"
  :contents="contents"
/>
