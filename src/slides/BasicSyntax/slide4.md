<script setup>
const contents = [
  // {
  //   label: 'System.out.printf — Formatted output',
  //   text: 'String name = "Alice";\nint age = 20;\ndouble gpa = 9.456;\n\nSystem.out.printf("Name: %s%n", name);\nSystem.out.printf("Age: %d%n", age);\nSystem.out.printf("GPA: %.2f%n", gpa);\n// Output:\n// Name: Alice\n// Age: 20\n// GPA: 9.46',
  //   codeEditor: true,
  //   lang: 'java',
  // },
  { text: '<b>printf</b> stands for <i>print formatted</i> — inserts values into a format string using placeholders called <b>format specifiers</b>.' },
  { text: '<b>%s</b> → String &nbsp;|&nbsp; <b>%d</b> → integer &nbsp;|&nbsp; <b>%f</b> → decimal &nbsp;|&nbsp; <b>%c</b> → char &nbsp;|&nbsp; <b>%b</b> → boolean' },
  { text: '<b>%.2f</b> — limits a decimal to exactly 2 places. <code>%8d</code> — right-aligns an integer in a field of width 8.' },
  { text: '<b>%n</b> — platform-safe newline (preferred over <code>\\n</code> inside <code>printf</code>). <code>\\t</code> inserts a tab.' },
  { text: '<b>Note:</b> Arguments must match their specifiers in order and type. A mismatch causes a runtime exception.', highlight: true },
]
</script>

<Slide
  topic="Basic Syntax"
  sub-topic="Printing — System.out.printf()"
  :contents="contents"
/>
