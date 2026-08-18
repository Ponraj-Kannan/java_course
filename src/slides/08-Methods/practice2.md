<script setup>
const contents = [
  { text: '<b>Problem:</b> Trace the following Java program and predict the exact console output, demonstrating your understanding of pass-by-value for primitives versus arrays.' },
  { text: '<b>Code:</b><br><code>static void modify(int x, int[] arr) {</code><br><code>&nbsp;&nbsp;x = 50;</code><br><code>&nbsp;&nbsp;arr[0] = 100;</code><br><code>}</code><br><code>int num = 10; int[] data = {1, 2, 3};</code><br><code>modify(num, data);</code><br><code>System.out.println(num + " " + data[0]);</code>' },
  { text: '<b>Expected Output:</b> <code>10 100</code>' },
  { text: '<b>Explanation:</b> <code>num</code> is a primitive so only its copy was modified inside the method (remains <code>10</code> in caller). <code>data</code> is an array reference, so <code>arr[0] = 100</code> mutates the underlying array object in the heap.' },
]
</script>

<Slide
  topic="Methods"
  sub-topic="Practice Problem 2 — Pass-by-Value Output Prediction"
  :contents="contents"
/>
