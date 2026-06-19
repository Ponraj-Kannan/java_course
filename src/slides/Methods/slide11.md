<script setup>
const contents = [
//   {
//     label: 'public — accessible from anywhere',
//     text: 'public int add(int a, int b) {\n    return a + b;\n}\n\n// Can be called from any class',
//     codeEditor: true,
//     lang: 'java',
//   },
//   {
//     label: 'private — accessible only within the same class',
//     text: 'private void validate() {\n    System.out.println("Validating...");\n}\n\n// Can only be called inside the same class',
//     codeEditor: true,
//     lang: 'java',
//   },
//   {
//     label: 'protected — accessible within package + subclasses',
//     text: 'protected double calculateTax(double amount) {\n    return amount * 0.18;\n}\n\n// Accessible in same package and by subclasses',
//     codeEditor: true,
//     lang: 'java',
//   },
//   {
//     label: 'default (no modifier) — accessible within the same package',
//     text: 'void display() {\n    System.out.println("Package-level access");\n}\n\n// No keyword — accessible only within the same package',
//     codeEditor: true,
//     lang: 'java',
//   },
  { text: '<b>public</b> — widest access; visible to all classes everywhere' },
  { text: '<b>private</b> — strictest access; hidden from all other classes; commonly used for helper methods' },
  { text: '<b>protected</b> — used in inheritance; subclasses can access even from a different package' },
  { text: '<b>Note:</b> If no access modifier is specified, Java applies <b>default</b> (package-private) access — the method is invisible outside its package.', highlight: true },
]
</script>

<Slide
  topic="Methods"
  sub-topic="Access Modifiers"
  :contents="contents"
/>