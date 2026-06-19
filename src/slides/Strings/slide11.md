<script setup>
const contents = [
 { text: '<b>Problem:</b> Reverse the order of words in a given sentence.'},
 { text: '<b>Input:</b> <code>"Hello World Java"</code>'},
 { text: '<b>Expected Output:</b> <code>"Java World Hello"</code>'},
 { text: '<b>Note:</b> The order of words is reversed, not the characters within each word.'},
 { text: '<b>Hint:</b> Use <code>split("\"")</code> to get words, then loop from the last word to the first and build the result using <b>StringBuilder</b>.', highlight: true }
 ]
</script>

<Slide
 topic="Strings"
 sub-topic="Practice Problem 4 - Reverse Words"
 :contents="contents"
/>
