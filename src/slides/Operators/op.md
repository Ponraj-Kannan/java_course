---
layout: default
title: "Operators: Syntax & Explanation"
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
        margin: 12px 10px;
    }
    .loop-grid {
        display: flex;
        flex-direction: row;
        flex-wrap: wrap;
        gap: 10px;
        padding: 0px 10px;
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
        line-height: 1.45;
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
    .tag-binary  { background-color: #dbeafe; color: #1e40af; border: 1px solid #93c5fd; }
    .tag-unary   { background-color: #dcfce7; color: #166534; border: 1px solid #86efac; }
    .tag-ternary { background-color: #fef9c3; color: #854d0e; border: 1px solid #fde047; }
    .footnote {
        font-size: .82rem;
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
<h2 class="navbar-title" style="font-size: 1.5rem;">Operators</h2>
<img src="../assets/logo.png"/>
</div>
<div class="slide-body">
<div v-click class="intro">An <b>operator</b> is a symbol that performs an operation on values or variables, called <b>operands</b>. Java groups them into <b>arithmetic</b>, <b>relational</b>, <b>logical</b>, <b>assignment</b>, <b>unary</b>, and <b>ternary</b> operators.</div>
<div class="loop-grid">
<div v-click class="loop-card">
<div class="loop-title">Arithmetic</div>
<span class="loop-tag tag-binary">Binary</span>
<pre class="loop-syntax">+   -   *   /   %
a + b
a % b   // remainder</pre>
<div class="loop-note">Perform basic maths. <code>%</code> (modulus) gives the <b>remainder</b> of a division.</div>
</div>
<div v-click class="loop-card">
<div class="loop-title">Relational</div>
<span class="loop-tag tag-binary">Binary</span>
<pre class="loop-syntax">==  !=  >  <  >=  <=
a >= b   // true / false</pre>
<div class="loop-note">Compare two values. The result is always a <b>boolean</b> (<code>true</code> or <code>false</code>).</div>
</div>
<div v-click class="loop-card">
<div class="loop-title">Bitwise</div>
<span class="loop-tag tag-binary">Binary</span>
<pre class="loop-syntax">&  |  ^  ~
&    |
|    ^</pre>
<div class="loop-note">Compare two values. The result is always a <b>number</b>.</div>
</div>
<div v-click class="loop-card">
<div class="loop-title">Logical</div>
<span class="loop-tag tag-binary">Binary</span>
<pre class="loop-syntax">&&    ||    !
a>0 && b>0</pre>
<div class="loop-note">Combine conditions. <code>&&</code> = AND, <code>||</code> = OR, <code>!</code> = NOT.</div>
</div>
<div v-click class="loop-card">
<div class="loop-title">Assignment</div>
<span class="loop-tag tag-binary">Binary</span>
<pre class="loop-syntax">=  +=  -=  *=  /=  %=
x += 5   // x = x + 5</pre>
<div class="loop-note">Store or <b>update</b> a value in a variable. Shorthand forms combine maths with assignment.</div>
</div>
<div v-click class="loop-card">
<div class="loop-title">Unary (++ / --)</div>
<span class="loop-tag tag-unary">Unary</span>
<pre class="loop-syntax">++    --
x++    ++x
x--    --x</pre>
<div class="loop-note">Change a value by <b>1</b>. <b>Pre</b> (<code>++x</code>) updates before use; <b>post</b> (<code>x++</code>) after.</div>
</div>
<div v-click class="loop-card" style="max-width:295px;">
<div class="loop-title">Ternary</div>
<span class="loop-tag tag-ternary">Ternary</span>
<pre class="loop-syntax">condition ? a : b
max = a>b ? a : b</pre>
<div class="loop-note">A short <b>if-else</b> in one line: returns <code>a</code> if the condition is true, else <code>b</code>.</div>
</div>
</div>
</div>
</div>
