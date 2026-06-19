<script setup>
const contents = [
  // {
  //   label: 'Relational (Comparison) Operators',
  //   text: 'public class Main {\n    public static void main(String[] args) {\n        int a = 10, b = 20;\n\n        System.out.println(a == b);  // false\n        System.out.println(a != b);  // true\n        System.out.println(a >  b);  // false\n        System.out.println(a <  b);  // true\n        System.out.println(a >= b);  // false\n        System.out.println(a <= b);  // true\n    }\n}',
  //   codeEditor: true,
  //   lang: 'java',
  // },
  { text: '<b>==</b> Equal to &nbsp;|&nbsp; <b>!=</b> Not equal to' },
  { text: '<b>&gt;</b> Greater than &nbsp;|&nbsp; <b>&lt;</b> Less than' },
  { text: '<b>&gt;=</b> Greater than or equal to &nbsp;|&nbsp; <b>&lt;=</b> Less than or equal to' },
  { text: '<b>Return type:</b> every relational expression evaluates to a <code>boolean</code>.' },
  { text: '<b>Common use:</b> relational operators are used inside <code>if</code>, <code>while</code>, and <code>for</code> conditions to control program flow.' },
  { text: '<b>Note:</b> Never use <code>==</code> to compare String values — use <code>.equals()</code> instead. <code>==</code> checks reference, not content.', highlight: true },
]
</script>

<Slide
  topic="Operators"
  sub-topic="Relational Operators"
  :contents="contents"
/>
