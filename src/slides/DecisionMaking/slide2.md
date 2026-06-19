<script setup>
const contents = [
  // {
  //   label: 'if-else if-else ladder',
  //   text: 'int marks = 75;\nif (marks >= 90) {\n    System.out.println("Grade: A");\n} else if (marks >= 75) {\n    System.out.println("Grade: B");\n} else if (marks >= 60) {\n    System.out.println("Grade: C");\n} else {\n    System.out.println("Grade: F");\n}',
  //   codeEditor: true,
  //   lang: 'java',
  // },
  { text: '<b>else if</b> — chains multiple conditions; checked top to bottom' },
  { text: '<b>Only one block executes</b> — the first condition that is <code>true</code> wins; the rest are skipped' },
  { text: '<b>Final else</b> — optional catch-all block when no condition matches' },
  { text: '<b>Order matters:</b> Place the most specific (narrowest) conditions first to avoid incorrect results.', highlight: true },
]
</script>

<Slide
  topic="Decision Making"
  sub-topic="if-else if-else Ladder"
  :contents="contents"
/>
