---
transition: fade
---

<script setup>
const contents = [
  {
    text: '<b>public class Main</b> — Every Java program lives inside a class. The class name must match the filename.'
  },
  {
    text: '<b>public static void main(String[] args)</b> — The entry point. Java always starts executing from here.'
  },
  {
    text: '<b>System.out.println()</b> — Prints text to the console followed by a newline.'
  }
]
</script>

<Slide
  topic="Getting Started with Java"
  sub-topic="First Program in Java"
  :contents="contents"
/>
