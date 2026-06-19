<script setup>
const contents = [
  { text: '<b>nextInt()</b> — reads <code>int</code> | example: <code>int age = sc.nextInt();</code>' },
  { text: '<b>nextDouble()</b> — reads <code>double</code> | example: <code>double price = sc.nextDouble();</code>' },
  { text: '<b>nextFloat()</b> — reads <code>float</code> | example: <code>float weight = sc.nextFloat();</code>' },
  { text: '<b>nextLong()</b> — reads <code>long</code> | example: <code>long bigNum = sc.nextLong();</code>' },
  { text: '<b>nextBoolean()</b> — reads <code>boolean</code> | example: <code>boolean flag = sc.nextBoolean();</code>' },
  { text: '<b>next()</b> — reads one word (<code>String</code>) | example: <code>String word = sc.next();</code>' },
  { text: '<b>nextLine()</b> — reads full line (<code>String</code>) | example: <code>String sentence = sc.nextLine();</code>' },
  { text: '<b>next().charAt(0)</b> — reads single <code>char</code> | example: <code>char ch = sc.next().charAt(0);</code>' },
  // { text: '<b>Remember:</b> always call <code>sc.nextLine()</code> to consume the leftover newline after <code>nextInt()</code> or <code>nextDouble()</code> before reading a line with <code>nextLine()</code>.', highlight: true },
]
</script>

<Slide
  topic="Input Methods"
  sub-topic="Scanner Methods — Quick Reference"
  :contents="contents"
/>
