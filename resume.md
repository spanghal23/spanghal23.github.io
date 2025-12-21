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
            overflow: hidden; /* Prevents double scrollbars */
            font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Helvetica, Arial, sans-serif;
        }

        .top-bar {
            background-color: #f6f8fa;
            border-bottom: 1px solid #d0d7de;
            padding: 10px 20px;
            display: flex;
            align-items: center;
            height: 40px;
        }

        .back-btn {
            text-decoration: none;
            color: #0969da;
            font-weight: 600;
            font-size: 14px;
        }
        
        .back-btn:hover {
            text-decoration: underline;
        }

        /* The PDF container */
        .pdf-container {
            height: calc(100% - 61px); /* 100% height minus the top bar height */
            width: 100%;
        }
        
        iframe {
            width: 100%;
            height: 100%;
            border: none;
        }
    </style>
</head>
<body>

    <div class="top-bar">
        <a href="/" class="back-btn">&larr; Back to Portfolio</a>
    </div>

    <div class="pdf-container">
        <iframe src="/assets/resumes/sameer_panghal_resume_master.pdf">
            <p>Your browser does not support PDFs. 
            <a href="/assets/resumes/sameer_panghal_resume_master.pdf">Download the PDF</a>.</p>
        </iframe>
    </div>

</body>
</html>
