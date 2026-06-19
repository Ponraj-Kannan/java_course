<script setup>
const contents = [
  // { text: '<b>ASCII</b> — American Standard Code for Information Interchange. A standard that assigns a unique number (0–127) to each character so computers can store and transmit text.' },
  // { text: 'Every character you type — letters, digits, punctuation — has an ASCII value. Java\'s <code>char</code> type is based on Unicode, which is a superset of ASCII.' },
  { text: '<b>Key ASCII ranges to remember:</b><br><b>Digits:</b> <code>\'0\'</code> = 48 to <code>\'9\'</code> = 57<br><b>Uppercase:</b> <code>\'A\'</code> = 65 to <code>\'Z\'</code> = 90<br><b>Lowercase:</b> <code>\'a\'</code> = 97 to <code>\'z\'</code> = 122' },
  { text: '<b>Gap between uppercase and lowercase:</b> 32. So <code>\'a\' - \'A\' = 32</code>. This is the basis for case conversion.' },
  // {
  //   label: 'Verifying ASCII values in Java',
  //   text: 'System.out.println((int) \'0\'); // 48\nSystem.out.println((int) \'A\'); // 65\nSystem.out.println((int) \'a\'); // 97\nSystem.out.println((int) \' \'); // 32  (space)\nSystem.out.println((int) \'\\n\');// 10  (newline)',
  //   codeEditor: true,
  //   lang: 'java',
  // },
  { text: '<b>In Java:</b> Casting a <code>char</code> to <code>int</code> gives its ASCII value. Casting an <code>int</code> to <code>char</code> gives the corresponding character.', highlight: true },
]
</script>

<Slide
  topic="Type Casting"
  sub-topic="Casting Between char and int"
  :contents="contents"
/>
