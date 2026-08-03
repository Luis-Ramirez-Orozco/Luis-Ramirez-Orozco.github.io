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
  <div style="position:relative; width:50%; flex-shrink:0; height:380px;">
    <img id="slide-img" src="images/Fidget Clicker/CNC not assembled.jpg" style="width:100%; height:100%; object-fit:contain; border-radius:8px; display:block; background:#f0f0ee;">
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
  { img: "images/Fidget Clicker/Concept2.jpg", caption: "The idea here was to start off easy. I needed a product with simple geometry that could help me learn the basics of both designing and manufacturing. Through crowdsourcing the idea of a mechanical keyboard fidget clicker was born. Attached are the initial dimensions taken from a keyboard switch that sacrificed its life to science." },

  { img: "images/Fidget Clicker/Concept.JPG", caption: "The idea here was to start off easy. I needed a product with simple geometry that could help me learn the basics of both designing and manufacturing. Through crowdsourcing the idea of a mechanical keyboard fidget clicker was born. Attached are the initial dimensions taken from a keyboard switch that sacrificed its life to science." },
  
  { img: "images/Fidget Clicker/CNC not assembled.jpg", caption: "I'm using a Genmitsu 3018. The main tools i've used for this project are:\n \n1) 1/8 Hozly flat end mill \n2) 1/4 Diablo flat end mill." },

  { img: "images/Fidget Clicker/V1.png", caption: "Version 1.0, had two extra bores to make room for some prongs that the keyswitch has; shown is version 1.2. Documentation was not kept up and I lost the revision history associated with version 1.0. within this model there were also some anomolies in the geometery that resulted when I extruded the pockets to incorrect depths. The result was a pedestal for the keyswitch to sit on. This concept actually made it all the way to version 2.0" }, 

  { img: "images/Fidget Clicker/Setup2.jpg", caption: "For my setups I'm using:\n \n•800 W spindle that maxes out at around 12K RPM. \n•OpenBuildsCONTROL to run the G code \n•Poplar"},
  
  { img: "images/Fidget Clicker/Prototype1.png", caption: "The main issue with version 1 was that the keys would rock laterally when the buttons were pressed. As the key switch design is meant to be pressfit into the cavity the lateral movement overtime caused the buttons to dislodge and fall out. This, along with learning how to how to manage run speeds and cut depths resulted in a real rough prototype" },
  
  { img: "images/Fidget Clicker/V3.png", caption: "The next big jump I made was at version 3. This is where I fixed the models ''pedestal'' and began to really experiment with run speeds and depths of cut (DOC)" },
  
  { img: "images/Fidget Clicker/Speeds&DOC test.JPEG", caption: "I began to test different depths of cut. I learned the machines capabilities and created solutions to problems I saw.... alot of vibration" },

  { img: "images/Fidget Clicker/Gantry vibration.png", caption: "Z-axis Vibration solved with springs" },

  { img: "images/Fidget Clicker/Speeds&DOC test2.JPG", caption: "Runspeeds figured out" },

  { img: "images/Fidget Clicker/Tape method.png", caption: "Clamping method figured out" }
  
  
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
