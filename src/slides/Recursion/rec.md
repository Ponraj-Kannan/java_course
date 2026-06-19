---
layout: default
title: "Recursion: Calling a Function Again & Again"
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
    .rec-left { flex: 0 0 38%; }
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
        font-size: .78rem;
        line-height: 1.5;
        border-radius: 4px;
        padding: 10px 12px;
        margin: 0 0 8px 0;
        white-space: pre;
        overflow-x: auto;
    }
    .legend {
        font-size: .76rem;
        color: #4b4b4b;
        line-height: 1.5;
    }
    .frame {
        background-color: #eaf2fe;
        border: 1px solid #b9d4f5;
        border-radius: 6px;
        padding: 5px 10px;
        font-family: 'Consolas', 'Courier New', monospace;
        font-size: .76rem;
        box-shadow: 0 1px 2px rgba(30,64,175,0.12);
    }
    .frame .fn { font-weight: 700; color: #1e40af; }
    .frame-base { background-color: #fff3cd; border-color: #ffdf7e; }
    .frame-base .fn { color: #b45309; }
    .calls-again {
        font-size: .72rem;
        font-weight: 700;
        color: #b3531f;
        margin: 3px 0 3px 14px;
    }
    .phase {
        font-size: .78rem;
        font-weight: 700;
        color: #15803d;
        margin: 8px 0 5px 0;
    }
    .ret {
        background-color: #e7f7ec;
        border: 1px solid #b3e3c2;
        border-radius: 6px;
        padding: 5px 10px;
        margin-bottom: 5px;
        font-family: 'Consolas', 'Courier New', monospace;
        font-size: .76rem;
    }
    .ret .fn { font-weight: 700; color: #15803d; }
    .footnote {
        font-size: .8rem;
        color: #374151;
        background-color: #f8fafc;
        border-left: 4px solid #ef5050ff;
        padding: 8px 12px;
        margin: 12px 10px 0 10px;
        border-radius: 0 4px 4px 0;
    }.slide-wrapper {
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
<div v-click class="intro">In recursion, the <b>same function calls itself again and again</b> with a smaller value. Each new call is a fresh copy <b>stacked</b> on top of the previous one, until the <b>base case</b> stops it. Watch <code>fact(4)</code> below.</div>
<div class="rec-wrap">
<div class="rec-left">
<div v-click class="panel-title">Sample program</div>
<pre v-click class="rec-code">int fact(int n)
{
    if (n == 1)
        return 1;          // base case
    return n * <span style="background:#ff914d;color:#1e1e1e;border-radius:3px;padding:0 3px;">fact(n - 1)</span>;
}                          // calls itself AGAIN</pre>
<div v-click class="legend">The highlighted line <b>calls <code>fact()</code> again</b> with <code>n-1</code>. Each call waits for the next one to finish.</div>
</div>
<div class="rec-right">
<div v-click class="panel-title">Each call stacks deeper &#8595;</div>
<div v-click style="margin-left:0px"><div class="frame"><span class="fn">fact(4)</span> &rarr; 4 * fact(3)</div><div class="calls-again">&#8595; calls fact() again</div></div>
<div v-click style="margin-left:18px"><div class="frame"><span class="fn">fact(3)</span> &rarr; 3 * fact(2)</div><div class="calls-again">&#8595; calls fact() again</div></div>
<div v-click style="margin-left:36px"><div class="frame"><span class="fn">fact(2)</span> &rarr; 2 * fact(1)</div><div class="calls-again">&#8595; calls fact() again</div></div>
<div v-click style="margin-left:54px"><div class="frame frame-base"><span class="fn">fact(1)</span> = 1 &#10003; base case &mdash; stop!</div></div>
<div v-click class="phase">Now each call returns &#8593; (reverse order)</div>
<div v-click class="ret" style="margin-left:54px"><span class="fn">fact(1)</span> returns 1</div>
<div v-click class="ret" style="margin-left:36px"><span class="fn">fact(2)</span> = 2 * 1 = 2</div>
<div v-click class="ret" style="margin-left:18px"><span class="fn">fact(3)</span> = 3 * 2 = 6</div>
<div v-click class="ret" style="margin-left:0px"><span class="fn">fact(4)</span> = 4 * 6 = 24 &#10003;</div>
</div>
</div>
</div>
<div v-click class="footnote"><b>Notice:</b> it is the <b>same function</b> running four times, each with its own <code>n</code>, paused on the <b>call stack</b>. The deepest call (the base case) finishes first, then the rest finish in <b>reverse order</b>.</div>
</div>
