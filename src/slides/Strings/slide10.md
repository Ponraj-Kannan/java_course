<script setup>
const contents = [
 { text: '<b>Problem:</b> Count the number of words in a given sentence.'},
 { text: '<b>Input:</b> <code>"Java is a programming language"</code>'},
 { text: '<b>Expected Output:</b> <code>5</code>'},
 { text: '<b>Note:</b> Words are separated by single spaces. Assume no leading/trailing spaces.'},
 { text: '<b>Hint:</b> Use <code>split("\"")</code> to break the sentence into an array of words, then return its <code>length</code>.', highlight: true }
 ]
</script>

<Slide
 topic="Strings"
 sub-topic="Practice Problem 3 - Count Words"
 :contents="contents"
/>
