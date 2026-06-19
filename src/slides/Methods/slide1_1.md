<script setup>
const contents = [
  // {
  //   label: 'Basic method syntax',
  //   text: 'accessModifier returnType methodName(parameterType paramName, ...) {\n    // method body\n    return value; // if returnType is not void\n}',
  //   codeEditor: true,
  //   lang: 'java',
  // },
  { text: '<b>Access Modifiers</b> — accessibility level for methods and instance variables.'
  },
  { text: '<b>Return Type</b> — data type of the method returns <code>Primitive types</code> and <code>Non-Primitive types</code>'},
  { text: '<b>Method Name</b> — follows camelCase convention; must start with a letter, <code>$</code>, <code>_</code>' },
  { text: '<b>Parameters</b> — inputs to the method. parentheses <code>()</code> are always mandatory even when empty' },
  // { text: '<b>Key Rule:</b> If return type is not <code>void</code>, a <code>return</code> statement is required in every code path — otherwise a compile error occurs.', highlight: true }
]
</script>

<Slide
  topic="Methods"
  sub-topic="User-defined Methods"
  :contents="contents"
/>
