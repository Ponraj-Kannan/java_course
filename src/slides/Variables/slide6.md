<script setup>
const contents = [
  { text: '<b>Scope</b> — the region of the program where a variable is accessible. A variable only exists within the block <code>{ }</code> it is declared in.' },
  // {
  //   label: 'Scope examples',
  //   text: 'public class Main {\n    public static void main(String[] args) {\n\n        int x = 10; // accessible throughout main()\n\n        if (x > 5) {\n            int y = 20; // only accessible inside this if block\n            System.out.println(x + y); // OK — both visible here\n        }\n\n        // System.out.println(y); // ERROR — y is out of scope here\n\n        for (int i = 0; i < 3; i++) {\n            // i is only accessible inside this for loop\n            System.out.println(i);\n        }\n        // System.out.println(i); // ERROR — i is out of scope\n    }\n}',
  //   codeEditor: true,
  //   lang: 'java',
  // },
  { text: '<b>Rule:</b> A variable declared inside <code>{ }</code> is destroyed when the closing <code>}</code> is reached. It cannot be accessed outside that block.' },
  { text: '<b>Good practice:</b> Declare variables as close to where they are used as possible to keep scope narrow and code easier to understand.', highlight: true },
]
</script>

<Slide
  topic="Variables"
  sub-topic="Variable Scope"
  :contents="contents"
/>
