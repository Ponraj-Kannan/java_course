<script setup>
const contents = [
  // {
  //   label: 'Unary Operators',
  //   text: 'public class Main {\n    public static void main(String[] args) {\n        int a = 5;\n\n        System.out.println(+a);   //  5  (unary plus)\n        System.out.println(-a);   // -5  (unary minus)\n        System.out.println(++a);  //  6  (pre-increment)\n        System.out.println(a++);  //  6  (post-increment, prints before adding)\n        System.out.println(a);    //  7  (now updated)\n        System.out.println(!true); // false (logical NOT)\n    }\n}',
  //   codeEditor: true,
  //   lang: 'java',
  // },
  { text: '<b>+</b> Unary plus — indicates a positive value (rarely used explicitly).' },
  { text: '<b>-</b> Unary minus — negates the value. <br><code>int a = 5; -a</code> → <code>-5</code>' },
  { text: '<b>++</b> Increment — increases value by 1.<br><b>Pre-increment</b> <code>++a</code> — increments first, then uses the value.<br><b>Post-increment</b> <code>a++</code> — uses the value first, then increments.' },
  { text: '<b>--</b> Decrement — decreases value by 1. Same pre/post behaviour as <code>++</code>.' },
  { text: '<b>Note:</b> <code>++a</code> vs <code>a++</code> only differs when the expression is used inside another statement (e.g. assignment or print).', highlight: true },
]
</script>

<Slide
  topic="Operators"
  sub-topic="Unary Operators"
  :contents="contents"
/>
