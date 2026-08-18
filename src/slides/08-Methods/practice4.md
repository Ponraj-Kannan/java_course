<script setup>
const contents = [
  { text: '<b>Problem:</b> Write a recursive static method <code>int sumDigits(int n)</code> that computes the sum of all digits of a non-negative integer <code>n</code> without using any loops or String conversions.' },
  { text: '<b>Sample Calls:</b><br><code>sumDigits(1234)</code><br><code>sumDigits(908)</code><br><code>sumDigits(5)</code>' },
  { text: '<b>Expected Outputs:</b><br><code>10</code> (1+2+3+4)<br><code>17</code> (9+0+8)<br><code>5</code>' },
  { text: '<b>Base Case & Recursive Step:</b> If <code>n == 0</code> return <code>0</code>; otherwise return <code>(n % 10) + sumDigits(n / 10)</code>.' },
]
</script>

<Slide
  topic="Methods"
  sub-topic="Practice Problem 4 — Recursive Sum of Digits"
  :contents="contents"
/>
