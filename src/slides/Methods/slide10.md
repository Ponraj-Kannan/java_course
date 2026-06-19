<script setup>
const contents = [
  // {
  //   label: 'No import needed — Math is in java.lang',
  //   text: 'Math.abs(-7)          // 7      — absolute value\nMath.max(4, 9)        // 9      — larger of two values\nMath.min(4, 9)        // 4      — smaller of two values\nMath.pow(2, 10)       // 1024.0 — 2 raised to the power 10\nMath.sqrt(49)         // 7.0    — square root\nMath.floor(3.9)       // 3.0    — round down\nMath.ceil(3.1)        // 4.0    — round up\nMath.round(3.5)       // 4      — round to nearest int\nMath.random()         // [0.0, 1.0) — random double',
  //   codeEditor: true,
  //   lang: 'java',
  // },
  // {
  //   label: 'Generating a random integer in a range',
  //   text: '// Random int between min (inclusive) and max (inclusive)\nint min = 1, max = 6;\nint roll = (int)(Math.random() * (max - min + 1)) + min;',
  //   codeEditor: true,
  //   lang: 'java',
  // },
  { text: '<b>Math.pow(a, b)</b> returns a <code>double</code> — cast to <code>int</code> if an integer result is needed' },
  { text: '<b>Math.random()</b> returns a <code>double</code> in the range [0.0, 1.0) — multiply and cast to get integers' },
  { text: '<b>Math.abs()</b> is overloaded — works with int, long, float, and double' },
  { text: '<b>Note:</b> All Math methods are static — call them directly as <code>Math.methodName()</code> without creating an object.', highlight: true },
]
</script>

<Slide
  topic="Methods"
  sub-topic="Built-in Methods — java.lang.Math"
  :contents="contents"
/>
