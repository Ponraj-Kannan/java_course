<script setup>
const contents = [
  { text: '<b>byte</b> — 1 byte | Range: -128 to 127 | Default: 0' },
  { text: '<b>short</b> — 2 bytes | Range: -32,768 to 32,767 | Default: 0' },
  { text: '<b>int</b> — 4 bytes | Range: -2.1 billion to 2.1 billion | Default: 0' },
  { text: '<b>long</b> — 8 bytes | Range: -9.2 x 10^18 to 9.2 x 10^18 | Default: 0L' },
  { text: '<b>float</b> — 4 bytes | Precision: ~7 decimal digits | Default: 0.0f' },
  { text: '<b>double</b> — 8 bytes | Precision: ~15 decimal digits | Default: 0.0d' },
  { text: '<b>char</b> — 2 bytes | Range: \'\\u0000\' to \'\\uffff\' (0 to 65,535) | Default: \'\\u0000\'' },
  { text: '<b>boolean</b> — 1 bit | Values: true / false | Default: false' },
  { text: '<b>Most commonly used:</b> <code>int</code> for whole numbers, <code>double</code> for decimals, <code>char</code> for characters, <code>boolean</code> for conditions.', highlight: true },
]
</script>

<Slide
  topic="Data Types"
  sub-topic="All 8 Primitive Types — Quick Reference"
  :contents="contents"
/>
