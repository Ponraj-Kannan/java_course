<script setup>
const contents = [
  { text: '<b>Input</b> — data provided by the user to the program at runtime, allowing programs to work with different values each time they run' },
  { text: 'Java does not have built-in input keywords like <code>print</code> — input is handled using classes from the <code>java.util</code> package' },
  { text: '<b>Most common input method:</b> the <code>Scanner</code> class — reads input from the keyboard (standard input stream <code>System.in</code>)' },
  { text: '<b>Steps to use Scanner:</b><br>1. Import <code>java.util.Scanner</code><br>2. Create a Scanner object<br>3. Call the appropriate method to read input<br>4. Close the Scanner when done' },
  // {
  //   label: 'Basic structure',
  //   text: 'import java.util.Scanner;\n\npublic class Main {\n    public static void main(String[] args) {\n        Scanner sc = new Scanner(System.in);\n\n        // read input here\n\n        sc.close();\n    }\n}',
  //   codeEditor: true,
  //   lang: 'java',
  // },
]
</script>

<Slide
  topic="Input Methods"
  sub-topic="Introduction to Java Input"
  :contents="contents"
/>
