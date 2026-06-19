<script setup>
const contents = [
  { text: '<b>Math.pow(base, exponent)</b> — returns base raised to the power of exponent. Both arguments and the return type are <code>double</code>.' },
  { text: '<b>Math.sqrt(n)</b> — returns the positive square root of n. Returns <code>NaN</code> for negative input.' },
  { text: '<b>Math.cbrt(n)</b> — returns the cube root of n. Works for negative numbers as well.' },
  { text: '<b>Math.exp(n)</b> — returns e raised to the power n (e^n).' },
  // {
  //   label: 'Examples',
  //   text: 'System.out.println(Math.pow(2, 10));  // 1024.0\nSystem.out.println(Math.pow(9, 0.5)); // 3.0 (same as sqrt)\n\nSystem.out.println(Math.sqrt(144));   // 12.0\nSystem.out.println(Math.sqrt(-4));    // NaN\n\nSystem.out.println(Math.cbrt(27));    // 3.0\nSystem.out.println(Math.cbrt(-8));    // -2.0\n\nSystem.out.println(Math.exp(1));      // 2.718281828459045',
  //   codeEditor: true,
  //   lang: 'java',
  // },
  { text: '<b>Note:</b> <code>Math.pow()</code> always returns a <code>double</code>. Cast to <code>int</code> if you need an integer result: <code>(int) Math.pow(2, 4)</code>', highlight: true },
]
</script>

<Slide
  topic="Math Built-in Functions"
  sub-topic="Power and Root Methods"
  :contents="contents"
/>
