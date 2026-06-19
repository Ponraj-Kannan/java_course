<script setup>
const contents = [
  // {
  //   label: 'Logical Operators',
  //   text: 'public class Main {\n    public static void main(String[] args) {\n        int age = 20;\n        boolean hasID = true;\n\n        // AND — both must be true\n        System.out.println(age >= 18 && hasID);   // true\n\n        // OR  — at least one must be true\n        System.out.println(age < 18 || hasID);    // true\n\n        // NOT — inverts the boolean\n        System.out.println(!hasID);               // false\n    }\n}',
  //   codeEditor: true,
  //   lang: 'java',
  // },
  { text: '<b>&&</b> Logical AND — returns <code>true</code> only when <u>both</u> operands are <code>true</code>' },
  { text: '<b>||</b> Logical OR — returns <code>true</code> when <u>at least one</u> operand is <code>true</code>' },
  { text: '<b>!</b> Logical NOT — flips the boolean value. <code>!true</code> → <code>false</code>, <code>!false</code> → <code>true</code>' },
  { text: '<b>Short-circuit evaluation:<br></b> For <code>&&</code>, if the left side is <code>false</code>, the right side is never evaluated.<br> For <code>||</code>, if the left side is <code>true</code>, the right side is skipped.', highlight: true },
  // { text: '<b>Note:</b> Logical operators work only on <code>boolean</code> expressions. Combine them to build complex conditions.', highlight: true },
]
</script>

<Slide
  topic="Operators"
  sub-topic="Logical Operators"
  :contents="contents"
/>
