<script setup>
const contents = [
  { text: '<b>char to ASCII value:</b> Cast the <code>char</code> to <code>int</code> using <code>(int)</code> or simply assign it to an <code>int</code> variable (implicit widening).' },
  { text: '<b>ASCII value to char:</b> Cast the <code>int</code> to <code>char</code> using <code>(char)</code> (explicit narrowing).' },
  // {
  //   label: 'char to ASCII and ASCII to char',
  //   text: '// char to ASCII\nchar ch1   = \'J\';\nint  val1  = (int) ch1;\nSystem.out.println(val1);  // 74\n\nchar ch2   = \'z\';\nint  val2  = ch2;          // implicit widening\nSystem.out.println(val2);  // 122\n\n// ASCII to char\nint  code1 = 77;\nchar ch3   = (char) code1;\nSystem.out.println(ch3);   // M\n\nint  code2 = 49;\nchar ch4   = (char) code2;\nSystem.out.println(ch4);   // 1  (digit character)',
  //   codeEditor: true,
  //   lang: 'java',
  // },
  { text: '<b>Case conversion using ASCII arithmetic:</b>' },
  // {
  //   label: 'Uppercase to lowercase and vice versa',
  //   text: 'char upper = \'G\';\nchar lower = (char)(upper + 32); // G → g\nSystem.out.println(lower); // g\n\nchar lc  = \'m\';\nchar uc  = (char)(lc - 32);      // m → M\nSystem.out.println(uc);    // M',
  //   codeEditor: true,
  //   lang: 'java',
  // },
  { text: '<b>Note:</b> Only apply +32 or -32 to alphabetic characters. Applying it to digits or special characters gives incorrect results.', highlight: true },
]
</script>

<Slide
  topic="Type Casting"
  sub-topic="Casting Between char and int"
  :contents="contents"
/>
