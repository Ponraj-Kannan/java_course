---
layout: default
title: "Arrays (2D): Concept & Syntax"
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
    .body-row { display: flex; flex-direction: row; gap: 14px; padding: 0 10px; align-items: flex-start; }
    .col-left { flex: 0 0 52%; }
    .col-right { flex: 1; }
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
        font-size: .74rem;
        line-height: 1.55;
        border-radius: 4px;
        padding: 10px 12px;
        margin: 0;
        white-space: pre;
        overflow-x: auto;
    }
    .grid-row { display: flex; flex-direction: row; gap: 6px; align-items: center; margin-bottom: 6px; }
    .rlabel { width: 50px; text-align: right; font-size: .72rem; color: #6b7280; font-family: 'Consolas', 'Courier New', monospace; }
    .chead { width: 42px; text-align: center; font-size: .72rem; color: #6b7280; font-family: 'Consolas', 'Courier New', monospace; }
    .cell {
        width: 42px;
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
    .cap { font-size: .76rem; color: #4b4b4b; margin-top: 4px; }
    .loop-grid {
        display: flex;
        flex-direction: row;
        flex-wrap: wrap;
        gap: 10px;
        padding: 8px 10px 0 10px;
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
<div v-click class="intro"><b>Two-Dimensional Arrays</b> arranges values in <b>rows and columns</b>, like a table or <b>matrix</b>. Each element needs <b>two indices</b> &mdash; the <b>row</b> first, then the <b>column</b>: <code>a[row][col]</code>.</div>
<div class="body-row">
<div class="col-left">
<div v-click class="panel-title">Declaration &amp; syntax</div>
<pre v-click class="loop-syntax">int[][] a = new int[2][3];               // 2 rows, 3 cols (all 0)
int[][] b = { {1, 2, 3}, {4, 5, 6} };    // declare + initialize
int x    = b[1][2];                      // row 1, col 2  ->  6
int rows = b.length;                     // number of rows -> 2
int cols = b[0].length;                  // cols per row   -> 3</pre>
</div>
<div class="col-right">
<div v-click class="panel-title">Rows &amp; columns</div>
<div v-click class="grid-row"><div class="rlabel"></div><div class="chead">col 0</div><div class="chead">col 1</div><div class="chead">col 2</div></div>
<div v-click class="grid-row"><div class="rlabel">row 0</div><div class="cell">1</div><div class="cell">2</div><div class="cell">3</div></div>
<div v-click class="grid-row"><div class="rlabel">row 1</div><div class="cell">4</div><div class="cell">5</div><div class="cell">6</div></div>
<div v-click class="cap"><code>b[1][2]</code> = row 1, col 2 = <b>6</b></div>
</div>
</div>
<div class="loop-grid">
<div v-click class="loop-card">
<div class="loop-title">Two indices</div>
<div class="loop-note">Reach any element with <b>[row][col]</b>. Both indices are <b>0-based</b>, e.g. <code>b[0][0]</code> is the top-left value.</div>
</div>
<div v-click class="loop-card">
<div class="loop-title">Rows &times; columns</div>
<div class="loop-note">A 2D array of size <code>2 &times; 3</code> holds <b>6</b> elements. The size is <b>fixed</b> and all elements share the <b>same type</b>.</div>
</div>
<div v-click class="loop-card">
<div class="loop-title">length</div>
<div class="loop-note"><code>b.length</code> = number of <b>rows</b> (2); <code>b[0].length</code> = number of <b>columns</b> in a row (3).</div>
</div>
</div>
</div>
<div v-click class="footnote"><b>In short:</b> a 2D array is a <b>grid of rows and columns</b> of the same type, with a <b>fixed</b> size, where each element is accessed by two 0-based indices &mdash; <code>array[row][column]</code>.</div>
</div>
