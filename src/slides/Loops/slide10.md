<script setup>
const contents = [
  {
    label: 'Syntax',
    text: 'for (Type element : collection) {\n    // use element\n}',
    codeEditor: true,
    lang: 'java',
  },
    // {
    //   label: 'Example — print all elements of an array',
    //   text: 'int[] numbers = {10, 20, 30, 40, 50};\nfor (int num : numbers) {\n    System.out.println(num);\n}',
    //   codeEditor: true,
    //   lang: 'java',
    // },
  { text: '<b>Type</b> — data type of each element in the array or collection (e.g., <code>int</code>, <code>String</code>)' },
  { text: '<b>element</b> — a temporary variable that holds the current element during each iteration' },
  { text: '<b>collection</b> — the array or list being iterated over' },
  { text: '<b>Limitation:</b> Cannot modify array elements directly and does not provide the index. Use a regular <code>for</code> loop when index access is needed.', highlight: true },
]
</script>

<Slide
  topic="Looping Statements"
  sub-topic="For-Each Loop"
  :contents="contents"
/>
