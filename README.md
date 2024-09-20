# sarahahmed.github.io
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Sarah Ahmed - Mobile Developer</title>
    <style>
        :root {
            --primary-color: #6A1B9A;
            --secondary-color: #E1BEE7;
            --accent-color: #9C27B0;
            --background-color: #F3E5F5;
            --text-color: #4A148C;
            --light-text-color: #FFFFFF;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Arial', sans-serif;
            line-height: 1.6;
            color: var(--text-color);
            background-color: var(--background-color);
        }

        .container {
            max-width: 1100px;
            margin: auto;
            overflow: hidden;
            padding: 0 2rem;
        }

        header {
            background: var(--primary-color);
            color: var(--light-text-color);
            padding: 1rem 0;
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1;
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
        }

        header .logo {
            float: left;
            font-size: 1.5rem;
        }

        header nav {
            float: right;
        }

        header nav ul {
            display: flex;
        }

        header nav ul li {
            list-style: none;
        }

        header nav ul li a {
            color: var(--light-text-color);
            text-decoration: none;
            padding: 0.75rem;
            transition: all 0.3s ease;
        }

        header nav ul li a:hover {
            background: var(--secondary-color);
            color: var(--text-color);
        }

        .hero {
            background: linear-gradient(rgba(106, 27, 154, 0.8), rgba(156, 39, 176, 0.8)), url('3.jpg') no-repeat center center/cover;
            height: 100vh;
            position: relative;
            color: var(--light-text-color);
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            text-align: center;
            padding: 0 20px;
        }

        .hero h1 {
            font-size: 4rem;
            margin-bottom: 1rem;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.1);
        }

        .hero p {
            font-size: 1.5rem;
            margin-bottom: 2rem;
        }

        .btn {
            display: inline-block;
            background: var(--accent-color);
            color: var(--light-text-color);
            padding: 0.75rem 1.5rem;
            text-decoration: none;
            border-radius: 5px;
            transition: all 0.3s ease;
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
        }

        .btn:hover {
            background: var(--secondary-color);
            color: var(--text-color);
            transform: translateY(-3px);
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
        }

        .section-title {
            text-align: center;
            font-size: 2.5rem;
            margin: 2rem 0;
            color: var(--primary-color);
        }

        .about {
            background-color: var(--secondary-color);
            padding: 3rem 0;
            margin-top: 2rem;
        }

        .about-content {
            display: flex;
            align-items: center;
            justify-content: space-between;
        }

        .about-text {
            flex: 1;
            padding-right: 2rem;
        }

        .about-image {
            flex: 1;
            text-align: center;
        }

        .about-image img {
            max-width: 100%;
            border-radius: 50%;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
        }

        .projects {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
            padding: 2rem 0;
        }

        .project {
            background: var(--light-text-color);
            border-radius: 10px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
            transition: all 0.3s ease;
            overflow: hidden;
            cursor: pointer;
        }

        .project:hover {
            transform: translateY(-5px);
            box-shadow: 0 6px 12px rgba(0, 0, 0, 0.15);
        }

        .project-carousel {
            position: relative;
            height: 200px;
            overflow: hidden;
        }

        .project-carousel img {
            width: 100%;
            height: 200px;
            object-fit: cover;
            position: absolute;
            top: 0;
            left: 0;
            opacity: 0;
            transition: opacity 0.5s ease-in-out;
        }

        .project-carousel img.active {
            opacity: 1;
        }

        .project-info {
            padding: 1.5rem;
        }

        .project-info h3 {
            margin-bottom: 0.5rem;
            color: var(--primary-color);
        }

        .skills {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            padding: 2rem 0;
        }

        .skill {
            background: var(--secondary-color);
            color: var(--text-color);
            padding: 0.5rem 1rem;
            margin: 0.5rem;
            border-radius: 20px;
            transition: all 0.3s ease;
            box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
        }

        .skill:hover {
            background: var(--accent-color);
            color: var(--light-text-color);
            transform: translateY(-3px);
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
        }

        footer {
            background: var(--primary-color);
            color: var(--light-text-color);
            text-align: center;
            padding: 1rem 0;
            box-shadow: 0 -2px 5px rgba(0, 0, 0, 0.1);
        }

        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }

        .fade-in {
            animation: fadeIn 1s ease-out;
        }
    </style>
