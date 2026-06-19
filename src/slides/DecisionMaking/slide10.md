<script setup>
const contents = [
  // {
  //   label: 'Comparison & Logical operators in action',
  //   text: 'int x = 10;\n// Comparison operators\nSystem.out.println(x > 5);   // true\nSystem.out.println(x == 10); // true\nSystem.out.println(x != 3);  // true\n\n// Logical operators\nboolean a = true, b = false;\nSystem.out.println(a && b);  // false\nSystem.out.println(a || b);  // true\nSystem.out.println(!a);      // false',
  //   codeEditor: true,
  //   lang: 'java',
  // },
  { text: '<b>==</b> equal to &nbsp;&nbsp; <b>!=</b> not equal &nbsp;&nbsp; <b>&gt;</b> greater &nbsp;&nbsp; <b>&lt;</b> less &nbsp;&nbsp; <b>&gt;=</b> greater or equal &nbsp;&nbsp; <b>&lt;=</b> less or equal' },
  { text: '<b>&&</b> (AND) — true only if <i>both</i> conditions are true' },
  { text: '<b>||</b> (OR) — true if <i>at least one</i> condition is true' },
  { text: '<b>!</b> (NOT) — inverts the boolean value: <code>!true</code> → <code>false</code>' },
  { text: '<b>Short-circuit evaluation:</b> In <code>&&</code>, if the left side is false, the right side is never evaluated. In <code>||</code>, if the left is true, the right is skipped.', highlight: true },
]
</script>

<Slide
  topic="Decision Making"
  sub-topic="Comparison & Logical Operators"
  :contents="contents"
/>
