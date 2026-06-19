<script setup>
const contents = [
  // {
  //   label: 'Casting in arithmetic expressions',
  //   text: 'int a = 5, b = 2;\n\n// Without cast — integer division\nSystem.out.println(a / b);          // 2\n\n// With cast — floating-point division\nSystem.out.println((double) a / b); // 2.5',
  //   codeEditor: true,
  //   lang: 'java',
  // },
  // {
  //   label: 'Overflow & precision loss',
  //   text: 'long bigVal = 130L;\nbyte b = (byte) bigVal; // overflow!\nSystem.out.println(b);  // -126\n\ndouble pi = 3.14159;\nint truncated = (int) pi;\nSystem.out.println(truncated); // 3 (fraction lost)',
  //   codeEditor: true,
  //   lang: 'java',
  // },
  { text: '<b>Integer division</b> — both operands <code>int</code> → result is <code>int</code>; fraction discarded' },
  { text: '<b>Fix:</b> Cast one operand before dividing: <code>(double) a / b</code>' },
  { text: '<b>Overflow</b> — value exceeds target type range; bits wrap around unpredictably' },
  { text: '<b>Common mistake:</b> <code>(double)(a/b)</code> casts after division — fraction already lost. Always cast before.', highlight: true },
]
</script>

<Slide
  topic="Type Casting"
  sub-topic="Casting in Expressions & Overflow"
  :contents="contents"
/>
