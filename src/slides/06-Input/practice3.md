<script setup>
const contents = [
  { text: '<b>Problem:</b> Write a Java program using <code>Scanner</code> that prompts the user for a valid positive integer. If the user enters non-integer input (e.g. text or float), display an error message and repeatedly ask until valid input is received.' },
  { text: '<b>Input Sequence:</b><br><code>hello</code> → <i>Invalid! Try again.</i><br><code>3.14</code> → <i>Invalid! Try again.</i><br><code>42</code> → <i>Accepted!</i>' },
  { text: '<b>Expected Output:</b> <code>Accepted number: 42</code>' },
  { text: '<b>Key Concepts:</b> Use a <code>while(!sc.hasNextInt())</code> loop, call <code>sc.next()</code> inside the loop to discard the invalid token, and call <code>sc.nextInt()</code> only once a valid integer is confirmed.' },
]
</script>

<Slide
  topic="Java Input Methods"
  sub-topic="Practice Problem 3 — Robust Input Validator"
  :contents="contents"
/>
