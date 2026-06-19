<script setup>
const contents = [
  { text: '<b>Control characters (0–31):</b> Non-printable. Examples: <code>9</code> = Tab, <code>10</code> = Newline, <code>13</code> = Carriage Return' },
  { text: '<b>Space:</b> <code>32</code>' },
  { text: '<b>Special characters:</b> <code>33</code> = <code>!</code> | <code>34</code> = <code>"</code> | <code>40</code> = <code>(</code> | <code>41</code> = <code>)</code> | <code>42</code> = <code>*</code> | <code>43</code> = <code>+</code> | <code>45</code> = <code>-</code>' },
  { text: '<b>Digits:</b> <code>48</code> = <code>0</code> | <code>49</code> = <code>1</code> | ... | <code>57</code> = <code>9</code>' },
  { text: '<b>Uppercase letters:</b> <code>65</code> = <code>A</code> | <code>66</code> = <code>B</code> | ... | <code>90</code> = <code>Z</code>' },
  { text: '<b>Lowercase letters:</b> <code>97</code> = <code>a</code> | <code>98</code> = <code>b</code> | ... | <code>122</code> = <code>z</code>' },
  // {
  //   label: 'Print the full ASCII table using a loop',
  //   text: 'for (int i = 32; i <= 126; i++) {\n    System.out.println(i + " = " + (char) i);\n}',
  //   codeEditor: true,
  //   lang: 'java',
  // },
  { text: '<b>Pattern to remember:</b> Lowercase = Uppercase + 32. This means <code>\'a\' = \'A\' + 32</code> and <code>\'A\' = \'a\' - 32</code>.', highlight: true },
]
</script>

<Slide
  topic="ASCII Conversion"
  sub-topic="ASCII Table — Key Values"
  :contents="contents"
/>
