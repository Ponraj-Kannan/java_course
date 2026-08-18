---
transition: fade
---

<script setup>
const contents = [
  { text: '<b>Problem:</b> Use <b>multiple</b> <code>System.out.println()</code> statements to display your college name and current year on separate lines.' },
  {
    text: '<b>Expected Output:</b><br><code>I study at [Your College Name]</code><br><code>Year: 2024</code>'
  },
  {
    text: '<b>Note:</b> Write <b>two separate</b> <code>System.out.println()</code> statements inside the <code>main</code> method. Replace <code>[Your College Name]</code> with your actual college. Each string must be wrapped in double quotes <code>" "</code>.'
  }
]
</script>

<Slide
  topic="Getting Started with Java"
  sub-topic="Practice Problem"
  :contents="contents"
/>
