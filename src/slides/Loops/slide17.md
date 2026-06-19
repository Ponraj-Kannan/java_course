<script setup>
const contents = [
  // {
  //   label: 'Example — skip even numbers, print only odd numbers',
  //   text: 'for (int i = 1; i <= 10; i++) {\n    if (i % 2 == 0) {\n        continue; // skips the rest of this iteration\n    }\n    System.out.println(i);\n}\n// Output: 1 3 5 7 9',
  //   codeEditor: true,
  //   lang: 'java',
  // },
  { text: '<b>continue</b> — skips the remaining statements in the current iteration and moves to the next iteration' },
  { text: 'The loop does <b>not</b> exit — only the current iteration is skipped' },
  { text: 'In a <b>for</b> loop, the update expression (<code>i++</code>) still executes after <code>continue</code>' },
  { text: '<b>break vs continue:</b> <code>break</code> exits the loop entirely. <code>continue</code> skips to the next iteration.', highlight: true },
]
</script>

<Slide
  topic="Looping Statements"
  sub-topic="Continue Statement"
  :contents="contents"
/>
