<script setup>
const contents = [
  // {
  //   label: 'Ternary Operator',
  //   text: 'public class Main {\n    public static void main(String[] args) {\n        int a = 10, b = 20;\n\n        // condition ? valueIfTrue : valueIfFalse\n        int max = (a > b) ? a : b;\n        System.out.println("Max = " + max); // Max = 20\n\n        String result = (a % 2 == 0) ? "Even" : "Odd";\n        System.out.println(result); // Even\n    }\n}',
  //   codeEditor: true,
  //   lang: 'java',
  // },
  { text: '<b>Syntax:</b> <code>condition ? valueIfTrue : valueIfFalse</code>' },
  { text: '<b>?</b> — separates the condition from the true-branch value.' },
  { text: '<b>:</b> — separates the true-branch value from the false-branch value.' },
  { text: '<b>Use case:</b> a compact replacement for a simple <code>if-else</code> when assigning a value or returning a result based on a condition.', highlight: true},
  // { text: '<b>Note:</b> Avoid nesting ternary operators — it reduces readability. Use <code>if-else</code> for complex logic.', highlight: true },
]
</script>

<Slide
  topic="Operators"
  sub-topic="Ternary Operator"
  :contents="contents"
/>
