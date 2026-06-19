<script setup>
const contents = [
  // {
  //   label: 'Nested if statement',
  //   text: 'int age = 20;\nboolean hasID = true;\n\nif (age >= 18) {\n    if (hasID) {\n        System.out.println("Access granted");\n    } else {\n        System.out.println("ID required");\n    }\n} else {\n    System.out.println("Underage");\n}',
  //   codeEditor: true,
  //   lang: 'java',
  // },
  { text: '<b>Nested if</b> — an <code>if</code> statement placed inside another <code>if</code> or <code>else</code> block' },
  { text: '<b>Use case</b> — when a second condition only makes sense after a first condition is already true' },
  { text: '<b>Each if</b> has its own independent condition and block' },
  { text: '<b>Tip:</b> Avoid deeply nested ifs — prefer logical operators (<code>&&</code>, <code>||</code>) to flatten conditions when possible.', highlight: true },
]
</script>

<Slide
  topic="Decision Making"
  sub-topic="Nested if Statements"
  :contents="contents"
/>
