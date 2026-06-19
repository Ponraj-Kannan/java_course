---
layout: default
title: "Looping: Syntax & Explanation"
---

<style>
    .box1 {
        margin-top: -10px; 
        margin-left: -30px; 
        padding-bottom: 10px; 
        width: 107%; 
        max-height: 72vh; 
        color:#464646ff;
        background-color: #ffffffff; 
        font-size: .8rem; 
        font-weight: 400; 
        overflow-x: auto; 
        scrollbar-width: none; 
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
        gap: 12px;
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
        font-size: .8rem;
        line-height: 1.4;
        border-radius: 4px;
        padding: 8px 10px;
        margin: 0 0 8px 0;
        white-space: pre;
        overflow-x: auto;
    }
    .loop-note {
        font-size: .82rem;
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
    .tag-entry { background-color: #dcfce7; color: #166534; border: 1px solid #86efac; }
    .tag-exit  { background-color: #fef9c3; color: #854d0e; border: 1px solid #fde047; }
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
  /* background-color: #9F8383; */

  background-color: #ffffffff;
  margin-top: -1px;
  /* border-bottom: 1px solid #5151517b;  */
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
<h2 class="navbar-title" style="font-size: 1.5rem">Looping Statements</h2>
<img src="../assets/logo.png"/>
</div>
<div class="slide-body">
<div v-click class="intro">A <b>loop</b> repeats a block of statements as long as a given <b>condition</b> stays true. It saves us from writing the same code again and again. Java provides three looping statements: <b>for</b>, <b>while</b>, and <b>do-while</b>.</div>
<div class="loop-grid">
<div v-click class="loop-card">
<div class="loop-title">For Loop</div>
<span class="loop-tag tag-entry">Entry-controlled</span>
<pre class="loop-syntax">for (init; condition; update)
{
    // body
}</pre>
<div class="loop-note">Used when the <b>number of iterations is known</b>. The initialization, condition, and update are written together in the loop header. The condition is checked <b>before</b> each pass, so the body may run <b>zero</b> times.</div>
</div>
<div v-click class="loop-card">
<div class="loop-title">While Loop</div>
<span class="loop-tag tag-entry">Entry-controlled</span>
<pre class="loop-syntax">while (condition)
{
    // body
    // update
}</pre>
<div class="loop-note">Used when the number of iterations is <b>not known</b> in advance. The condition is tested <b>first</b>; if false at the start, the body runs <b>zero</b> times. You must update the control variable inside the body.</div>
</div>
<div v-click class="loop-card">
<div class="loop-title">Do-While Loop</div>
<span class="loop-tag tag-exit">Exit-controlled</span>
<pre class="loop-syntax">do
{
    // body
    // update
} while (condition);</pre>
<div class="loop-note">The body runs <b>first</b>, then the condition is checked. So the body always executes <b>at least once</b>, even if the condition is false. Note the <b>semicolon</b> after <code>while</code>.</div>
</div>
</div>
</div>
<div v-click class="footnote"><b>Key difference:</b> <b>for</b> and <b>while</b> are <i>entry-controlled</i> (condition checked before the body), while <b>do-while</b> is <i>exit-controlled</i> (condition checked after the body, guaranteeing one execution).</div>
</div>
