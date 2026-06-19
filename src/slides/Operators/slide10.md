<script setup>
const contents = [
  { text: '<b>Problem:</b> Using only the ternary operator (no <code>if-else</code>), solve the following three tasks.' },
  { text: '<b>Task 1:</b> Given <code>int x = 7</code>, print <code>Positive</code> if <code>x &gt; 0</code>, else print <code>Non-positive</code>.' },
  { text: '<b>Task 2:</b> Given <code>int a = 4, b = 9</code>, find and print the larger of the two numbers.' },
  { text: '<b>Task 3:</b> Given <code>int n = 14</code>, print <code>Even</code> if divisible by 2, else print <code>Odd</code>.' },
  { text: '<b>Hint:</b> Each task is one line using <code>condition ? valueIfTrue : valueIfFalse</code>. Store the result in a <code>String</code> variable and print it using <code>System.out.println()</code>.', highlight: true },
]
</script>

<Slide
  topic="Operators"
  sub-topic="Practice Problem 3 — Ternary Operator"
  :contents="contents"
/>
