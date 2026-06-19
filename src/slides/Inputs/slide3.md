<script setup>
const contents = [
  { text: '<b>nextInt()</b> — reads an <code>int</code> value' },
  { text: '<b>nextDouble()</b> — reads a <code>double</code> value' },
  { text: '<b>nextFloat()</b> — reads a <code>float</code> value' },
  { text: '<b>nextLong()</b> — reads a <code>long</code> value' },
  { text: '<b>nextBoolean()</b> — reads a <code>boolean</code> value (<code>true</code> or <code>false</code>)' },
  { text: '<b>next()</b> — reads a single word (stops at whitespace)' },
  { text: '<b>nextLine()</b> — reads the entire line including spaces' },
  // {
  //   label: 'Reading multiple data types',
  //   text: 'import java.util.Scanner;\n\npublic class Main {\n    public static void main(String[] args) {\n        Scanner sc = new Scanner(System.in);\n\n        System.out.print("Enter age: ");\n        int age = sc.nextInt();\n\n        System.out.print("Enter GPA: ");\n        double gpa = sc.nextDouble();\n\n        System.out.print("Enter name: ");\n        sc.nextLine(); // consume leftover newline\n        String name = sc.nextLine();\n\n        System.out.println(name + " | Age: " + age + " | GPA: " + gpa);\n        sc.close();\n    }\n}',
  //   codeEditor: true,
  //   lang: 'java',
  // },
]
</script>

<Slide
  topic="Input Methods"
  sub-topic="Scanner — Reading Different Data Types"
  :contents="contents"
/>
