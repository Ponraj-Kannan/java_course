<script setup>
const contents = [
  { text: '<b>Variable</b> — a named memory location that stores a value which can be used and changed during program execution' },
  { text: 'Think of a variable as a labelled box: the label is the variable name, and the content inside is the value' },
  { text: 'Every variable in Java has three properties:<br><b>Name</b> — the identifier used to access it<br><b>Type</b> — the kind of data it holds (e.g., <code>int</code>, <code>String</code>)<br><b>Value</b> — the actual data stored in it' },
  // {
  //   label: 'Example',
  //   text: 'int age = 20;       // name: age | type: int | value: 20\nString name = "Alice"; // name: name | type: String | value: "Alice"\ndouble gpa = 8.5;   // name: gpa | type: double | value: 8.5',
  //   codeEditor: true,
  //   lang: 'java',
  // },
  { text: '<b>Why use variables?</b> To store input, hold intermediate results, avoid repetition, and make programs flexible and readable.', highlight: true },
]
</script>

<Slide
  topic="Variables"
  sub-topic="Introduction"
  :contents="contents"
/>
