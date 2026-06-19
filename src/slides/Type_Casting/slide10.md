<script setup>
const contents = [
  { text: '<b>Problem:</b> A student scored 7 marks out of 3 tests. Calculate the average. The program currently gives a wrong answer due to integer division — fix it using type casting.' },
  // {
  //   label: 'Buggy code',
  //   text: 'int totalMarks = 7;\nint tests      = 3;\ndouble average = totalMarks / tests; // BUG\nSystem.out.println("Average: " + average); // prints 2.0 (wrong)',
  //   codeEditor: true,
  //   lang: 'java',
  // },
  { text: '<b>Expected Output:</b><br><code>Average: 2.3333333333333335</code>' },
  { text: '<b>Note:</b> <code>7 / 3</code> performs integer division giving <code>2</code>, which is then widened to <code>2.0</code>. The division must happen as a decimal operation.' },
  // { text: '<b>Hint:</b> Cast one of the operands to <code>double</code> before the division: <code>(double) totalMarks / tests</code>. The division now produces a decimal result.', highlight: true },
]
</script>

<Slide
  topic="Type Casting"
  sub-topic="Practice Problem 2 — Fix Integer Division"
  :contents="contents"
/>
