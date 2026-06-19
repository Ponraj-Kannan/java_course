<script setup>
const contents = [
  // {
  //   label: 'Side-by-side comparison',
  //   text: '// println — newline after output\nSystem.out.println("Line 1");\nSystem.out.println("Line 2");\n\n// print — no newline, continues on same line\nSystem.out.print("A ");\nSystem.out.print("B ");\nSystem.out.print("C\\n"); // manual newline\n\n// printf — formatted, no automatic newline\nSystem.out.printf("%-10s %5d %8.2f%n", "Alice", 20, 9.45);\nSystem.out.printf("%-10s %5d %8.2f%n", "Bob",   19, 8.90);',
  //   codeEditor: true,
  //   lang: 'java',
  // },
  { text: '<b>println(val)</b> — prints value + moves to next line. Best for simple, line-by-line output.' },
  { text: '<b>print(val)</b> — prints value, stays on same line. Best when building output piece by piece.' },
  { text: '<b>printf(format, args…)</b> — formats and prints. Best for tables, aligned columns, and controlled decimal places.' },
  { text: '<b>%-10s</b> — left-aligns a string in 10 chars | <b>%5d</b> — right-aligns int in 5 chars | <b>%8.2f</b> — float in 8 chars, 2 decimal places' },
  { text: '<b>Rule of thumb:</b> use <code>println</code> for general output, <code>print</code> when staying on the same line, and <code>printf</code> when formatting matters.', highlight: true },
]
</script>

<Slide
  topic="Basic Syntax"
  sub-topic="Printing — Comparison of All Three Methods"
  :contents="contents"
/>
