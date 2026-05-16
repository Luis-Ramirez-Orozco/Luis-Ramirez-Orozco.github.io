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

<div id="slide" style="display:flex; gap:20px; align-items:flex-start; max-width:700px;">
  <img id="slide-img" src="images/2.jpeg" style="width:50%; height:450px; object-fit:contain; border-radius:8px; flex-shrink:0;">  
  <div style="flex:1; background:#f7f7f5; border-radius:12px; padding:16px;">
    <p id="slide-caption" style="color:#444; font-size:15px; line-height:1.7; margin:0;"></p>
  </div>
</div>
<div style="margin-top:12px; display:flex; align-items:center; gap:12px;">
  <button onclick="changeSlide(-1)" style="padding:8px 20px; cursor:pointer;">← Prev</button>
  <span id="slide-count">1 / 4</span>
  <button onclick="changeSlide(1)" style="padding:8px 20px; cursor:pointer;">Next →</button>
</div>

<script>
const slides = [
  { img: "images/Fidget Clicker/CNC not assembled.jpg", caption: "First thing i had to do was dust off my hobby CNC machine." }
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
