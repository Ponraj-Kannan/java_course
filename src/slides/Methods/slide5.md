<script setup>
const contents = [
  // {
  //   label: 'Overloaded methods — same name, different parameters',
  //   text: 'static int add(int a, int b) {\n    return a + b;\n}\n\nstatic double add(double a, double b) {\n    return a + b;\n}\n\nstatic int add(int a, int b, int c) {\n    return a + b + c;\n}',
  //   codeEditor: true,
  //   lang: 'java',
  // },
  // {
  //   label: 'Java picks the right version automatically',
  //   text: 'System.out.println(add(2, 3));        // calls int version  → 5\nSystem.out.println(add(1.5, 2.5));    // calls double version → 4.0\nSystem.out.println(add(1, 2, 3));     // calls 3-param version → 6',
  //   codeEditor: true,
  //   lang: 'java',
  // },
  { text: '<b>Method Overloading</b> — defining multiple methods with the same name but different parameter lists' },
  // { text: '<b>Compiler resolves</b> the correct method at compile time based on the number and type of arguments' },
  // { text: '<b>Valid differences:</b> number of parameters, type of parameters, or both' },
  { text: '<b>Return type alone is NOT enough</b> to overload — two methods with the same name and parameters but different return types cause a compile error.', highlight: true },
]
</script>

<Slide
  topic="Methods"
  sub-topic="Method Overloading"
  :contents="contents"
/>
