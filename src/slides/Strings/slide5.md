<script setup>
const contents = [
//  {
//  label: 'Creating a StringBuilder object',
//  text: 'StringBuilder sb = new StringBuilder("Hello");',
//  codeEditor: true,
//  lang: 'java',
//  },
 {
 text: '<b>append(s)</b> — adds text to the end<br><code>sb.append("World") → "Hello World"</code>',
 },
 {
 text: '<b>insert(i, s)</b> — inserts text at index i<br><code>sb.insert(5, ",") → "Hello, World"</code>',
 },
 {
 text: '<b>delete(s, e)</b> — removes chars from index s to e-1<br><code>sb.delete(5, 6) → "Hello World"</code>',
 },
 {
 text: '<b>replace(s, e, str)</b> — replaces chars in range with str<br><code>sb.replace(0, 5, "Hi") → "Hi World"</code>',
 },
 {
 text: '<b>reverse()</b> — reverses the character sequence<br><code>sb.reverse() → "dlroW iH"</code>',
 },
 {
 text: '<b>toString()</b> — converts StringBuilder back to String',
 },
//  {
//  text: '<b>Why use StringBuilder?</b> It is <i>mutable</i> — modifies in place without creating new objects. Much faster for repeated string operations.',
//  highlight: true,
//  },
]
</script>

<Slide
 topic="Strings"
 sub-topic="StringBuilder (Mutable)"
 :contents="contents"
/>
