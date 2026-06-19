<script setup>
const contents = [
  { text: '<b>Problem:</b> Read n numbers from the user and print their sum and average.' },
  { text: '<b>Input:</b><br><code>How many numbers? 5</code><br><code>Enter numbers: 10 20 30 40 50</code>' },
  { text: '<b>Expected Output:</b><br><code>Sum = 150</code><br><code>Average = 30.0</code>' },
  { text: '<b>Note:</b> Read n first using <code>nextInt()</code>, then use a <code>for</code> loop to read n numbers using <code>nextInt()</code> inside the loop.' },
  // { text: '<b>Hint:</b> Declare <code>int sum = 0</code> before the loop. Add each input to <code>sum</code> inside the loop. After the loop, calculate average as <code>(double) sum / n</code>.', highlight: true },
]
</script>

<Slide
  topic="Input Methods"
  sub-topic="Practice Problem 3 — Sum and Average of N Numbers"
  :contents="contents"
/>
