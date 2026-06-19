<script setup>
const contents = [
  { text: '<b>Default values</b> — Java automatically assigns default values to instance and static variables if they are not initialized. Local variables do NOT get default values.' },
  { text: '<b>byte, short, int, long</b> — default: <code>0</code>' },
  { text: '<b>float, double</b> — default: <code>0.0</code>' },
  { text: '<b>char</b> — default: <code>\'\\u0000\'</code> (null character)' },
  { text: '<b>boolean</b> — default: <code>false</code>' },
  { text: '<b>All non-primitive types (String, Array, Object)</b> — default: <code>null</code>' },
  // {
  //   label: 'Local variable — must initialize before use',
  //   text: 'public static void main(String[] args) {\n    int x;                   // declared but not initialized\n    System.out.println(x);   // COMPILE ERROR\n                             // local variables have no default\n\n    int y = 0;               // explicitly initialized\n    System.out.println(y);   // OK — prints 0\n}',
  //   codeEditor: true,
  //   lang: 'java',
  // },
  { text: '<b>Rule:</b> Always initialize local variables before using them. Relying on default values is only valid for instance and static variables.', highlight: true },
]
</script>

<Slide
  topic="Data Types"
  sub-topic="Default Values"
  :contents="contents"
/>
