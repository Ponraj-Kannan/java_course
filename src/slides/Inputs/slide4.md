<script setup>
const contents = [
  { text: '<b>next()</b> — reads one token (word). Stops reading at the first whitespace character. Does not consume the newline.' },
  { text: '<b>nextLine()</b> — reads the entire line until the Enter key is pressed. Consumes the newline character at the end.' },
  // {
  //   label: 'Difference between next() and nextLine()',
  //   text: 'Scanner sc = new Scanner(System.in);\n\n// Input: "Hello World"\nString word = sc.next();     // reads "Hello" only\nString rest = sc.nextLine(); // reads " World" (rest of line)\n\nSystem.out.println(word); // Hello\nSystem.out.println(rest); // (space)World',
  //   codeEditor: true,
  //   lang: 'java',
  // },
  { text: '<b>Common problem — phantom newline:</b> After calling <code>nextInt()</code>, a newline character (<code>\\n</code>) is left in the input buffer. If <code>nextLine()</code> is called immediately after, it reads that leftover newline instead of the user\'s next input.' },
  // {
  //   label: 'Fix — consume the leftover newline',
  //   text: 'int age = sc.nextInt();\nsc.nextLine(); // consume the leftover newline\nString name = sc.nextLine(); // now reads correctly',
  //   codeEditor: true,
  //   lang: 'java',
  // },
  { text: '<b>Rule:</b> Always add <code>sc.nextLine()</code> after any <code>nextInt()</code>, <code>nextDouble()</code>, or similar call if you plan to use <code>nextLine()</code> next.', highlight: true },
]
</script>

<Slide
  topic="Input Methods"
  sub-topic="next() vs nextLine()"
  :contents="contents"
/>
