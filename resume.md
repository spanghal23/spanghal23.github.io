---
layout: default
title: Resume
permalink: /resume/
---

<style>
/* "Breakout" CSS to escape the narrow theme column */
.resume-wrapper {
    /* 1. Force the width to be 95% of the user's screen */
    width: 80vw; 
    
    /* 2. Cap the width for huge monitors (optional, remove if you want full stretch) */
    max-width: 1400px; 
    
    /* 3. The Magic: Center the element relative to the screen, not the theme column */
    position: relative;
    left: 50%;
    right: 50%;
    margin-left: -47.5vw; /* This must be half of the width (95vw / 2) */
    margin-right: -47.5vw;
    
    /* 4. Height settings */
    height: 85vh;
    margin-top: 20px;
    margin-bottom: 40px;
    
    /* 5. Visuals */
    box-shadow: 0 4px 15px rgba(0,0,0,0.1);
    border: 1px solid #ddd;
    background: #fff;
}

object {
    width: 100%;
    height: 100%;
    display: block;
}
</style>

<div class="resume-wrapper">
    <object data="/assets/resumes/sameer_panghal_resume_master.pdf" type="application/pdf">
        <div style="padding: 20px; text-align: center;">
            <p>Your browser does not support embedded PDFs.</p>
            <a href="/assets/resumes/sameer_panghal_resume_master.pdf" style="background: #333; color: #fff; padding: 10px 20px; text-decoration: none; border-radius: 5px;">Download Resume PDF</a>
        </div>
    </object>
</div>
