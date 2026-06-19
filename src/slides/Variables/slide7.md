<script setup>
const contents = [
  { text: '<b>Problem:</b> Declare two integer variables, assign values to them, swap their values using a third temporary variable, and print the result.' },
  { text: '<b>Input (hardcoded):</b> <code>a = 5, b = 10</code>' },
  { text: '<b>Expected Output:</b><br><code>Before swap: a = 5, b = 10</code><br><code>After swap:  a = 10, b = 5</code>' },
  { text: '<b>Note:</b> Use a third variable <code>temp</code> to hold one value during the swap.' },
  { text: '<b>Hint:</b> Store <code>a</code> in <code>temp</code>, then assign <code>b</code> to <code>a</code>, then assign <code>temp</code> to <code>b</code>.', highlight: true },
]
</script>

<Slide
  topic="Variables"
  sub-topic="Practice Problem 1 — Swap Two Variables"
  :contents="contents"
/>
