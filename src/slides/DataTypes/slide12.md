<script setup>
const contents = [
  { text: '<b>Problem:</b> Demonstrate integer overflow by storing a value one greater than the maximum value of <code>byte</code> and <code>int</code>, and observe what happens.' },
  { text: '<b>Expected Output:</b><br><code>byte max      : 127</code><br><code>byte overflow : -128</code><br><code>int max       : 2147483647</code><br><code>int overflow  : -2147483648</code>' },
  { text: '<b>What is overflow?</b> When a value exceeds the maximum a type can hold, it wraps around to the minimum value. This is called integer overflow.' },
  // {
  //   label: 'Overflow example code',
  //   text: 'byte maxByte  = 127;\nbyte overflow = (byte)(maxByte + 1); // wraps to -128\n\nint maxInt    = Integer.MAX_VALUE;\nint overInt   = maxInt + 1;          // wraps to -2147483648\n\nSystem.out.println("byte max      : " + maxByte);\nSystem.out.println("byte overflow : " + overflow);\nSystem.out.println("int max       : " + maxInt);\nSystem.out.println("int overflow  : " + overInt);',
  //   codeEditor: true,
  //   lang: 'java',
  // },
  { text: '<b>Lesson:</b> Always choose a data type whose range comfortably fits the expected values to avoid silent overflow bugs.', highlight: true },
]
</script>

<Slide
  topic="Data Types"
  sub-topic="Practice Problem 3 — Integer Overflow"
  :contents="contents"
/>
