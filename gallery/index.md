---
layout: page
permalink: /gallery/
title: Photography
tags: [photography, gallery]
modified: 12-24-2025
comments: false
share: false
---

<style>
.gallery-intro {
  text-align: center;
  margin-bottom: 30px;
  color: #666;
  font-style: italic;
}

.gallery-container {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
  gap: 20px;
  margin-top: 20px;
}

.gallery-item {
  position: relative;
  overflow: hidden;
  border-radius: 8px;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
  transition: transform 0.3s ease, box-shadow 0.3s ease;
  background: #f5f5f5;
}

.gallery-item:hover {
  transform: translateY(-5px);
  box-shadow: 0 8px 15px rgba(0, 0, 0, 0.2);
}

.gallery-item img {
  width: 100%;
  height: 250px;
  object-fit: cover;
  display: block;
  transition: transform 0.3s ease;
}

.gallery-item:hover img {
  transform: scale(1.05);
}

.gallery-item .caption {
  padding: 15px;
  background: #fff;
}

.gallery-item .caption h3 {
  margin: 0 0 5px 0;
  font-size: 16px;
  color: #333;
}

.gallery-item .caption p {
  margin: 0;
  font-size: 13px;
  color: #888;
}

.gallery-category {
  margin-top: 40px;
  margin-bottom: 20px;
  padding-bottom: 10px;
  border-bottom: 2px solid #333;
}

/* Lightbox styles */
.lightbox {
  display: none;
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: rgba(0, 0, 0, 0.9);
  z-index: 9999;
  justify-content: center;
  align-items: center;
}

.lightbox.active {
  display: flex;
}

.lightbox img {
  max-width: 90%;
  max-height: 90%;
  object-fit: contain;
}

.lightbox-close {
  position: absolute;
  top: 20px;
  right: 30px;
  color: #fff;
  font-size: 40px;
  cursor: pointer;
  z-index: 10000;
}

.lightbox-close:hover {
  color: #ccc;
}
</style>

<p class="gallery-intro">
  📷 Photography is one of my passions. Here I share some moments I've captured from my travels and academic life.
</p>

<h2 class="gallery-category">🌅 Landscapes</h2>
<div class="gallery-container">
  <div class="gallery-item" onclick="openLightbox(this)">
    <img src="{{ site.url }}/images/gallery/OdaibaNight.jpg" alt="Tokyo Tower Night View from Odaiba">
    <div class="caption">
      <h3>Tokyo Tower at Night</h3>
      <p>Odaiba, Tokyo · 2025</p>
    </div>
  </div>

  <div class="gallery-item" onclick="openLightbox(this)">
    <img src="{{ site.url }}/images/gallery/OdaibaFireworkShow.JPG" alt="Odaiba Firework Show">
    <div class="caption">
      <h3>Odaiba Firework Show</h3>
      <p>Odaiba, Tokyo · 2025<br><strong>🏆 Grand Prize Winner - 2025 TIEC Photo Contest</strong><br><a href="https://www.facebook.com/photo?fbid=858450030165093&set=pcb.858457793497650" target="_blank">Source</a></p>
    </div>
  </div>

  <div class="gallery-item" onclick="openLightbox(this)">
    <img src="{{ site.url }}/images/gallery/Ogimachi.JPG" alt="Ogimachi, Shirakawa-go">
    <div class="caption">
      <h3>Shirakawa-go</h3>
      <p>Ogimachi, Japan · 2025</p>
    </div>
  </div>
</div>

<h2 class="gallery-category">🎓 Academic Life</h2>
<div class="gallery-container">
  <div class="gallery-item" onclick="openLightbox(this)">
    <img src="{{ site.url }}/images/gallery/RikenWakoFall.jpg" alt="Riken Wako Fall">
    <div class="caption">
      <h3>Riken Wako Fall</h3>
      <p>RIKEN, Wako · Fall 2025</p>
    </div>
  </div>
</div>



<!-- Lightbox -->
<div class="lightbox" id="lightbox" onclick="closeLightbox()">
  <span class="lightbox-close">&times;</span>
  <img id="lightbox-img" src="" alt="Full size image">
</div>

<script>
function openLightbox(element) {
  var img = element.querySelector('img');
  var lightbox = document.getElementById('lightbox');
  var lightboxImg = document.getElementById('lightbox-img');
  lightboxImg.src = img.src;
  lightbox.classList.add('active');
  document.body.style.overflow = 'hidden';
}

function closeLightbox() {
  var lightbox = document.getElementById('lightbox');
  lightbox.classList.remove('active');
  document.body.style.overflow = 'auto';
}

document.addEventListener('keydown', function(e) {
  if (e.key === 'Escape') {
    closeLightbox();
  }
});
</script>

<br>
<p style="text-align: center; color: #888; font-size: 14px;">
  <i>More photos coming soon... 🌟</i>
</p>
