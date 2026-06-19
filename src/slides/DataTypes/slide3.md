<script setup>
const contents = [
  { text: '<b>Floating-point types</b> — store numbers with a decimal point. Java provides two levels of precision.' },
  { text: '<b>float</b> — 4 bytes (32 bits) | Precision: ~6–7 decimal digits | Append <code>f</code> or <code>F</code> to the literal (e.g., <code>3.14f</code>)' },
  { text: '<b>double</b> — 8 bytes (64 bits) | Precision: ~15–16 decimal digits | Default type for decimal numbers in Java. No suffix needed.' },
  // {
  //   label: 'Examples',
  //   text: 'float  pi      = 3.14f;\nfloat  tax     = 18.5f;\n\ndouble precise = 3.141592653589793;\ndouble salary  = 75000.50;\n\n// float vs double precision\nfloat  f = 1.0f / 3.0f;\ndouble d = 1.0  / 3.0;\nSystem.out.println(f); // 0.33333334  (less precise)\nSystem.out.println(d); // 0.3333333333333333',
  //   codeEditor: true,
  //   lang: 'java',
  // },
  // { text: '<b>Default choice:</b> Always use <code>double</code> for decimal numbers. Use <code>float</code> only when memory is limited and lower precision is acceptable.', highlight: true },
  { text: '<b>Note:</b> Never use floating-point types for currency calculations — rounding errors can occur. Use <code>BigDecimal</code> instead for financial data.', highlight: true },
]
</script>

<Slide
  topic="Data Types"
  sub-topic="Primitive Types — Floating-Point (float, double)"
  :contents="contents"
/>
