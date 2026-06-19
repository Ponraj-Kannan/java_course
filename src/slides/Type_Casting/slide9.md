<script setup>
const contents = [
  { text: '<b>Problem:</b> Demonstrate both widening and narrowing casting. Convert an <code>int</code> to <code>double</code> (widening) and a <code>double</code> to <code>int</code> (narrowing), and print the results.' },
  { text: '<b>Input (hardcoded):</b> <code>int a = 150</code> and <code>double b = 47.89</code>' },
  { text: '<b>Expected Output:</b><br><code>int to double   : 150.0</code><br><code>double to int   : 47</code><br><code>Math.round(b)   : 48</code>' },
  { text: '<b>Note:</b> Observe that casting <code>double</code> to <code>int</code> truncates (not rounds). Use <code>Math.round()</code> for rounding.' },
  // { text: '<b>Hint:</b> For widening, assign <code>int</code> directly to a <code>double</code> variable. For narrowing, use <code>(int) b</code>. For rounding, use <code>Math.round(b)</code>.', highlight: true },
]
</script>

<Slide
  topic="Type Casting"
  sub-topic="Practice Problem 1 — Widening and Narrowing"
  :contents="contents"
/>
