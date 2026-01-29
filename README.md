<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>The Chikeluba Modozie | Backend Engineer & Process Architect</title>
    <link rel="stylesheet" href="some.css">
   <style>
            * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        :root {
            --primary-color: #6c63ff;
            --secondary-color: #ff6584;
            --dark-bg: #1a1a2e;
            --darker-bg: #16162a;
            --text-light: #ffffff;
            --text-gray: #a0a0a0;
            --accent-color: #00d9ff;
        }

        html {
            scroll-behavior: smooth;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            line-height: 1.6;
            color: var(--text-light);
            background-color: var(--dark-bg);
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        .navbar {
            position: fixed;
            top: 0;
            width: 100%;
            background: rgba(26, 26, 46, 0.95);
            backdrop-filter: blur(10px);
            z-index: 1000;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.3);
        }

        .navbar .container {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 1rem 20px;
        }

        .nav-brand a {
            font-size: 1.8rem;
            font-weight: bold;
            color: var(--primary-color);
            text-decoration: none;
        }

        .nav-toggle {
            display: none;
        }

        .nav-toggle-label {
            display: none;
            font-size: 1.5rem;
            cursor: pointer;
            color: var(--text-light);
        }

        .nav-menu {
            display: flex;
            list-style: none;
            gap: 2rem;
        }

        .nav-menu a {
            color: var(--text-light);
            text-decoration: none;
            font-weight: 500;
            transition: color 0.3s ease;
        }

        .nav-menu a:hover,
        .nav-menu a:focus {
            color: var(--primary-color);
        }

        .hero {
            min-height: 100vh;
            display: flex;
            align-items: center;
            background: linear-gradient(135deg, var(--darker-bg) 0%, var(--dark-bg) 100%);
            padding-top: 80px;
        }

        .hero-content {
            text-align: center;
            max-width: 800px;
            margin: 0 auto;
            animation: fadeInUp 1s ease;
        }

        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        .hero-greeting {
            font-size: 1.2rem;
            color: var(--text-gray);
            margin-bottom: 1rem;
        }

        .hero-name {
            font-size: 3.5rem;
            margin-bottom: 1rem;
            background: linear-gradient(135deg, var(--primary-color), var(--accent-color));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .hero-title {
            font-size: 1.5rem;
            color: var(--text-gray);
            margin-bottom: 1.5rem;
            font-weight: 400;
        }

        .hero-description {
            font-size: 1.1rem;
            color: var(--text-gray);
            margin-bottom: 2rem;
            line-height: 1.8;
        }

        .btn {
            display: inline-block;
            padding: 12px 30px;
            text-decoration: none;
            border-radius: 5px;
            font-weight: 600;
            transition: all 0.3s ease;
            border: 2px solid transparent;
        }

        .btn-primary {
            background: var(--primary-color);
            color: var(--text-light);
        }

        .btn-primary:hover,
        .btn-primary:focus {
            background: transparent;
            border-color: var(--primary-color);
            transform: translateY(-2px);
        }

        .btn-outline {
            background: transparent;
            border-color: var(--primary-color);
            color: var(--primary-color);
        }

        .btn-outline:hover,
        .btn-outline:focus {
            background: var(--primary-color);
            color: var(--text-light);
        }

        .about {
            padding: 100px 0;
            background: var(--darker-bg);
        }

        .section-header {
            text-align: center;
            margin-bottom: 3rem;
        }

        .section-header h2 {
            font-size: 2.5rem;
            margin-bottom: 1rem;
        }

        .section-header h3 {
            font-size: 2rem;
            color: var(--text-gray);
            margin-bottom: 1rem;
        }

        .section-header p {
            color: var(--text-gray);
            max-width: 600px;
            margin: 0 auto;
        }

        .about-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 3rem;
            align-items: center;
        }

        .about-text h3 {
            font-size: 1.8rem;
            margin-bottom: 1.5rem;
            color: var(--primary-color);
        }

        .about-text p {
            color: var(--text-gray);
            margin-bottom: 1.5rem;
            line-height: 1.8;
        }

        .about-image {
            display: flex;
            justify-content: center;
        }

        .image-placeholder,
        .video-placeholder {
            background: linear-gradient(135deg, var(--primary-color), var(--accent-color));
            border-radius: 10px;
            width: 100%;
            height: 400px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.2rem;
            color: var(--text-light);
        }

        .skills {
            padding: 100px 0;
            background: var(--dark-bg);
        }

        .skills-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 3rem;
        }

        .technical-skills h3 {
            font-size: 1.8rem;
            margin-bottom: 2rem;
            color: var(--primary-color);
        }

        .skill-item {
            margin-bottom: 1.5rem;
        }

        .skill-header {
            display: flex;
            justify-content: space-between;
            margin-bottom: 0.5rem;
            color: var(--text-light);
        }

        .skill-bar {
            width: 100%;
            height: 10px;
            background: var(--darker-bg);
            border-radius: 5px;
            overflow: hidden;
        }

        .skill-progress {
            height: 100%;
            background: linear-gradient(90deg, var(--primary-color), var(--accent-color));
            animation: fillBar 1.5s ease forwards;
        }

        @keyframes fillBar {
            from {
                transform: translateX(-100%);
            }
            to {
                transform: translateX(0);
            }
        }

        .tabs {
            position: relative;
        }

        .tabs input[type="radio"] {
            position: absolute;
            opacity: 0;
        }

        .tabs label.tab-btn {
            display: inline-block;
            padding: 10px 20px;
            background: transparent;
            border: 2px solid var(--primary-color);
            color: var(--primary-color);
            border-radius: 5px;
            cursor: pointer;
            transition: all 0.3s ease;
            font-size: 1rem;
            margin-right: 1rem;
            margin-bottom: 2rem;
        }

        .tabs input[type="radio"]:checked + label.tab-btn {
            background: var(--primary-color);
            color: var(--text-light);
        }

        .tabs label.tab-btn:hover {
            background: var(--primary-color);
            color: var(--text-light);
        }

        .tab-content {
            display: none;
        }

        #tab-experience:checked ~ .tab-experience-content {
            display: block;
        }

        #tab-education:checked ~ .tab-education-content {
            display: block;
        }

        .timeline-item {
            padding: 1.5rem;
            background: var(--darker-bg);
            border-radius: 8px;
            margin-bottom: 1rem;
            border-left: 4px solid var(--primary-color);
            transition: transform 0.3s ease;
        }

        .timeline-item:hover {
            transform: translateX(10px);
        }

        .timeline-item h4 {
            font-size: 1.2rem;
            margin-bottom: 0.5rem;
            color: var(--text-light);
        }

        .timeline-date {
            color: var(--accent-color);
            font-size: 0.9rem;
            margin-bottom: 0.3rem;
        }

        .timeline-company {
            color: var(--text-gray);
            font-size: 0.95rem;
        }

        .services {
            padding: 100px 0;
            background: var(--darker-bg);
        }

        .services .section-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            text-align: left;
        }

        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 2rem;
        }

        .service-card {
            background: var(--dark-bg);
            padding: 2rem;
            border-radius: 10px;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            border: 1px solid rgba(108, 99, 255, 0.2);
        }

        .service-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 10px 30px rgba(108, 99, 255, 0.3);
        }

        .service-card h4 {
            font-size: 1.5rem;
            margin-bottom: 1rem;
            color: var(--primary-color);
        }

        .service-card p {
            color: var(--text-gray);
            line-height: 1.8;
        }

        .projects {
            padding: 100px 0;
            background: var(--dark-bg);
        }

        .project-filters {
            display: flex;
            justify-content: center;
            gap: 1rem;
            margin-bottom: 3rem;
            flex-wrap: wrap;
        }

        .project-filters input[type="radio"] {
            position: absolute;
            opacity: 0;
        }

        .project-filters label.filter-btn {
            padding: 10px 25px;
            background: transparent;
            border: 2px solid var(--primary-color);
            color: var(--primary-color);
            border-radius: 5px;
            cursor: pointer;
            transition: all 0.3s ease;
            font-size: 1rem;
        }

        .project-filters input[type="radio"]:checked + label.filter-btn {
            background: var(--primary-color);
            color: var(--text-light);
        }

        .project-filters label.filter-btn:hover {
            background: var(--primary-color);
            color: var(--text-light);
        }

        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(320px, 1fr));
            gap: 2rem;
        }

        .project-card {
            background: var(--darker-bg);
            border-radius: 10px;
            overflow: hidden;
            transition: transform 0.3s ease, box-shadow 0.3s ease, opacity 0.3s ease;
        }

        .project-card {
            display: block;
            opacity: 1;
        }

        #filter-all:checked ~ .projects-grid .project-card {
            display: block;
            opacity: 1;
        }

        #filter-personal:checked ~ .projects-grid .project-card {
            display: none;
            opacity: 0;
        }

        #filter-personal:checked ~ .projects-grid .project-card.personal {
            display: block;
            opacity: 1;
        }

        #filter-teranium:checked ~ .projects-grid .project-card {
            display: none;
            opacity: 0;
        }

        #filter-teranium:checked ~ .projects-grid .project-card.teranium {
            display: block;
            opacity: 1;
        }

        #filter-events:checked ~ .projects-grid .project-card {
            display: none;
            opacity: 0;
        }

        #filter-events:checked ~ .projects-grid .project-card.events {
            display: block;
            opacity: 1;
        }

        .project-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 30px rgba(0, 217, 255, 0.2);
        }

        .project-card .image-placeholder {
            height: 200px;
            background: linear-gradient(135deg, var(--primary-color), var(--accent-color));
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.1rem;
        }

        .project-info {
            padding: 1.5rem;
        }

        .project-info h4 {
            font-size: 1.2rem;
            margin-bottom: 0.8rem;
            color: var(--text-light);
        }

        .project-info p {
            color: var(--text-gray);
            font-size: 0.95rem;
        }
        .contact {
            padding: 100px 0;
            background: var(--darker-bg);
        }

        .contact-content {
            display: grid;
            grid-template-columns: 1fr 1.5fr;
            gap: 3rem;
        }

        .contact-info {
            display: flex;
            flex-direction: column;
            gap: 2rem;
        }

        .info-item h4 {
            font-size: 1.3rem;
            margin-bottom: 0.5rem;
            color: var(--primary-color);
        }

        .info-item p {
            color: var(--text-gray);
        }

        .social-links {
            display: flex;
            gap: 1rem;
        }

        .social-link {
            padding: 8px 15px;
            background: var(--primary-color);
            color: var(--text-light);
            text-decoration: none;
            border-radius: 5px;
            transition: all 0.3s ease;
        }

        .social-link:hover,
        .social-link:focus {
            background: var(--accent-color);
            transform: translateY(-2px);
        }


        .contact-form {
            background: var(--dark-bg);
            padding: 2rem;
            border-radius: 10px;
        }

        .form-group {
            margin-bottom: 1.5rem;
        }

        .form-group input,
        .form-group textarea {
            width: 100%;
            padding: 12px;
            background: var(--darker-bg);
            border: 2px solid rgba(108, 99, 255, 0.3);
            border-radius: 5px;
            color: var(--text-light);
            font-size: 1rem;
            transition: border-color 0.3s ease;
        }

        .form-group input::placeholder,
        .form-group textarea::placeholder {
            color: var(--text-gray);
        }

        .form-group input:focus,
        .form-group textarea:focus {
            outline: none;
            border-color: var(--primary-color);
        }

        .form-group textarea {
            resize: vertical;
        }

        .footer {
            background: var(--darker-bg);
            padding: 2rem 0;
            text-align: center;
            border-top: 1px solid rgba(108, 99, 255, 0.2);
        }

        .footer p {
            color: var(--text-gray);
            margin: 0.5rem 0;
        }

        @media (max-width: 768px) {
            .nav-toggle-label {
                display: block;
            }

            .nav-menu {
                position: absolute;
                top: 100%;
                left: 0;
                right: 0;
                background: var(--darker-bg);
                flex-direction: column;
                padding: 1rem;
                gap: 0;
                max-height: 0;
                overflow: hidden;
                transition: max-height 0.3s ease;
            }

            .nav-menu li {
                padding: 0.5rem 0;
                border-bottom: 1px solid rgba(108, 99, 255, 0.2);
            }

            .nav-toggle:checked ~ .nav-menu {
                max-height: 400px;
            }
            
            .hero-name {
                font-size: 2.5rem;
            }
            
            .hero-title {
                font-size: 1.2rem;
            }
            
            .about-content,
            .skills-content,
            .contact-content {
                grid-template-columns: 1fr;
            }
            
            .section-header h2 {
                font-size: 2rem;
            }
            
            .services .section-header {
                flex-direction: column;
                gap: 1rem;
                text-align: center;
            }
            
            .projects-grid {
                grid-template-columns: 1fr;
            }

            .tabs label.tab-btn {
                font-size: 0.9rem;
                padding: 8px 15px;
            }
        }

        @media (max-width: 480px) {
            .hero-name {
                font-size: 2rem;
            }
            
            .section-header h2 {
                font-size: 1.8rem;
            }
            
            .services-grid {
                grid-template-columns: 1fr;
            }

            .project-filters label.filter-btn {
                font-size: 0.9rem;
                padding: 8px 15px;
            }
        }

        a:focus,
        button:focus,
        input:focus,
        textarea:focus,
        label:focus {
            outline: 2px solid var(--primary-color);
            outline-offset: 2px;
        }

        @media print {
            .navbar,
            .project-filters,
            .contact-form {
                display: none;
            }
            
            body {
                background: white;
                color: black;
            }
        }
    
   </style>
