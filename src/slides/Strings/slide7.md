<Slide
 topic="Strings"
 sub-topic="String vs StringBuilder vs StringBuffer"
 :contents="[
 { text: '<b>Comparison Table</b>', highlight: true },
 { text: '<b>String</b> — Immutable | Not thread-safe | Slowest for modifications | Stored in String Pool'},
 { text: '<b>StringBuilder</b> — Mutable | Not thread-safe | Fastest | Best for single-threaded apps'},
 { text: '<b>StringBuffer</b> — Mutable | Thread-safe | Moderate speed | Best for multi-threaded'},
 { text: '<b>Rule of thumb:</b> Read-only text → <b>String</b> | Loop/frequent changes → <b>StringBuilder</b> | Concurrent access → <b>StringBuffer</b>', highlight: true },
 { text: 'All three share similar methods: <code>append()</code>, <code>insert()</code>, <code>delete()</code>, <code>replace()</code>, <code>reverse()</code>, <code>length()</code>, <code>charAt()</code>'},
 ]"
/>
