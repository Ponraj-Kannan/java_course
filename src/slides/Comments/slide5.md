<script setup>
const contents = [
  { text: '<b>Single-line</b> <code>//</code> — one line only | used for inline notes and short explanations | most commonly used' },
  { text: '<b>Multi-line</b> <code>/* ... */</code> — spans multiple lines | used for longer descriptions or temporarily disabling code' },
  { text: '<b>Documentation</b> <code>/** ... */</code> — spans multiple lines | used with <code>javadoc</code> to generate HTML documentation | supports special tags like <code>@param</code> and <code>@return</code>' },
  // {
  //   label: 'All three types in one program',
  //   text: '/**\n * Main class for the grading application.\n * @author Student\n */\npublic class Main {\n\n    /*\n       Entry point of the program.\n       Reads marks and prints the grade.\n    */\n    public static void main(String[] args) {\n        int marks = 85; // student marks out of 100\n         System.out.println("Grade: A");\n    }\n}',
  //   codeEditor: true,
  //   lang: 'java',
  // },
  { text: '<b>Rule of thumb:</b> Use <code>//</code> for daily code, <code>/* */</code> for blocks, and <code>/** */</code> for all public APIs and class-level descriptions.', highlight: true }
]
</script>

<Slide
  topic="Comments"
  sub-topic="Comparison of Comment Types"
  :contents="contents"
/>
