<script setup>
const contents = [
  { text: '<b>Problem:</b> Given an array of words, write a Java program that combines them into a single comma-separated sentence using <code>StringBuilder</code> inside a loop, without creating unnecessary String objects.' },
  { text: '<b>Input:</b> <code>String[] words = {"Apple", "Banana", "Cherry", "Mango"};</code>' },
  { text: '<b>Expected Output:</b> <code>"Apple, Banana, Cherry, Mango"</code>' },
  { text: '<b>Key Concepts:</b> Initialize a <code>StringBuilder</code>. Iterate through the array with a loop, appending each word with <code>sb.append(words[i])</code>. Only append the delimiter <code>", "</code> when <code>i &lt; words.length - 1</code> to avoid trailing commas, then convert with <code>sb.toString()</code>.' },
]
</script>

<Slide
  topic="Java Strings"
  sub-topic="Practice Problem 5 — StringBuilder in a Loop"
  :contents="contents"
/>
