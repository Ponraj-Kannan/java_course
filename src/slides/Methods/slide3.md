<script setup>
const contents = [
  // {
  //   label: 'Different return types',
  //   text: 'static int getAge() { return 20; }\n\nstatic double getPi() { return 3.14159; }\n\nstatic boolean isEven(int n) { return n % 2 == 0; }\n\nstatic String greet(String name) { return "Hello, " + name; }',
  //   codeEditor: true,
  //   lang: 'java',
  // },
  // {
  //   label: 'Using the returned value',
  //   text: 'int age = getAge();           // 20\ndouble pi = getPi();          // 3.14159\nboolean flag = isEven(4);     // true\nString msg = greet("Bob");    // "Hello, Bob"',
  //   codeEditor: true,
  //   lang: 'java',
  // },
  { text: '<b>Return type</b> — declared before the method name; must exactly match what is returned' },
  { text: '<b>void</b> — no return value' },
  { text: '<b>Primitive and Non-primitive Data types</b> — method returns a value of the same type' },
  { text: '<b>return statement</b> — exits the method immediately; any code after it is unreachable' },
  { text: '<b>Note:</b> Every non-void method must have a return statement that covers all code paths, otherwise a compile error occurs.', highlight: true },
]
</script>

<Slide
  topic="Methods"
  sub-topic="Return Types"
  :contents="contents"
/>
