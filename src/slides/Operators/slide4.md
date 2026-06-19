<script setup>
const contents = [
  // {
  //   label: 'Assignment Operators',
  //   text: 'public class Main {\n    public static void main(String[] args) {\n        int x = 10;\n\n        x += 5;   System.out.println(x); // 15\n        x -= 3;   System.out.println(x); // 12\n        x *= 2;   System.out.println(x); // 24\n        x /= 4;   System.out.println(x); // 6\n        x %= 4;   System.out.println(x); // 2\n    }\n}',
  //   codeEditor: true,
  //   lang: 'java',
  // },
  { text: '<b>=</b> Simple assignment — assigns the right-hand value to the left-hand variable.' },
  { text: '<b>+=</b> &nbsp;<code>x += 5</code> is shorthand for <code>x = x + 5</code>' },
  { text: '<b>-=</b> &nbsp;<code>x -= 3</code> is shorthand for <code>x = x - 3</code>' },
  { text: '<b>*=</b> &nbsp;<code>x *= 2</code> is shorthand for <code>x = x * 2</code>' },
  { text: '<b>/=</b> &nbsp;<code>x / = 4</code> is shorthand for <code>x = x / 4</code><br>' },
  { text: '<b>%=</b> &nbsp;<code>x %= 4</code> is shorthand for <code>x = x % 4</code>' },
  // { text: '<b>Note:</b> Compound assignment operators apply the operation and reassign the result in one step — they make code shorter and are widely used inside loops.', highlight: true },
]
</script>

<Slide
  topic="Operators"
  sub-topic="Assignment Operators"
  :contents="contents"
/>
