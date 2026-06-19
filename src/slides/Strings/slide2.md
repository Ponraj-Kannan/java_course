<script setup>
const contents = [
 {
 text: '<b>+ Operator </b> — concatenate content<br><code>s1 + s2</code>',
 },
 {
 text: '<b>concat()</b> — concatenate content (use this!)<br><code>s1.concat(s2)</code>',
 },
 {
 text: '<b>equals()</b> — compares content (use this!)<br><code>s1.equals(s2)</code>',
 },
 {
 text: '<b>equalsIgnoreCase()</b> — case-insensitive content comparison<br><code>s1.equalsIgnoreCase(s2)</code>',
 },
 {
 text: '<b>== operator</b> compares <i>references</i> (memory address), NOT content. Avoid for string comparison.',
 highlight: true,
 },
]
</script>

<Slide
 topic="Strings"
 sub-topic="Concatenation & Comparison"
 :contents="contents"
/>
