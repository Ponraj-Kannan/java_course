<script setup>
const contents = [
  { text: '<b>Math.sin(radians)</b> — returns the sine of an angle given in radians' },
  { text: '<b>Math.cos(radians)</b> — returns the cosine of an angle given in radians' },
  { text: '<b>Math.tan(radians)</b> — returns the tangent of an angle given in radians' },
  { text: '<b>Math.toRadians(degrees)</b> — converts degrees to radians. Use this before passing to sin/cos/tan.' },
  { text: '<b>Math.toDegrees(radians)</b> — converts radians to degrees.' },
  // {
  //   label: 'Examples',
  //   text: '// Convert degrees to radians first\ndouble angle = Math.toRadians(90);\n\nSystem.out.println(Math.sin(angle));  // 1.0\nSystem.out.println(Math.cos(angle));  // ~0.0 (very small floating point)\nSystem.out.println(Math.tan(Math.toRadians(45))); // 1.0\n\n// Convert back\nSystem.out.println(Math.toDegrees(Math.PI)); // 180.0',
  //   codeEditor: true,
  //   lang: 'java',
  // },
  { text: '<b>Important:</b> Java trig functions take angles in <b>radians</b>, not degrees. Always convert using <code>Math.toRadians()</code> first.', highlight: true },
]
</script>

<Slide
  topic="Math Built-in Functions"
  sub-topic="Trigonometry Methods"
  :contents="contents"
/>
