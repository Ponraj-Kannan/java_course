<script setup>
const contents = [
  { text: '<b>Integer types</b> — store whole numbers (no decimal point). Java provides four sizes to balance memory usage and range.' },
  { text: '<b>byte</b> — 1 byte (8 bits) | Range: -128 to 127 | Use: small counters, raw binary data' },
  { text: '<b>short</b> — 2 bytes (16 bits) | Range: -32,768 to 32,767 | Use: memory-constrained environments' },
  { text: '<b>int</b> — 4 bytes (32 bits) | Range: -2,147,483,648 to 2,147,483,647 | Use: default choice for whole numbers' },
  { text: '<b>long</b> — 8 bytes (64 bits) | Range: -9.2 x 10^18 to 9.2 x 10^18 | Use: very large numbers (population, file sizes). Append <code>L</code> to the literal.' },
  // {
  //   label: 'Examples',
  //   text: 'byte  level    = 100;\nshort year     = 2024;\nint   marks    = 95;\nlong  distance = 9460730472580800L; // light year in metres\n\nSystem.out.println(Integer.MAX_VALUE); // 2147483647\nSystem.out.println(Long.MAX_VALUE);    // 9223372036854775807',
  //   codeEditor: true,
  //   lang: 'java',
  // },
  // { text: '<b>Default choice:</b> Always use <code>int</code> for whole numbers unless the value exceeds its range, then use <code>long</code>.', highlight: true },
]
</script>

<Slide
  topic="Data Types"
  sub-topic="Primitive Types — Integer (byte, short, int, long)"
  :contents="contents"
/>
