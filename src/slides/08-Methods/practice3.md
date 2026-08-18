<script setup>
const contents = [
  { text: '<b>Problem:</b> Write a utility class named <code>MathUtils</code> containing two <code>public static</code> methods:<br>1. <code>boolean isPrime(int n)</code> — returns <code>true</code> if <code>n</code> is a prime number, <code>false</code> otherwise.<br>2. <code>int gcd(int a, int b)</code> — returns the greatest common divisor of <code>a</code> and <code>b</code> using the Euclidean algorithm.' },
  { text: '<b>Sample Invocations:</b><br><code>MathUtils.isPrime(17); // returns true</code><br><code>MathUtils.isPrime(15); // returns false</code><br><code>MathUtils.gcd(48, 18);  // returns 6</code>' },
  { text: '<b>Expected Output:</b> Direct boolean and integer results without creating an object of <code>MathUtils</code>.' },
]
</script>

<Slide
  topic="Methods"
  sub-topic="Practice Problem 3 — Static Utility Methods"
  :contents="contents"
/>
