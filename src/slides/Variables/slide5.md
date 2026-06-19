<script setup>
const contents = [
  { text: '<b>Constant</b> — a variable whose value cannot be changed once it is assigned. Declared using the <code>final</code> keyword.' },
  { text: 'Trying to reassign a <code>final</code> variable causes a <b>compile-time error</b>.' },
  // {
  //   label: 'Declaring and using constants',
  //   text: 'final double PI = 3.14159;\nfinal int MAX_STUDENTS = 60;\nfinal String SCHOOL_NAME = "ABC School";\n\n// These lines would cause a compile error:\n// PI = 3.0;           // ERROR: cannot assign to final variable\n// MAX_STUDENTS = 100; // ERROR\n\n// Using constants in a calculation\ndouble area = PI * 7 * 7;\nSystem.out.println("Area = " + area);',
  //   codeEditor: true,
  //   lang: 'java',
  // },
  { text: '<b>Naming convention for constants:</b> Use ALL_CAPS with underscores between words (e.g., <code>MAX_SIZE</code>, <code>TAX_RATE</code>).' },
  { text: '<b>Why use constants?</b> Prevents accidental changes to important values, makes the code easier to read, and simplifies updating a value used in multiple places.', highlight: true },
]
</script>

<Slide
  topic="Variables"
  sub-topic="Constants — final Keyword"
  :contents="contents"
/>
