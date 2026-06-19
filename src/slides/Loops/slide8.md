<script setup>
const contents = [
  { text: '<b>Problem:</b> Count the number of digits in a given integer.' },
  { text: '<b>Input:</b> <code>n = 7462</code>' },
  { text: '<b>Expected Output:</b> <code>Number of digits: 4</code>' },
  { text: '<b>Note:</b> Use a <b>do-while</b> loop. This ensures the loop runs at least once, which correctly handles the case where <code>n = 0</code> (which has 1 digit).' },
  // { text: '<b>Hint:</b> Initialize <code>count = 0</code>. Inside the loop, divide <code>n = n / 10</code> and increment <code>count</code>. Repeat while <code>n != 0</code>.', highlight: true },
]
</script>

<Slide
  topic="Looping Statements"
  sub-topic="Do-While Loop — Practice Problem 1"
  :contents="contents"
/>
