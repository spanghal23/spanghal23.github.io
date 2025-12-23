---
layout: single
permalink: /projects/
title: Projects
---

<style>
/* --- 1. Main Grid Layout --- */
.projects-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
    gap: 40px;
    padding: 20px 0;
}

/* --- 2. Card Container --- */
.project-card {
    background: #fff;
    border: 1px solid #e1e4e8;
    border-radius: 8px;
    overflow: hidden;
    box-shadow: 0 4px 10px rgba(0,0,0,0.05);
    display: flex;
    flex-direction: column;
}

/* --- 3. Main Top Image --- */
.project-main-image {
    width: 100%;
    height: auto; /* CHANGED: Allows image to show full height without cropping */
    max-height: 500px; /* Optional cap so it doesn't take up the WHOLE screen */
    object-fit: contain; /* CHANGED: Ensures the whole image is seen */
    border-bottom: 1px solid #eee;
    cursor: pointer;
    background-color: #f6f8fa; /* Light grey background for non-rectangular images */
}

/* --- 4. Text Content --- */
.project-content {
    padding: 20px;
}

.project-title {
    font-size: 1.5rem;
    font-weight: 700;
    margin: 0 0 15px 0;
    color: #24292e;
}

.project-desc {
    font-size: 0.95rem;
    color: #586069;
    line-height: 1.6;
    margin-bottom: 20px;
}

/* --- 5. Secondary Images Grid --- */
.secondary-gallery {
    display: grid;
    grid-template-columns: 1fr; /* CHANGED: 1 Column so images are full width (bigger) */
    gap: 20px;
    margin-bottom: 25px;
}

.gallery-item {
    display: flex;
    flex-direction: column;
}

.gallery-img {
    width: 100%;
    height: auto; /* CHANGED: Let height scale naturally so diagrams aren't squished */
    object-fit: contain;
    border-radius: 4px;
    border: 1px solid #eee;
    margin-bottom: 5px;
    cursor: zoom-in;
    transition: transform 0.2s, box-shadow 0.2s;
}

.gallery-img:hover {
    transform: scale(1.01);
    box-shadow: 0 4px 12px rgba(0,0,0,0.15);
}

.caption {
    font-size: 0.85rem;
    color: #555;
    font-style: italic;
    text-align: center;
    margin-top: 5px;
}

/* --- 6. Video Section --- */
.video-container {
    width: 100%;
    margin-bottom: 20px;
    border-radius: 4px;
    overflow: hidden;
    background: #000;
}

video {
    width: 100%;
    height: auto;
    display: block;
}

/* --- 7. Repo Link --- */
.repo-link-container {
    text-align: center;
    padding-top: 10px;
    border-top: 1px solid #eee;
}

.repo-link {
    font-size: 0.95rem;
    font-weight: bold;
    color: #0366d6;
    text-decoration: none;
}

.repo-link:hover {
    text-decoration: underline;
}

/* --- 8. Lightbox Modal --- */
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
    max-width: 95%; /* Increased width for better visibility */
    max-height: 90vh;
    border-radius: 5px;
    box-shadow: 0 0 20px rgba(255,255,255,0.2);
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
    transition: 0.3s;
    cursor: pointer;
}

.close:hover,
.close:focus {
    color: #bbb;
    text-decoration: none;
    cursor: pointer;
}
</style>

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
                    <img class="gallery-img gallery-trigger" src="/assets/images/CV Mapping.png" alt="Computer Vision Pose Mapping">
                    <span class="caption">Computer Vision Pose Mapping</span>
                </div>

                <div class="gallery-item">
                    <img class="gallery-img gallery-trigger" src="/assets/images/Electrical Schematic.png" alt="Electrical Architecture">
                    <span class="caption">Electrical Architecture</span>
                </div>

                <div class="gallery-item">
                    <img class="gallery-img gallery-trigger" src="/assets/images/Actuator Design.png" alt="Actuator Design">
                    <span class="caption">Actuator Design</span>
                </div>

            </div>

            <div class="video-container">
                <video controls>
                    <source src="/assets/images/Robot_Arm_Demo.mp4" type="video/mp4">
                    Your browser does not support the video tag.
                </video>
            </div>

            <div class="repo-link-container">
                <a href="INSERT_YOUR_GITHUB_REPO_URL_HERE" class="repo-link" target="_blank">
                    View Project Repository on GitHub &rarr;
                </a>
            </div>

        </div>
    </article>
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
</script>