</head>
<body>
    <header>
        <div class="container">
            <div class="logo">Sarah Ahmed</div>
            <nav>
                <ul>
                    <li><a href="#home">Home</a></li>
                    <li><a href="#about">About</a></li>
                    <li><a href="#projects">Projects</a></li>
                    <li><a href="#skills">Skills</a></li>
                    <li><a href="#contact">Contact</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <section id="home" class="hero">
        <h1 class="fade-in">Sarah Ahmed</h1>
        <p class="fade-in">Mobile Developer </p>
        <a href="#projects" class="btn fade-in">View My Work</a>
    </section>

    <section id="about" class="about">
        <div class="container">
            <h2 class="section-title">About Me</h2>
            <div class="about-content">
                <div class="about-text">
                    <p>Hello! I'm Sarah Ahmed, a fresh graduate from Assiut University's Faculty of Computers and Informatics. I'm passionate about mobile development and currently volunteering as a Monitor at Google Developer Student Club (GDSC).</p>
                    <p>My journey in mobile development began during my university years, where I honed my skills in Java, Kotlin, OOP principles, Dart, and Flutter. I'm dedicated to applying these skills to real-world projects and staying updated with the latest technological advancements.</p>
                    <p>As a GDSC Monitor, I help students with mobile development courses, providing feedback and assisting with problem-solving to ensure effective learning outcomes. I'm excited about the opportunity to grow in the field of mobile development and contribute to innovative projects.</p>
                </div>
                <div class="about-image">
                    <img src="20.jpg" alt="Sarah Ahmed">
                </div>
            </div>
        </div>
    </section>

    <section id="projects">
        <div class="container">
            <h2 class="section-title">My Projects</h2>
            <div class="projects">
                <div class="project fade-in" onclick="window.open('demo1.html', '_blank')">
                    <div class="project-carousel">
                        <img src="4.jpg" alt="Digital Copyrights 1" class="active">
                        <img src="5.jpg" alt="Digital Copyrights 2">
                        <img src="6.jpg" alt="Digital Copyrights 3">
                        <img src="7.jpg" alt="Digital Copyrights 3">
                        <img src="8.jpg" alt="Digital Copyrights 3">
                        <img src="9.jpg" alt="Digital Copyrights 3">
                        
                    
                    </div>
                    <div class="project-info">
                        <h3>Digital Copyrights (Graduation Project)</h3>
                        <p>A social network platform with a unique feature to detect and prevent unauthorized sharing of digital content. Built using Django REST framework and Flutter.</p>
                    </div>
                </div>
                <div class="project fade-in" onclick="window.open('demo2.html', '_blank')">
                    <div class="project-carousel">
                        <img src="11.jpg" alt="Digital Copyrights 3">
                        <img src="12.jpg" alt="Digital Copyrights 3">
                        <img src="13.jpg" alt="Digital Copyrights 3">
                        <img src="14.jpg" alt="Digital Copyrights 3">
                        <img src="15.jpg" alt="Digital Copyrights 3">

                    </div>
                    <div class="project-info">
                        <h3>ChatApp</h3>
                        <p>Developed a simple ChatApp using Java, which allows users to create accounts and send
                            text messages to one another.</p>
                            <p>The project features a basic user registration and login system, enabling account creation
                            and authentication. Once logged in, users can exchange text messages in real-time with
                            other registered accounts.
                            </p>
                    </div>
                </div>
                
            </div>
        </div>
    </section>

    <section id="skills">
        <div class="container">
            <h2 class="section-title">My Skills</h2>
            <div class="skills">
                <div class="skill fade-in">Java</div>
                <div class="skill fade-in">Dart</div>
                <div class="skill fade-in">Flutter</div>
                <div class="skill fade-in">OOP</div>
                <div class="skill fade-in">UI/UX Design</div>
                <div class="skill fade-in">REST APIs</div>
            </div>
        </div>
    </section>

    <footer id="contact">
        <div class="container">
            <p>&copy; 2024 Sarah Ahmed. All rights reserved.</p>
            <p>Email: saraahmed512@gmail.com | Phone: +201066401241</p>
            <p>Location: Assiut, Egypt</p>
        </div>
    </footer>

    <script>
        document.addEventListener('DOMContentLoaded', (event) => {
            const fadeElems = document.querySelectorAll('.fade-in');
            const observer = new IntersectionObserver((entries) => {
                entries.forEach(entry => {
                    if (entry.isIntersecting) {
                        entry.target.style.opacity = 1;
                        entry.target.style.transform = 'translateY(0)';
                    }
                });
            }, {
                threshold: 0.1
            });

            fadeElems.forEach(elem => {
                observer.observe(elem);
            });

            // Smooth scrolling for navigation links
            document.querySelectorAll('a[href^="#"]').forEach(anchor => {
                anchor.addEventListener('click', function (e) {
                    e.preventDefault();
                    document.querySelector(this.getAttribute('href')).scrollIntoView({
                        behavior: 'smooth'
                    });
                });
            });

            // Automated image carousel for projects
            const carousels = document.querySelectorAll('.project-carousel');
            carousels.forEach(carousel => {
                const images = carousel.querySelectorAll('img');
                let currentIndex = 0;

                setInterval(() => {
                    images[currentIndex].classList.remove('active');
                    currentIndex = (currentIndex + 1) % images.length;
                    images[currentIndex].classList.add('active');
                }, 3000); // Change image every 3 seconds
            });
        });
    </script>
</body>
</html>
