<script setup>
const contents = [
  // {
  //   label: 'ASCII table — key ranges',
  //   text: '// Digits\nSystem.out.println((int) \'0\'); // 48\nSystem.out.println((int) \'9\'); // 57\n\n// Uppercase letters\nSystem.out.println((int) \'A\'); // 65\nSystem.out.println((int) \'Z\'); // 90\n\n// Lowercase letters\nSystem.out.println((int) \'a\'); // 97\nSystem.out.println((int) \'z\'); // 122',
  //   codeEditor: true,
  //   lang: 'java',
  // },
  // {
  //   label: 'Uppercase ↔ Lowercase conversion',
  //   text: 'char upper = \'G\';\nchar lower = (char) (upper + 32); // G → g\nSystem.out.println(lower); // g\n\nchar lc = \'m\';\nchar uc = (char) (lc - 32);       // m → M\nSystem.out.println(uc); // M',
  //   codeEditor: true,
  //   lang: 'java',
  // },
  { text: '<b>Digits 0–9</b> — ASCII 48 to 57' },
  { text: '<b>Uppercase A–Z</b> — ASCII 65 to 90' },
  { text: '<b>Lowercase a–z</b> — ASCII 97 to 122' },
  // { text: '<b>Case conversion trick:</b> Lowercase = Uppercase + 32 &nbsp;|&nbsp; Uppercase = Lowercase − 32', highlight: true },
]
</script>

<Slide
  topic="Type Casting"
  sub-topic="ASCII Table & Case Conversion"
  :contents="contents"
/>
