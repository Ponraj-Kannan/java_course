<script setup>
const contents = [
  { text: '<b>Math.log(n)</b> — returns the natural logarithm (base e) of n. Returns <code>NaN</code> for negative values, <code>-Infinity</code> for 0.' },
  { text: '<b>Math.log10(n)</b> — returns the base-10 logarithm of n.' },
  { text: '<b>Custom base logarithm</b> — Java does not have a direct method. Use the change of base formula: <code>Math.log(n) / Math.log(base)</code>' },
  // {
  //   label: 'Examples',
  //   text: 'System.out.println(Math.log(Math.E)); // 1.0  (ln(e) = 1)\nSystem.out.println(Math.log(1));      // 0.0  (ln(1) = 0)\nSystem.out.println(Math.log(0));      // -Infinity\nSystem.out.println(Math.log(-1));     // NaN\n\nSystem.out.println(Math.log10(100));  // 2.0\nSystem.out.println(Math.log10(1000)); // 3.0\n\n// log base 2 of 8\ndouble log2 = Math.log(8) / Math.log(2);\nSystem.out.println(log2); // 3.0',
  //   codeEditor: true,
  //   lang: 'java',
  // },
  { text: '<b>Note:</b> Always ensure input is positive before calling <code>Math.log()</code> or <code>Math.log10()</code> to avoid <code>NaN</code> or <code>-Infinity</code> results.', highlight: true },
]
</script>

<Slide
  topic="Math Built-in Functions"
  sub-topic="Logarithm Methods"
  :contents="contents"
/>
