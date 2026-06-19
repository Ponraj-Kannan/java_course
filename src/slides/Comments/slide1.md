<script setup>
const contents = [
  { text: '<b>Comments</b> — lines in a program that are ignored by the Java compiler and not executed' },
  // { text: 'Comments are written for humans — they explain what the code does, why a decision was made, or how a method works' },
  { text: '<b>Types of Comments in Java:</b><br>1. Single-line comment — <code>//</code><br>2. Multi-line comment — <code>/* ... */</code><br>3. Documentation comment — <code>/** ... */</code>' },
  // { text: '<b>Good comments</b> explain the <i>why</i>, not just the <i>what</i>. If the code is clear enough to read, a comment repeating it adds no value.', highlight: true },
  // { text: '<b>Bad practice:</b> <code>i++; // increment i by 1</code><br><b>Good practice:</b> <code>i++; // move to the next student record</code>' },
]
</script>

<Slide
  topic="Comments"
  sub-topic="Introduction"
  :contents="contents"
/>
