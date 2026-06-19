<script setup>
const contents = [
  { text: '<b>Reverse a String:</b> Rearrange characters so the last character comes first<br><code>reverse("Java") = "avaJ"</code>' },
  // {
  //   label: 'Recursive reverse method',
  //   text: 'static String reverse(String s) {\n    if (s.length() <= 1) { // base case\n        return s;\n    }\n    // move first character to the end\n    return reverse(s.substring(1)) + s.charAt(0);\n}\n\n// reverse("Java")\n// = reverse("ava") + \'J\'\n// = reverse("va") + \'a\' + \'J\'\n// = reverse("a") + \'v\' + \'a\' + \'J\'\n// = "a" + "v" + "a" + "J"  =  "avaJ"',
  //   codeEditor: true,
  //   lang: 'java',
  // },
  { text: '<b>Base case:</b> string length is 0 or 1 — already reversed, return as is' },
  // { text: '<b>Recursive case:</b> reverse the rest of the string, then append the first character at the end' },
  // { text: '<b>substring(1)</b> returns the string from index 1 to the end, effectively removing the first character each call', highlight: true },
]
</script>

<Slide
  topic="Recursion"
  sub-topic="Reverse a String"
  :contents="contents"
/>
