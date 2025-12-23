---
layout: single
permalink: /projects/
title: Projects
---

<style>
/* --- 0. Layout Overrides --- */

/* 1. HIDE THEME HEADER: This removes the automatic "Projects" title */
.page__title, .page-header, .page__header {
    display: none !important;
}

/* 2. FORCE WIDE LAYOUT */
.page__inner-wrap {
    width: 100% !important;
    max-width: 100% !important;
}

.projects-container {
    width: 75vw; /* 75% of screen width */
    max-width: 1400px;
    margin: 0 auto;
    position: relative;
    left: 50%;
    right: 50%;
    margin-left: -37.5vw;
    margin-right: -37.5vw;
}

/* --- 1. Header Styling --- */
.page-header-text {
    text-align: center;
    margin-bottom: 40px;
    padding-top: 10px;
}

.page-header-text p {
    font-size: 1.2rem;
    color: #666;
    max-width: 800px;
    margin: 0 auto;
}

/* --- 2. Card Styling --- */
.projects-grid {
    display: grid;
    grid-template-columns: 1fr;
    gap: 40px;
    padding-bottom: 40px;
}

.project-card {
    background: #fff;
    border: 1px solid #e1e4e8;
    border-radius: 8px;
    overflow: hidden;
    box-shadow: 0 4px 10px rgba(0,0,0,0.05);
    display: flex;
    flex-direction: column;
}

/* --- 3. Main Image --- */
.project-main-image {
    width: 100%;
    height: auto;
    max-height: 600px;
    /* Use contain for main image so the whole robot is visible */
    object-fit: contain; 
    border-bottom: 1px solid #eee;
    cursor: pointer;
    background-color: #f6f8fa;
}

/* --- 4. Content Area --- */
.project-content {
    padding: 30px;
}

.project-title {
    font-size: 1.8rem;
    font-weight: 700;
    margin: 0 0 20px 0;
    color: #24292e;
    text-align: center;
}

.project-desc {
    font-size: 1.05rem;
    color: #586069;
    line-height: 1.6;
    margin-bottom: 30px;
    width: 100%; /* Stretches text across the whole card */
    text-align: left;
}

/* --- 5. Gallery (No White Space) --- */
.secondary-gallery {
    display: grid;
    /* 4 columns to fit all images in one row */
    grid-template-columns: repeat(4, 1fr); 
    gap: 15px; 
    margin-bottom: 30px;
}

.gallery-item {
    display: flex;
    flex-direction: column;
}

.gallery-img {
    width: 100%;
    height: 180px; /* Fixed height for uniformity */
    /* COVER fills the box completely (no white space), might crop edges slightly */
    object-fit: cover; 
    border-radius: 4px;
    border: 1px solid #eee;
    margin-bottom: 8px;
    cursor: zoom-in;
    transition: transform 0.2s;
}

.gallery-img:hover {
    transform: scale(1.03);
    box-shadow: 0 4px 12px rgba(0,0,0,0.15);
}

.caption {
    font-size: 0.85rem;
    color: #555;
    font-style: italic;
    text-align: center;
}

/* --- 6. Video --- */
.video-container {
    width: 100%;
    margin-bottom: 30px;
    border-radius: 4px;
    overflow: hidden;
    background: #000;
}

video {
    width: 100%;
    height: auto;
    display: block;
    max-height: 600px;
}

/* --- 7. Repo Link --- */
.repo-link-container {
    text-align: center;
    padding-top: 20px;
    border-top: 1px solid #eee;
}

.repo-link {
    font-size: 1.1rem;
    font-weight: bold;
    color: #0366d6;
    text-decoration: none;
}

.repo-link:hover {
    text-decoration: underline;
}

/* --- 8. Lightbox --- */
#imageModal {
    display: none;
    position: fixed;
    z-index: 9999;
    padding-top: 50px;
    left: 0;
    top: 0;
    width: 100%;
    height: 100%;
    overflow: auto;
    background-color: rgba(0,0,0,0.9);
}

.modal-content {
    margin: auto;
    display: block;
    max-width: 90%;
    max-height: 90vh;
    border-radius: 5px;
}

#modalCaption {
    margin: auto;
    display: block;
    width: 80%;
    max-width: 700px;
    text-align: center;
    color: #ccc;
    padding: 10px 0;
    height: 150px;
}

.close {
    position: absolute;
    top: 15px;
    right: 35px;
    color: #f1f1f1;
    font-size: 40px;
    font-weight: bold;
    cursor: pointer;
}
</style>

<div class="projects-container">

    <div class="projects-grid">

        <article class="project-card">
            
            <img class="project-main-image gallery-trigger" src="/assets/images/Final Assembly.png" alt="Robot Arm Main View">

            <div class="project-content">
                
                <h2 class="project-title">Teleoperated Robot Arm</h2>
                
                <p class="project-desc">
                    Designed and fabricated a 4-DOF arm with custom 10:1 planetary gearboxes, validated in MATLAB to achieve 18.8 N-m holding torque with a 1.3 safety factor. The 600W system utilizes ODrive S1 FOC and STM32 via CANBUS, driven by a custom Python teleoperation pipeline mapping computer vision for precision control.
                </p>

                <div class="secondary-gallery">
                    
                    <div class="gallery-item">
                        <img class="gallery-img gallery-trigger" src="/assets/images/GUI SC.png" alt="Teleoperation GUI">
                        <span class="caption">Teleoperation GUI</span>
                    </div>

                    <div class="gallery-item">
                        <img class="gallery-img gallery-trigger" src="/assets/images/CV Mapping.png" alt="CV Pose Mapping">
                        <span class="caption">CV Pose Mapping</span>
                    </div>

                    <div class="gallery-item">
                        <img class="gallery-img gallery-trigger" src="/assets/images/Electrical Schematic.png" alt="Electrical Schematic">
                        <span class="caption">Electrical Schematic</span>
                    </div>

                    <div class="gallery-item">
                        <img class="gallery-img gallery-trigger" src="/assets/images/Actuator Design.png" alt="Actuator Design">
                        <span class="caption">Actuator Design</span>
                    </div>

                </div>

                <div class="video-container">
                    <video controls muted>
                        <source src="/assets/images/Robot_Arm_Demo.mp4" type="video/mp4">
                        Your browser does not support the video tag.
                    </video>
                </div>

                <div class="repo-link-container">
                    <a href="https://github.com/spanghal23/Teleoperated_Robot_Arm.git" class="repo-link" target="_blank">
                        View Project Repository on GitHub &rarr;
                    </a>
                </div>

            </div>
        </article>
    </div>
</div>

<div id="imageModal">
  <span class="close">&times;</span>
  <img class="modal-content" id="img01">
  <div id="modalCaption"></div>
</div>

<script>
    var modal = document.getElementById("imageModal");
    var modalImg = document.getElementById("img01");
    var captionText = document.getElementById("modalCaption");
    var images = document.querySelectorAll(".gallery-trigger");

    images.forEach(function(img) {
        img.onclick = function(){
            modal.style.display = "block";
            modalImg.src = this.src;
            captionText.innerHTML = this.alt;
        }
    });

    var span = document.getElementsByClassName("close")[0];
    span.onclick = function() { 
        modal.style.display = "none";
    }
    modal.onclick = function(event) {
        if (event.target === modal) {
            modal.style.display = "none";
        }
    }

    <style>
  .caption, figcaption {
    font-style: normal !important;
    text-transform: none !important; /* Optional: Stops it from being uppercase if set */
  }
</style>
</script>
