<script setup>
const contents = [
  // {
  //   label: 'if statement',
  //   text: 'int age = 18;\nif (age >= 18) {\n    System.out.println("Eligible to vote");\n}',
  //   codeEditor: true,
  //   lang: 'java',
  // },
  // {
  //   label: 'if-else statement',
  //   text: 'int age = 15;\nif (age >= 18) {\n    System.out.println("Eligible to vote");\n} else {\n    System.out.println("Not eligible");\n}',
  //   codeEditor: true,
  //   lang: 'java',
  // },
  { text: '<b>if</b> — executes the block only when the condition is <code>true</code>' },
  { text: '<b>else</b> — executes when the <code>if</code> condition is <code>false</code>' },
  { text: '<b>Condition</b> — must be a boolean expression (evaluates to <code>true</code> or <code>false</code>)' },
  { text: '<b>Note:</b> Curly braces <code>{}</code> are optional for a single statement, but always using them is a good practice.', highlight: true },
]
</script>

<Slide
  topic="Decision Making"
  sub-topic="if and if-else Statements"
  :contents="contents"
/>
