<script setup>
const contents = [
  { text: '<b>Problem:</b> Declare one variable of each primitive data type, assign appropriate values, and print them all with labels.' },
  { text: '<b>Expected Output:</b><br><code>byte    : 100</code><br><code>short   : 30000</code><br><code>int     : 500000</code><br><code>long    : 9876543210</code><br><code>float   : 3.14</code><br><code>double  : 9.999999999</code><br><code>char    : J</code><br><code>boolean : true</code>' },
  { text: '<b>Note:</b> Use correct literal suffixes — <code>L</code> for long, <code>f</code> for float. Use single quotes for char.', highlight: true  },
  // { text: '<b>Hint:</b> Declare all 8 variables at the top of <code>main()</code>, then use <code>System.out.println()</code> for each with a descriptive label string.', highlight: true },
]
</script>

<Slide
  topic="Data Types"
  sub-topic="Practice Problem 1 — Declare All Primitive Types"
  :contents="contents"
/>
