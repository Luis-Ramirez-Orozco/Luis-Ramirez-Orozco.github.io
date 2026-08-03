---
layout: page
title: Pool Table
---

# Pool Table Assembly

## Purpose
I wanted make something that required working with multiple materials. As well as introduce fasteners into the design.

## Challenge
The steepest learning curve here was learning to machine Aluminum. I purchased 6061 Aluminum bars 4" x 2" x 1" as this is an upper bound of the machine I'm running (Temper Unknown, Amazon Seller did not include this detail). 

## The Process

<div style="display:flex; gap:20px; align-items:center; max-width:700px; margin:0 auto;">
  <div style="position:relative; width:50%; flex-shrink:0; height:380px;">
    <img id="slide-img" src="images/Pool Table/Bench Made Clicks-27.jpg" style="width:100%; height:100%; object-fit:contain; border-radius:8px; display:block; background:#f0f0ee;">
    <button onclick="changeSlide(-1)" style="position:absolute; left:10px; top:50%; transform:translateY(-50%); background:rgba(0,0,0,0.4); color:white; border:none; border-radius:50%; width:36px; height:36px; font-size:18px; cursor:pointer;">‹</button>
    <button onclick="changeSlide(1)" style="position:absolute; right:10px; top:50%; transform:translateY(-50%); background:rgba(0,0,0,0.4); color:white; border:none; border-radius:50%; width:36px; height:36px; font-size:18px; cursor:pointer;">›</button>
    <span id="slide-count" style="position:absolute; bottom:10px; left:50%; transform:translateX(-50%); background:rgba(0,0,0,0.25); color:rgba(255,255,255,0.8); font-size:12px; padding:3px 10px; border-radius:99px;">1 / 4</span>
  </div>
  <div style="flex:1; display:flex; align-items:center;">
    <p id="slide-caption" style="color:#444; font-size:15px; line-height:1.7; background:#f9f9f9; border-radius:8px; padding:16px; box-shadow:0 2px 8px rgba(0,0,0,0.08); text-align:justify; margin:0;"></p>
  </div>
</div>

<script>
const slides = [
  { img: "images/Pool Table/Bench Made Clicks-27.jpg", caption: "What I wanted to make was a pool table. The Design had to incorporate the following:\n \n• Wood \n• Metal \n•Fasteners" },

  
];
let current = 0;
function changeSlide(dir) {
  current = (current + dir + slides.length) % slides.length;
  document.getElementById('slide-img').src = slides[current].img;
  document.getElementById('slide-caption').innerText = slides[current].caption;
  document.getElementById('slide-count').innerText = (current+1) + ' / ' + slides.length;
}
document.getElementById('slide-img').src = slides[0].img;
document.getElementById('slide-caption').innerText = slides[0].caption;
document.getElementById('slide-count').innerText = '1 / ' + slides.length;
</script>

## Socials

<a href="https://www.etsy.com/listing/4497052829/clicker-fidget-toy-fun-desk-accessory" target="_blank">
  <img src="images/Etsy.png" style="height:40px;">
</a>
