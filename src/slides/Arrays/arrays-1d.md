---
layout: default
title: "Arrays (1D): Concept & Syntax"
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
        font-size: .9rem;
        color: #374151;
        background-color: #e2f0feff;
        border: 1px solid #a9c4d2ff;
        padding: 8px 12px;
        margin: 12px 10px 8px 10px;
    }
    .decl { padding: 0 10px; margin-bottom: 8px; }
    .panel-title {
        font-size: .9rem;
        font-weight: 700;
        border-radius: 4px;
        padding: 4px 10px;
        margin-bottom: 6px;
        background-color: #ff914d4e;
        border: 1px solid #ff914dd3;
        color: #b3531f;
        display: inline-block;
    }
    .loop-syntax {
        background-color: #1e1e1e;
        color: #e6e6e6;
        font-family: 'Consolas', 'Courier New', monospace;
        font-size: .78rem;
        line-height: 1.55;
        border-radius: 4px;
        padding: 10px 12px;
        margin: 0;
        white-space: pre;
        overflow-x: auto;
    }
    .diagram { padding: 0 10px; margin-bottom: 8px; }
    .char-row { display: flex; flex-direction: row; gap: 6px; align-items: flex-end; }
    .char-cell { display: flex; flex-direction: column; align-items: center; }
    .char-box {
        width: 46px;
        height: 38px;
        border: 1px solid #b9d4f5;
        background-color: #eaf2fe;
        color: #1e40af;
        border-radius: 6px;
        display: flex;
        align-items: center;
        justify-content: center;
        font-family: 'Consolas', 'Courier New', monospace;
        font-size: 1rem;
        font-weight: 700;
    }
    .char-idx { font-size: .72rem; color: #6b7280; margin-top: 3px; }
    .cap { font-size: .76rem; color: #4b4b4b; margin-top: 6px; }
    .loop-grid {
        display: flex;
        flex-direction: row;
        flex-wrap: wrap;
        gap: 10px;
        padding: 0 10px;
        align-items: stretch;
    }
    .loop-card {
        flex: 1 1 30%;
        min-width: 180px;
        border: 1px solid #cbd5e1;
        border-radius: 6px;
        padding: 10px;
        display: flex;
        flex-direction: column;
    }
    .loop-title {
        font-size: .95rem;
        font-weight: 700;
        text-align: center;
        border-radius: 4px;
        padding: 5px 10px;
        margin-bottom: 8px;
        background-color: #ff914d4e;
        border: 1px solid #ff914dd3;
        color: #b3531f;
    }
    .loop-note {
        font-size: .8rem;
        color: #374151;
        line-height: 1.45;
    }
    .footnote {
        font-size: .8rem;
        color: #374151;
        background-color: #f8fafc;
        border-left: 4px solid #ef5050ff;
        padding: 8px 12px;
        margin: 12px 10px 0 10px;
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
<h2 class="navbar-title" style="font-size: 1.5rem;">Arrays</h2>
<img src="../assets/logo.png"/>
</div>
<div class="slide-body">
<div v-click class="intro"><b>One-Dimensional Arrays</b> is a collection of <b>multiple values of the same type</b> stored together under <b>one variable name</b>. Each value (called an <b>element</b>) is reached by its <b>index</b> &mdash; its position in the array.</div>
<div v-click class="decl">
<div class="panel-title">Declaration &amp; syntax</div>
<pre class="loop-syntax">int[] a = new int[5];              // 5 ints, all default 0
int[] b = {10, 20, 30, 40, 50};    // declare + initialize
int x = b[2];                      // read element   ->  30
int n = b.length;                  // number of elements -> 5</pre>
</div>
<div v-click class="diagram">
<div class="panel-title">Elements are indexed (start at 0)</div>
<div class="char-row">
<div class="char-cell"><div class="char-box">10</div><div class="char-idx">0</div></div>
<div class="char-cell"><div class="char-box">20</div><div class="char-idx">1</div></div>
<div class="char-cell"><div class="char-box">30</div><div class="char-idx">2</div></div>
<div class="char-cell"><div class="char-box">40</div><div class="char-idx">3</div></div>
<div class="char-cell"><div class="char-box">50</div><div class="char-idx">4</div></div>
</div>
<div class="cap">Array <code>b</code> has <b>5</b> elements at indices <b>0 to 4</b>. So <code>b[0]</code> is <b>10</b> (first) and <code>b[4]</code> (length-1) is <b>50</b> (last).</div>
</div>
<div class="loop-grid">
<div v-click class="loop-card">
<div class="loop-title">Fixed size</div>
<div class="loop-note">The size is decided <b>when the array is created</b> and <b>cannot change</b> later. A size-5 array always holds 5 elements.</div>
</div>
<div v-click class="loop-card">
<div class="loop-title">Same data type</div>
<div class="loop-note">Every element must be of the <b>same type</b> (e.g. all <code>int</code>, or all <code>String</code>). You cannot mix types.</div>
</div>
<div v-click class="loop-card">
<div class="loop-title">length</div>
<div class="loop-note"><code>b.length</code> gives the <b>number of elements</b> (here 5). Valid indices run from <b>0</b> to <b>length - 1</b>.</div>
</div>
<div v-click class="footnote"><b>In short:</b> a 1D array stores many values of the <b>same type</b> in one variable, has a <b>fixed size</b>, and each element is accessed by a <b>0-based index</b> from <code>0</code> to <code>length - 1</code>.</div>
</div>
</div>
</div>
