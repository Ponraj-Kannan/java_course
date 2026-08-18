<script setup>
const contents = [
  { text: '<b>Problem:</b> Write a Java program using <code>Scanner</code> to read a student\'s ID (integer), GPA (double), and full name (multi-word string with spaces). Correctly handle the newline buffer before reading the name, and display the formatted profile.' },
  { text: '<b>Input:</b><br><code>101</code><br><code>3.85</code><br><code>Alice Smith</code>' },
  { text: '<b>Expected Output:</b><br><code>ID: 101</code><br><code>GPA: 3.85</code><br> <code>Name: Alice Smith</code>' },
  { text: '<b>Key Concepts:</b> Use <code>sc.nextInt()</code> for ID, <code>sc.nextDouble()</code> for GPA, a dummy <code>sc.nextLine()</code> to consume the trailing newline, and <code>sc.nextLine()</code> to read the full name.' },
]
</script>

<Slide
  topic="Java Input Methods"
  sub-topic="Practice Problem 1 — Student Profile"
  :contents="contents"
/>
