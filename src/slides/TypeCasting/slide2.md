<script setup>
const contents = [
  // {
  //   label: 'char → int (ASCII value)',
  //   text: 'char ch = \'A\';\nint ascii = ch;           // widening: no cast needed\nSystem.out.println(ascii); // 65\n\nchar lower = \'a\';\nSystem.out.println((int) lower); // 97',
  //   codeEditor: true,
  //   lang: 'java',
  // },
  // {
  //   label: 'int → char (ASCII to character)',
  //   text: 'int code = 66;\nchar letter = (char) code;    // narrowing: cast required\nSystem.out.println(letter);   // B\n\nSystem.out.println((char) 65); // A\nSystem.out.println((char) 97); // a',
  //   codeEditor: true,
  //   lang: 'java',
  // },
  { text: '<b>char → int</b> — widening; Java automatically reads the ASCII/Unicode value of the character' },
  { text: '<b>int → char</b> — narrowing; requires explicit cast <code>(char)</code>; maps the integer to its ASCII character' },
  // { text: '<b>Key ASCII values:</b> A=65, Z=90 &nbsp;|&nbsp; a=97, z=122 &nbsp;|&nbsp; 0=48, 9=57' },
  { text: '<b>Tip:</b> <code>\'A\' + 1</code> gives <code>66</code> (int), not <code>\'B\'</code>. Cast back: <code>(char)(\'A\' + 1)</code> → <code>\'B\'</code>', highlight: true },
]
</script>

<Slide
  topic="Type Casting"
  sub-topic="char ↔ int — ASCII Conversion"
  :contents="contents"
/>
