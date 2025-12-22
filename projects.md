---
layout: single
permalink: /projects/
title: Projects  # <--- Define the main page title here
---

<article class="project-card">
    <div class="project-media">
        <img src="/assets/images/robot-arm.jpg" alt="Teleoperated Robot Arm">
    </div>
    <div class="project-content">
        <h2 class="project-title">Teleoperated Robot Arm</h2>
        <div class="project-specs">
            <span class="spec-tag">Python & C++</span>
            <span class="spec-tag">CANBUS</span>
            <span class="spec-tag">Field-Oriented Control</span>
            <span class="spec-tag">MATLAB</span>
        </div>
        <p class="project-desc">
            This project involved the complete design and fabrication of a 4-DOF robotic arm driven by custom actuators with 10:1 planetary gearboxes. The mechanical design was validated through static load calculations in MATLAB, achieving a holding torque of 18.8 N-m with a safety factor of 1.3. On the electrical side, I engineered a 600W power distribution architecture and implemented closed-loop Field-Oriented Control (FOC) using ODrive S1 units and an STM32 microcontroller via CANBUS. [cite_start]The system is controlled through a custom teleoperation pipeline I developed in Python, which maps computer vision outputs directly to actuator setpoints to execute synchronized, high-precision motion[cite: 51, 52, 55, 56, 57].
        </p>
    </div>
    <div class="project-links">
        <a href="#" class="btn-link">View Code &rarr;</a>
        <a href="#" class="btn-link">Watch Demo</a>
    </div>
</article>


<article class="project-card">
    <div class="project-media">
        <img src="/assets/images/ball-levitation.jpg" alt="Ball Levitation Project">
    </div>
    <div class="project-content">
        <h2 class="project-title">Variable Input Ball Levitation</h2>
        <div class="project-specs">
            <span class="spec-tag">Control Theory (PID)</span>
            <span class="spec-tag">Signal Processing</span>
            <span class="spec-tag">Mechatronics</span>
        </div>
        <p class="project-desc">
            To achieve stable levitation of a ball at variable heights, I built a closed-loop mechatronic system grounded in a physics-based plant model derived from first principles. By validating this model against experimental data, I achieved 95% simulation accuracy, which allowed for precise control law design. I implemented a PD-based height controller that outperformed standard PID implementations, maintaining the ball's position within 2mm of the target. [cite_start]The system reliability was further enhanced by applying Kalman filters and moving averages to mitigate sensor noise, alongside a hardware-software co-design that optimized the integration of ultrasonic sensors and brushless DC fan airflow[cite: 65, 68, 69, 70, 72].
        </p>
    </div>
    <div class="project-links">
        <a href="#" class="btn-link">Read Report &rarr;</a>
    </div>
</article>

<article class="project-card">
    <div class="project-media">
        <img src="/assets/images/eoat.jpg" alt="End of Arm Tooling">
    </div>
    <div class="project-content">
        <h2 class="project-title">Custom Cobot End-of-Arm-Tool</h2>
        <div class="project-specs">
            <span class="spec-tag">SolidWorks</span>
            <span class="spec-tag">FEA Analysis</span>
            <span class="spec-tag">GD&T</span>
            <span class="spec-tag">Robotics</span>
        </div>
        <p class="project-desc">
            During my time at the Schaeffler Group, I designed and deployed a custom End-Of-Arm-Tool (EOAT) for Techman and Universal Robots capable of handling 2.5kg loads. I utilized Finite Element Analysis (FEA) to simulate force loading, which drove design changes that reduced cantilever beam deflection by 3 degrees. The final components were professionally machined from MIC6-Aluminum based on extensive GD&T drawings I created to ensure dimensional stability. [cite_start]I also programmed the robot's vision sensing to detect rack vacancies, optimizing the pick-and-place cycle and contributing to an estimated $720,000 in annual savings[cite: 31, 32, 33, 34, 35].
        </p>
    </div>
    <div class="project-links">
        <a href="#" class="btn-link">View Project &rarr;</a>
    </div>
</article>
