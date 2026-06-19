<script setup>
const contents = [
  { text: '<b>Problem:</b> Store the following details of a student using appropriate data types and print a formatted report.' },
  { text: '<b>Details to store:</b><br>Name — <code>"Ravi Kumar"</code><br>Age — <code>19</code><br>Grade — <code>\'A\'</code><br>GPA — <code>9.2</code><br>Passed — <code>true</code><br>Roll Number — <code>20240001L</code>' },
  { text: '<b>Expected Output:</b><br><code>Name        : Ravi Kumar</code><br><code>Age         : 19</code><br><code>Grade       : A</code><br><code>GPA         : 9.2</code><br><code>Passed      : true</code><br><code>Roll Number : 20240001</code>' },
  // { text: '<b>Note:</b> Choose the most appropriate data type for each field. Roll Number uses <code>long</code> as it may be large. GPA uses <code>double</code> for precision.' },
  // { text: '<b>Hint:</b> Declare each variable with its correct type and literal format. Use <code>System.out.println()</code> with string concatenation to format the output.', highlight: true },
]
</script>

<Slide
  topic="Data Types"
  sub-topic="Practice Problem 2 — Student Report"
  :contents="contents"
/>
