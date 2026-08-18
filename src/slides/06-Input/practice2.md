<script setup>
const contents = [
  { text: '<b>Problem:</b> Write a Java program using <code>BufferedReader</code> and <code>StringTokenizer</code> to read three space-separated integers on a single line and print their sum.' },
  { text: '<b>Input:</b> <code>"15 25 35"</code>' },
  { text: '<b>Expected Output:</b> <code>Sum = 75</code>' },
  { text: '<b>Key Concepts:</b> Instantiate <code>BufferedReader</code> with <code>InputStreamReader(System.in)</code>, read the line with <code>br.readLine()</code>, tokenize it with <code>new StringTokenizer(line)</code>, convert tokens with <code>Integer.parseInt(st.nextToken())</code>, and handle <code>throws IOException</code>.' },
]
</script>

<Slide
  topic="Java Input Methods"
  sub-topic="Practice Problem 2 — Fast Sum with BufferedReader"
  :contents="contents"
/>
