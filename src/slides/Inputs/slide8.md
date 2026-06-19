<script setup>
const contents = [
  { text: '<b>Problem:</b> Take two integers as input from the user and print their sum, difference, product, and quotient.' },
  { text: '<b>Input:</b><br><code>Enter first number: 12</code><br><code>Enter second number: 4</code>' },
  { text: '<b>Expected Output:</b><br><code>Sum = 16</code><br><code>Difference = 8</code><br><code>Product = 48</code><br><code>Quotient = 3</code>' },
  { text: '<b>Note:</b> Use <code>nextInt()</code> to read both numbers. For quotient, use integer division.' },
  // { text: '<b>Hint:</b> Create a <code>Scanner</code> object, call <code>nextInt()</code> twice for the two values, then compute and print each result using <code>+</code>, <code>-</code>, <code>*</code>, and <code>/</code>.', highlight: true },
]
</script>

<Slide
  topic="Input Methods"
  sub-topic="Practice Problem 1 — Simple Calculator"
  :contents="contents"
/>