</head>
<body>
   
    <nav class="navbar">
        <div class="container">
            <div class="nav-brand">
                <a href="#home">TCM</a>
            </div>
            <input type="checkbox" id="nav-toggle" class="nav-toggle">
            <label for="nav-toggle" class="nav-toggle-label">☰</label>
            <ul class="nav-menu">
                <li><a href="#home">Home</a></li>
                <li><a href="#about">My Story</a></li>
                <li><a href="#skill">Skills & Quals</a></li>
                <li><a href="#service">Services</a></li>
                <li><a href="#project">Projects</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </div>
    </nav>

    <section id="home" class="hero">
        <div class="container">
            <div class="hero-content">
                <p class="hero-greeting">Hello, I am</p>
                <h1 class="hero-name">The Chikeluba Modozie</h1>
                <h2 class="hero-title">Backend Engineer, Process Architect, Growth Catalyst</h2>
                <p class="hero-description">I don't just build websites. I engineer systems that streamline your workflow and make your processes efficient.</p>
                <a href="#project" class="btn btn-primary">See My Work</a>
            </div>
        </div>
    </section>

    <section id="about" class="about">
        <div class="container">
            <div class="section-header">
                <h3>The Journey</h3>
            </div>
            <div class="about-content">
                <div class="about-text">
                    <h3>From Nigerian Breweries to Backend Engineering</h3>
                    <p>Two years ago, I was working at Nigerian Breweries Plc. The job offered stability, but I knew I wanted more—I was eager to challenge myself and grow in a field where I could truly impact lives.</p>
                    
                    <p>I saved up, bought a laptop, and made the difficult decision to leave my job. The transition wasn't smooth. I enrolled in ALX but had to drop out because balancing side hustles to stay afloat made it impossible to meet their standards.</p>
                    
                    <p>But I didn't give up. I joined Genesys Tech Hub, then AltSchool Africa, and now Miva Open University. Today, I have grown from an intern into a dedicated engineer, committed to learning unto mastery and building systems that work.</p>
                    
                    <a href="#skill" class="btn btn-outline">View Qualifications</a>
                </div>
                <div class="about-image">
                    <div class="image-placeholder">
                        <div class="video-placeholder">
                            <span>Intro Video</span>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <section id="skill" class="skills">
        <div class="container">
            <div class="section-header">
                <h2>Skills & Competence</h2>
                <p>My journey has been defined by continuous learning. These are the technical tools I have mastered to engineer robust systems.</p>
            </div>
            
            <div class="skills-content">
                <div class="technical-skills">
                    <h3>Technical Skills</h3>
                    
                    <div class="skill-item">
                        <div class="skill-header">
                            <span>PHP (Backend)</span>
                            <span>90%</span>
                        </div>
                        <div class="skill-bar">
                            <div class="skill-progress" style="width: 90%"></div>
                        </div>
                    </div>

                    <div class="skill-item">
                        <div class="skill-header">
                            <span>Laravel Framework</span>
                            <span>95%</span>
                        </div>
                        <div class="skill-bar">
                            <div class="skill-progress" style="width: 95%"></div>
                        </div>
                    </div>

                    <div class="skill-item">
                        <div class="skill-header">
                            <span>Database Architecture</span>
                            <span>90%</span>
                        </div>
                        <div class="skill-bar">
                            <div class="skill-progress" style="width: 90%"></div>
                        </div>
                    </div>

                    <div class="skill-item">
                        <div class="skill-header">
                            <span>HTML/CSS</span>
                            <span>95%</span>
                        </div>
                        <div class="skill-bar">
                            <div class="skill-progress" style="width: 95%"></div>
                        </div>
                    </div>

                    <div class="skill-item">
                        <div class="skill-header">
                            <span>Bootstrap</span>
                            <span>90%</span>
                        </div>
                        <div class="skill-bar">
                            <div class="skill-progress" style="width: 90%"></div>
                        </div>
                    </div>

                    <div class="skill-item">
                        <div class="skill-header">
                            <span>Javascript</span>
                            <span>95%</span>
                        </div>
                        <div class="skill-bar">
                            <div class="skill-progress" style="width: 95%"></div>
                        </div>
                    </div>

                    <div class="skill-item">
                        <div class="skill-header">
                            <span>Git & Github</span>
                            <span>65%</span>
                        </div>
                        <div class="skill-bar">
                            <div class="skill-progress" style="width: 65%"></div>
                        </div>
                    </div>
                </div>

                <div class="experience-education">
                    <div class="tabs">
                        <input type="radio" name="tabs" id="tab-experience" checked>
                        <label for="tab-experience" class="tab-btn">Experience</label>
                        
                        <input type="radio" name="tabs" id="tab-education">
                        <label for="tab-education" class="tab-btn">Education</label>

                        <div class="tab-content tab-experience-content">
                            <div class="timeline-item">
                                <h4>Founder & Lead</h4>
                                <p class="timeline-date">2024 - Present</p>
                                <p class="timeline-company">TCMLogic & Thryve Trybe</p>
                            </div>

                            <div class="timeline-item">
                                <h4>Chief Technical Officer</h4>
                                <p class="timeline-date">2023 - Present</p>
                                <p class="timeline-company">Auntie Jay's Group</p>
                            </div>

                            <div class="timeline-item">
                                <h4>Fullstack Engineer / Technical Support</h4>
                                <p class="timeline-date">2023 - 2024</p>
                                <p class="timeline-company">Teranium Co.</p>
                            </div>

                            <div class="timeline-item">
                                <h4>HOD Media</h4>
                                <p class="timeline-date">2023 - Present</p>
                                <p class="timeline-company">Church Media Dept.</p>
                            </div>

                            <div class="timeline-item">
                                <h4>Fullstack Engineer (Intern)</h4>
                                <p class="timeline-date">2022 - 2023</p>
                                <p class="timeline-company">Teranium Co.</p>
                            </div>

                            <div class="timeline-item">
                                <h4>Electronic Bottle Inspection(EBI)</h4>
                                <p class="timeline-date">2021</p>
                                <p class="timeline-company">Nigerian Breweries Plc</p>
                            </div>
                        </div>

                        <div class="tab-content tab-education-content">
                            <div class="timeline-item">
                                <h4>B.Sc Software Engineering</h4>
                                <p class="timeline-date">In View</p>
                                <p class="timeline-company">Miva Open University</p>
                            </div>

                            <div class="timeline-item">
                                <h4>Backend Engineering</h4>
                                <p class="timeline-date">Diploma</p>
                                <p class="timeline-company">AltSchool Africa</p>
                            </div>

                            <div class="timeline-item">
                                <h4>Upskill Program</h4>
                                <p class="timeline-date">Certificate</p>
                                <p class="timeline-company">Genesys Tech Hub</p>
                            </div>

                            <div class="timeline-item">
                                <h4>Self-Taught</h4>
                                <p class="timeline-date">Continuous</p>
                                <p class="timeline-company">Udemy & Coursera</p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <section id="service" class="services">
        <div class="container">
            <div class="section-header">
                <h2>My Services</h2>
                <a href="#contact" class="btn btn-primary">Hire Me</a>
            </div>
            
            <div class="services-grid">
                <div class="service-card">
                    <h4>System Engineering</h4>
                    <p>Beyond just building websites, I engineer complete systems. I ensure that your digital platform talks to your physical operations seamlessly.</p>
                </div>

                <div class="service-card">
                    <h4>Workflow Optimization</h4>
                    <p>I analyze your current business process and build software that streamlines your workflow, making your process efficient and scalable.</p>
                </div>

                <div class="service-card">
                    <h4>Backend Development</h4>
                    <p>Using PHP and Laravel, I build secure and robust backends that power your innovative ideas and handle complex data logic.</p>
                </div>

                <div class="service-card">
                    <h4>Technical Training</h4>
                    <p>Sharing knowledge through Thryve Trybe and mentorship. I help others navigate the vast sea of tech resources.</p>
                </div>
            </div>
        </div>
    </section>

    <section id="project" class="projects">
        <div class="container">
            <div class="section-header">
                <h2>Featured Projects</h2>
            </div>

            <div class="project-filters">
                <input type="radio" name="filter" id="filter-all" checked>
                <label for="filter-all" class="filter-btn">All</label>
                
                <input type="radio" name="filter" id="filter-personal">
                <label for="filter-personal" class="filter-btn">Personal</label>
                
                <input type="radio" name="filter" id="filter-teranium">
                <label for="filter-teranium" class="filter-btn">Teranium Co</label>
                
                <input type="radio" name="filter" id="filter-events">
                <label for="filter-events" class="filter-btn">Events</label>
            </div>

            <div class="projects-grid">
                <div class="project-card events">
                    <div class="project-image">
                        <div class="image-placeholder">Fireside Chat</div>
                    </div>
                    <div class="project-info">
                        <h4>Fireside Chat with The Growth Catalyst. Theme: From Sweat to Systems</h4>
                        <p>This isn't a motivational talk—it's a kairos moment captured in time</p>
                    </div>
                </div>

                <div class="project-card events">
                    <div class="project-image">
                        <div class="image-placeholder">Web3 CN 1.0</div>
                    </div>
                    <div class="project-info">
                        <h4>Onboarding With Web3 with CN 1.0</h4>
                        <p>Profile Optimization And How to Narrow down your Niche</p>
                    </div>
                </div>

                <div class="project-card events">
                    <div class="project-image">
                        <div class="image-placeholder">Web3 CN 2.0</div>
                    </div>
                    <div class="project-info">
                        <h4>Onboarding Web3 with CN 2.0</h4>
                        <p>Profile Optimization And How to Narrow down your Niche</p>
                    </div>
                </div>

                <div class="project-card teranium">
                    <div class="project-image">
                        <div class="image-placeholder">Hospital Portal</div>
                    </div>
                    <div class="project-info">
                        <h4>Hospital Website and Management Portal</h4>
                        <p>Christ Our Foundation Hospital</p>
                    </div>
                </div>

                <div class="project-card teranium">
                    <div class="project-image">
                        <div class="image-placeholder">Church Portal</div>
                    </div>
                    <div class="project-info">
                        <h4>Church Website and Administration Portal</h4>
                        <p>The Father's Delight International Ministries Global</p>
                    </div>
                </div>

                <div class="project-card teranium">
                    <div class="project-image">
                        <div class="image-placeholder">News CMS</div>
                    </div>
                    <div class="project-info">
                        <h4>News Website and Content Management System</h4>
                        <p>GlintNews</p>
                    </div>
                </div>

                <div class="project-card personal">
                    <div class="project-image">
                        <div class="image-placeholder">TCMLogic</div>
                    </div>
                    <div class="project-info">
                        <h4>Company Website and management system</h4>
                        <p>Company Website and management system for TCMLogic</p>
                    </div>
                </div>

                <div class="project-card teranium">
                    <div class="project-image">
                        <div class="image-placeholder">Ogbuoji System</div>
                    </div>
                    <div class="project-info">
                        <h4>Ogbuoji Management System</h4>
                        <p>A management system to help streamline their workflow and 10x productivity</p>
                    </div>
                </div>

                <div class="project-card personal">
                    <div class="project-image">
                        <div class="image-placeholder">Wedding RSVP</div>
                    </div>
                    <div class="project-info">
                        <h4>Wedding Website & Guest tracking system (RSVP)</h4>
                        <p>#chiOma</p>
                    </div>
                </div>

                <div class="project-card personal">
                    <div class="project-image">
                        <div class="image-placeholder">Wedding Site</div>
                    </div>
                    <div class="project-info">
                        <h4>Wedding Website</h4>
                        <p>#TheMafiaLoveStory</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <section id="contact" class="contact">
        <div class="container">
            <div class="section-header">
                <h2>Let's Connect</h2>
            </div>

            <div class="contact-content">
                <div class="contact-info">
                    <div class="info-item">
                        <h4>My Office:</h4>
                        <p>Enugu, Nigeria</p>
                    </div>

                    <div class="info-item">
                        <h4>Email:</h4>
                        <p>thechikelubamodozie@gmail.com</p>
                    </div>

                    <div class="info-item">
                        <h4>Follow me:</h4>
                        <div class="social-links">
                            <a href="#" class="social-link">LinkedIn</a>
                            <a href="#" class="social-link">Twitter</a>
                            <a href="#" class="social-link">GitHub</a>
                        </div>
                    </div>
                </div>

                <div class="contact-form">
                    <form action="#contact" method="get">
                        <div class="form-group">
                            <input type="text" name="name" placeholder="Your Name" required>
                        </div>
                        <div class="form-group">
                            <input type="email" name="email" placeholder="Your Email" required>
                        </div>
                        <div class="form-group">
                            <input type="text" name="subject" placeholder="Subject" required>
                        </div>
                        <div class="form-group">
                            <textarea name="message" placeholder="Message" rows="5" required></textarea>
                        </div>
                        <button type="submit" class="btn btn-primary">Send Message</button>
                    </form>
                </div>
            </div>
        </div>
    </section>

    <footer class="footer">
        <div class="container">
            <p>&copy; The Chikeluba Modozie, All Right Reserved.</p>
            <p>Powered by TCMLogic</p>
        </div>
    </footer>
</body>
</html>
