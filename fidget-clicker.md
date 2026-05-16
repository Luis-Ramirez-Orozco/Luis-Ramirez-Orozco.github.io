---
layout: page
title: Fidget Clicker
---

# Fidget Clicker

## Purpose
A hands-on project to experience the full product development cycle — from initial concept through design, iteration, and final manufactured product.

## Challenges
Learning CAM software from scratch was the steepest part of the process — translating a design into machine-ready toolpaths required understanding both the software and the manufacturing constraints at the same time.

## The Process

<div style="display:flex; gap:20px; align-items:center; max-width:700px; margin:0 auto;">
  <div style="position:relative; width:50%; flex-shrink:0;">
    <img id="slide-img" src="images/Fidget Clicker/CNC not assembled.jpg" style="width:100%; border-radius:8px; display:block;">
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
  { img: "images/Fidget Clicker/CNC not assembled.jpg", caption: "First thing i had to do was dust off my hobby CNC machine. I'm using a Genmitsu 3018. The main tools i've used for this project are the 1/8 Hozly flat end mill and 1/4 Diablo flat end mill." }
];
let current = 0;
function changeSlide(dir) {
  current = (current + dir + slides.length) % slides.length;
  document.getElementById('slide-img').src = slides[current].img;
  document.getElementById('slide-caption').innerText = slides[current].caption;
  document.getElementById('slide-count').innerText = (current+1) + ' / ' + slides.length;
}
document.getElementById('slide-caption').innerText = slides[0].caption;
</script>

## Purchase

[Final Product](https://www.etsy.com/listing/4497052829/clicker-fidget-toy-fun-desk-accessory)
