<script setup>
const contents = [
  // {
  //   label: 'Widening (Implicit) Conversion',
  //   text: 'int i = 100;\nlong l = i;      // int → long (automatic)\ndouble d = l;   // long → double (automatic)\nSystem.out.println(d); // 100.0',
  //   codeEditor: true,
  //   lang: 'java',
  // },
  // {
  //   label: 'Narrowing (Explicit) Conversion',
  //   text: 'double d = 9.99;\nint i = (int) d;   // double → int (manual cast)\nSystem.out.println(i); // 9  (decimal part is truncated)',
  //   codeEditor: true,
  //   lang: 'java',
  // },
  { text: '<b>Widening</b> — smaller type is automatically converted to a larger type. No data loss.' },
  { text: '<b>Narrowing</b> — larger type is manually cast to a smaller type using <code>(type)</code> syntax. May lose data.' },
  // { text: '<b>Widening order:</b> byte → short → int → long → float → double' },
  { text: '<b>Note:</b> Narrowing never happens automatically — you must write the cast explicitly, or the code will not compile.', highlight: true },
]
</script>

<Slide
  topic="Type Casting"
  sub-topic="Widening & Narrowing Conversion"
  :contents="contents"
/>
