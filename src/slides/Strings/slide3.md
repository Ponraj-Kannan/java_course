<script setup>
const contents = [
 {
 text: '<b>length()</b> — returns number of characters<br><code>"Hello".length() → 5</code>',
 },
 {
 text: '<b>charAt(i)</b> — returns character at index i<br><code>"Hello".charAt(1) → \'e\'</code>',
 },
 {
 text: '<b>substring(s, e)</b> — extracts from index s to e-1<br><code>"Hello".substring(1,4) → "ell"</code>',
 },
 {
 text: '<b>toUpperCase()</b> — converts all chars to uppercase<br><code>"hello".toUpperCase() → "HELLO"</code>',
 },
 {
 text: '<b>toLowerCase()</b> — converts all chars to lowercase<br><code>"HELLO".toLowerCase() → "hello"</code>',
 }
]
</script>

<Slide
 topic="Strings"
 sub-topic="Built-in Methods"
 :contents="contents"
/>
