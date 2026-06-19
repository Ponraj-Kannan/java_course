<script setup>
const contents = [
  { text: '<b>Math.round(n)</b> — rounds to the nearest integer. Returns <code>long</code> for <code>double</code> input, <code>int</code> for <code>float</code>.' },
  { text: '<b>Math.ceil(n)</b> — rounds up to the nearest integer (ceiling). Always returns a <code>double</code>.' },
  { text: '<b>Math.floor(n)</b> — rounds down to the nearest integer (floor). Always returns a <code>double</code>.' },
  // {
  //   label: 'Examples',
  //   text: 'System.out.println(Math.round(4.4));  // 4\nSystem.out.println(Math.round(4.5));  // 5\nSystem.out.println(Math.round(4.6));  // 5\n\nSystem.out.println(Math.ceil(4.1));   // 5.0\nSystem.out.println(Math.ceil(4.9));   // 5.0\nSystem.out.println(Math.ceil(-4.1));  // -4.0\n\nSystem.out.println(Math.floor(4.9));  // 4.0\nSystem.out.println(Math.floor(-4.1)); // -5.0',
  //   codeEditor: true,
  //   lang: 'java',
  // },
  { text: '<b>Memory tip:</b> ceil = ceiling = go UP | floor = go DOWN | round = go to the NEAREST', highlight: true },
]
</script>

<Slide
  topic="Math Built-in Functions"
  sub-topic="Rounding Methods"
  :contents="contents"
/>
