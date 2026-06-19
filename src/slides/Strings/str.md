---
layout: default
title: "Strings: Concept & Syntax"
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
        width: 38px;
        height: 38px;
        border: 1px solid #b9d4f5;
        background-color: #eaf2fe;
        color: #1e40af;
        border-radius: 6px;
        display: flex;
        align-items: center;
        justify-content: center;
        font-family: 'Consolas', 'Courier New', monospace;
        font-size: 1.1rem;
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
<h2 class="navbar-title" style="font-size: 1.5rem;">Strings</h2>
<img src="../assets/logo.png"/>
</div>
<div class="slide-body">
<div v-click class="intro">A <b>String</b> is a sequence of characters written inside <b>double quotes</b>, like <code>"Hello"</code>. In Java a String is an <b>object</b> (not a primitive type), and it is <b>immutable</b> &mdash; once created, its characters cannot be changed.</div>
<div v-click class="decl">
<div class="panel-title">Declaration &amp; syntax</div>
<pre class="loop-syntax">String s1 = "Hello";               // string literal (common way)
String s2 = new String("World");   // using the new keyword
String name = "Java";              // example
System.out.println(name);          // prints: Java</pre>
</div>
<div v-click class="diagram">
<div class="panel-title">A String is indexed (starts at 0)</div>
<div class="char-row">
<div class="char-cell"><div class="char-box">H</div><div class="char-idx">0</div></div>
<div class="char-cell"><div class="char-box">e</div><div class="char-idx">1</div></div>
<div class="char-cell"><div class="char-box">l</div><div class="char-idx">2</div></div>
<div class="char-cell"><div class="char-box">l</div><div class="char-idx">3</div></div>
<div class="char-cell"><div class="char-box">o</div><div class="char-idx">4</div></div>
</div>
<div class="cap">The String <code>"Hello"</code> has <b>5</b> characters at positions <b>0 to 4</b>. The first character is at index <b>0</b>, not 1.</div>
</div>
<div class="loop-grid">
<div v-click class="loop-card">
<div class="loop-title">Object type</div>
<div class="loop-note">A String is a <b>reference type</b> (an object), unlike primitives such as <code>int</code> or <code>char</code>. The variable holds a reference to the text.</div>
</div>
<div v-click class="loop-card">
<div class="loop-title">Immutable</div>
<div class="loop-note">Once created, the characters <b>never change</b>. Any "edit" actually produces a <b>brand-new</b> String; the original stays as it was.</div>
</div>
<div v-click class="loop-card">
<div class="loop-title">String pool</div>
<div class="loop-note">Identical literals like <code>"Hello"</code> are stored <b>once</b> and shared from a special memory area called the <b>string pool</b>.</div>
</div>
</div>
</div>
<div v-click class="footnote"><b>In short:</b> a String holds text as a sequence of characters, is created with double quotes (or <code>new</code>), is read using <b>0-based</b> positions, and cannot be modified after it is made.</div>
</div>
