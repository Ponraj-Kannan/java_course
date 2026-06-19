<script setup>
const contents = [
  // {
  //   label: 'Fall-through in switch',
  //   text: 'int month = 2;\nswitch (month) {\n    case 1:\n    case 3:\n    case 5:\n        System.out.println("31 days");\n        break;\n    case 2:\n        System.out.println("28 or 29 days");\n        break;\n    default:\n        System.out.println("Other month");\n}',
  //   codeEditor: true,
  //   lang: 'java',
  // },
  // {
  //   label: 'Ternary operator',
  //   text: 'int a = 10, b = 20;\nint max = (a > b) ? a : b;\nSystem.out.println("Max: " + max);',
  //   codeEditor: true,
  //   lang: 'java',
  // },
  { text: '<b>Fall-through</b> — when multiple cases share the same action, stack them without a <code>break</code>' },
  { text: '<b>Ternary operator</b> — a compact one-liner for simple if-else: <code>condition ? valueIfTrue : valueIfFalse</code>' },
  { text: '<b>Ternary vs if-else:</b> Use ternary only for simple value assignments — avoid nesting ternaries as they hurt readability.', highlight: true },
]
</script>

<Slide
  topic="Decision Making"
  sub-topic="Fall-through & Ternary Operator"
  :contents="contents"
/>
