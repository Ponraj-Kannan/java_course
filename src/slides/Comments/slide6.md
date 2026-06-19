<script setup>
const contents = [
  { text: '<b>Write comments that explain WHY, not WHAT</b> — the code itself shows what is happening; comments should explain the reasoning behind it' },
  { text: '<b>Keep comments up to date</b> — an outdated comment that contradicts the code is worse than no comment at all' },
  { text: '<b>Do not over-comment</b> — clear, well-named variables and methods reduce the need for comments' },
  // { text: '<b>Use comments to mark TODOs</b> — <code>// TODO: validate user input before processing</code>' },
  { text: '<b>Avoid commented-out code in final submissions</b> — remove unused code rather than leaving it commented out permanently' },
  // {
  //   label: 'Good vs bad commenting',
  //   text: '// BAD: obvious comment\nint age = 20; // set age to 20\n\n// GOOD: explains intent\nint age = 20; // minimum age required for voter registration',
  //   codeEditor: true,
  //   lang: 'java',
  // },
]
</script>

<Slide
  topic="Comments"
  sub-topic="Best Practices"
  :contents="contents"
/>
