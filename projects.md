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

/* --- 2. Card Styling --- */
.project-card {
    background: #fff;
    border: 1px solid #e1e4e8;
    border-radius: 8px;
    overflow: hidden;
    box-shadow: 0 4px 10px rgba(0,0,0,0.05);
    transition: transform 0.2s ease;
    display: flex;
    flex-direction: column;
}

.project-card:hover {
    transform: translateY(-5px);
    box-shadow: 0 8px 20px rgba(0,0,0,0.1);
}

/* --- 3. The Gallery (Scrollable Row) --- */
.project-gallery {
    display: flex;
    overflow-x: auto; /* Enables horizontal scrolling */
    scroll-snap-type: x mandatory; /* Snaps images into place */
    height: 250px; /* Fixed height for consistency */
    background-color: #f6f8fa;
    border-bottom: 1px solid #eee;
}

/* Hide scrollbar for cleaner look (optional) */
.project-gallery::-webkit-scrollbar {
    height: 8px;
}
.project-gallery::-webkit-scrollbar-thumb {
    background: #ccc;
    border-radius: 4px;
}

.gallery-item {
    flex: 0 0 100%; /* Shows one full image at a time */
    scroll-snap-align: start;
    position: relative;
    border-right: 1px solid #fff;
}

.gallery-item img, 
.gallery-item iframe {
    width: 100%;
    height: 100%;
    object-fit: cover; /* Ensures images fill the box */
    border: none;
}

/* Label for images (e.g., "Wiring Diagram") */
.gallery-label {
    position: absolute;
    bottom: 10px;
    left: 10px;
    background: rgba(0, 0, 0, 0.7);
    color: white;
    padding: 4px 8px;
    border-radius: 4px;
    font-size: 0.75rem;
    font-weight: bold;
    pointer-events: none;
}

/* --- 4. Content & Text --- */
.project-content {
    padding: 20px 20px 10px 20px;
}

.project-title {
    font-size: 1.4rem;
    font-weight: 700;
    margin: 0 0 10px 0;
    color: #24292e;
}

.project-desc {
    font-size: 0.95rem;
    color: #586069;
    line-height: 1.5;
    margin-bottom: 15px;
}

/* --- 5. Tags (Pills) --- */
.project-specs {
    padding: 0 20px 15px 20px;
    display: flex;
    flex-wrap: wrap;
    gap: 8px;
}

.spec-tag {
    background: #e1ecf4;
    color: #0366d6;
    font-size: 0.75rem;
    font-weight: 600;
    padding: 4px 10px;
    border-radius: 15px; /* Makes them pill-shaped */
    border: 1px solid #cce0f5;
}

/* --- 6. Buttons --- */
.project-links {
    padding: 15px 20px;
    background-color: #fafbfc;
    border-top: 1px solid #e1e4e8;
    display: flex;
    gap: 15px;
    margin-top: auto; /* Pushes to bottom */
}

.btn-link {
    font-size: 0.9rem;
    font-weight: 600;
    text-decoration: none;
    color: #24292e;
    border: 1px solid #d1d5da;
    padding: 6px 12px;
    border-radius: 6px;
    transition: background 0.2s;
}

.btn-link:hover {
    background: #f3f4f6;
    text-decoration: none;
}
</style>

<div class="projects-grid">

    <article class="project-card">
        
        <div class="project-gallery">
            
            <div class="gallery-item">
                 <iframe src="https://www.youtube.com/embed/VIDEO_ID" title="Demo Video" allowfullscreen></iframe>
            </div>

            <div class="gallery-item">
                <span class="gallery-label">Robot Arm Assembly</span>
                <img src="/assets/images/robot-arm.jpg" alt="Robot Arm">
            </div>

            <div class="gallery-item">
                <span class="gallery-label">Python Teleop GUI</span>
                <img src="/assets/images/gui-screenshot.jpg" alt="GUI">
            </div>

            <div class="gallery-item">
                <span class="gallery-label">Electrical Wiring</span>
                <img src="/assets/images/wiring-diagram.jpg" alt="Wiring Diagram">
            </div>

            <div class="gallery-item">
                <span class="gallery-label">Computer Vision Pipeline</span>
                <img src="/assets/images/cv-demo.jpg" alt="CV Pipeline">
            </div>

        </div>

        <div class="project-content">
            <h2 class="project-title">Teleoperated Robot Arm</h2>
            <p class="project-desc">
                Designed and fabricated a 4-DOF arm with custom 10:1 planetary gearboxes, validated in MATLAB to achieve 18.8 N-m holding torque with a 1.3 safety factor. The 600W system utilizes ODrive S1 FOC and STM32 via CANBUS, driven by a custom Python teleoperation pipeline mapping computer vision for precision control.
            </p>
        </div>

        <div class="project-specs">
            <span class="spec-tag">Python & C++</span>
            <span class="spec-tag">CANBUS</span>
            <span class="spec-tag">Mechanical Design</span>
            <span class="spec-tag">Computer Vision</span>
        </div>

        <div class="project-links">
            <a href="#" class="btn-link">View Code &rarr;</a>
            <a href="#" class="btn-link">Read Report</a>
        </div>

    </article>
    </div>
