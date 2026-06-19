---
layout: default
title: "Decision Making: Syntax & Explanation"
---

<style>
    .box1 {
        margin-top: -10px; 
        margin-left: -30px; 
        padding-bottom: 10px; 
        width: 107%; 
        max-height: 480px; 
        color:#464646ff;
        background-color: #ffffffff; 
        font-size: .8rem; 
        font-weight: 400; 
        overflow-x: auto; 
        scrollbar-width: thin; 
        overflow-y: auto;
    }
    .box2{
        display: flex; 
        flex-direction:row; 
        justify-content: space-between; 
        align-items:center; 
        gap: 0.75rem; 
        padding:0px 10px; 
        color: #ffffff; 
        margin-bottom: 4px; 
    }
    .box2 > img {
        height: 30px;
    }
    .box3{
        margin: 0; 
        font-size: 1.5rem; 
        font-weight: 700; 
        background-color: #ef5050ff; 
        color: #ffffffff; 
        width: 80%; 
        padding-left:10px; 
        margin-left:-10px
    }
    .intro {
        border-radius: 4px;
        font-size: .95rem;
        color: #374151;
        background-color: #e2f0feff;
        border: 1px solid #a9c4d2ff;
        padding: 8px 12px;
        margin: 14px 10px;
    }
    .loop-grid {
        display: flex;
        flex-direction: row;
        gap: 10px;
        padding: 0px 10px;
        align-items: stretch;
    }
    .loop-card {
        flex: 1;
        border: 1px solid #cbd5e1;
        border-radius: 6px;
        padding: 10px;
        display: flex;
        flex-direction: column;
    }
    .loop-title {
        font-size: 1rem;
        font-weight: 700;
        text-align: center;
        border-radius: 4px;
        padding: 5px 10px;
        margin-bottom: 8px;
        background-color: #ff914d4e;
        border: 1px solid #ff914dd3;
        color: #b3531f;
    }
    .loop-syntax {
        background-color: #1e1e1e;
        color: #e6e6e6;
        font-family: 'Consolas', 'Courier New', monospace;
        font-size: .75rem;
        line-height: 1.4;
        border-radius: 4px;
        padding: 8px 10px;
        margin: 0 0 8px 0;
        white-space: pre;
        overflow-x: auto;
    }
    .loop-note {
        font-size: .8rem;
        color: #374151;
        line-height: 1.4;
    }
    .loop-tag {
        display: inline-block;
        font-size: .7rem;
        font-weight: 600;
        border-radius: 3px;
        padding: 1px 6px;
        margin-bottom: 6px;
    }
    .tag-one   { background-color: #dcfce7; color: #166534; border: 1px solid #86efac; }
    .tag-two   { background-color: #dbeafe; color: #1e40af; border: 1px solid #93c5fd; }
    .tag-multi { background-color: #fef9c3; color: #854d0e; border: 1px solid #fde047; }
    .footnote {
        font-size: .82rem;
        color: #374151;
        background-color: #f8fafc;
        border-left: 4px solid #ef5050ff;
        padding: 8px 12px;
        margin: 14px 10px 0 10px;
        border-radius: 0 4px 4px 0;
    }

    .slide-wrapper {
  margin-top: -10px;
  margin-left: -30px;
  width: 107%;
  max-height: 65vh;
  font-size: 0.8rem;
  font-weight: 400;
  overflow-x: auto;
  overflow-y: auto;
  scrollbar-width: none;

  /* background-color: #9B8EC7; */
}

.navbar {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: center;
  gap: 0.75rem;
  padding: 0 10px;
  color: #ffffff;
  position: fixed;
  width: 94.7%;
}

.navbar > img {
  height: 30px;
}

.navbar-title {
  margin: 0;
  font-size: 1.5rem;
  font-weight: 700;
  background-color: #ef5050;
  color: #ffffff;
  width: 80%;
  padding-left: 10px;
  margin-left: -10px;
  border-radius: 5px;
}

.slide-body {
  display: flex;
  flex-direction: column;
  border-radius: 4px;

  /* background-color: cornflowerblue; */
  margin-top: 36px;
} 
</style>

<div class="slide-wrapper">
<div class="navbar">
<h2 class="navbar-title" style="font-size: 1.5rem;">Decision Making</h2>
<img src="../assets/logo.png"/>
</div>
<div class="slide-body">
<div v-click class="intro">A <b>decision-making</b> statement lets a program <b>choose</b> which block of code to run based on a <b>condition</b> (true or false). Java provides <b>if</b>, <b>if-else</b>, the <b>else-if ladder</b>, and <b>switch</b>.</div>
<div class="loop-grid">
<div v-click class="loop-card">
<div class="loop-title">if</div>
<span class="loop-tag tag-one">One-way</span>
<pre class="loop-syntax">if (condition)
{
    // runs only
    // if true
}</pre>
<div class="loop-note">Runs the block <b>only when</b> the condition is true. If it is false, the block is <b>skipped</b>.</div>
</div>
<div v-click class="loop-card">
<div class="loop-title">if-else</div>
<span class="loop-tag tag-two">Two-way</span>
<pre class="loop-syntax">if (condition)
{
    // true block
}
else
{
    // false block
}</pre>
<div class="loop-note">Chooses between <b>two</b> paths: one block runs when true, the other when false. Exactly one runs.</div>
</div>
<div v-click class="loop-card">
<div class="loop-title">else-if ladder</div>
<span class="loop-tag tag-multi">Multi-way</span>
<pre class="loop-syntax">if (cond1)
{ ... }
else if (cond2)
{ ... }
else
{ ... }</pre>
<div class="loop-note">Tests conditions <b>top to bottom</b>. The first true block runs; if none match, the final <b>else</b> runs.</div>
</div>
<div v-click class="loop-card">
<div class="loop-title">switch</div>
<span class="loop-tag tag-multi">Multi-way</span>
<pre class="loop-syntax">switch (expr)
{
  case v1:
    // ...
    break;
  default:
    // ...
}</pre>
<div class="loop-note">Compares one value against many <b>cases</b>. Use <b>break</b> to stop fall-through; <b>default</b> handles no match.</div>
</div>
</div>
</div>
<div v-click class="footnote"><b>When to use what:</b> use <b>if</b> / <b>if-else</b> for one or two outcomes and range checks (e.g. <code>marks &gt; 50</code>); use the <b>else-if ladder</b> for several conditions; use <b>switch</b> when comparing a single variable against many fixed constant values.</div>
</div>
