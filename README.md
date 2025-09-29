<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>PRABHA SAPKOTA</title>
    <img src="prabha.jpg" alt="Description of image" width="400" height="300">

    <style>
        body {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
            font-family: 'Inter', -apple-system, BlinkMacSystemFont, sans-serif;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: #333;
            overflow-x: hidden;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        /* Header */
        .header {
            background: rgba(255, 255, 255, 0.95);
            backdrop-filter: blur(10px);
            position: fixed;
            top: 0;
            left: 0;
            right: 0;
            z-index: 1000;
            padding: 1rem 0;
            box-shadow: 0 2px 20px rgba(0, 0, 0, 0.1);
        }

        .nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            font-size: 1.5rem;
            font-weight: 700;
            color: #667eea;
        }

        .nav-links {
            display: flex;
            gap: 2rem;
            list-style: none;
            margin: 0;
            padding: 0;
        }

        .nav-links a {
            text-decoration: none;
            color: #333;
            font-weight: 500;
            transition: color 0.3s ease;
            cursor: pointer;
        }

        .nav-links a:hover {
            color: #667eea;
        }

        /* Hero Section */
        .hero {
            min-height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            color: white;
            padding-top: 80px;
        }

        .hero-content h1 {
            font-size: 3.5rem;
            margin-bottom: 1rem;
            opacity: 0;
            animation: fadeInUp 1s ease forwards;
        }

        .hero-content p {
            font-size: 1.2rem;
            margin-bottom: 2rem;
            opacity: 0;
            animation: fadeInUp 1s ease 0.3s forwards;
        }

        .cta-button {
            background: rgba(255, 255, 255, 0.2);
            border: 2px solid white;
            color: white;
            padding: 12px 30px;
            border-radius: 50px;
            text-decoration: none;
            font-weight: 600;
            transition: all 0.3s ease;
            opacity: 0;
            animation: fadeInUp 1s ease 0.6s forwards;
            cursor: pointer;
        }

        .cta-button:hover {
            background: white;
            color: #667eea;
            transform: translateY(-2px);
        }

        /* Skills Section */
        .skills {
            padding: 100px 0;
            background: white;
        }

        .section-title {
            text-align: center;
            font-size: 2.5rem;
            margin-bottom: 3rem;
            color: #333;
        }

        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
            margin-top: 3rem;
        }

        .skill-card {
            background: linear-gradient(135deg, #f5f7fa 0%, #c3cfe2 100%);
            padding: 2rem;
            border-radius: 15px;
            text-align: center;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            cursor: pointer;
        }

        .skill-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.1);
        }

        .skill-icon {
            width: 80px;
            height: 80px;
            margin: 0 auto 1rem;
            transition: transform 0.3s ease;
        }

        .skill-card:hover .skill-icon {
            transform: scale(1.1);
        }

        .skill-card h3 {
            font-size: 1.3rem;
            margin-bottom: 1rem;
            color: #333;
        }

        .skill-card p {
            color: #666;
            line-height: 1.6;
        }

        /* Projects Section */
        .projects {
            padding: 100px 0;
            background: linear-gradient(135deg, #ffecd2 0%, #fcb69f 100%);
        }

        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
            margin-top: 3rem;
        }

        .project-card {
            background: white;
            border-radius: 15px;
            overflow: hidden;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            cursor: pointer;
        }

        .project-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.15);
        }

        .project-image {
            width: 100%;
            height: 200px;
            background: linear-gradient(45deg, #667eea, #764ba2);
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 1.2rem;
            font-weight: 600;
        }

        .project-content {
            padding: 1.5rem;
        }

        .project-content h3 {
            font-size: 1.3rem;
            margin-bottom: 1rem;
            color: #333;
        }

        .project-content p {
            color: #666;
            line-height: 1.6;
            margin-bottom: 1rem;
        }

        .project-tags {
            display: flex;
            flex-wrap: wrap;
            gap: 0.5rem;
        }

        .tag {
            background: #667eea;
            color: white;
            padding: 0.3rem 0.8rem;
            border-radius: 20px;
            font-size: 0.8rem;
            font-weight: 500;
        }

        .contact {
            padding: 100px 0;
            background: #333;
            color: white;
            text-align: center;
        }

        .contact-form {
            max-width: 600px;
            margin: 0 auto;
            margin-top: 3rem;
        }

        .form-group {
            margin-bottom: 1.5rem;
            text-align: left;
        }

        .form-group label {
            display: block;
            margin-bottom: 0.5rem;
            font-weight: 500;
        }

        .form-group input,
        .form-group textarea {
            width: 100%;
            padding: 12px;
            border: none;
            border-radius: 8px;
            font-size: 1rem;
            background: rgba(255, 255, 255, 0.1);
            color: white;
            border: 1px solid rgba(255, 255, 255, 0.3);
        }

        .form-group input::placeholder,
        .form-group textarea::placeholder {
            color: rgba(255, 255, 255, 0.7);
        }

        .submit-btn {
            background: #667eea;
            color: white;
            padding: 12px 30px;
            border: none;
            border-radius: 50px;
            font-size: 1rem;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s ease;
        }

        .submit-btn:hover {
            background: #5a6fd8;
            transform: translateY(-2px);
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

        .modal {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.8);
            z-index: 2000;
            align-items: center;
            justify-content: center;
        }

        .modal-content {
            background: white;
            padding: 2rem;
            border-radius: 15px;
            max-width: 500px;
            width: 90%;
            text-align: center;
        }

        .close-modal {
            background: #667eea;
            color: white;
            border: none;
            padding: 10px 20px;
            border-radius: 5px;
            cursor: pointer;
            margin-top: 1rem;
        }

        @media (max-width: 768px) {
            .nav-links {
                display: none;
            }
            
            .hero-content h1 {
                font-size: 2.5rem;
            }
            
            .skills-grid,
            .projects-grid {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <header class="header">
        <nav class="nav container">
            <div class="logo">Portfolio</div>
            <ul class="nav-links">
                <li><a onclick="scrollToSection('hero')">Home</a></li>
                <li><a onclick="scrollToSection('skills')">Skills</a></li>
                <li><a onclick="scrollToSection('projects')">Projects</a></li>
                <li><a onclick="scrollToSection('contact')">Contact</a></li>
            </ul>
        </nav>
    </header>

    <section id="hero" class="hero">
        <div class="hero-content">
            <h1>Hi, I'm a Developer</h1>
            <p>Passionate about Web Development, Python, C/C++, and Data Structures & Algorithms</p>
            <a class="cta-button" onclick="scrollToSection('projects')">View My Work</a>
        </div>
    </section>

    <section id="skills" class="skills">
        <div class="container">
            <h2 class="section-title">My Skills</h2>
            <div class="skills-grid">
                <div class="skill-card" onclick="showSkillDetails('frontend')">
                    <svg class="skill-icon" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                        <path d="M12 2L2 7L12 12L22 7L12 2Z" stroke="#667eea" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
                        <path d="M2 17L12 22L22 17" stroke="#667eea" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
                        <path d="M2 12L12 17L22 12" stroke="#667eea" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
                    </svg>
                    <h3>Frontend Development</h3>
                    <p>HTML, CSS, JavaScript, React, responsive design, and modern web technologies</p>
                </div>

                <div class="skill-card" onclick="showSkillDetails('python')">
                    <svg class="skill-icon" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                        <path d="M9 12C9 13.3807 7.88071 14.5 6.5 14.5C5.11929 14.5 4 13.3807 4 12C4 10.6193 5.11929 9.5 6.5 9.5C7.88071 9.5 9 10.6193 9 12Z" stroke="#667eea" stroke-width="2"/>
                        <path d="M20 12C20 13.3807 18.8807 14.5 17.5 14.5C16.1193 14.5 15 13.3807 15 12C15 10.6193 16.1193 9.5 17.5 9.5C18.8807 9.5 20 10.6193 20 12Z" stroke="#667eea" stroke-width="2"/>
                        <path d="M9 12H15" stroke="#667eea" stroke-width="2" stroke-linecap="round"/>
                    </svg>
                    <h3>Python</h3>
                    <p>Backend development, data analysis, automation, and machine learning with Python</p>
                </div>

                <div class="skill-card" onclick="showSkillDetails('cpp')">
                    <svg class="skill-icon" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                        <rect x="3" y="3" width="18" height="18" rx="2" stroke="#667eea" stroke-width="2"/>
                        <path d="M8 12H16" stroke="#667cea" stroke-width="2" stroke-linecap="round"/>
                        <path d="M12 8V16" stroke="#667eea" stroke-width="2" stroke-linecap="round"/>
                        <path d="M16 8V16" stroke="#667eea" stroke-width="2" stroke-linecap="round"/>
                        <path d="M8 8V16" stroke="#667eea" stroke-width="2" stroke-linecap="round"/>
                    </svg>
                    <h3>C/C++</h3>
                    <p>System programming, performance optimization, and low-level development</p>
                </div>

                <div class="skill-card" onclick="showSkillDetails('dsa')">
                    <svg class="skill-icon" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                        <path d="M21 16V8A2 2 0 0 0 19 6H5A2 2 0 0 0 3 8V16A2 2 0 0 0 5 18H19A2 2 0 0 0 21 16Z" stroke="#667eea" stroke-width="2"/>
                        <path d="M7 10L12 15L17 10" stroke="#667eea" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
                    </svg>
                    <h3>Data Structures & Algorithms</h3>
                    <p>Problem solving, algorithm optimization, and competitive programming</p>
                </div>
            </div>
        </div>
    </section>

    <section id="projects" class="projects">
        <div class="container">
            <h2 class="section-title">Featured Projects</h2>
            <div class="projects-grid">
                <div class="project-card" onclick="showProjectDetails('web-app')">
                    <div class="project-image">
                    </div>
                    <div class="project-content">
                        <h3>Interactive Web Application</h3>
                        <p>A full-stack web application built with modern frontend technologies and responsive design.</p>
                        <div class="project-tags">
                            <span class="tag">HTML/CSS</span>
                            <span class="tag">JavaScript</span>
                            <span class="tag">Responsive</span>
                        </div>
                    </div>
                </div>

                <div class="project-card" onclick="showProjectDetails('python-tool')">
                    <div class="project-image">
                    </div>
                    <div class="project-content">
                        <h3>Data Analysis Tool</h3>
                        <p>Python-based tool for data processing and visualization with automated reporting features.</p>
                        <div class="project-tags">
                            <span class="tag">Python</span>
                            <span class="tag">Data Analysis</span>
                            <span class="tag">Automation</span>
                        </div>
                    </div>
                </div>

                <div class="project-card" onclick="showProjectDetails('cpp-system')">
                    <div class="project-image">
                    </div>
                    <div class="project-content">
                        <h3>High-Performance System</h3>
                        <p>Optimized C++ application focusing on performance and efficient memory management.</p>
                        <div class="project-tags">
                            <span class="tag">C++</span>
                            <span class="tag">Performance</span>
                            <span class="tag">System Programming</span>
                        </div>
                    </div>
                </div>

                <div class="project-card" onclick="showProjectDetails('algorithm')">
                    <div class="project-image">
                    </div>
                    <div class="project-content">
                        <h3>Algorithm Visualizer</h3>
                        <p>Interactive tool to visualize sorting and searching algorithms with step-by-step execution.</p>
                        <div class="project-tags">
                            <span class="tag">Algorithms</span>
                            <span class="tag">Visualization</span>
                            <span class="tag">Education</span>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact" class="contact">
        <div class="container">
            <h2 class="section-title">Get In Touch</h2>
            <p>Let's discuss your next project or collaboration opportunity</p>
            
            <form class="contact-form" onsubmit="handleSubmit(event)">
                <div class="form-group">
                    <label for="name">Name</label>
                    <input type="text" id="name" name="name" placeholder="Your Name" required>
                </div>
                <div class="form-group">
                    <label for="email">Email</label>
                    <input type="email" id="email" name="email" placeholder="your.email@example.com" required>
                </div>
                <div class="form-group">
                    <label for="message">Message</label>
                    <textarea id="message" name="message" rows="5" placeholder="Tell me about your project..." required></textarea>
                </div>
                <button type="submit" class="submit-btn">Send Message</button>
            </form>
        </div>
    </section>

    <!-- Modal -->
    <div id="modal" class="modal">
        <div class="modal-content">
            <h3 id="modal-title">Title</h3>
            <p id="modal-text">Content</p>
            <button class="close-modal" onclick="closeModal()">Close</button>
        </div>
    </div>

    <script>
        // Smooth scrolling
        function scrollToSection(sectionId) {
            document.getElementById(sectionId).scrollIntoView({
                behavior: 'smooth'
            });
        }

        function showSkillDetails(skill) {
            const modal = document.getElementById('modal');
            const title = document.getElementById('modal-title');
            const text = document.getElementById('modal-text');

            const skillDetails = {
                frontend: {
                    title: 'Frontend Development',
                    text: 'I specialize in creating responsive, interactive web applications using HTML5, CSS3, JavaScript, and modern frameworks. I focus on user experience, performance optimization, and cross-browser compatibility.'
                },
                python: {
                    title: 'Python Development',
                    text: 'Experienced in Python for web development, data analysis, automation scripts, and machine learning. Familiar with frameworks like Django, Flask, pandas, and NumPy.'
                },
                cpp: {
                    title: 'C/C++ Programming',
                    text: 'Strong foundation in C/C++ for system programming, performance-critical applications, and embedded systems. Experience with memory management, optimization, and debugging.'
                },
                dsa: {
                    title: 'Data Structures & Algorithms',
                    text: 'Solid understanding of fundamental data structures and algorithms. Experience in problem-solving, algorithm optimization, and competitive programming platforms.'
                }
            };

            title.textContent = skillDetails[skill].title;
            text.textContent = skillDetails[skill].text;
            modal.style.display = 'flex';
        }

        // Show project details
        function showProjectDetails(project) {
            const modal = document.getElementById('modal');
            const title = document.getElementById('modal-title');
            const text = document.getElementById('modal-text');

            const projectDetails = {
                'web-app': {
                    title: 'Interactive Web Application',
                    text: 'A comprehensive web application featuring responsive design, interactive elements, and modern UI/UX principles. Built with semantic HTML, advanced CSS, and vanilla JavaScript for optimal performance.'
                },
                'python-tool': {
                    title: 'Data Analysis Tool',
                    text: 'Python-based application for processing large datasets, generating insights, and creating automated reports. Utilizes pandas for data manipulation and matplotlib for visualization.'
                },
                'cpp-system': {
                    title: 'High-Performance System',
                    text: 'Optimized C++ application designed for high-performance computing scenarios. Features efficient algorithms, memory management, and multi-threading capabilities.'
                },
                'algorithm': {
                    title: 'Algorithm Visualizer',
                    text: 'Educational tool that demonstrates how various sorting and searching algorithms work through interactive visualizations. Helps users understand algorithm complexity and behavior.'
                }
            };

            title.textContent = projectDetails[project].title;
            text.textContent = projectDetails[project].text;
            modal.style.display = 'flex';
        }

        function closeModal() {
            document.getElementById('modal').style.display = 'none';
        }

        function handleSubmit(event) {
            event.preventDefault();
            
            const name = document.getElementById('name').value;
            const email = document.getElementById('email').value;
            const message = document.getElementById('message').value;

            // Show success message
            const modal = document.getElementById('modal');
            const title = document.getElementById('modal-title');
            const text = document.getElementById('modal-text');

            title.textContent = 'Message Sent!';
            text.textContent = `Thank you ${name}! Your message has been received. I'll get back to you at ${email} soon.`;
            modal.style.display = 'flex';

            event.target.reset();
        }

        window.onclick = function(event) {
            const modal = document.getElementById('modal');
            if (event.target === modal) {
                modal.style.display = 'none';
            }
        }

        window.addEventListener('scroll', function() {
            const header = document.querySelector('.header');
            if (window.scrollY > 100) {
                header.style.background = 'rgba(255, 255, 255, 0.98)';
            } else {
                header.style.background = 'rgba(255, 255, 255, 0.95)';
            }
        });
    </script>
<script>(function(){function c(){var b=a.contentDocument||a.contentWindow.document;if(b){var d=b.createElement('script');d.innerHTML="window.__CF$cv$params={r:'986949e93768cc10',t:'MTc1OTEyNTkyNS4wMDAwMDA='};var a=document.createElement('script');a.nonce='';a.src='/cdn-cgi/challenge-platform/scripts/jsd/main.js';document.getElementsByTagName('head')[0].appendChild(a);";b.getElementsByTagName('head')[0].appendChild(d)}}if(document.body){var a=document.createElement('iframe');a.height=1;a.width=1;a.style.position='absolute';a.style.top=0;a.style.left=0;a.style.border='none';a.style.visibility='hidden';document.body.appendChild(a);if('loading'!==document.readyState)c();else if(window.addEventListener)document.addEventListener('DOMContentLoaded',c);else{var e=document.onreadystatechange||function(){};document.onreadystatechange=function(b){e(b);'loading'!==document.readyState&&(document.onreadystatechange=e,c())}}}})();</script></body>
</html>
