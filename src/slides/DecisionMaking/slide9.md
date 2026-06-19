<script setup>
const contents = [
  { text: '<b>Problem:</b> Check whether a given year is a leap year or not.' },
  { text: '<b>Input:</b> <code>year = 2024</code>' },
  { text: '<b>Expected Output:</b> <code>2024 is a Leap Year</code>' },
  { text: '<b>Leap Year Rules:</b><br>1. Divisible by 4 → leap year<br>2. But if divisible by 100 → NOT a leap year<br>3. Unless also divisible by 400 → leap year again' },
  { text: '<b>Hint:</b> Use nested <code>if-else</code> or combine conditions with <code>&&</code> and <code>||</code>. Example: <code>(year % 4 == 0 && year % 100 != 0) || (year % 400 == 0)</code>', highlight: true },
]
</script>

<Slide
  topic="Decision Making"
  sub-topic="Practice Problem 4 — Leap Year"
  :contents="contents"
/>
