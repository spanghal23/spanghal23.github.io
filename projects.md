---
layout: single
permalink: /projects/
title: Projects
---

<style>
/* --- 0. Layout Overrides --- */
.page__title, .page-header, .page__header { display: none !important; }

.page__inner-wrap {
    width: 100% !important;
    max-width: 100% !important;
}

.projects-container {
    width: 75vw;
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
    object-fit: contain; 
    border-bottom: 1px solid #eee;
    cursor: pointer;
    background-color: #f6f8fa;
    min-height: 300px;
}

/* --- 4. Content Area --- */
.project-content { padding: 30px; }

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
    width: 100%; 
    text-align: left;
}

/* --- 5. Gallery --- */
.secondary-gallery {
    display: grid;
    grid-template-columns: repeat(4, 1fr); 
    gap: 15px; 
    margin-bottom: 30px;
}

.gallery-item { display: flex; flex-direction: column; }

.gallery-img {
    width: 100%;
    height: 180px; 
    object-fit: cover; 
    border-radius: 4px;
    border: 1px solid #eee;
    margin-bottom: 8px;
    cursor: zoom-in;
    transition: transform 0.2s;
    background-color: #f6f8fa;
}

.gallery-img:hover {
    transform: scale(1.03);
    box-shadow: 0 4px 12px rgba(0,0,0,0.15);
}

.caption {
    font-size: 0.85rem;
    color: #555;
    font-style: normal;
    text-align: center;
}

/* --- 6. Video --- */
.video-container {
    width: 100%;
    margin-bottom: 30px;
    border-radius: 4px;
    overflow: hidden;
    background: #000;
    min-height: 50px;
}

video {
    width: 100%;
    height: auto;
    display: block;
    max-height: 600px;
}

/* IMPORTANT: This fixes the YouTube Aspect Ratio */
.video-container iframe {
    width: 100%;
    aspect-ratio: 16 / 9;
    border: none;
    display: block;
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
.repo-link:hover { text-decoration: underline; }

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

        <article class="project-card">
            
            <img class="project-main-image gallery-trigger" src="/assets/images/Ball Lev.png" alt="Ball Levitation System">

            <div class="project-content">
                
                <h2 class="project-title">Hand Commanded Ball Levitation</h2>
                
                <p class="project-desc">
                    Achieved <2mm position accuracy via a PD-controlled closed-loop system validated by a ~95% accurate physics model. Implemented 10-point moving average and Kalman filtering to reject sensor noise and optimize servo-actuated throttle response.
                </p>

                <div class="video-container">
                    <iframe 
                        src="https://www.youtube.com/embed/rYfxVyBq8CA" 
                        allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" 
                        allowfullscreen>
                    </iframe>
                </div>

                <div class="repo-link-container">
                    <a href="https://github.com/spanghal23/Hand-Controlled-Ball-Levitation.git" class="repo-link" target="_blank">
                        View Project Repository on GitHub &rarr;
                    </a>
                </div>

            </div>
        </article>

       <article class="project-card">
            
            <img class="project-main-image gallery-trigger" src="/assets/images/EOAT Assembly.jpg" alt="Final EOAT Assembly">

            <div class="project-content">
                
                <h2 class="project-title">Custom EOAT For Cobot Operations</h2>

                <p class="project-desc">
                    Engineered a custom MIC6-aluminum EOAT for UR10e/TM12S cobots to handle 2.5kg+ payloads. Utilizing FEA to reduce beam deflection by 3°, this precision design enabled a vision-guided automation cell that drove $720,000 in annual savings.
                </p>

                <div style="display: flex; flex-wrap: wrap; gap: 20px; margin-top: 20px; border-top: 1px solid #eee; padding-top: 20px;">
                    
                    <div style="flex: 1; min-width: 300px;">
                        <h3 style="text-align: center; font-size: 1rem; color: #555; margin-bottom: 10px;">Demo Video</h3>
                        <div class="video-container" style="background: black; margin-bottom: 0;">
                            <video controls muted style="width: 100%; height: auto; display: block;">
                                <source src="/assets/images/EOAT Demo.mp4" type="video/mp4">
                                Your browser does not support the video tag.
                            </video>
                        </div>
                    </div>

                    <div style="flex: 1; min-width: 300px; display: flex; flex-direction: column; gap: 10px;">
                        <h3 style="text-align: center; font-size: 1rem; color: #555; margin-bottom: 10px;">Gallery</h3>
                        
                        <img class="gallery-img gallery-trigger" style="height: auto; width: 100%; margin-bottom: 0;" src="/assets/images/Gripper Iterations.jpg" alt="Gripper Iterations">
                        <img class="gallery-img gallery-trigger" style="height: auto; width: 100%; margin-bottom: 0;" src="/assets/images/PLA Prototype.jpg" alt="PLA Prototype">
                        <img class="gallery-img gallery-trigger" style="height: auto; width: 100%; margin-bottom: 0;" src="/assets/images/High Level Code.jpg" alt="High Level Code">
                    </div>

                </div>

            </div>
        </article>

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
            if(this.getAttribute('src')) { 
                modal.style.display = "block";
                modalImg.src = this.src;
                captionText.innerHTML = this.alt;
            }
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
