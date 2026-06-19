---
layout: default
---

<script setup>
const helloCode = `public class Main 
{
    public static void main(String[] args) 
    {
        // Write your code here
    }
}`;
</script>

<style>
    .box1 {
        margin-top: -10px; margin-left: -30px; padding-bottom: 10px; width: 107%;
        max-height: 72vh; color:#464646ff; background-color: #ffffffff;
        font-size: .8rem; font-weight: 400; overflow-x: auto;
        scrollbar-width: none; overflow-y: auto;
    }
    .box2 { display: flex; flex-direction:row; justify-content: space-between;
        align-items:center; gap: 0.75rem; padding:0px 10px; color: #ffffff; margin-bottom: 4px; }
    .box2 > img { height: 30px; }
    .box3 { margin: 0; font-size: 1.5rem; font-weight: 700; background-color: #ef5050ff;
        color: #ffffffff; width: 80%; padding-left:10px; margin-left:-10px }
    .box4 { display: flex; align-items: left; border-radius: 4px; flex-direction: row; }
    .container1 { width: 65%; min-height: 10vh; }
    .container2 { width: 33%; min-height: 10vh; margin-left: 1%; }
    .mini-container { border-radius: 4px; font-size: .9rem; color: #374151;
        background-color: #e2f0feff; border: 1px solid #a9c4d2ff; display: inline-block;
        min-width: 32px; margin-right: 3px; padding: 5px; width:100%; margin-bottom: 5px; }
    .mini-container-1 { border-radius: 4px; font-size: 1rem; display: inline-block;
        min-width: 32px; text-align: center; margin-right: 3px; background-color: #ff914d4e;
        padding:5px 10px; margin-top:10px; border: 1px solid #ff914dd3; }
</style>

<div class="box1">
  <div class="box2">
    <h2 class="box3">Type Casting</h2>
    <img src="../assets/logo.png"/>
  </div>
  <div class="box4" style="margin-top:20px">
    <div class="container1">
      <div v-click class="mini-container-1" style="margin-bottom:10px;margin-top:-10px;">int → char (ASCII)</div>
      <JavaRunner v-click/>
    </div>
    <div class="container2" style="margin-top:38px">
      <div v-click class="mini-container">Given <code>int code = 97</code>, print the corresponding <b>character</b>.</div><br>
      <div v-click class="mini-container">Print characters for ASCII values <b>65</b>, <b>90</b>, <b>48</b>, and <b>57</b>.</div>
    </div>
  </div>
</div>
