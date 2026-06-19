<script setup>
const contents = [
 {
 label: 'String literal (stored in String Pool)',
 text: 'String s1 = "Hello";',
 codeEditor: true,
 lang: 'java',
 },
 {
 text: '<b>String Pool:</b> Reuses existing string objects — memory efficient'
 },
 {
 label: 'Using new keyword (stored in Heap memory)',
 text: 'String s2 = new String("Hello");',
 codeEditor: true,
 lang: 'java',
 },
 {
 text: '<b>Heap:</b> Always creates a new object, even if value already exists'
 },
 {
 text: '<b>Immutable:</b> Once created, a String\'s value cannot be changed. Operations return a <i>new</i> String.',  highlight: true
 },
//  {
//  text: 'Use <b>String</b> for read-only text, <b>StringBuilder</b> for mutable text',
//  },
]
</script>

<Slide
 topic="Strings"
 sub-topic="Declaration & Memory Model"
 :contents="contents"
/>
