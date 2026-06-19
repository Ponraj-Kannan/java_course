<script setup>
const contents = [
 { text: '<b>Problem:</b> Find the most frequently occurring character in a string.'},
 { text: '<b>Input:</b> <code>"programming"</code>'},
 { text: '<b>Expected Output:</b> <code>\'g\'</code> (appears 2 times)'},
 { text: '<b>Note:</b> If two characters have the same frequency, return the one that appears first.'},
 { text: '<b>Hint:</b> Use a loop with <code>charAt()</code> and count occurrences. Compare counts to track the maximum.', highlight: true }
 ]
</script>

<Slide
 topic="Strings"
 sub-topic="Practice Problem 5 - Most frequent character"
 :contents="contents"
/>
