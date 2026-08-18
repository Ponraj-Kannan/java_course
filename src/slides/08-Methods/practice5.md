<script setup>
const contents = [
  { text: '<b>Problem:</b> Given the recursive method below, trace the complete call stack progression when <code>mystery(3)</code> is called and determine the final printed output.' },
  { text: '<b>Code:</b><br><code>static void mystery(int n) {</code><br><code>&nbsp;&nbsp;if (n == 0) return;</code><br><code>&nbsp;&nbsp;System.out.print(n + " ");</code><br><code>&nbsp;&nbsp;mystery(n - 1);</code><br><code>&nbsp;&nbsp;System.out.print(n + " ");</code><br><code>}</code>' },
  { text: '<b>Expected Output:</b> <code>3 2 1 1 2 3 </code>' },
  { text: '<b>Explanation:</b> Each stack frame prints <code>n</code> before the recursive call on the way down (winding phase: <code>3 2 1</code>), and prints <code>n</code> again after the recursive call returns on the way up (unwinding phase: <code>1 2 3</code>).' },
]
</script>

<Slide
  topic="Methods"
  sub-topic="Practice Problem 5 — Call Stack Winding & Unwinding Trace"
  :contents="contents"
/>
