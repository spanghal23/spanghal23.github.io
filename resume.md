---
layout: default
title: Resume
permalink: /resume/
---

<style>
    /* Ensure the theme allows content to overflow the central column */
    .wrapper, .container, .page-content, article {
        overflow: visible !important;
    }

    .resume-breakout {
        /* 1. Set width to 80% of the screen width */
        width: 80vw;

        /* 2. Center the element relative to the viewport */
        position: relative;
        left: 50%;
        margin-left: -40vw; /* This pulls it back by half the width (80vw / 2) */
        
        /* 3. Height and spacing */
        height: 85vh;
        margin-top: 30px;
        margin-bottom: 50px;
        
        /* 4. Visuals */
        box-shadow: 0 4px 12px rgba(0,0,0,0.15);
        border: 1px solid #ddd;
        background: #fff;
    }

    object {
        width: 100%;
        height: 100%;
        display: block;
    }
</style>

<div class="resume-breakout">
    <object data="/assets/resumes/sameer_panghal_resume_master.pdf" type="application/pdf">
        <div style="display: flex; justify-content: center; align-items: center; height: 100%; background: #f6f8fa; color: #333;">
            <div style="text-align: center; padding: 20px;">
                <p style="margin-bottom: 15px;">Your browser does not support embedded PDFs.</p>
                <a href="/assets/resumes/sameer_panghal_resume_master.pdf" style="background: #0366d6; color: #fff; padding: 10px 20px; text-decoration: none; border-radius: 6px;">Download Resume PDF</a>
            </div>
        </div>
    </object>
</div>
