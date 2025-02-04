<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Student Portfolio</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.1/css/all.min.css">
    <style>
        body {
            display: flex;
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            height: 100vh;
            background-color: #f5f5f5;
        }
        .left-panel {
            width: 25%;
            background-color: #2c3e50;
            color: white;
            display: flex;
            flex-direction: column;
            align-items: center;
            padding-top: 20px;
        }
        .left-panel img {
            width: 100px;
            height: 100px;
            border-radius: 50%;
            margin-bottom: 20px;
        }
        .nav-links {
            display: flex;
            flex-direction: column;
            width: 100%;
            text-align: center;
        }
        .nav-links a {
            text-decoration: none;
            color: white;
            padding: 15px;
            display: block;
            transition: 0.3s;
        }
        .nav-links a:hover {
            background-color: #34495e;
        }
        .right-panel {
            width: 75%;
            padding: 40px;
        }
        .card {
            background: white;
            padding: 20px;
            margin-top: 20px;
            border-radius: 8px;
            box-shadow: 0px 4px 6px rgba(0, 0, 0, 0.1);
            cursor: pointer;
            text-align: center;
        }
        .skills-bar {
            display: none;
            width: 100%;
        }
        .skill {
            margin: 10px 0;
        }
        .bar {
            width: 100%;
            background-color: #ddd;
            border-radius: 5px;
            overflow: hidden;
        }
        .bar div {
            height: 20px;
            text-align: right;
            padding-right: 5px;
            line-height: 20px;
            color: white;
            background-color: #3498db;
        }
        .contact-form input, .contact-form textarea {
            width: 100%;
            padding: 10px;
            margin: 10px 0;
            border-radius: 5px;
            border: 1px solid #ccc;
        }
        .contact-form button {
            width: 100%;
            padding: 10px;
            background-color: #2c3e50;
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }
        .project-cards {
            display: flex;
            gap: 30px;
            flex-wrap: wrap;
            justify-content: space-evenly;
        }
        .project-card {
            width: 300px;
            min-height: 250px;
            background: white;
            border-radius: 8px;
            box-shadow: 0px 4px 6px rgba(0, 0, 0, 0.1);
            text-align: center;
            display: flex;
            flex-direction: column;
            justify-content: space-between;
            padding: 20px;
            cursor: pointer;
            transition: transform 0.3s ease, background-color 0.3s ease;
        }
        .project-card:hover {
            transform: translateY(-10px);
        }
        .project-card h3 {
            font-size: 1.5rem;
            margin: 10px 0;
        }
        .project-card p {
            font-size: 1rem;
            margin-bottom: 15px;
            color: #555;
        }
        .project-card a {
            margin-top: 10px;
            text-decoration: none;
            color: #3498db;
            font-weight: bold;
            font-size: 1.1rem;
        }
        /* Colorful background for each project card */
        .project-card:nth-child(1) {
            background-color: #f39c12; /* Yellow */
            color: #fff;
        }
        .project-card:nth-child(2) {
            background-color: #1abc9c; /* Teal */
            color: #fff;
        }
        .project-card:nth-child(3) {
            background-color: #9b59b6; /* Purple */
            color: #fff;
        }
        .project-card:nth-child(4) {
            background-color: #e67e22; /* Orange */
            color: #fff;
        }
        .section-header {
            display: flex;
            align-items: center;
        }
        .section-header i {
            margin-right: 10px;
        }
    </style>
    <script>
        function toggleSkills() {
            var skills = document.getElementById("skills");
            skills.style.display = skills.style.display === "none" ? "block" : "none";
        }
    </script>
</head>
<body>
    <div class="left-panel">
        <img src="myp.jpg" alt="Profile Picture">
        <div class="nav-links">
            <a href="#about">About Me</a>
            <a href="#projects">Projects</a>
            <a href="#contact">Contact Me</a>
        </div>
    </div>
    <div class="right-panel">
        <h1>About Me</h1>
        <p>Hello, I’m Tridib Deb Pabel, a dedicated competitive programmer with a passion for solving complex problems and creating intuitive, high-performance web applications.</p>
        
        <div class="card">
            <h2 class="section-header"><i class="fas fa-graduation-cap"></i> Education</h2>
            <p>Bachelor of Science in Computer Science & Engineering, Premier University Chittagong</p>
        </div>
        
        <div class="card" onclick="toggleSkills()">
            <h2 class="section-header"><i class="fas fa-cogs"></i> Technical Skills</h2>
            <div id="skills" class="skills-bar" style="display: none;">
                <div class="skill">DSA <div class="bar"><div style="width: 70%">70%</div></div></div>
                <div class="skill">HTML <div class="bar"><div style="width: 85%">85%</div></div></div>
                <div class="skill">CSS <div class="bar"><div style="width: 80%">80%</div></div></div>
                <div class="skill">JavaScript <div class="bar"><div style="width: 75%">75%</div></div></div>
                <div class="skill">Bootstrap <div class="bar"><div style="width: 70%">70%</div></div></div>
            </div>
        </div>
        
        <div class="card">
            <h2 class="section-header"><i class="fas fa-briefcase"></i> Experience</h2>
            <p>Experienced in solving problems for 2 years.</p>
        </div>
        
        <!-- Achievements Section -->
        <div class="card">
            <h2 class="section-header"><i class="fas fa-trophy"></i> Achievements</h2>
            <h3>Online Judges</h3>
            <p><strong>Codeforces:</strong> Username: ELSE_IF_TRIDIB21</p>
            <p>Solved 700+ Problems</p>
            <p>Max Rating: 1143</p>
            <p><strong>Codechef:</strong> Username: tridib21</p>
            <p>Solved 250+ Problems</p>
            <p>Max Rating: 1506</p>
        </div>
        
        <h1 id="projects">Projects</h1>
        <div class="project-cards">
            <div class="project-card">
                <h3>Portfolio Website Without Using Bootstrap</h3>
                <p>Designed and developed a personal portfolio website without using Bootstrap to showcase my skills and projects.</p>
                <a href="https://tridibdeb21.github.io/PWOB/" target="_blank" class="btn btn-primary">Learn More</a>
            </div>
            <div class="project-card">
                <h3>Portfolio Website</h3>
                <p>Designed and developed a personal portfolio website to showcase my skills and projects.</p>
                <a href="https://tridibdeb21.github.io/PWB/" target="_blank" class="btn btn-primary">Learn More</a>
            </div>
        </div>
        
        <h1 id="contact">Contact Me</h1>
        <p><i class="fas fa-envelope"></i> Email: tridibdeb21@gmail.com</p>
        <p><i class="fas fa-phone"></i> Phone: +880 1886560232</p>
        <p><i class="fas fa-map-marker-alt"></i> Location: Chittagong, Bangladesh</p>
        <p><i class="fab fa-linkedin"></i> LinkedIn: <a href="https://www.linkedin.com/in/tridib-deb-407048297">Linkedin</a></p>
        <form class="contact-form">
            <input type="text" placeholder="Your Name">
            <input type="email" placeholder="Your Email">
            <textarea placeholder="Your Message"></textarea>
            <button type="submit">Send Message</button>
        </form>
    </div>
</body>
</html>
