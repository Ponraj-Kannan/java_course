<script setup>
const contents = [
  { text: '<b>Problem:</b> Read a student\'s name, age, and GPA from the user and print a formatted summary.' },
  { text: '<b>Input:</b><br><code>Enter name: Alice Johnson</code><br><code>Enter age: 20</code><br><code>Enter GPA: 8.7</code>' },
  { text: '<b>Expected Output:</b><br><code>Name : Alice Johnson</code><br><code>Age  : 20</code><br><code>GPA  : 8.7</code>' },
  { text: '<b>Note:</b> The name may contain spaces — use <code>nextLine()</code>. Age is an <code>int</code> — use <code>nextInt()</code>. GPA is a <code>double</code> — use <code>nextDouble()</code>.' },
  // { text: '<b>Hint:</b> Read age first with <code>nextInt()</code>, then GPA with <code>nextDouble()</code>, then call <code>sc.nextLine()</code> to clear the buffer before reading the full name with <code>nextLine()</code>.', highlight: true },
]
</script>

<Slide
  topic="Input Methods"
  sub-topic="Practice Problem 2 — Student Details"
  :contents="contents"
/>
