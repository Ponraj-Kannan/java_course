<script setup>
const contents = [
  { text: '<b>Documentation comment</b> — begins with <code>/**</code> and ends with <code>*/</code>. Used to generate official API documentation using the <code>javadoc</code> tool.' },
  { text: 'Written immediately above a class, method, or field. Uses special tags to describe parameters, return values, and exceptions.' },
  // {
  //   label: 'Common Javadoc tags',
  //   text: '/**\n * Calculates the area of a rectangle.\n *\n * @param length  the length of the rectangle in cm\n * @param width   the width of the rectangle in cm\n * @return        the area of the rectangle in sq cm\n */\nstatic int calculateArea(int length, int width) {\n    return length * width;\n}',
  //   codeEditor: true,
  //   lang: 'java',
  // },
  { text: '<b>@param</b> — describes a method parameter' },
  // { text: '<b>@return</b> — describes the return value' },
  { text: '<b>@author</b> — name of the author | <b>@version</b> — version of the class' },
  { text: '<b>Use documentation comments</b> for all public classes and methods in professional or team projects. IDEs like IntelliJ and Eclipse display these as tooltips.', highlight: true },
]
</script>

<Slide
  topic="Comments"
  sub-topic="Documentation Comment ( /** ... */ )"
  :contents="contents"
/>
