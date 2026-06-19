<script setup>
const contents = [
  // {
  //   label: 'Method with multiple parameters',
  //   text: 'static int add(int a, int b) {\n    return a + b;\n}\n\nint sum = add(10, 20); // sum = 30',
  //   codeEditor: true,
  //   lang: 'java',
  // },
  // {
  //   label: 'Method with different data types',
  //   text: 'static void printInfo(String name, int age) {\n    System.out.println(name + " is " + age + " years old.");\n}\n\nprintInfo("Alice", 21);',
  //   codeEditor: true,
  //   lang: 'java',
  // },
  { text: '<b>Parameter</b> — variable declared in the method signature: <code>int a, int b</code>' },
  { text: '<b>Argument</b> — actual value passed during the method call: <code>add(10, 20)</code>' },
  { text: '<b>Order matters:</b> arguments are mapped to parameters left to right by position' },
  { text: '<b>Type must match:</b> passing a String where int is expected causes a compile error' },
  { text: '<b>Pass by value:</b> Java passes a copy of the value — changes to parameters inside the method do not affect the original variable.', highlight: true },
]
</script>

<Slide
  topic="Methods"
  sub-topic="Parameters and Arguments"
  :contents="contents"
/>
