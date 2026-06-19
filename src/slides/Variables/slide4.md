<script setup>
const contents = [
  // { text: '<b>Rules (enforced by the compiler — must follow):</b>' },
  { text: 'Must start with a letter (<code>a–z</code>, <code>A–Z</code>), underscore (<code>_</code>), or dollar sign (<code>$</code>). Cannot start with a digit.' },
  { text: 'Can contain letters, digits, underscores, and dollar signs after the first character.' },
  { text: 'Cannot use Java reserved keywords (e.g., <code>int</code>, <code>class</code>, <code>if</code>) as variable names.' },
  { text: 'Case-sensitive — <code>age</code>, <code>Age</code>, and <code>AGE</code> are three different variables.' },
  // {
  //   label: 'Valid and invalid variable names',
  //   text: '// Valid names\nint age;\nint _count;\nint totalMarks;\nint $value;\nint age2;\n\n// Invalid names\nint 2age;      // starts with a digit\nint my-name;   // hyphen not allowed\nint class;     // reserved keyword\nint my name;   // space not allowed',
  //   codeEditor: true,
  //   lang: 'java',
  // },
  { text: '<b>Conventions (best practices — should follow):</b> Use camelCase for variable names (<code>firstName</code>, <code>totalMarks</code>). Use meaningful names. Avoid single letters except for loop counters (<code>i</code>, <code>j</code>).', highlight: true },
]
</script>

<Slide
  topic="Variables"
  sub-topic="Naming Rules and Conventions"
  :contents="contents"
/>
