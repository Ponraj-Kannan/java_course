<script setup>
const contents = [
  // {
  //   label: 'Arithmetic Operators',
  //   text: 'public class Main {\n    public static void main(String[] args) {\n        int a = 10, b = 3;\n\n        System.out.println(a + b);  // 13\n        System.out.println(a - b);  // 7\n        System.out.println(a * b);  // 30\n        System.out.println(a / b);  // 3  (integer division)\n        System.out.println(a % b);  // 1  (remainder)\n    }\n}',
  //   codeEditor: true,
  //   lang: 'java',
  // },
  { text: '<b>+</b> Addition &nbsp;|&nbsp; <b>-</b> Subtraction &nbsp;|&nbsp; <b>*</b> Multiplication' },
  { text: '<b>/</b> Division — when both operands are <code>int</code>, the result is an integer. <code>10 / 3</code> → <code>3</code>, not <code>3.33</code>' },
  { text: '<b>%</b> Modulus — returns the remainder after division.' },
  // { text: '<b>Integer vs floating-point division:</b><br><code>10 / 3</code> → <code>3</code> &nbsp;|&nbsp; <code>10.0 / 3</code> → <code>3.3333...</code>' },
  { text: '<b>Note:</b> To get a decimal result from two integers, cast one operand: <code>(double) a / b</code>', highlight: true },
]
</script>

<Slide
  topic="Operators"
  sub-topic="Arithmetic Operators"
  :contents="contents"
/>
