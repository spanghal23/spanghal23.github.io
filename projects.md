---
layout: single
permalink: /projects/
title: Projects  # <--- Define the main page title here
---

## Teleoperated Robot Arm
Built a robot arm
## Variable Input Ball Levitation
Built a ball levitation system using transient commands from input hand height
## Techman Cobot Custom End-of-Arm-Tool
Designed, fabricated, and installed custom EOAT for line techman cobots to assist in material handling

---
layout: default
title: Projects
permalink: /projects/
---

<style>
/* --- Projects Page Styling --- */

/* The Grid Container: Holds all project cards */
.projects-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); /* Auto-scales columns */
    gap: 40px; /* Space between cards */
    padding: 20px 0;
}

/* Individual Project Card */
.project-card {
    background: #fff;
    border: 1px solid #e1e4e8;
    border-radius: 8px;
    overflow: hidden;
    box-shadow: 0 2px 5px rgba(0,0,0,0.05);
    transition: transform 0.2s ease, box-shadow 0.2s ease;
    display: flex;
    flex-direction: column;
}

.project-card:hover {
    transform: translateY(-5px);
    box-shadow: 0 5px 15px rgba(0,0,0,0.1);
}

/* Media Area (Video/Image) */
.project-media {
    width: 100%;
    height: 200px; /* Fixed height for consistency */
    background-color: #f6f8fa;
    border-bottom: 1px solid #e1e4e8;
    position: relative;
    overflow: hidden;
}

.project-media img, 
.project-media video, 
.project-media iframe {
    width: 100%;
    height: 100%;
    object-fit: cover; /* Ensures image fills the box without stretching */
    border: none;
}

/* Content Area */
.project-content {
    padding: 20px;
    flex-grow: 1; /* Pushes buttons to the bottom */
}

.project-title {
    font-size: 1.25rem;
    font-weight: 700;
    margin-bottom: 10px;
    color: #24292e;
}

/* Specs / Tags (e.g., Python, CAD) */
.project-specs {
    margin-bottom: 15px;
    display: flex;
    flex-wrap: wrap;
    gap: 8px;
}

.spec-tag {
    background: #f1f8ff;
    color: #0366d6;
    font-size: 0.75rem;
    font-weight: 600;
    padding: 2px 8px;
    border-radius: 12px;
}

.project-desc {
    font-size: 0.95rem;
    color: #586069;
    line-height: 1.5;
    margin-bottom: 20px;
}

/* Links / Buttons */
.project-links {
    padding: 20px;
    background-color: #fcfcfc;
    border-top: 1px solid #e1e4e8;
    display: flex;
    gap: 15px;
}

.btn-link {
    font-size: 0.9rem;
    font-weight: 600;
    text-decoration: none;
    color: #0366d6;
}

.btn-link:hover {
    text-decoration: underline;
}

</style>

<h1 style="margin-bottom: 40px; text-align: center;">My Technical Projects</h1>

<div class="projects-grid">

    <article class="project-card">
        <div class="project-media">
            <img src="/assets/images/robot-arm.jpg" alt="Robot Arm Project">
        </div>
        <div class="project-content">
            <h2 class="project-title">Teleoperated Robot Arm</h2>
            <div class="project-specs">
                <span class="spec-tag">Python</span>
                <span class="spec-tag">ROS</span>
                <span class="spec-tag">SolidWorks</span>
            </div>
            <p class="project-desc">
                Designed and built a 6-DOF robotic arm capable of mimicking human hand gestures in real-time. 
                Used inverse kinematics for precise control and minimal latency.
            </p>
        </div>
        <div class="project-links">
            <a href="https://github.com/username/project-repo" class="btn-link">View Code &rarr;</a>
            <a href="#" class="btn-link">Read Report</a>
        </div>
    </article>

    <article class="project-card">
        <div class="project-media">
            <iframe src="https://www.youtube.com/embed/dQw4w9WgXcQ" title="Project Video" allowfullscreen></iframe>
        </div>
        <div class="project-content">
            <h2 class="project-title">Autonomous Drone</h2>
            <div class="project-specs">
                <span class="spec-tag">C++</span>
                <span class="spec-tag">Computer Vision</span>
            </div>
            <p class="project-desc">
                Developed an obstacle avoidance algorithm for a quadcopter using Lidar and optical flow sensors.
                Achieved 95% success rate in dense forest environments.
            </p>
        </div>
        <div class="project-links">
            <a href="#" class="btn-link">Watch Demo &rarr;</a>
        </div>
    </article>

    <article class="project-card">
        <div class="project-media">
            <img src="https://via.placeholder.com/400x200" alt="Placeholder">
        </div>
        <div class="project-content">
            <h2 class="project-title">New Project Title</h2>
            <div class="project-specs">
                <span class="spec-tag">Skill 1</span>
                <span class="spec-tag">Skill 2</span>
            </div>
            <p class="project-desc">
                Write a short description of your project here. What problem did you solve? What tools did you use?
            </p>
        </div>
        <div class="project-links">
            <a href="#" class="btn-link">Link 1 &rarr;</a>
            <a href="#" class="btn-link">Link 2</a>
        </div>
    </article>

</div>
