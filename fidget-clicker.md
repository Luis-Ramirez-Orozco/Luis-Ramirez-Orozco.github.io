---
layout: page
title: Fidget Clicker
---

# Fidget Clicker

## Purpose
A hands-on project to experience the full product development cycle — from initial concept through design, iteration, and final manufactured product.

## Challenges
Learning CAM software from scratch was the steepest part of the process — translating a design into machine-ready toolpaths required understanding both the software and the manufacturing constraints at the same time.

## Photos

<div style="max-width:500px; margin:0 auto; text-align:center;">
  <img id="slide-img" src="IMG_2671.jpeg" style="width:100%; height:300px; object-fit:cover; border-radius:8px;">
  <p id="slide-caption" style="margin-top:12px; color:#666; font-size:14px;">Caption for photo 1</p>
  <div style="margin-top:12px; display:flex; justify-content:center; gap:12px;">
    <button onclick="changeSlide(-1)" style="padding:8px 20px; cursor:pointer;">← Prev</button>
    <span id="slide-count" style="line-height:2.2;">1 / 4</span>
    <button onclick="changeSlide(1)" style="padding:8px 20px; cursor:pointer;">Next →</button>
  </div>
</div>

<script>
const slides = [
  { img: "IMG_2671.jpeg", caption: "Write your caption for this photo here" },
  { img: "IMG_2678.jpeg", caption: "Write your caption for this photo here" },
  { img: "IMG_2680.jpeg", caption: "Write your caption for this photo here" },
  { img: "IMG_2705.jpeg", caption: "Write your caption for this photo here" }
];
let current = 0;
function changeSlide(dir) {
  current = (current + dir + slides.length) % slides.length;
  document.getElementById('slide-img').src = slides[current].img;
  document.getElementById('slide-caption').innerText = slides[current].caption;
  document.getElementById('slide-count').innerText = (current+1) + ' / ' + slides.length;
}
</script>

## Purchase

[Final Product](https://www.etsy.com/listing/4497052829/clicker-fidget-toy-fun-desk-accessory)
