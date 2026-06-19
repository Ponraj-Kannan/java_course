<script setup>
const contents = [
  { text: '<b>Power and Root:</b> <code>Math.pow(a,b)</code> — a^b | <code>Math.sqrt(n)</code> — square root | <code>Math.cbrt(n)</code> — cube root | <code>Math.exp(n)</code> — e^n' },
  { text: '<b>Rounding:</b> <code>Math.round(n)</code> — nearest integer | <code>Math.ceil(n)</code> — round up | <code>Math.floor(n)</code> — round down' },
  { text: '<b>Min / Max / Abs:</b> <code>Math.min(a,b)</code> — smaller | <code>Math.max(a,b)</code> — larger | <code>Math.abs(n)</code> — remove sign' },
  { text: '<b>Random:</b> <code>Math.random()</code> — double in [0.0, 1.0)' }
]
</script>

<Slide
  topic="Math Built-in Functions"
  sub-topic="Quick Reference"
  :contents="contents"
/>
