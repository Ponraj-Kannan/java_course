<script setup>
const contents = [
 {
 text: '<b>indexOf(s)</b> — returns first index of substring (-1 if not found)<br><code>"Hello".indexOf("l") → 2</code>', },
 {
 text: '<b>lastIndexOf(s)</b> — returns last occurrence index<br><code>"Hello".lastIndexOf("l") → 3</code>',
 },
 {
 text: '<b>startsWith(prefix)</b> — checks if string begins with prefix<br><code>"Hello".startsWith("He") → true</code>',
 },
 {
 text: '<b>endsWith(suffix)</b> — checks if string ends with suffix<br><code>"Hello".endsWith("lo") → true</code>',
 },
 {
 text: '<b>isEmpty()</b> — true if length is 0<br><code>"".isEmpty() → true</code>',
 }
]
</script>

<Slide
 topic="Strings"
 sub-topic="Built-in Methods"
 :contents="contents"
/>
