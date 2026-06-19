<script setup>
const contents = [
   { text: '<b>No Arguments and No Return Value</b>'},
  { text: '<b>Arguments and No Return Value</b>'},
  { text: '<b>No Arguments and a Return Value</b>' },
  { text: '<b>Arguments and a Return Value</b>'},
  // { text: '<b>Note:</b> A method must be defined before or after main — not inside it. Calling a method transfers control to it and resumes after it returns.', highlight: true },
]
</script>

<Slide
  topic="Methods"
  sub-topic="Methods based on arguments (parameters) and return types"
  :contents="contents"
/>