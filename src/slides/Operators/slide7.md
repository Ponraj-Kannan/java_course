<script setup>
const contents = [
  // {
  //   label: 'Bitwise Operators',
  //   text: 'public class Main {\n    public static void main(String[] args) {\n        int a = 5;  // binary: 0101\n        int b = 3;  // binary: 0011\n\n        System.out.println(a & b);   // 1   (AND)\n        System.out.println(a | b);   // 7   (OR)\n        System.out.println(a ^ b);   // 6   (XOR)\n        System.out.println(~a);      // -6  (NOT)\n        System.out.println(a << 1);  // 10  (left shift)\n        System.out.println(a >> 1);  // 2   (right shift)\n    }\n}',
  //   codeEditor: true,
  //   lang: 'java',
  // },
  { text: '<b>&</b> Bitwise AND — bit is 1 only if both bits are 1 &nbsp;|&nbsp; <b>|</b> Bitwise OR — bit is 1 if either bit is 1' },
  { text: '<b>^</b> Bitwise XOR — bit is 1 if bits are different &nbsp;|&nbsp; <b>~</b> Bitwise NOT — flips all bits' },
  { text: '<b>&lt;&lt;</b> Left shift — shifts bits left, fills with 0s. Equivalent to multiplying by 2 for each position shifted.' },
  { text: '<b>&gt;&gt;</b> Right shift — shifts bits right. Equivalent to dividing by 2 for each position shifted.' },
  { text: '<b>Note:</b> Bitwise operators work directly on binary representations of integers. Commonly used in low-level programming, flags, and performance-critical logic.', highlight: true },
]
</script>

<Slide
  topic="Operators"
  sub-topic="Bitwise Operators"
  :contents="contents"
/>
