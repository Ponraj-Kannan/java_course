---
transition: slide-up
---

<!-- ═══════════════════════════════════════════════════════
     SLIDE 2 — JAVA TIMELINE
═══════════════════════════════════════════════════════ -->

<Slide2 topic="Introduction to Java">
  <template #content>
<div class="slide-h1" style="margin-bottom:16px;">Java's <span class="highlight">Timeline</span></div>

<div style="position:relative;padding-left:24px;">
  <!-- vertical line -->
  <div style="position:absolute;left:18px;top:0;bottom:0;width:3px;background:linear-gradient(to bottom,#ef5050,#3182ce);border-radius:2px;"></div>

  <div v-click style="display:flex;gap:14px;align-items:flex-start;margin-bottom:14px;position:relative;">
    <div style="position:absolute;left:-14px;width:16px;height:16px;border-radius:50%;background:#ef5050;border:1px solid #fff;box-shadow:0 0 0 2px #ef5050;top:2px;"></div>
    <div style="padding-left:18px;">
      <div style="display:flex;align-items:center;gap:8px;">
        <span class="pill pill-red">1991–1995</span>
        <span class="slide-h3">Birth of Java</span>
      </div>
      <div class="body-text">James Gosling designs Java at Sun Microsystems for embedded devices. <strong>Java 1.0</strong> publicly released in 1995.</div>
    </div>
  </div>

  <div v-click style="display:flex;gap:14px;align-items:flex-start;margin-bottom:14px;position:relative;">
    <div style="position:absolute;left:-14px;width:16px;height:16px;border-radius:50%;background:#dd6b20;border:1px solid #fff;box-shadow:0 0 0 2px #dd6b20;top:2px;"></div>
    <div style="padding-left:18px;">
      <div style="display:flex;align-items:center;gap:8px;">
        <span class="pill pill-orange">2004</span>
        <span class="slide-h3">Java 5 (Generics era)</span>
      </div>
      <div class="body-text">Introduced generics, annotations, enums, and the enhanced for-loop. Huge leap in expressiveness.</div>
    </div>
  </div>

  <div v-click style="display:flex;gap:14px;align-items:flex-start;margin-bottom:14px;position:relative;">
    <div style="position:absolute;left:-14px;width:16px;height:16px;border-radius:50%;background:#3182ce;border:1px solid #fff;box-shadow:0 0 0 2px #3182ce;top:2px;"></div>
    <div style="padding-left:18px;">
      <div style="display:flex;align-items:center;gap:8px;">
        <span class="pill pill-blue">2014</span>
        <span class="slide-h3">Java 8 — Lambda Revolution</span>
      </div>
      <div class="body-text">Lambda expressions, Streams API, and Optional. <strong>Most widely deployed Java version ever.</strong></div>
    </div>
  </div>

  <div v-click style="display:flex;gap:14px;align-items:flex-start;position:relative;">
    <div style="position:absolute;left:-14px;width:16px;height:16px;border-radius:50%;background:#38a169;border:1px solid #fff;box-shadow:0 0 0 2px #38a169;top:2px;"></div>
    <div style="padding-left:18px;">
      <div style="display:flex;align-items:center;gap:8px;">
        <span class="pill pill-green">2024+</span>
        <span class="slide-h3">Java 21+ (LTS)</span>
      </div>
      <div class="body-text">Virtual threads, pattern matching, records, sealed classes. Java remains top-3 in every language ranking.</div>
    </div>
  </div>

</div>

<div v-click style="margin-top:14px;" class="callout callout-info">
  <div><strong>Note:</strong> Java releases a new version <strong>every 6 months</strong>. Long-Term Support (LTS) versions (8, 11, 17, 21) are recommended for production.</div>
</div>

  </template>
</Slide2>
