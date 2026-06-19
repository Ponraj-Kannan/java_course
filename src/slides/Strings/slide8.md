
<script setup>
const contents = [{ text: '<b>Problem:</b> Count the number of vowels in a given string.'},
 { text: '<b>Input:</b> <code>\"Hello, World!\"</code>'},
 { text: '<b>Expected Output:</b> <code>3</code> (e, o, o)'},
 { text: '<b>Note:</b> Count both uppercase and lowercase vowels (A, E, I, O, U, a, e, i, o, u).'},
 { text: '<b>Hint:</b> Use <code>charAt()</code> inside a loop and check against a vowel string using <code>indexOf()</code> or a condition.', highlight: true }]
</script>

<Slide
 topic="Strings"
 sub-topic="Practice Problem 1 - Vowels count"
 :contents="contents"
/>