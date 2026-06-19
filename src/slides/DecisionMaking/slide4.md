<script setup>
const contents = [
  // {
  //   label: 'switch statement',
  //   text: 'int day = 3;\nswitch (day) {\n    case 1:\n        System.out.println("Monday");\n        break;\n    case 2:\n        System.out.println("Tuesday");\n        break;\n    case 3:\n        System.out.println("Wednesday");\n        break;\n    default:\n        System.out.println("Other day");\n}',
  //   codeEditor: true,
  //   lang: 'java',
  // },
  { text: '<b>switch</b> — matches the value of a variable against multiple <code>case</code> labels' },
  { text: '<b>case</b> — defines a value to match; executes its block if matched' },
  { text: '<b>break</b> — exits the switch; without it, execution falls through to the next case' },
  { text: '<b>default</b> — optional; runs when no case matches (like the final <code>else</code>)' },
  { text: '<b>Works with:</b> <code>int</code>, <code>char</code>, <code>String</code>, and <code>enum</code> types only — not <code>float</code> or <code>double</code>.', highlight: true },
]
</script>

<Slide
  topic="Decision Making"
  sub-topic="switch Statement"
  :contents="contents"
/>
