<script setup>
const contents = [
  { text: '<b>char</b> — 2 bytes (16 bits) | Stores a single Unicode character | Value is enclosed in <b>single quotes</b>: <code>\'A\'</code>' },
  { text: '<b>boolean</b> — 1 bit (JVM-dependent) | Stores only two values: <code>true</code> or <code>false</code> | Used for conditions and flags' },
  // {
  //   label: 'char examples',
  //   text: 'char grade   = \'A\';\nchar symbol  = \'@\';\nchar digit   = \'7\';\nchar newline = \'\\n\'; // escape sequence\n\n// char is stored as a Unicode number internally\nchar ch = 65;\nSystem.out.println(ch); // prints A  (ASCII 65 = \'A\')\n\n// Arithmetic on char\nSystem.out.println((int) \'A\'); // 65\nSystem.out.println((char)(\'A\' + 1)); // B',
  //   codeEditor: true,
  //   lang: 'java',
  // },
  // {
  //   label: 'boolean examples',
  //   text: 'boolean isPassed  = true;\nboolean isRaining = false;\n\nint marks = 75;\nboolean eligible = (marks >= 50); // true\n\nSystem.out.println(eligible); // true',
  //   codeEditor: true,
  //   lang: 'java',
  // },
  { text: '<b>Note:</b> <code>char</code> uses single quotes <code>\'A\'</code>. <code>String</code> uses double quotes <code>"A"</code>. They are different types.', highlight: true },
]
</script>

<Slide
  topic="Data Types"
  sub-topic="Primitive Types — char and boolean"
  :contents="contents"
/>
