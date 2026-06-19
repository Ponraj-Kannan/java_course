<script setup>
const contents = [
  // {
  //   label: 'System.out.println — Print with newline',
  //   text: 'System.out.println("Hello, World!");\nSystem.out.println(42);\nSystem.out.println(3.14);\nSystem.out.println(true);\nSystem.out.println(); // prints a blank line',
  //   codeEditor: true,
  //   lang: 'java',
  // },
  { text: '<b>println</b> stands for <i>print line</i> — prints the value and then moves the cursor to the next line.' },
  { text: '<b>System</b> — built-in Java class that provides access to system-level features.' },
  { text: '<b>out</b> — a static field of System representing the standard output stream (the console).' },
  { text: '<b>Accepts any type:</b> String, int, double, boolean, char, or even objects (calls their <code>.toString()</code> method).' },
  { text: '<b>Key behaviour:</b> each <code>println()</code> call starts output on a new line. Calling it with no arguments prints just a blank line.', highlight: true },
]
</script>

<Slide
  topic="Basic Syntax"
  sub-topic="Printing — System.out.println()"
  :contents="contents"
/>
