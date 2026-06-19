<script setup>
const contents = [
  {
    label: 'Syntax',
    text: 'initialization\nwhile (condition) {\n    // body\n    update\n}',
    codeEditor: true,
    lang: 'java',
  },
  // {
  //   label: 'Example — print 1 to 5',
  //   text: 'int i = 1;\nwhile (i <= 5) {\n    System.out.println(i);\n    i++;\n}',
  //   codeEditor: true,
  //   lang: 'java',
  // },
  { text: '<b>Initialization</b> — declared outside the loop before the <code>while</code> keyword.' },
  { text: '<b>Condition</b> — checked before every iteration; loop runs only while this is true.' },
  { text: '<b>Update</b> — must be written inside the loop body; forgetting it causes an infinite loop' },
  { text: '<b>Use a while loop</b> when the number of iterations is not known in advance — it depends on a condition.', highlight: true },
]
</script>

<Slide
  topic="Looping Statements"
  sub-topic="While Loop"
  :contents="contents"
/>
