<script setup>
const contents = [
  { text: '<b>Problem:</b> Given two integers <code>a</code> and <code>b</code>, compute and print the result of all five arithmetic operations.' },
  { text: '<b>Input:</b> <code>a = 17</code>, <code>b = 5</code>' },
  { text: '<b>Expected Output:</b><br><code>Sum = 22</code><br><code>Difference = 12</code><br><code>Product = 85</code><br><code>Quotient = 3</code><br><code>Remainder = 2</code>' },
  { text: '<b>Bonus:</b> Also print the result of <code>(double) a / b</code> and observe the difference from integer division.', highlight: true},
  // { text: '<b>Hint:</b> Declare <code>int a = 17, b = 5;</code> and use <code>+</code>, <code>-</code>, <code>*</code>, <code>/</code>, <code>%</code>. For the bonus, cast <code>(double) a / b</code> and store in a <code>double</code> variable.', highlight: true },
]
</script>

<Slide
  topic="Operators"
  sub-topic="Practice Problem 1 — Arithmetic"
  :contents="contents"
/>
