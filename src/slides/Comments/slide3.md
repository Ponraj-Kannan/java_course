<script setup>
const contents = [
  { text: '<b>Multi-line comment</b> — begins with <code>/*</code> and ends with <code>*/</code>. Everything between these markers is ignored by the compiler.' },
  // { text: 'Can span any number of lines. Useful for longer explanations, disabling a block of code temporarily, or describing a section of logic.' },
  // {
  //   label: 'Examples',
  //   text: '/*\n   This program reads two numbers from the user,\n   calculates their sum and average,\n   and prints the result to the console.\n*/\npublic class Main {\n    public static void main(String[] args) {\n\n        int a = 20;\n        int b = 30;\n\n        /* Temporarily disabled\n        int c = a - b;\n        System.out.println(c);\n        */\n\n        System.out.println("Sum: " + (a + b));\n    }\n}',
  //   codeEditor: true,
  //   lang: 'java',
  // },
  { text: '<b>Note:</b> Multi-line comments cannot be nested. Writing <code>/* outer /* inner */ */</code> will cause a compile error.', highlight: true },
]
</script>

<Slide
  topic="Comments"
  sub-topic="Multi-Line Comment ( /* ... */ )"
  :contents="contents"
/>
