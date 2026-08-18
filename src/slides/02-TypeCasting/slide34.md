---
transition: fade
---

<script setup>
const contents = [
  { text: '<b>Problem:</b> Read a character from the user and print its ASCII value, whether it is uppercase, lowercase, or a digit, and its opposite-case character (if it is a letter).' },
  { text: '<b>Input:</b> <code>Enter a character: G</code>' },
  { text: '<b>Expected Output:</b><br><code>ASCII value : 71</code><br><code>Type        : Uppercase letter</code><br><code>Lowercase   : g</code>' },
  { text: '<b>Note:</b> Use <code>sc.next().charAt(0)</code> to read a character. Cast to <code>int</code> for ASCII. Check ranges with <code>if</code>: uppercase 65–90, lowercase 97–122, digits 48–57. Convert case by adding or subtracting 32 with a <code>(char)</code> cast.' }
]
</script>

<Slide
  topic="Type Casting in Java"
  sub-topic="Practice Problem"
  :contents="contents"
/>
