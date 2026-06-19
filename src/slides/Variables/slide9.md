<script setup>
const contents = [
  { text: '<b>Problem:</b> Store a temperature in Celsius in a variable and convert it to Fahrenheit. Print both values.' },
  { text: '<b>Input (hardcoded):</b> <code>celsius = 37.0</code>' },
  { text: '<b>Expected Output:</b><br><code>Celsius    : 37.0</code><br><code>Fahrenheit : 98.6</code>' },
  { text: '<b>Formula:</b> Fahrenheit = (Celsius x 9 / 5) + 32' },
  { text: '<b>Hint:</b> Declare <code>double celsius = 37.0</code>. Declare a second variable <code>double fahrenheit</code> and apply the formula. Print both using <code>System.out.println()</code>.', highlight: true },
]
</script>

<Slide
  topic="Variables"
  sub-topic="Practice Problem 3 — Temperature Conversion"
  :contents="contents"
/>
