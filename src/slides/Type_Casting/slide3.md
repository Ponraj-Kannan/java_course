<script setup>
const contents = [
  { text: '<b>Narrowing chain:</b> <code>double → float → long → int → short → byte</code>' },
  { text: '<b>Syntax:</b> <code>(targetType) value</code>' },
  // { text: '<b>Risks of narrowing:</b><br>Decimal part is <b>truncated</b> (cut off, not rounded) when converting from <code>double</code> to <code>int</code><br>Value may <b>overflow</b> if it exceeds the range of the target type' },
  // {
  //   label: 'Explicit casting examples',
  //   text: '// double → int  (decimal is truncated)\ndouble price = 19.99;\nint    cost  = (int) price;\nSystem.out.println(cost);  // 19  (not 20)\n\n// long → int\nlong bigNum = 1234567890L;\nint  small  = (int) bigNum;\nSystem.out.println(small); // 1234567890 (fits, no loss)\n\n// double → byte  (overflow)\ndouble d = 300.75;\nbyte   bt = (byte) d;\nSystem.out.println(bt); // 44  (overflow — 300 mod 256)',
  //   codeEditor: true,
  //   lang: 'java',
  // },
  { text: '<b>Remember:</b> Explicit casting <b>truncates</b>, it does not round. <code>(int) 9.9</code> gives <code>9</code>, not <code>10</code>. Use <code>Math.round()</code> if rounding is needed.', highlight: true },
]
</script>

<Slide
  topic="Type Casting"
  sub-topic="Explicit (Narrowing) Casting"
  :contents="contents"
/>
