<script setup>
const contents = [
 { text: '<b>Problem:</b> Check whether a given string is a palindrome or not.'},
 { text: '<b>Input:</b> <code>\"level\"</code> → <code>true</code>'},
 { text: '<b>Input:</b> <code>\"Hello\"</code> → <code>false</code>'},
 { text: '<b>Note:</b> Ignore case while comparing (treat uppercase and lowercase as equal).'},
 { text: '<b>Hint:</b> Convert to lowercase using <code>toLowerCase()</code>, then compare the string with its <code>reverse()</code> using <b>StringBuilder</b>.', highlight: true }]
</script>

<Slide
 topic="Strings"
 sub-topic="Practice Problem 2 - Palindrome check"
 :contents="contents"
/>
