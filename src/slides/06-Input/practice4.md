<script setup>
const contents = [
  { text: '<b>Problem:</b> Write a Java program that reads two numbers passed as command-line arguments (<code>args[0]</code> and <code>args[1]</code>), verifies that at least two arguments were provided, and prints their product.' },
  { text: '<b>Invocation:</b> <code>java MultiplyApp 7 8</code>' },
  { text: '<b>Expected Output:</b> <code>7 * 8 = 56</code>' },
  { text: '<b>Key Concepts:</b> Check <code>args.length &gt;= 2</code> before accessing array elements to prevent <code>ArrayIndexOutOfBoundsException</code>, and convert string arguments to integers with <code>Integer.parseInt(args[0])</code>.' },
]
</script>

<Slide
  topic="Java Input Methods"
  sub-topic="Practice Problem 4 — Command-Line Argument Multiplier"
  :contents="contents"
/>
