<script setup>
const contents = [
  // { text: '<b>Implicit casting</b> (also called <b>widening conversion</b>) — Java automatically converts a smaller data type to a larger one. No syntax required. No data is lost.' },
  { text: '<b>Widening chain:</b> <code>byte → short → int → long → float → double</code>' },
  // {
  //   label: 'Implicit casting examples',
  //   text: 'byte   b = 42;\nshort  s = b;    // byte → short\nint    i = s;    // short → int\nlong   l = i;    // int → long\nfloat  f = l;    // long → float\ndouble d = f;    // float → double\n\nSystem.out.println(d); // 42.0\n\n// Implicit casting in expressions\nint    x = 5;\ndouble y = 2.0;\ndouble result = x + y; // x is promoted to double\nSystem.out.println(result); // 7.0',
  //   codeEditor: true,
  //   lang: 'java',
  // },
  // { text: '<b>In expressions:</b> When an <code>int</code> and a <code>double</code> are used together, Java automatically promotes the <code>int</code> to <code>double</code> before computing the result.' },
  // { text: '<b>Note:</b> <code>int / int</code> gives integer division (e.g., <code>5 / 2 = 2</code>). To get a decimal result, at least one operand must be a <code>double</code>.', highlight: true },
]
</script>

<Slide
  topic="Type Casting"
  sub-topic="Implicit (Widening) Casting"
  :contents="contents"
/>
