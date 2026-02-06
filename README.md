<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Data Analytics Portfolio - Showcasing data analysis projects and skills">
    <title>Your Name | Data Analytics Portfolio</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        :root {
            --primary-color: #2563eb;
            --secondary-color: #1e40af;
            --text-dark: #1f2937;
            --text-light: #6b7280;
            --bg-light: #f9fafb;
            --bg-white: #ffffff;
            --border-color: #e5e7eb;
            --accent-color: #10b981;
        }

        body {
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
            line-height: 1.6;
            color: var(--text-dark);
            background-color: var(--bg-white);
        }

        /* Navigation */
        nav {
            background: var(--bg-white);
            padding: 1rem 0;
            position: sticky;
            top: 0;
            box-shadow: 0 2px 4px rgba(0,0,0,0.1);
            z-index: 1000;
        }

        nav .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 2rem;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        nav .logo {
            font-size: 1.5rem;
            font-weight: 700;
            color: var(--primary-color);
        }

        nav ul {
            display: flex;
            list-style: none;
            gap: 2rem;
        }

        nav a {
            text-decoration: none;
            color: var(--text-dark);
            font-weight: 500;
            transition: color 0.3s;
        }

        nav a:hover {
            color: var(--primary-color);
        }

        /* Hero Section */
        .hero {
            background: linear-gradient(135deg, var(--primary-color) 0%, var(--secondary-color) 100%);
            color: white;
            padding: 6rem 2rem;
            text-align: center;
        }

        .hero h1 {
            font-size: 3rem;
            margin-bottom: 1rem;
            animation: fadeInUp 0.8s ease;
        }

        .hero p {
            font-size: 1.25rem;
            margin-bottom: 2rem;
            opacity: 0.9;
            animation: fadeInUp 0.8s ease 0.2s backwards;
        }

        .hero .cta-buttons {
            display: flex;
            gap: 1rem;
            justify-content: center;
            animation: fadeInUp 0.8s ease 0.4s backwards;
        }

        .btn {
            padding: 0.75rem 2rem;
            border-radius: 0.5rem;
            text-decoration: none;
            font-weight: 600;
            transition: all 0.3s;
            display: inline-block;
        }

        .btn-primary {
            background: white;
            color: var(--primary-color);
        }

        .btn-primary:hover {
            transform: translateY(-2px);
            box-shadow: 0 4px 12px rgba(0,0,0,0.2);
        }

        .btn-secondary {
            background: transparent;
            color: white;
            border: 2px solid white;
        }

        .btn-secondary:hover {
            background: white;
            color: var(--primary-color);
        }

        /* Container */
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 2rem;
        }

        /* Section */
        section {
            padding: 5rem 2rem;
        }

        .section-title {
            text-align: center;
            font-size: 2.5rem;
            margin-bottom: 3rem;
            color: var(--text-dark);
        }

        /* About Section */
        .about-content {
            max-width: 800px;
            margin: 0 auto;
            text-align: center;
        }

        .about-content p {
            font-size: 1.125rem;
            color: var(--text-light);
            margin-bottom: 2rem;
        }

        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
            margin-top: 3rem;
        }

        .skill-card {
            background: var(--bg-light);
            padding: 2rem;
            border-radius: 0.5rem;
            text-align: center;
            transition: transform 0.3s;
        }

        .skill-card:hover {
            transform: translateY(-5px);
        }

        .skill-card h3 {
            color: var(--primary-color);
            margin-bottom: 1rem;
        }

        .skill-card ul {
            list-style: none;
            color: var(--text-light);
        }

        .skill-card li {
            padding: 0.25rem 0;
        }

        /* Projects Section */
        #projects {
            background: var(--bg-light);
        }

        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
            gap: 2rem;
        }

        .project-card {
            background: white;
            border-radius: 0.5rem;
            overflow: hidden;
            box-shadow: 0 2px 8px rgba(0,0,0,0.1);
            transition: all 0.3s;
        }

        .project-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 4px 16px rgba(0,0,0,0.15);
        }

        .project-image {
            width: 100%;
            height: 200px;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 3rem;
        }

        .project-content {
            padding: 1.5rem;
        }

        .project-content h3 {
            margin-bottom: 0.5rem;
            color: var(--text-dark);
        }

        .project-tags {
            display: flex;
            flex-wrap: wrap;
            gap: 0.5rem;
            margin: 1rem 0;
        }

        .tag {
            background: var(--bg-light);
            padding: 0.25rem 0.75rem;
            border-radius: 1rem;
            font-size: 0.875rem;
            color: var(--text-light);
        }

        .project-links {
            display: flex;
            gap: 1rem;
            margin-top: 1rem;
        }

        .project-links a {
            color: var(--primary-color);
            text-decoration: none;
            font-weight: 600;
            font-size: 0.875rem;
        }

        .project-links a:hover {
            text-decoration: underline;
        }

        /* Contact Section */
        .contact-content {
            max-width: 600px;
            margin: 0 auto;
            text-align: center;
        }

        .contact-links {
            display: flex;
            justify-content: center;
            gap: 2rem;
            margin-top: 2rem;
            flex-wrap: wrap;
        }

        .contact-link {
            display: flex;
            align-items: center;
            gap: 0.5rem;
            color: var(--text-dark);
            text-decoration: none;
            font-weight: 500;
            transition: color 0.3s;
        }

        .contact-link:hover {
            color: var(--primary-color);
        }

        /* Footer */
        footer {
            background: var(--text-dark);
            color: white;
            text-align: center;
            padding: 2rem;
        }

        footer p {
            opacity: 0.8;
        }

        /* Animations */
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

        /* Responsive */
        @media (max-width: 768px) {
            .hero h1 {
                font-size: 2rem;
            }

            .hero p {
                font-size: 1rem;
            }

            nav ul {
                gap: 1rem;
            }

            .cta-buttons {
                flex-direction: column;
            }

            .projects-grid {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <!-- Navigation -->
    <nav>
        <div class="container">
            <div class="logo">YourName</div>
            <ul>
                <li><a href="#about">About</a></li>
                <li><a href="#projects">Projects</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </div>
    </nav>

    <!-- Hero Section -->
    <section class="hero">
        <h1>Data Analytics Portfolio</h1>
        <p>Transforming Data into Actionable Insights</p>
        <div class="cta-buttons">
            <a href="#projects" class="btn btn-primary">View Projects</a>
            <a href="#contact" class="btn btn-secondary">Get in Touch</a>
        </div>
    </section>

    <!-- About Section -->
    <section id="about">
        <div class="container">
            <h2 class="section-title">About Me</h2>
            <div class="about-content">
                <p>
                    I'm a data analyst passionate about uncovering insights from complex datasets. 
                    With expertise in statistical analysis, data visualization, and machine learning, 
                    I help organizations make data-driven decisions that drive growth and efficiency.
                </p>
                
                <div class="skills-grid">
                    <div class="skill-card">
                        <h3>📊 Data Analysis</h3>
                        <ul>
                            <li>Python (Pandas, NumPy)</li>
                            <li>R (dplyr, ggplot2)</li>
                            <li>Statistical Modeling</li>
                            <li>A/B Testing</li>
                        </ul>
                    </div>
                    <div class="skill-card">
                        <h3>📈 Visualization</h3>
                        <ul>
                            <li>Tableau</li>
                            <li>Power BI</li>
                            <li>Matplotlib & Seaborn</li>
                            <li>Google Data Studio</li>
                        </ul>
                    </div>
                    <div class="skill-card">
                        <h3>🗄️ Data Management</h3>
                        <ul>
                            <li>SQL (PostgreSQL, MySQL)</li>
                            <li>Excel (Advanced)</li>
                            <li>ETL Processes</li>
                            <li>Database Design</li>
                        </ul>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Projects Section -->
    <section id="projects">
        <div class="container">
            <h2 class="section-title">Featured Projects</h2>
            <div class="projects-grid">
                <!-- Project 1 -->
                <div class="project-card">
                    <div class="project-image">📊</div>
                    <div class="project-content">
                        <h3>Customer Segmentation Analysis</h3>
                        <p>Performed RFM analysis and K-means clustering to identify 5 distinct customer segments, enabling targeted marketing strategies.</p>
                        <div class="project-tags">
                            <span class="tag">Python</span>
                            <span class="tag">Scikit-learn</span>
                            <span class="tag">Clustering</span>
                        </div>
                        <div class="project-links">
                            <a href="#">View Project →</a>
                            <a href="#">GitHub →</a>
                        </div>
                    </div>
                </div>

                <!-- Project 2 -->
                <div class="project-card">
                    <div class="project-image">📈</div>
                    <div class="project-content">
                        <h3>Sales Dashboard & Forecasting</h3>
                        <p>Built an interactive Power BI dashboard with time-series forecasting, improving forecast accuracy by 15%.</p>
                        <div class="project-tags">
                            <span class="tag">Power BI</span>
                            <span class="tag">DAX</span>
                            <span class="tag">SQL</span>
                        </div>
                        <div class="project-links">
                            <a href="#">View Dashboard →</a>
                            <a href="#">GitHub →</a>
                        </div>
                    </div>
                </div>

                <!-- Project 3 -->
                <div class="project-card">
                    <div class="project-image">🔍</div>
                    <div class="project-content">
                        <h3>E-commerce Data Analysis</h3>
                        <p>Conducted comprehensive EDA on 500K+ transactions, uncovering seasonal patterns and customer behavior trends.</p>
                        <div class="project-tags">
                            <span class="tag">Python</span>
                            <span class="tag">Pandas</span>
                            <span class="tag">Plotly</span>
                        </div>
                        <div class="project-links">
                            <a href="#">View Notebook →</a>
                            <a href="#">GitHub →</a>
                        </div>
                    </div>
                </div>

                <!-- Project 4 -->
                <div class="project-card">
                    <div class="project-image">🎯</div>
                    <div class="project-content">
                        <h3>A/B Testing Analysis</h3>
                        <p>Designed and analyzed A/B tests for website optimization, resulting in a 12% increase in conversion rate.</p>
                        <div class="project-tags">
                            <span class="tag">Statistics</span>
                            <span class="tag">Python</span>
                            <span class="tag">Hypothesis Testing</span>
                        </div>
                        <div class="project-links">
                            <a href="#">View Report →</a>
                            <a href="#">GitHub →</a>
                        </div>
                    </div>
                </div>

                <!-- Project 5 -->
                <div class="project-card">
                    <div class="project-image">💾</div>
                    <div class="project-content">
                        <h3>SQL Database Analysis</h3>
                        <p>Wrote complex SQL queries analyzing employee performance and operational efficiency across departments.</p>
                        <div class="project-tags">
                            <span class="tag">PostgreSQL</span>
                            <span class="tag">SQL</span>
                            <span class="tag">Data Mining</span>
                        </div>
                        <div class="project-links">
                            <a href="#">View Queries →</a>
                            <a href="#">GitHub →</a>
                        </div>
                    </div>
                </div>

                <!-- Project 6 -->
                <div class="project-card">
                    <div class="project-image">🤖</div>
                    <div class="project-content">
                        <h3>Predictive Analytics Model</h3>
                        <p>Developed machine learning models to predict customer churn with 85% accuracy, informing retention strategies.</p>
                        <div class="project-tags">
                            <span class="tag">Machine Learning</span>
                            <span class="tag">Python</span>
                            <span class="tag">Scikit-learn</span>
                        </div>
                        <div class="project-links">
                            <a href="#">View Project →</a>
                            <a href="#">GitHub →</a>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact">
        <div class="container">
            <h2 class="section-title">Get in Touch</h2>
            <div class="contact-content">
                <p>I'm always interested in new opportunities and collaborations. Feel free to reach out!</p>
                <div class="contact-links">
                    <a href="mailto:your.email@example.com" class="contact-link">
                        📧 Email
                    </a>
                    <a href="https://linkedin.com/in/yourprofile" class="contact-link" target="_blank">
                        💼 LinkedIn
                    </a>
                    <a href="https://github.com/yourusername" class="contact-link" target="_blank">
                        💻 GitHub
                    </a>
                    <a href="https://twitter.com/yourhandle" class="contact-link" target="_blank">
                        🐦 Twitter
                    </a>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <p>&copy; 2026 Your Name. All rights reserved.</p>
        </div>
    </footer>

    <script>
        // Smooth scrolling for navigation links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                const target = document.querySelector(this.getAttribute('href'));
                if (target) {
                    target.scrollIntoView({
                        behavior: 'smooth',
                        block: 'start'
                    });
                }
            });
        });

        // Add animation on scroll
        const observerOptions = {
            threshold: 0.1,
            rootMargin: '0px 0px -100px 0px'
        };

        const observer = new IntersectionObserver(function(entries) {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.style.animation = 'fadeInUp 0.8s ease forwards';
                }
            });
        }, observerOptions);

        document.querySelectorAll('.project-card, .skill-card').forEach(el => {
            observer.observe(el);
        });
    </script>
</body>
</html>
