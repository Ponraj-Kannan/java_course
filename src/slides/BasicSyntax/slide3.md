<script setup>
const contents = [
  // {
  //   label: 'System.out.print — Print without newline',
  //   text: 'System.out.print("Hello, ");\nSystem.out.print("World!");\n// Output: Hello, World!\n\nSystem.out.print(1);\nSystem.out.print(2);\nSystem.out.print(3);\n// Output: 123',
  //   codeEditor: true,
  //   lang: 'java',
  // },
  { text: '<b>print</b> — prints the value but does <u>not</u> move to the next line. The next output continues on the same line.' },
  // { text: '<b>Use case:</b> building output on one line across multiple statements, such as printing array elements side by side.' },
  { text: '<b>Comparison:</b><br><code>print("A"); print("B");</code> → <code>AB</code><br><code>println("A"); println("B");</code> → <br><code>A</code> then <code>B</code> on next line' },
  { text: '<b>Adding spaces manually </b>include spaces in the string <code>print("Hello ")</code>' },
  { text: '<b>Note:</b> <code>System.out.print()</code> with no argument is a compile error — unlike <code>println()</code>, it requires at least one argument.', highlight: true },
]
</script>

<Slide
  topic="Basic Syntax"
  sub-topic="Printing — System.out.print()"
  :contents="contents"
/>
