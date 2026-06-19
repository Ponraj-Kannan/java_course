<script setup>
const contents = [
  { text: '<b>Single-line comment</b> — begins with <code>//</code> and extends to the end of that line' },
  { text: 'Everything after <code>//</code> on the same line is ignored by the compiler' },
  // {
  //   label: 'Examples',
  //   text: '// This program calculates the area of a rectangle\npublic class Main {\n    public static void main(String[] args) {\n\n        int length = 10;  // length in centimetres\n        int width  = 5;   // width in centimetres\n\n        int area = length * width; // multiply to get area\n\n        System.out.println("Area: " + area);\n    }\n}',
  //   codeEditor: true,
  //   lang: 'java',
  // },
  { text: '<b>Use single-line comments</b> to explain a specific line, label a variable, or leave a short note above a block of code', highlight: true },
]
</script>

<Slide
  topic="Comments"
  sub-topic="Single-Line Comment ( // )"
  :contents="contents"
/>
