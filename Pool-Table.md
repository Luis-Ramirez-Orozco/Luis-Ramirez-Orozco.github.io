---
layout: page
title: Pool Table
---
<div>
{% include header.html %}
# Pool Table Assembly
</div>  

## Purpose
I wanted make something that required working with multiple materials. As well as introduce fasteners into the design. jijijijiji

## Challenge
The steepest learning curve here was learning to machine Aluminum. I purchased 6061 Aluminum bars 4" x 2" x 1" as this is within the bounds of the machine I'm running (Temper Unknown, Amazon Seller did not include this detail, likely T6). 

## The Process

{% include carousel.html id="pool" folder="/images/Pool Table" images="Bench Made Clicks-27.jpg|IMG_3552 2.JPG|IMG_0028.jpg|IMG_3523.jpg" %}

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
  { img: "images/Pool Table/Bench Made Clicks-27.jpg", caption: "What I wanted to make was a pool table. The design had to incorporate the following:\n \n• Wood \n• Metal \n• Fasteners" },

  { img: "images/Pool Table/IMG_3522.jpg", caption: "For my metallic material, I chose 6061 Aluminum. it's an easier metal to machine due to its hardness, 95 HB, compared to other materials like 1018 Mild Steel ~126 HB or annealed 17-4PH stainless steel <363 HB. Machining this however still required plenty of trials." },

  { img: "images/Pool Table/IMG_0028.jpg", caption: "The wood I chose to work with was Maple.\n \nI had already worked with Poplar, a very soft Hardwood ~540 lbf Janka Hardness. So, I decided to try out some Maple, which has a Janka Hardness of ~ 1400 lbf. The benefit of this material is that it looks nice, when stained" },

  { img: "images/Pool Table/IMG_3523.jpg", caption: "The machining process took time to develop, about 4 different iterations and 48 different programs to achieve the final version. Most of the work revolved around the aluminum pool table."},

  { img: "images/Pool Table/0.250 Ball end mill.jpg", caption: "Tooling became much more important than it was with previous projects. Working with aluminum meant I had to learn and consider the materials thermal properties when running operations. Running tools at too high of an RPM and too slow of a cutting speed and the material will essentially melt while cutting, and weld itself onto the cutting tool. If you use a tool with too many flutes chips may not evacuate the cutting area increasing material cutting/re-cutting and in effect increase heat and welding risk. for this reason I've included a list of tools used and how they were used below."},

  { img:"images/Pool Table/tap and die set.jpg", caption:"Tapping material for M4x0.7 bolts to fasten wood to aluminum"},

  { img:"images/Pool Table/legs.jpg", caption:"Machining the Maple was relatively simple compared to the aluminum. the main thing was that it has a tendency to burn. slower RPM and higher cutting feeds reduces the problem"}
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

## Tools

<div style="display:flex; gap:20px; align-items:center; max-width:700px; margin:0 auto;">
  <div style="position:relative; width:50%; flex-shrink:0; height:380px;">
    <img id="slide-img-tools" src="" style="width:100%; height:100%; object-fit:contain; border-radius:8px; display:block; background:#f0f0ee;">
    <button onclick="changeSlideTools(-1)" style="position:absolute; left:10px; top:50%; transform:translateY(-50%); background:rgba(0,0,0,0.4); color:white; border:none; border-radius:50%; width:36px; height:36px; font-size:18px; cursor:pointer;">‹</button>
    <button onclick="changeSlideTools(1)" style="position:absolute; right:10px; top:50%; transform:translateY(-50%); background:rgba(0,0,0,0.4); color:white; border:none; border-radius:50%; width:36px; height:36px; font-size:18px; cursor:pointer;">›</button>
    <span id="slide-count-tools" style="position:absolute; bottom:10px; left:50%; transform:translateX(-50%); background:rgba(0,0,0,0.25); color:rgba(255,255,255,0.8); font-size:12px; padding:3px 10px; border-radius:99px;">1 / 1</span>
  </div>
  <div style="flex:1; display:flex; align-items:center;">
    <p id="slide-caption-tools" style="color:#444; font-size:15px; line-height:1.7; background:#f9f9f9; border-radius:8px; padding:16px; box-shadow:0 2px 8px rgba(0,0,0,0.08); text-align:justify; margin:0;"></p>
  </div>
</div>

<script>
const slidesTools = [
  { img: "images/Pool Table/0.250 Ball end mill.jpg", caption: "0.250\" Ball End Mill — used for..." }
];

let currentTools = 0;
function changeSlideTools(dir) {
  currentTools = (currentTools + dir + slidesTools.length) % slidesTools.length;
  document.getElementById('slide-img-tools').src = slidesTools[currentTools].img;
  document.getElementById('slide-caption-tools').innerText = slidesTools[currentTools].caption;
  document.getElementById('slide-count-tools').innerText = (currentTools+1) + ' / ' + slidesTools.length;
}
document.getElementById('slide-img-tools').src = slidesTools[0].img;
document.getElementById('slide-caption-tools').innerText = slidesTools[0].caption;
document.getElementById('slide-count-tools').innerText = '1 / ' + slidesTools.length;
</script>

## Socials

<a href="https://www.etsy.com/listing/4497052829/clicker-fidget-toy-fun-desk-accessory" target="_blank">
  <img src="images/Etsy.png" style="height:40px;">
</a>
