---
layout: default
title: Resume
permalink: /resume/
---

<style>
    /* This class targets the main content container of many common Jekyll themes.
       We set overflow to visible to allow our PDF box to extend outside of it. */
    .wrapper, .container, .page-content, article {
        overflow: visible !important;
    }

    /* This is the container for your PDF */
    .resume-breakout {
        /* 1. Make the width exactly the full width of the browser window */
        width: 100vw;
        
        /* 2. The magic calculation to center a full-width element inside a narrow parent */
        margin-left: calc(50% - 50vw);
        margin-right: 0;

        /* 3. Height and vertical spacing settings */
        height: 85vh; /* Uses 85% of the screen height */
        margin-top: 30px;
        margin-bottom: 50px;
        
        /* 4. Visual styling */
        box-shadow: 0 6px 15px rgba(0,0,0,0.15); /* A more pronounced shadow */
        border-top: 1px solid #e1e4e8;
        border-bottom: 1px solid #e1e4e8;
        background: #fff;
    }

    /* Make the PDF object fill its container */
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
                <p style="margin-bottom: 15px; font-size: 1.1em;">Your browser does not support embedded PDFs.</p>
                <a href="/assets/resumes/sameer_panghal_resume_master.pdf" style="background: #0366d6; color: #fff; padding: 12px 24px; text-decoration: none; border-radius: 6px; font-weight: bold;">Download Resume PDF</a>
            </div>
        </div>
    </object>
</div>
