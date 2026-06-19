<script setup>
const contents = [
  { text: '<b>Problem:</b> Read a person\'s age and check eligibility using logical operators. Print appropriate messages.' },
  { text: '<b>Rules:</b><br>• Age &gt;= 18 AND age &lt;= 60 → <code>Eligible to work</code><br>• Age &lt; 18 OR age &gt; 60 → <code>Not eligible to work</code><br>• Age == 18 → additionally print <code>Just became eligible!</code>' },
  { text: '<b>Input:</b> <code>age = 18</code>' },
  { text: '<b>Expected Output:</b><br><code>Eligible to work</code><br><code>Just became eligible!</code>' },
  // { text: '<b>Hint:</b> Use <code>&&</code> for the range check, <code>||</code> for the ineligibility check, and a separate <code>if</code> with <code>==</code> for the exact-age message.', highlight: true },
]
</script>

<Slide
  topic="Operators"
  sub-topic="Practice Problem 2 — Relational &amp; Logical"
  :contents="contents"
/>
