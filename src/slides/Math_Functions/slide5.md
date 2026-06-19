<script setup>
const contents = [
  { text: '<b>Math.random()</b> — returns a random <code>double</code> value in the range <code>[0.0, 1.0)</code> (includes 0.0, excludes 1.0). Result is different every time it is called.' },
  // {
  //   label: 'Generating random numbers in a custom range',
  //   text: '// Random double between 0.0 and 1.0\ndouble r = Math.random();\n\n// Random integer between 0 and 9 (inclusive)\nint r1 = (int)(Math.random() * 10);\n\n// Random integer between 1 and 10 (inclusive)\nint r2 = (int)(Math.random() * 10) + 1;\n\n// Random integer between min and max (inclusive)\n// Formula: (int)(Math.random() * (max - min + 1)) + min\nint min = 5, max = 15;\nint r3 = (int)(Math.random() * (max - min + 1)) + min;',
  //   codeEditor: true,
  //   lang: 'java',
  // },
  { text: '<b>Formula to remember:</b> <code>(int)(Math.random() * (max - min + 1)) + min</code>' },
  { text: '<b>Common uses:</b> dice roll, lottery number, random quiz question, shuffling' },
  // { text: '<b>Note:</b> For more control over randomness (seeding, nextInt, nextDouble), use the <code>Random</code> class from <code>java.util</code> instead.', highlight: true },
]
</script>

<Slide
  topic="Math Built-in Functions"
  sub-topic="Math.random()"
  :contents="contents"
/>
