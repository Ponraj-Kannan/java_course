<script setup>
const contents = [
  { text: '<b>Data Type</b> — defines what kind of value a variable can hold, how much memory it uses, and what operations can be performed on it' },
  // { text: 'Java is a <b>statically typed</b> language — every variable must have its type declared before use and the type cannot change after declaration' },
  { text: '<b>Two categories of data types in Java:</b><br><b>1. Primitive</b> — built-in types that store simple values directly in memory (8 types)<br><b>2. Non-Primitive (Reference)</b> — store the memory address of an object, not the value itself' },
  // {
  //   label: 'Example — declaring variables of different types',
  //   text: '// Primitive types\nint age      = 20;\ndouble price = 99.99;\nchar grade   = \'A\';\nboolean pass = true;\n\n// Non-primitive types\nString name  = "Alice";\nint[] scores = {90, 85, 78};',
  //   codeEditor: true,
  //   lang: 'java',
  // },
  // { text: '<b>Why data types matter:</b> They control memory allocation, valid value ranges, numeric precision, and the operations that can be performed on a variable.', highlight: true },
]
</script>

<Slide
  topic="Data Types"
  sub-topic="Introduction"
  :contents="contents"
/>
