---
transition: slide-up
---

<script setup>
const contents = [
  { text: '<b>Problem:</b> Write a complete Java program that takes a student\'s <code>name</code> and <code>marks</code> (0–100). Use an <code>if-else-if</code> ladder to calculate the letter <b>Grade</b>, and a <code>switch</code> statement to determine the <b>Academic Remark</b>.' },
  { text: '<b>Input:</b><br><code>Name: Priya</code><br><code>Marks: 85</code>' },
  {
    text: '<b>Expected Output:</b><br><code>--- Student Report Card ---</code><br><code>Name &nbsp;&nbsp;: Priya</code><br><code>Marks &nbsp;: 85</code><br><code>Grade &nbsp;: A</code><br><code>Remark : Excellent Performance</code><br><br><b>Grade & Remark Rules:</b><br>• <code>90–100</code> → Grade \'S\' → "Outstanding"<br>• <code>80–89</code> &nbsp;→ Grade \'A\' → "Excellent Performance"<br>• <code>70–79</code> &nbsp;→ Grade \'B\' → "Good Job"<br>• <code>50–69</code> &nbsp;→ Grade \'C\' → "Satisfactory"<br>• <code>0–49</code> &nbsp;&nbsp;→ Grade \'F\' → "Needs Improvement"'
  },
  {
    text: '<b>Key Concepts:</b> Use <code>if-else-if</code> ladder for range checking (marks), assign a char grade, then use <code>switch (grade)</code> to select the remark string before printing the report.'
  }
]
</script>

<Slide
  topic="Decision-making statements"
  sub-topic="Practice Problem"
  :contents="contents"
/>
