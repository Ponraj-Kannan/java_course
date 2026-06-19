<script setup>
const contents = [
  { text: '<b>Problem:</b> Write a method that checks whether a given number is prime and returns <code>true</code> or <code>false</code>.' },
  // { text: '<b>Method signature:</b> <code>static boolean isPrime(int n)</code>' },
  { text: '<b>Input:</b> <code>n = 7</code> → <b>Output:</b> <code>true</code><br><b>Input:</b> <code>n = 10</code> → <b>Output:</b> <code>false</code>' },
  { text: '<b>Note:</b> A prime number is divisible only by 1 and itself. Numbers less than 2 are not prime.' },
  // { text: '<b>Hint:</b> Loop from <code>2</code> to <code>n-1</code>. If <code>n % i == 0</code> for any <code>i</code>, return <code>false</code>. If the loop completes without finding a divisor, return <code>true</code>.', highlight: true },
]
</script>

<Slide
  topic="Methods"
  sub-topic="Practice Problem 1 — isPrime"
  :contents="contents"
/>
