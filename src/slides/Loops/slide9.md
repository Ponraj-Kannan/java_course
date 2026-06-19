<script setup>
const contents = [
  { text: '<b>Problem:</b> Calculate the sum of digits of a given number.' },
  { text: '<b>Input:</b> <code>n = 1234</code>' },
  { text: '<b>Expected Output:</b> <code>Sum of digits: 10</code>  (1 + 2 + 3 + 4)' },
  { text: '<b>Note:</b> Use a <b>do-while</b> loop. Extract the last digit using the modulus operator <code>%</code>.' },
  // { text: '<b>Hint:</b> Initialize <code>sum = 0</code>. Inside the loop, add <code>n % 10</code> to <code>sum</code>, then divide <code>n = n / 10</code>. Repeat while <code>n != 0</code>.', highlight: true },
]
</script>

<Slide
  topic="Looping Statements"
  sub-topic="Do-While Loop — Practice Problem 2"
  :contents="contents"
/>
