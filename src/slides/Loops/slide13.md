<script setup>
const contents = [
  {
    label: 'Syntax',
    text: 'for (int i = 0; i < outer; i++) {\n    for (int j = 0; j < inner; j++) {\n        // body\n    }\n}',
    codeEditor: true,
    lang: 'java',
  },
  // {
  //   label: 'Example — print a 3x3 grid of numbers',
  //   text: 'for (int i = 1; i <= 3; i++) {\n    for (int j = 1; j <= 3; j++) {\n        System.out.print(j + " ");\n    }\n    System.out.println();\n}',
  //   codeEditor: true,
  //   lang: 'java',
  // },
  { text: '<b>Outer loop</b> — controls the number of rows' },
  { text: '<b>Inner loop</b> — controls the number of columns; runs completely for every single outer iteration' },
  { text: '<b>Total iterations</b> = outer count x inner count (e.g., 3 x 3 = 9 iterations)' },
  { text: '<b>Common uses:</b> printing patterns, working with 2D arrays, matrix operations', highlight: true },
]
</script>

<Slide
  topic="Looping Statements"
  sub-topic="Nested Loops"
  :contents="contents"
/>
