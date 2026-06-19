<script setup>
const contents = [
  // { text: '<b>Non-primitive types</b> (also called Reference types) — store the memory address of an object, not the value itself. Created using classes.' },
  { text: '<b>String</b> — stores a sequence of characters. Most commonly used non-primitive type. Enclosed in double quotes.' },
  { text: '<b>Arrays</b> — stores multiple values of the same type in a single variable.' },
  { text: '<b>Classes</b> — user-defined types (e.g., <code>Scanner</code>, <code>ArrayList</code>, or your own classes).' },
  // {
  //   label: 'Examples of non-primitive types',
  //   text: '// String\nString name    = "Alice";\nString city    = "Chennai";\n\n// Array\nint[]    marks = {85, 90, 78};\nString[] days  = {"Mon", "Tue", "Wed"};\n\n// Class (Scanner is a non-primitive type)\nimport java.util.Scanner;\nScanner sc = new Scanner(System.in);',
  //   codeEditor: true,
  //   lang: 'java',
  // },
  { text: '<b>Key difference from primitives:</b> Non-primitive variables can be <code>null</code> (meaning they point to nothing). Primitives always hold a value and can never be null.', highlight: true },
]
</script>

<Slide
  topic="Data Types"
  sub-topic="Non-Primitive (Reference) Types"
  :contents="contents"
/>
