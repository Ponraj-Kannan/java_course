<script setup>
const contents = [
  // {
  //   label: 'Example — stop the loop when i equals 5',
  //   text: 'for (int i = 1; i <= 10; i++) {\n    if (i == 5) {\n        break; // exits the loop immediately\n    }\n    System.out.println(i);\n}\n// Output: 1 2 3 4',
  //   codeEditor: true,
  //   lang: 'java',
  // },
  { text: '<b>break</b> — immediately exits the nearest enclosing loop or switch block' },
  { text: 'Execution continues with the first statement after the loop' },
  { text: 'In a <b>nested loop</b>, <code>break</code> only exits the innermost loop it is placed in' },
  { text: '<b>Common uses:</b> stopping a search once a result is found, exiting a menu loop on user request', highlight: true },
]
</script>

<Slide
  topic="Looping Statements"
  sub-topic="Break Statement"
  :contents="contents"
/>
