---
transition: fade
---

<script setup>
const contents = [
  { text: '<b>Problem:</b> Write your very first Java program! Use <code>System.out.println()</code> to display your name on the screen.' },
  {
    text: '<b>Expected Output:</b><br><code>My name is [Your Name]</code>'
  },
  {
    text: '<b>Note:</b> Create a class named <code>MyName</code>, add the <code>main</code> method, and use <code>System.out.println()</code>. Save as <code>MyName.java</code>. Remember every statement ends with a <code>;</code>'
  }
]
</script>

<Slide
  topic="Getting Started with Java"
  sub-topic="Practice Problem"
  :contents="contents"
/>
