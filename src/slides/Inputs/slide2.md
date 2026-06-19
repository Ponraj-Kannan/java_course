<script setup>
const contents = [
  // { text: '<b>Scanner</b> — a class in <code>java.util</code> that reads input from various sources: keyboard, file, or string' },
  { text: '<b>Step 1 — Import:</b> <code>import java.util.Scanner;</code><br>Must be written before the class declaration' },
  { text: '<b>Step 2 — Create object:</b> <code>Scanner sc = new Scanner(System.in);</code><br><code>System.in</code> tells the Scanner to read from the keyboard' },
  { text: '<b>Step 3 — Read input:</b> call the appropriate method depending on the data type expected' },
  { text: '<b>Step 4 — Close:</b> <code>sc.close();</code> — releases the system resource. Always close the Scanner when input reading is complete.' },
  // {
  //   label: 'Scanner object with a prompt message',
  //   text: 'import java.util.Scanner;\n\npublic class Main {\n    public static void main(String[] args) {\n        Scanner sc = new Scanner(System.in);\n\n        System.out.print("Enter your name: ");\n        String name = sc.nextLine();\n\n        System.out.println("Hello, " + name + "!");\n\n        sc.close();\n    }\n}',
  //   codeEditor: true,
  //   lang: 'java',
  // },
  // { text: '<b>Convention:</b> Use <code>System.out.print()</code> (without newline) for the prompt so the cursor stays on the same line as the user types.', highlight: true },
]
</script>

<Slide
  topic="Input Methods"
  sub-topic="Scanner — Setup and Object Creation"
  :contents="contents"
/>
