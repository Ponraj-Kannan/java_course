<script setup>
const contents = [
  {
    label: 'Syntax',
    text: 'for (initialization; condition; update) {\n    // body\n}',
    codeEditor: true,
    lang: 'java',
  },
  // {
  //   label: 'Example — print 1 to 5',
  //   text: 'for (int i = 1; i <= 5; i++) {\n    System.out.println(i);\n}',
  //   codeEditor: true,
  //   lang: 'java',
  // },
  { text: '<b>Initialization</b> — declares and sets the loop variable before the loop starts.' },
  { text: '<b>Condition</b> — checked before every iteration; loop runs only while this is true.' },
  { text: '<b>Update</b> — executes after every iteration to change the loop variable.' },
  { text: '<b>Use a for loop</b> when the number of iterations is known in advance.', highlight: true },
]
</script>

<Slide
  topic="Looping Statements"
  sub-topic="For Loop"
  :contents="contents"
/>
