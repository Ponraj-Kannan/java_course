<script setup>
const contents = [
  { text: '<b>Logarithm:</b> <code>Math.log(n)</code> — natural log | <code>Math.log10(n)</code> — log base 10' },
  { text: '<b>Trigonometry:</b> <code>Math.sin(r)</code> | <code>Math.cos(r)</code> | <code>Math.tan(r)</code> | <code>Math.toRadians(d)</code> | <code>Math.toDegrees(r)</code>' },
  { text: '<b>Constants:</b> <code>Math.PI</code> = 3.14159... | <code>Math.E</code> = 2.71828...' },
  { text: '<b>All methods are static</b> — call them as <code>Math.methodName()</code> without creating a Math object. No import needed.', highlight: true },
]
</script>

<Slide
  topic="Math Built-in Functions"
  sub-topic="Quick Reference"
  :contents="contents"
/>
