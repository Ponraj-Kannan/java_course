<script setup>
const contents = [
  { text: '<b>Scenario 1 — Integer Division Trap:</b> Dividing two integers always gives an integer result, even if the answer has a decimal.' },
  { text: '<b>Scenario 2 — Correct Average Calculation:</b> Cast one operand to <code>double</code> to get a decimal result from integer division.' },
  { text: '<b>Scenario 3 — Truncation vs Rounding:</b> Explicit cast truncates. Use <code>Math.round()</code> for rounding.' },
  // {
  //   label: 'All three scenarios',
  //   text: '// Scenario 1 — wrong average\nint sum   = 7;\nint count = 2;\nSystem.out.println(sum / count);          // 3  (wrong)\n\n// Scenario 2 — correct average\nSystem.out.println((double) sum / count); // 3.5 (correct)\n\n// Scenario 3 — truncation vs rounding\ndouble d = 7.9;\nSystem.out.println((int) d);              // 7  (truncated)\nSystem.out.println(Math.round(d));        // 8  (rounded)',
  //   codeEditor: true,
  //   lang: 'java',
  // },
  { text: '<b>Scenario 4 — Mixing String and number:</b> Use <code>Integer.parseInt()</code> or <code>Double.parseDouble()</code> to convert a String to a number. This is <b>parsing</b>, not casting.' },
  // {
  //   label: 'Parsing strings to numbers',
  //   text: 'String s   = "42";\nint    num = Integer.parseInt(s);    // 42\ndouble d2  = Double.parseDouble("3.14"); // 3.14',
  //   codeEditor: true,
  //   lang: 'java',
  // },
]
</script>

<Slide
  topic="Type Casting"
  sub-topic="Common Scenarios and Pitfalls"
  :contents="contents"
/>
