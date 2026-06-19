<script setup>
const contents = [
  // { text: '<b>char and int</b> — a <code>char</code> is stored internally as a 16-bit unsigned integer (its Unicode / ASCII value). Casting between <code>char</code> and <code>int</code> is very common in Java.' },
  { text: '<b>char → int</b> (implicit or explicit): gives the numeric ASCII/Unicode value of the character' },
  { text: '<b>int → char</b> (explicit): gives the character whose ASCII/Unicode value equals the integer' },
  // {
  //   label: 'char and int casting examples',
  //   text: '// char → int  (get ASCII value)\nchar ch    = \'A\';\nint  ascii = ch;       // implicit widening\nSystem.out.println(ascii); // 65\n\n// Also explicit\nSystem.out.println((int) \'a\'); // 97\nSystem.out.println((int) \'0\'); // 48\n\n// int → char  (get character from ASCII)\nint  code = 66;\nchar letter = (char) code;    // explicit narrowing\nSystem.out.println(letter);   // B\n\n// Arithmetic with char\nchar next = (char)(\'A\' + 3);\nSystem.out.println(next);     // D',
  //   codeEditor: true,
  //   lang: 'java',
  // },
  // { text: '<b>Useful pattern:</b> <code>(char)(\'a\' + n)</code> gives the nth letter after \'a\'. For example, <code>(char)(\'a\' + 4)</code> gives <code>\'e\'</code>.', highlight: true },
]
</script>

<Slide
  topic="Type Casting"
  sub-topic="Casting Between char and int"
  :contents="contents"
/>
