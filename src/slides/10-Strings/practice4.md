<script setup>
const contents = [
  { text: '<b>Problem:</b> Trace the following Java code snippet by hand and predict the output printed to the console.' },
  { text: '<b>Code:</b><br><code>String s1 = "Java";</code><br><code>String s2 = "Java";</code><br><code>String s3 = new String("Java");</code><br><code>s1.concat("8");</code><br><code>System.out.println(s1 == s2);</code><br><code>System.out.println(s1 == s3);</code><br><code>System.out.println(s1.equals(s3));</code><br><code>System.out.println(s1);</code>' },
  { text: '<b>Expected Output:</b><br><code>true</code><br><code>false</code><br><code>true</code><br><code>Java</code>' },
  { text: '<b>Explanation:</b> <code>s1</code> and <code>s2</code> refer to the same String Pool object. <code>s3</code> is a new Heap object, so <code>s1 == s3</code> is <code>false</code> while <code>s1.equals(s3)</code> is <code>true</code>. Since Strings are immutable and the return value of <code>s1.concat("8")</code> was not reassigned, <code>s1</code> remains <code>"Java"</code>.' },
]
</script>

<Slide
  topic="Java Strings"
  sub-topic="Practice Problem 4 — Output Prediction"
  :contents="contents"
/>
