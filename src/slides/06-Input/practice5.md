<script setup>
const contents = [
  { text: '<b>Problem:</b> Trace the following code given the input sequence below and predict what is stored in variables <code>a</code>, <code>b</code>, and <code>c</code>.' },
  { text: '<b>Input Stream:</b><br><code>100 Java Programming</code><br><code>Rocks!</code>' },
  { text: '<b>Code:</b><br><code>int a = sc.nextInt();</code><br><code>String b = sc.next();</code><br><code>String c = sc.nextLine();</code>' },
  { text: '<b>Expected Values:</b><br><code>a = 100</code><br><code>b = "Java"</code><br><code>c = " Programming"</code> (including leading space!)' },
  { text: '<b>Explanation:</b> <code>nextInt()</code> reads <code>100</code>, <code>next()</code> skips leading space and reads <code>"Java"</code>, and <code>nextLine()</code> reads the remainder of the first line (<code>" Programming"</code>) up to the newline.' },
]
</script>

<Slide
  topic="Java Input Methods"
  sub-topic="Practice Problem 5 — Output Prediction"
  :contents="contents"
/>
