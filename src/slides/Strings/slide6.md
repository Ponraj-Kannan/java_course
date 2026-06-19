<script setup>
const contents = [
//  {
//  label: 'Creating a StringBuffer object',
//  text: 'StringBuffer sb = new StringBuffer("Hello");',
//  codeEditor: true,
//  lang: 'java',
//  },
 {
 text: '<b>append(s)</b> — adds text to the end<br><code>sb.append("World") → "Hello World"</code>',
 },
 {
 text: '<b>insert(i, s)</b> — inserts text at position i<br><code>sb.insert(5, ",") → "Hello, World"</code>',
 },
 {
 text: '<b>delete(s, e)</b> — removes characters from s to e-1<br><code>sb.delete(5, 6) → "Hello World"</code>',
 },
 {
 text: '<b>replace(s, e, str)</b> — replaces the specified range<br><code>sb.replace(0, 5, "Hi") → "Hi World"</code>',
 },
 {
 text: '<b>reverse()</b> — reverses the character sequence',
 },
 {
 text: '<b>Thread-Safe:</b> StringBuffer is <i>synchronized</i> — safe for use in multi-threaded programs.',
 highlight: true,
 },
//  {
//  text: '<b>StringBuilder vs StringBuffer:</b> Use <b>StringBuilder</b> in single-threaded apps (faster). Use <b>StringBuffer</b> in multi-threaded apps (thread-safe).',
//  highlight: true,
//  },
]
</script>

<Slide
 topic="Strings"
 sub-topic="StringBuffer (Thread-Safe)"
 :contents="contents"
/>
