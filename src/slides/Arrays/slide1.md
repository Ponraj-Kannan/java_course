<script setup>
const contents = [
  {
    label: 'Declaration with size',
    text: '// Declaration\nint[] arr = new int[5];',
    codeEditor: true,
    lang: 'java',
  },
  // {
  //   label: 'Declaration with values',
  //   text: '// Initialization at declaration\nint[] arr = {10, 20, 30, 40, 50};',
  //   codeEditor: true,
  //   lang: 'java',
  // },
  { text: '<b>int</b> — data type of each element' },
  { text: '<b>[]</b> — declares the variable as an array' },
  { text: '<b>arr</b> — variable name (identifier)' },
  { text: '<b>new int[5]</b> — allocates memory for 5 integer elements in heap' },
  { text: '<b>Default values:</b> int → 0, double → 0.0, boolean → false, String → null' },
  // { text: '<b>Access:</b> arr[0] — reads element at index 0<br><b>Update:</b> arr[0] = 99 — writes value at index 0' },
  { text: '<b>Index range:</b> 0 to length-1. Accessing arr[5] on a 5-element array throws ArrayIndexOutOfBoundsException.', highlight: true },
]
</script>

<Slide
  topic="Arrays"
  sub-topic="One-Dimensional Arrays"
  :contents="contents"
/>
