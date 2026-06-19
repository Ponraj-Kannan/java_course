---
layout: default
title: "Recursion: Fibonacci Calls"
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
        margin: 12px 10px;
    }
    .rec-wrap {
        display: flex;
        flex-direction: row;
        gap: 14px;
        padding: 0px 10px;
        align-items: flex-start;
    }
    .rec-left { flex: 0 0 36%; }
    .rec-right { flex: 1; }
    .panel-title {
        font-size: .95rem;
        font-weight: 700;
        text-align: center;
        border-radius: 4px;
        padding: 4px 10px;
        margin-bottom: 8px;
        background-color: #ff914d4e;
        border: 1px solid #ff914dd3;
        color: #b3531f;
    }
    .rec-code {
        background-color: #1e1e1e;
        color: #e6e6e6;
        font-family: 'Consolas', 'Courier New', monospace;
        font-size: .76rem;
        line-height: 1.5;
        border-radius: 4px;
        padding: 10px 12px;
        margin: 0 0 8px 0;
        white-space: pre;
        overflow-x: auto;
    }
    .legend {
        font-size: .75rem;
        color: #4b4b4b;
        line-height: 1.5;
        margin-bottom: 6px;
    }
    .swatch { display:inline-block; width:10px; height:10px; border-radius:2px; margin-right:3px; vertical-align:middle; }
    .sw-rec  { background:#eaf2fe; border:1px solid #b9d4f5; }
    .sw-base { background:#fff3cd; border:1px solid #ffdf7e; }
    .calc {
        background-color: #e7f7ec;
        border: 1px solid #b3e3c2;
        border-radius: 6px;
        padding: 5px 10px;
        margin: 6px 10px 0 0;
        font-family: 'Consolas', 'Courier New', monospace;
        font-size: .76rem;
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
    .tree text { font-family: 'Consolas', 'Courier New', monospace; font-size: 11px; }
    .tree line { stroke: #cbd5e1; stroke-width: 1.5; }
    
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
<h2 class="navbar-title" style="font-size: 1.5rem;">Recursion</h2>
<img src="../assets/logo.png"/>
</div>
<div class="slide-body">
<div v-click class="intro">Fibonacci calls itself <b>twice</b> each time: <code>fib(n) = fib(n-1) + fib(n-2)</code>. So one call branches into <b>two</b> new calls, again and again, forming a <b>tree</b> until it hits the base cases <code>fib(0)=0</code> and <code>fib(1)=1</code>.</div>
<div class="rec-wrap">
<div class="rec-left">
<div v-click class="panel-title">Sample program</div>
<pre v-click class="rec-code">int fib(int n)
{
    if (n &lt;= 1)
        return n;     // base case
    return <span style="background:#ff914d;color:#1e1e1e;border-radius:3px;padding:0 3px;">fib(n-1) + fib(n-2)</span>;
}</pre>
<div v-click class="legend"><span class="swatch sw-rec"></span>recursive call &nbsp; <span class="swatch sw-base"></span>base case (stops)</div>
<div v-click class="calc">Base: fib(1)=1, fib(0)=0</div>
<div v-click class="calc">fib(2)=1+0=<b>1</b>, fib(3)=1+1=<b>2</b></div>
<div v-click class="calc">fib(4)=fib(3)+fib(2)=2+1=<b>3</b></div>
</div>
<div class="rec-right">
<div v-click class="panel-title">Call tree for fib(4) &#8595;</div>
<svg class="tree" viewBox="0 0 560 262" xmlns="http://www.w3.org/2000/svg">
<g v-click>
<rect x="274" y="19" width="52" height="26" rx="6" fill="#eaf2fe" stroke="#b9d4f5"/>
<text x="300" y="36" text-anchor="middle" fill="#1e40af">fib(4)</text>
</g>
<g v-click>
<line x1="300" y1="45" x2="170" y2="87"/>
<line x1="300" y1="45" x2="440" y2="87"/>
<rect x="144" y="87" width="52" height="26" rx="6" fill="#eaf2fe" stroke="#b9d4f5"/>
<text x="170" y="104" text-anchor="middle" fill="#1e40af">fib(3)</text>
<rect x="414" y="87" width="52" height="26" rx="6" fill="#eaf2fe" stroke="#b9d4f5"/>
<text x="440" y="104" text-anchor="middle" fill="#1e40af">fib(2)</text>
</g>
<g v-click>
<line x1="170" y1="113" x2="100" y2="155"/>
<line x1="170" y1="113" x2="240" y2="155"/>
<line x1="440" y1="113" x2="380" y2="155"/>
<line x1="440" y1="113" x2="500" y2="155"/>
<rect x="74" y="155" width="52" height="26" rx="6" fill="#eaf2fe" stroke="#b9d4f5"/>
<text x="100" y="172" text-anchor="middle" fill="#1e40af">fib(2)</text>
<rect x="214" y="155" width="52" height="26" rx="6" fill="#fff3cd" stroke="#ffdf7e"/>
<text x="240" y="172" text-anchor="middle" fill="#b45309">fib(1)</text>
<rect x="354" y="155" width="52" height="26" rx="6" fill="#fff3cd" stroke="#ffdf7e"/>
<text x="380" y="172" text-anchor="middle" fill="#b45309">fib(1)</text>
<rect x="474" y="155" width="52" height="26" rx="6" fill="#fff3cd" stroke="#ffdf7e"/>
<text x="500" y="172" text-anchor="middle" fill="#b45309">fib(0)</text>
</g>
<g v-click>
<line x1="100" y1="181" x2="62" y2="223"/>
<line x1="100" y1="181" x2="150" y2="223"/>
<rect x="36" y="223" width="52" height="26" rx="6" fill="#fff3cd" stroke="#ffdf7e"/>
<text x="62" y="240" text-anchor="middle" fill="#b45309">fib(1)</text>
<rect x="124" y="223" width="52" height="26" rx="6" fill="#fff3cd" stroke="#ffdf7e"/>
<text x="150" y="240" text-anchor="middle" fill="#b45309">fib(0)</text>
</g>
</svg>
</div>
</div></div>
<div v-click class="footnote"><b>Notice the repeats:</b> computing <code>fib(4)</code> makes <b>9 calls</b> &mdash; <code>fib(2)</code> runs twice and <code>fib(1)</code> runs three times. Plain recursion redoes the same work; storing results (<b>memoization</b>) removes the duplicates.</div>
</div>
