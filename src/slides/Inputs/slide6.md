<script setup>
const contents = [
  { text: 'Multiple values can be entered on a single line separated by spaces. Scanner reads each token one at a time using the appropriate method.' },
  // {
  //   label: 'Reading multiple values on one line',
  //   text: 'import java.util.Scanner;\n\npublic class Main {\n    public static void main(String[] args) {\n        Scanner sc = new Scanner(System.in);\n\n        // User types: 10 20 30\n        System.out.print("Enter three numbers: ");\n        int a = sc.nextInt();\n        int b = sc.nextInt();\n        int c = sc.nextInt();\n\n        System.out.println("Sum = " + (a + b + c));\n        sc.close();\n    }\n}',
  //   codeEditor: true,
  //   lang: 'java',
  // },
  { text: '<b>How it works:</b> Scanner treats spaces and newlines as delimiters. Each call to <code>nextInt()</code> reads the next available integer from the stream.' },
  { text: '<b>Reading an array of inputs:</b> use a loop with <code>nextInt()</code> inside to fill an array element by element', highlight: true },
  // {
  //   label: 'Reading array input in a loop',
  //   text: 'int n = sc.nextInt();\nint[] arr = new int[n];\nfor (int i = 0; i < n; i++) {\n    arr[i] = sc.nextInt();\n}',
  //   codeEditor: true,
  //   lang: 'java',
  // },
]
</script>

<Slide
  topic="Input Methods"
  sub-topic="Multiple Inputs and Array Input"
  :contents="contents"
/>
