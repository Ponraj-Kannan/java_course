<script setup>
const contents = [
  { text: '<b>Type Casting</b> — converting a value from one data type to another.' },
  { text: '<b>Two types of casting in Java:</b><br><b>1. Implicit (Widening)</b> — done automatically by Java. Converts a smaller type to a larger type. No data loss.<br><b>2. Explicit (Narrowing)</b> — done manually by the programmer. Converts a larger type to a smaller type. Possible data loss.' },
  // { text: '<b>Widening order (automatic, safe):</b><br><code>byte → short → int → long → float → double</code>' },
  // {
  //   label: 'Quick overview of both types',
  //   text: '// Implicit — automatic, no syntax needed\nint    a = 100;\ndouble b = a;       // int promoted to double\nSystem.out.println(b); // 100.0\n\n// Explicit — programmer writes the cast in parentheses\ndouble x = 9.99;\nint    y = (int) x; // double narrowed to int\nSystem.out.println(y); // 9  (decimal part is truncated)',
  //   codeEditor: true,
  //   lang: 'java',
  // },
  // { text: '<b>Key rule:</b> Widening is always safe. Narrowing may lose data — the programmer takes responsibility by writing the cast explicitly.', highlight: true },
]
</script>

<Slide
  topic="Type Casting"
  sub-topic="Introduction"
  :contents="contents"
/>
