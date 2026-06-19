<script setup>
const contents = [
  { text: '<b>Declaration</b> — tells the compiler the variable\'s name and data type. Memory is reserved but no value is assigned yet.' },
  { text: '<b>Initialization</b> — assigns a value to the declared variable for the first time.' },
  { text: '<b>Declaration + Initialization</b> — both can be done together in a single statement.' },
  // {
  //   label: 'Declaration, Initialization, and combined',
  //   text: '// Declaration only\nint marks;\n\n// Initialization (after declaration)\nmarks = 95;\n\n// Declaration + Initialization (most common)\nint marks = 95;\n\n// Multiple variables of the same type\nint a = 10, b = 20, c = 30;\n\n// Re-assignment (changing the value)\nmarks = 80; // value updated from 95 to 80',
  //   codeEditor: true,
  //   lang: 'java',
  // },
  { text: '<b>Note:</b> A variable must be declared before it can be used. Using an uninitialized local variable causes a compile-time error in Java.', highlight: true },
]
</script>

<Slide
  topic="Variables"
  sub-topic="Declaration and Initialization"
  :contents="contents"
/>
