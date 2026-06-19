<script setup>
const contents = [
  { text: '<b>Scanner has no nextChar() method.</b> To read a single character, read a String and extract the first character using <code>charAt(0)</code>.' },
  // {
  //   label: 'Reading a char using Scanner',
  //   text: 'import java.util.Scanner;\n\npublic class Main {\n    public static void main(String[] args) {\n        Scanner sc = new Scanner(System.in);\n\n        System.out.print("Enter a character: ");\n        char ch = sc.next().charAt(0);\n\n        System.out.println("You entered: " + ch);\n        sc.close();\n    }\n}',
  //   codeEditor: true,
  //   lang: 'java',
  // },
  { text: '<b>How it works:</b><br>1. <code>sc.next()</code> reads the input as a String<br>2. <code>.charAt(0)</code> extracts the first character from that String' },
  { text: '<b>Example:</b> User types <code>A</code> → <code>sc.next()</code> returns <code>"A"</code> → <code>charAt(0)</code> returns <code>\'A\'</code>' },
  { text: '<b>Note:</b> If the user types more than one character, only the first character is used. The rest is ignored.', highlight: true },
]
</script>

<Slide
  topic="Input Methods"
  sub-topic="Reading char Input"
  :contents="contents"
/>
