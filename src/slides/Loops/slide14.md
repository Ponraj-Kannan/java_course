<script setup>
const contents = [
  { text: '<b>Problem:</b> Display the following number grid pattern using a nested loop.' },
  {
    label: 'Expected Output',
    text: '1 2 3\n4 5 6\n7 8 9',
    codeEditor: true,
    lang: 'java',
  },
  { text: '<b>Note:</b> Use a nested <b>for</b> loop. The outer loop controls the rows and the inner loop controls the columns.' },
  // { text: '<b>Hint:</b> Declare a variable <code>num = 1</code> before both loops. Inside the inner loop, print <code>num</code> and increment it. Use <code>System.out.println()</code> after the inner loop to move to the next row.', highlight: true },
]
</script>

<Slide
  topic="Looping Statements"
  sub-topic="Nested Loops — Practice Problem 1"
  :contents="contents"
/>
