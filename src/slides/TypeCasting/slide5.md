<script setup>
const contents = [
  // {
  //   label: 'String to int / double',
  //   text: 'String s1 = "42";\nint n = Integer.parseInt(s1);      // 42\n\nString s2 = "3.14";\ndouble d = Double.parseDouble(s2); // 3.14\n\nSystem.out.println(n + 1);  // 43\nSystem.out.println(d + 1);  // 4.14',
  //   codeEditor: true,
  //   lang: 'java',
  // },
  // {
  //   label: 'int / double to String',
  //   text: 'int age = 20;\nString s1 = String.valueOf(age);   // "20"\nString s2 = Integer.toString(age); // "20"\nString s3 = "" + age;              // "20"\n\nSystem.out.println(s1 + " years"); // 20 years',
  //   codeEditor: true,
  //   lang: 'java',
  // },
  { text: '<b>Integer.parseInt(str)</b> — converts a numeric String to <code>int</code>' },
  { text: '<b>Double.parseDouble(str)</b> — converts a numeric String to <code>double</code>' },
  { text: '<b>String.valueOf(n)</b> — converts any primitive to <code>String</code>' },
  { text: '<b>Note:</b> Passing a non-numeric string like <code>"abc"</code> to <code>parseInt()</code> throws <code>NumberFormatException</code> at runtime.', highlight: true },
]
</script>

<Slide
  topic="Type Casting"
  sub-topic="String ↔ Primitive Conversion"
  :contents="contents"
/>
