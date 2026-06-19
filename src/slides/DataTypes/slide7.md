<script setup>
const contents = [
  { text: '<b>Primitive</b> — 8 fixed types built into Java | Stores value directly in memory (stack) | Cannot be null | Starts with lowercase (<code>int</code>, <code>char</code>)' },
  { text: '<b>Non-Primitive</b> — unlimited (any class) | Stores memory address (reference) in stack, object in heap | Can be null | Starts with uppercase (<code>String</code>, <code>Scanner</code>)' },
  { text: '<b>Memory:</b> Primitives are stored on the <b>stack</b>. Non-primitives store a reference on the stack and the actual object data on the <b>heap</b>.' },
  // {
  //   label: 'Primitives vs non-primitives in action',
  //   text: '// Primitive — copy of value is made\nint a = 10;\nint b = a;  // b gets a copy of a\'s value\nb = 20;\nSystem.out.println(a); // 10 — a is unchanged\n\n// Non-primitive — copy of reference is made\nint[] x = {1, 2, 3};\nint[] y = x;  // y points to the same array\ny[0] = 99;\nSystem.out.println(x[0]); // 99 — x is also changed!',
  //   codeEditor: true,
  //   lang: 'java',
  // },
  { text: '<b>Important:</b> Assigning one non-primitive variable to another makes both point to the same object. Changes through one variable affect the other.', highlight: true },
]
</script>

<Slide
  topic="Data Types"
  sub-topic="Primitive vs Non-Primitive — Key Differences"
  :contents="contents"
/>
