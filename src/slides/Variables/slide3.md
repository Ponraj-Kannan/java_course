<script setup>
const contents = [
  { text: '<b>1. Local Variable</b> — declared inside a method or block. Only accessible within that method or block. Must be initialized before use. Not given a default value by Java.' },
  { text: '<b>2. Instance Variable</b> — declared inside a class but outside any method. Each object of the class has its own copy. Gets a default value (0, false, null) if not initialized.' },
  { text: '<b>3. Static Variable</b> — declared with the <code>static</code> keyword inside a class. Shared across all objects of the class. Only one copy exists in memory.' },
  // {
  //   label: 'Example showing all three types',
  //   text: 'public class Student {\n    static String school = "ABC School"; // static variable\n    String name;                          // instance variable\n\n    void display() {\n        int marks = 95;                   // local variable\n        System.out.println(name + " | " + marks + " | " + school);\n    }\n}',
  //   codeEditor: true,
  //   lang: 'java',
  // },
  // { text: '<b>For first-year students:</b> Most programs use local variables. Instance and static variables become important when learning classes and objects.', highlight: true },
]
</script>

<Slide
  topic="Variables"
  sub-topic="Types of Variables"
  :contents="contents"
/>
