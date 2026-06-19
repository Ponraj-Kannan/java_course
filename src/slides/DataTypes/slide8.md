<script setup>
const contents = [
  { text: '<b>Literal</b> — a fixed value written directly in the source code. Each data type has a specific way to write its literal.' },
  // { text: '<b>int</b> — plain number: <code>42</code>, <code>-100</code>, <code>0</code>' },
  { text: '<b>long</b> — append <code>L</code>: <code>1000000L</code> (required when value exceeds int range)' },
  { text: '<b>float</b> — append <code>f</code>: <code>3.14f</code> (required, otherwise Java treats it as double)' },
  // { text: '<b>double</b> — plain decimal: <code>3.14</code>, <code>99.99</code>' },
  { text: '<b>char</b> — single quotes: <code>\'A\'</code>, <code>\'9\'</code>, <code>\'\\n\'</code>' },
  { text: '<b>boolean</b> — keywords: <code>true</code> or <code>false</code> (lowercase only)' },
  { text: '<b>String</b> — double quotes: <code>"Hello"</code>, <code>"123"</code>' },
  // {
  //   label: 'Common literal mistakes',
  //   text: 'float  x = 3.14;   // ERROR — missing f suffix\nfloat  y = 3.14f;  // CORRECT\n\nlong   a = 9999999999; // ERROR — exceeds int range without L\nlong   b = 9999999999L;// CORRECT\n\nchar   c = "A";    // ERROR — double quotes = String\nchar   d = \'A\';    // CORRECT',
  //   codeEditor: true,
  //   lang: 'java',
  // },
]
</script>

<Slide
  topic="Data Types"
  sub-topic="Type Literals and Special Notation"
  :contents="contents"
/>
