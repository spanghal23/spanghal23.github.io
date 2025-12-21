---
permalink: /resume/
layout: null
---
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Resume - Sameer Panghal</title>
    <style>
        body, html {
            margin: 0;
            padding: 0;
            height: 100%;
            overflow: hidden; /* Locks the page so only the PDF scrolls */
            background-color: #525659; /* Matches standard PDF viewer background */
            font-family: sans-serif;
        }

        /* Minimal Header */
        .header {
            height: 40px;
            background-color: #333;
            color: white;
            display: flex;
            align-items: center;
            padding: 0 20px;
        }

        .header a {
            color: #fff;
            text-decoration: none;
            font-size: 14px;
            font-weight: bold;
        }

        .header a:hover {
            text-decoration: underline;
        }

        /* The Embed Container */
        .resume-container {
            width: 100%;
            height: calc(100% - 40px); /* Subtract header height */
        }

        embed {
            width: 100%;
            height: 100%;
        }
    </style>
</head>
<body>

    <div class="header">
        <a href="/">&larr; Back to Portfolio</a>
    </div>

    <div class="resume-container">
        <embed 
            src="/assets/resumes/sameer_panghal_resume_master.pdf" 
            type="application/pdf"
            width="100%" 
            height="100%"
        />
    </div>

</body>
</html>
