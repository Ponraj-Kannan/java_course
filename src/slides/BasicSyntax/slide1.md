<script setup>
const contents = [
  // {
  //   label: 'Minimal Java Program',
  //   text: 'public class Main {\n    public static void main(String[] args) {\n        // Your code goes here\n        System.out.println("Hello, World!");\n    }\n}',
  //   codeEditor: true,
  //   lang: 'java',
  // },
  { text: '<b>public class Main</b> — defines a class named <code>Main</code>. The filename must match the class name exactly.' },
  { text: '<b>public static void main(String[] args)</b> — entry point of every Java program. JVM calls this method first.' },
  { text: '<b>public</b> — accessible from anywhere | <b>static</b> — belongs to the class, not an object | <b>void</b> — returns nothing | <b>main</b> — method name' },
  { text: '<b>String[] args</b> — array of command-line arguments passed to the program' },
  { text: '<b>Note:</b> Java is case-sensitive. <code>Main</code> and <code>main</code> are different. Every statement ends with a semicolon <code>;</code>.', highlight: true },
]
</script>

<Slide
  topic="Basic Syntax"
  sub-topic="Java Program Structure"
  :contents="contents"
/>
