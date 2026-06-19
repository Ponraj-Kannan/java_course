<script setup>
const contents = [
  {
    label: 'Syntax',
    text: 'initialization\ndo {\n    // body\n    update\n} while (condition);',
    codeEditor: true,
    lang: 'java',
  },
  // {
  //   label: 'Example — print 1 to 5',
  //   text: 'int i = 1;\ndo {\n    System.out.println(i);\n    i++;\n} while (i <= 5);',
  //   codeEditor: true,
  //   lang: 'java',
  // },
  { text: '<b>Initialization</b> — declared outside the loop before the <code>do</code> keyword' },
  { text: '<b>Body executes first</b> — the loop body always runs at least once, regardless of the condition' },
  { text: '<b>Condition</b> — checked after each iteration.' },
  { text: '<b>Use a do-while loop</b> when the body must execute at least once — such as menu-driven programs or input validation.', highlight: true },
]
</script>

<Slide
  topic="Looping Statements"
  sub-topic="Do-While Loop"
  :contents="contents"
/>
