<script setup>
const contents = [
 {
 text: '<b>trim()</b> — removes leading & trailing whitespace<br><code>"Hi ".trim() → "Hi"</code>',
 },
 {
 text: '<b>replace(old, new)</b> — replaces all occurrences<br><code>"aabbaa".replace("a","x") → "xxbbxx"</code>',
 },
 {
 text: '<b>contains(seq)</b> — returns true if substring exists<br><code>"Hello World".contains("World") → true</code>',
 },
 {
 text: '<b>equals(s)</b> — content comparison (case-sensitive)<br><code>"Hi".equals("hi") → false</code>',
 },
 {
 text: '<b>split(regex)</b> — splits string into an array<br><code>"a,b,c".split(",") → ["a","b","c"]</code>',
 }
]
</script>

<Slide
 topic="Strings"
 sub-topic="Built-in Methods"
 :contents="contents"
/>
