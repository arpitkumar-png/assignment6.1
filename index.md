HTML
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Assignment 6.1 — Box Model Inspection</title>
    <!-- Link to External Stylesheet -->
    <link rel="stylesheet" href="box-style.css">
</head>
<body>

    <!-- Header -->
    <header class="page-header">
        <h1>CSS Box Model Inspection</h1>
        <p>Exploring content, padding, border, and margin across different boxes.</p>
    </header>

    <main class="container">
        <!-- Box 1 -->
        <div class="box box-one">
            <h2>Box One</h2>
            <p>This box demonstrates compact padding, a thin solid border, and standard content sizing.</p>
        </div>

        <!-- Box 2 -->
        <div class="box box-two">
            <h2>Box Two</h2>
            <p>This box features generous padding, a thick dashed border, and wider margins.</p>
        </div>

        <!-- Box 3 -->
        <div class="box box-three">
            <h2>Box Three</h2>
            <p>This box highlights <strong>border-box</strong> sizing, ensuring padding and borders are included within the set width.</p>
        </div>
    </main>

    <!-- Footer -->
    <footer>
        <p>&copy; 2026 Student Box Model Lab. All rights reserved.</p>
    </footer>

</body>
</html>
File 2: box-style.css
CSS
/* --- Global Reset & Box Sizing Demonstration --- */
* {
    /* Step 4: By default, modern CSS uses border-box so padding/borders don't expand total width unexpectedly */
    box-sizing: border-box; 
}

body {
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    background-color: #f1f5f9;
    color: #334155;
    line-height: 1.6;
    padding: 2rem;
}

/* --- Header Styling --- */
.page-header {
    text-align: center;
    margin-bottom: 2.5rem;
}

.page-header h1 {
    color: #1e3a8a;
    font-size: 2rem;
    margin-bottom: 0.5rem;
}

.page-header p {
    color: #64748b;
}

/* --- Main Container --- */
.container {
    max-width: 600px;
    margin: 0 auto;
}

/* --- Base Box Styles --- */
.box {
    background-color: #ffffff;
    border-radius: 8px;
    box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.05);
}

.box h2 {
    font-size: 1.25rem;
    color: #1e293b;
    margin-bottom: 0.5rem;
}

.box p {
    font-size: 0.95rem;
    color: #475569;
}

/* --- 3. Unique Box Styling (Padding, Border, Margin) --- */

/* Box One: Compact and standard */
.box-one {
    width: 100%;
    padding: 1rem;                  /* Padding */
    border: 2px solid #3b82f6;      /* Border */
    margin-bottom: 1.5rem;          /* Margin */
}

/* Box Two: Generous padding, dashed accent border, larger margin */
.box-two {
    width: 100%;
    padding: 2rem;                  /* Larger Padding */
    border: 4px dashed #f59e0b;     /* Thick Dashed Border */
    margin-bottom: 2rem;            /* Larger Margin */
}

/* Box Three: Explicit styling to inspect box-sizing */
.box-three {
    width: 100%;
    padding: 1.5rem;                /* Padding */
    border: 3px solid #10b981;      /* Green Solid Border */
    margin-bottom: 1rem;            /* Margin */
    /* 
       Note on content-box vs border-box:
       - content-box: width = content only (padding & border add ON TOP of width).
       - border-box: width = content + padding + border (stays contained).
    */
    box-sizing: border-box; 
}