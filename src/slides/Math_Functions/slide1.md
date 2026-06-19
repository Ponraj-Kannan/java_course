<script setup>
const contents = [
  { text: '<b>java.lang.Math</b> — a built-in Java class that provides commonly used mathematical functions and constants' },
  // { text: 'No import is needed — <code>java.lang</code> is automatically available in every Java program' },
  { text: 'All methods in the Math class are <b>static</b> — they are called directly on the class without creating an object' },
  // {
  //   label: 'Calling syntax',
  //   text: '// Math.methodName(arguments)\ndouble result = Math.sqrt(25);  // returns 5.0\ndouble power  = Math.pow(2, 8); // returns 256.0',
  //   codeEditor: true,
  //   lang: 'java',
  // },
  { text: '<b>Math constants:</b><br><code>Math.PI</code> — value of pi (3.141592653589793)<br><code>Math.E</code> — base of natural logarithm (2.718281828459045)' },
  // { text: '<b>Categories of Math methods:</b> Rounding, Power & Root, Trigonometry, Logarithm, Min / Max / Abs, Random', highlight: true },
]
</script>

<Slide
  topic="Math Built-in Functions"
  sub-topic="Introduction to java.lang.Math"
  :contents="contents"
/>
