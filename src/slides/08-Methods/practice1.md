<script setup>
const contents = [
  { text: '<b>Problem:</b> Write a Java class with overloaded static methods named <code>calculateArea</code> to compute the area of:<br>1. A square: <code>calculateArea(double side)</code><br>2. A rectangle: <code>calculateArea(double length, double width)</code><br>3. A circle: <code>calculateArea(double radius, boolean isCircle)</code>' },
  { text: '<b>Sample Calls:</b><br><code>calculateArea(4.0)</code><br><code>calculateArea(4.0, 5.0)</code><br><code>calculateArea(3.0, true)</code>' },
  { text: '<b>Expected Outputs:</b><br><code>Square Area = 16.0</code><br><code>Rectangle Area = 20.0</code><br><code>Circle Area ≈ 28.27</code>' },
]
</script>

<Slide
  topic="Methods"
  sub-topic="Practice Problem 1 — Method Overloading"
  :contents="contents"
/>
