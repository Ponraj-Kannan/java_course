<script setup>
const contents = [
  // {
  //   label: 'Local variable — exists only inside the method',
  //   text: 'static void printDouble(int n) {\n    int result = n * 2; // local variable\n    System.out.println(result);\n}\n// result is NOT accessible here — compile error',
  //   codeEditor: true,
  //   lang: 'java',
  // },
  // {
  //   label: 'Each method has its own scope',
  //   text: 'static void methodA() {\n    int x = 10;\n    System.out.println(x); // OK\n}\n\nstatic void methodB() {\n    // System.out.println(x); // ERROR: x not in scope\n    int x = 99; // different x, independent of methodA\n    System.out.println(x);\n}',
  //   codeEditor: true,
  //   lang: 'java',
  // },
  { text: '<b>Local variable</b> — declared inside a method; created when the method is called, destroyed when it returns' },
  { text: '<b>Scope</b> — the region of code where a variable is accessible' },
  { text: '<b>Block scope:</b> variables declared inside <code>if</code>, <code>for</code>, or <code>while</code> blocks are only visible within that block' },
  { text: '<b>Note:</b> Two different methods can declare variables with the same name — they are completely independent and do not interfere.', highlight: true },
]
</script>

<Slide
  topic="Methods"
  sub-topic="Scope of Variables"
  :contents="contents"
/>
