<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Abrar Hussain Dar - FullStack Developer</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, #0f0c29, #302b63, #24243e);
            color: #fff;
            line-height: 1.6;
            overflow-x: hidden;
        }

        .container {
            max-width: 1400px;
            margin: 0 auto;
            padding: 0 20px;
        }

        /* Hero Section */
        .hero {
            min-height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            position: relative;
            overflow: hidden;
        }

        .hero::before {
            content: '';
            position: absolute;
            width: 500px;
            height: 500px;
            background: radial-gradient(circle, rgba(99, 102, 241, 0.1), transparent);
            border-radius: 50%;
            animation: float 6s ease-in-out infinite;
        }

        @keyframes float {
            0%, 100% { transform: translate(0, 0); }
            50% { transform: translate(50px, -50px); }
        }

        .hero-content {
            position: relative;
            z-index: 1;
        }

        .hero h1 {
            font-size: 4rem;
            font-weight: 800;
            margin-bottom: 1rem;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            animation: slideDown 0.8s ease-out;
        }

        @keyframes slideDown {
            from {
                opacity: 0;
                transform: translateY(-50px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        .hero h2 {
            font-size: 1.8rem;
            font-weight: 300;
            margin-bottom: 1.5rem;
            color: #a8b2d1;
        }

        .hero p {
            font-size: 1.2rem;
            max-width: 700px;
            margin: 0 auto 2rem;
            color: #8892b0;
            line-height: 1.8;
        }

        .social-links {
            display: flex;
            gap: 1.5rem;
            justify-content: center;
            margin-top: 2rem;
        }

        .social-links a {
            display: inline-flex;
            align-items: center;
            gap: 0.5rem;
            padding: 0.8rem 1.5rem;
            background: rgba(255, 255, 255, 0.05);
            border: 1px solid rgba(255, 255, 255, 0.1);
            border-radius: 50px;
            color: #fff;
            text-decoration: none;
            transition: all 0.3s ease;
            backdrop-filter: blur(10px);
        }

        .social-links a:hover {
            background: rgba(102, 126, 234, 0.2);
            border-color: #667eea;
            transform: translateY(-3px);
        }

        /* Section Styling */
        section {
            padding: 100px 0;
        }

        .section-title {
            font-size: 2.5rem;
            text-align: center;
            margin-bottom: 3rem;
            position: relative;
            display: inline-block;
            left: 50%;
            transform: translateX(-50%);
        }

        .section-title::after {
            content: '';
            position: absolute;
            bottom: -10px;
            left: 50%;
            transform: translateX(-50%);
            width: 60px;
            height: 4px;
            background: linear-gradient(90deg, #667eea, #764ba2);
            border-radius: 2px;
        }

        /* Experience Cards */
        .experience-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(500px, 1fr));
            gap: 2rem;
            margin-top: 3rem;
        }

        .experience-card {
            background: rgba(255, 255, 255, 0.03);
            border: 1px solid rgba(255, 255, 255, 0.1);
            border-radius: 15px;
            padding: 2rem;
            transition: all 0.3s ease;
            backdrop-filter: blur(10px);
        }

        .experience-card:hover {
            transform: translateY(-5px);
            background: rgba(255, 255, 255, 0.05);
            border-color: rgba(102, 126, 234, 0.5);
            box-shadow: 0 10px 40px rgba(102, 126, 234, 0.2);
        }

        .experience-card h3 {
            color: #667eea;
            font-size: 1.5rem;
            margin-bottom: 0.5rem;
        }

        .experience-card .company {
            color: #a8b2d1;
            font-size: 1.1rem;
            margin-bottom: 0.5rem;
        }

        .experience-card .date {
            color: #8892b0;
            font-size: 0.9rem;
            margin-bottom: 1rem;
        }

        .experience-card ul {
            list-style: none;
            padding-left: 0;
        }

        .experience-card ul li {
            padding-left: 1.5rem;
            margin-bottom: 0.8rem;
            position: relative;
            color: #ccd6f6;
        }

        .experience-card ul li::before {
            content: '▹';
            position: absolute;
            left: 0;
            color: #667eea;
            font-size: 1.2rem;
        }

        /* Projects Grid */
        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(350px, 1fr));
            gap: 2rem;
            margin-top: 3rem;
        }

        .project-card {
            background: rgba(255, 255, 255, 0.03);
            border: 1px solid rgba(255, 255, 255, 0.1);
            border-radius: 15px;
            padding: 2rem;
            transition: all 0.3s ease;
            backdrop-filter: blur(10px);
            position: relative;
            overflow: hidden;
        }

        .project-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 3px;
            background: linear-gradient(90deg, #667eea, #764ba2);
            transform: scaleX(0);
            transition: transform 0.3s ease;
        }

        .project-card:hover::before {
            transform: scaleX(1);
        }

        .project-card:hover {
            transform: translateY(-8px);
            background: rgba(255, 255, 255, 0.05);
            border-color: rgba(102, 126, 234, 0.5);
            box-shadow: 0 15px 50px rgba(102, 126, 234, 0.3);
        }

        .project-header {
            display: flex;
            justify-content: space-between;
            align-items: flex-start;
            margin-bottom: 1rem;
        }

        .project-icon {
            font-size: 2rem;
        }

        .project-card h3 {
            color: #ccd6f6;
            font-size: 1.4rem;
            margin-bottom: 0.5rem;
        }

        .project-card .tag {
            display: inline-block;
            padding: 0.3rem 0.8rem;
            background: rgba(102, 126, 234, 0.2);
            border-radius: 20px;
            font-size: 0.75rem;
            color: #667eea;
            margin-bottom: 1rem;
        }

        .project-card p {
            color: #8892b0;
            margin-bottom: 1.5rem;
            line-height: 1.6;
        }

        .tech-stack {
            display: flex;
            flex-wrap: wrap;
            gap: 0.5rem;
            margin-top: 1rem;
        }

        .tech-stack span {
            padding: 0.4rem 0.8rem;
            background: rgba(255, 255, 255, 0.05);
            border-radius: 5px;
            font-size: 0.85rem;
            color: #a8b2d1;
        }

        .project-link {
            display: inline-flex;
            align-items: center;
            gap: 0.5rem;
            color: #667eea;
            text-decoration: none;
            margin-top: 1rem;
            transition: all 0.3s ease;
        }

        .project-link:hover {
            color: #764ba2;
            transform: translateX(5px);
        }

        /* Skills Section */
        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 2rem;
            margin-top: 3rem;
        }

        .skill-category {
            background: rgba(255, 255, 255, 0.03);
            border: 1px solid rgba(255, 255, 255, 0.1);
            border-radius: 15px;
            padding: 2rem;
            backdrop-filter: blur(10px);
            transition: all 0.3s ease;
        }

        .skill-category:hover {
            transform: translateY(-5px);
            border-color: rgba(102, 126, 234, 0.5);
            box-shadow: 0 10px 40px rgba(102, 126, 234, 0.2);
        }

        .skill-category h3 {
            color: #667eea;
            font-size: 1.3rem;
            margin-bottom: 1.5rem;
        }

        .skill-tags {
            display: flex;
            flex-wrap: wrap;
            gap: 0.8rem;
        }

        .skill-tags span {
            padding: 0.6rem 1rem;
            background: rgba(255, 255, 255, 0.05);
            border: 1px solid rgba(255, 255, 255, 0.1);
            border-radius: 8px;
            color: #ccd6f6;
            transition: all 0.3s ease;
        }

        .skill-tags span:hover {
            background: rgba(102, 126, 234, 0.2);
            border-color: #667eea;
            transform: translateY(-2px);
        }

        /* Footer */
        footer {
            text-align: center;
            padding: 3rem 0;
            background: rgba(0, 0, 0, 0.3);
            border-top: 1px solid rgba(255, 255, 255, 0.1);
        }

        footer p {
            color: #8892b0;
            font-size: 1rem;
        }

        /* Responsive */
        @media (max-width: 768px) {
            .hero h1 {
                font-size: 2.5rem;
            }

            .hero h2 {
                font-size: 1.3rem;
            }

            .projects-grid {
                grid-template-columns: 1fr;
            }

            .experience-grid {
                grid-template-columns: 1fr;
            }

            .section-title {
                font-size: 2rem;
            }
        }
    </style>
</head>
<body>
    <!-- Hero Section -->
    <section class="hero">
        <div class="hero-content">
            <h1>Abrar Hussain Dar</h1>
            <h2>FullStack Developer | SaaS Builder | Cloud Enthusiast</h2>
            <p>Crafting scalable web applications, innovative SaaS platforms, and robust backends with expertise in Node.js, Next.js, TypeScript, and PostgreSQL. Building solutions that scale, perform, and create lasting impact.</p>
            
            <div class="social-links">
                <a href="mailto:abrardar988651@gmail.com">📧 Email</a>
                <a href="https://linkedin.com/in/abrarhussain0366" target="_blank">💼 LinkedIn</a>
                <a href="https://github.com/Abrarhussaindar" target="_blank">💻 GitHub</a>
            </div>
        </div>
    </section>

    <!-- Experience Section -->
    <section id="experience">
        <div class="container">
            <h2 class="section-title">💼 Professional Journey</h2>
            <div class="experience-grid">
                <div class="experience-card">
                    <h3>Backend Developer</h3>
                    <p class="company">Navrekh Technologies Pvt. Ltd.</p>
                    <p class="date">April 2024 – July 2025</p>
                    <ul>
                        <li>Architected and maintained high-performance backend services and RESTful APIs using Node.js</li>
                        <li>Optimized SQL & NoSQL database operations, ensuring scalability and enhanced performance</li>
                        <li>Implemented robust authentication and authorization mechanisms for enterprise applications</li>
                    </ul>
                </div>

                <div class="experience-card">
                    <h3>Full Stack Developer</h3>
                    <p class="company">Daisy Online Media and Gaming Pvt. Ltd.</p>
                    <p class="date">February 2023 – December 2023</p>
                    <ul>
                        <li>Developed full-stack applications with modern JavaScript frameworks and Node.js backend</li>
                        <li>Designed and implemented RESTful APIs for seamless client-server data exchange</li>
                        <li>Collaborated with cross-functional teams to deliver production-ready applications</li>
                    </ul>
                </div>
            </div>
        </div>
    </section>

    <!-- Projects Section -->
    <section id="projects">
        <div class="container">
            <h2 class="section-title">🚀 Featured Projects</h2>
            <div class="projects-grid">
                <div class="project-card">
                    <div class="project-header">
                        <div class="project-icon">💼</div>
                    </div>
                    <h3>BillMatrix</h3>
                    <span class="tag">SaaS Platform</span>
                    <p>Comprehensive billing automation platform with invoicing, subscriptions, payment processing, and analytics dashboards. Features role-based access control and real-time revenue tracking.</p>
                    <div class="tech-stack">
                        <span>Next.js</span>
                        <span>Node.js</span>
                        <span>PostgreSQL</span>
                        <span>TailwindCSS</span>
                        <span>Shadcn/ui</span>
                    </div>
                    <a href="https://billmatrix.in" target="_blank" class="project-link">View Live →</a>
                </div>

                <div class="project-card">
                    <div class="project-header">
                        <div class="project-icon">🏥</div>
                    </div>
                    <h3>Tabeeb Medical Solutions</h3>
                    <span class="tag">Healthcare SaaS</span>
                    <p>Modern healthcare platform integrating Razorpay payments, real-time video consultations, and digital prescription management for seamless patient care.</p>
                    <div class="tech-stack">
                        <span>Next.js</span>
                        <span>Node.js</span>
                        <span>PostgreSQL</span>
                        <span>Razorpay</span>
                        <span>WebRTC</span>
                    </div>
                    <a href="https://tabeeb.co.in" target="_blank" class="project-link">View Live →</a>
                </div>

                <div class="project-card">
                    <div class="project-header">
                        <div class="project-icon">⚽</div>
                    </div>
                    <h3>YourSportz</h3>
                    <span class="tag">Real-time App</span>
                    <p>Live football scoring application with real-time updates using Socket.io for instant score broadcasting and match statistics.</p>
                    <div class="tech-stack">
                        <span>Node.js</span>
                        <span>Socket.io</span>
                        <span>React</span>
                        <span>MongoDB</span>
                    </div>
                    <a href="https://yoursportz.in" target="_blank" class="project-link">View Live →</a>
                </div>

                <div class="project-card">
                    <div class="project-header">
                        <div class="project-icon">📊</div>
                    </div>
                    <h3>EcomMatrix</h3>
                    <span class="tag">Analytics Dashboard</span>
                    <p>Smart e-commerce analytics dashboard providing insights to track sales, customer behavior, and optimize online store performance.</p>
                    <div class="tech-stack">
                        <span>Next.js</span>
                        <span>Node.js</span>
                        <span>PostgreSQL</span>
                        <span>Chart.js</span>
                    </div>
                </div>

                <div class="project-card">
                    <div class="project-header">
                        <div class="project-icon">📄</div>
                    </div>
                    <h3>ResumeMatrix</h3>
                    <span class="tag">AI-Powered Tool</span>
                    <p>AI-powered resume builder creating ATS-optimized resumes that boost interview callbacks by 300%. Features intelligent formatting and keyword optimization.</p>
                    <div class="tech-stack">
                        <span>Next.js</span>
                        <span>OpenAI</span>
                        <span>PostgreSQL</span>
                        <span>TailwindCSS</span>
                    </div>
                    <a href="https://resumematrix.devmatrix.org/" target="_blank" class="project-link">View Live →</a>
                </div>

                <div class="project-card">
                    <div class="project-header">
                        <div class="project-icon">🏠</div>
                    </div>
                    <h3>ReHome</h3>
                    <span class="tag">Marketplace</span>
                    <p>Sustainable marketplace platform for buying and selling affordable pre-loved items, promoting circular economy and environmental consciousness.</p>
                    <div class="tech-stack">
                        <span>Next.js</span>
                        <span>Node.js</span>
                        <span>MongoDB</span>
                        <span>Stripe</span>
                    </div>
                    <a href="https://rehome.devmatrix.org/" target="_blank" class="project-link">View Live →</a>
                </div>

                <div class="project-card">
                    <div class="project-header">
                        <div class="project-icon">🛍️</div>
                    </div>
                    <h3>ShopMatrix</h3>
                    <span class="tag">E-commerce</span>
                    <p>Modern e-commerce platform delivering premium shopping experience with secure checkout, inventory management, and order tracking.</p>
                    <div class="tech-stack">
                        <span>Next.js</span>
                        <span>Node.js</span>
                        <span>PostgreSQL</span>
                        <span>Stripe</span>
                    </div>
                    <a href="https://shopmatrix.devmatrix.org/" target="_blank" class="project-link">View Live →</a>
                </div>

                <div class="project-card">
                    <div class="project-header">
                        <div class="project-icon">📚</div>
                    </div>
                    <h3>Brilliance Academy</h3>
                    <span class="tag">EdTech Platform</span>
                    <p>Smart coaching platform for classes 7-10 with comprehensive curriculum coverage, expert faculty, and interactive learning modules.</p>
                    <div class="tech-stack">
                        <span>Next.js</span>
                        <span>Node.js</span>
                        <span>PostgreSQL</span>
                        <span>AWS</span>
                    </div>
                    <a href="https://brillianceacademy.devmatrix.org/" target="_blank" class="project-link">View Live →</a>
                </div>

                <div class="project-card">
                    <div class="project-header">
                        <div class="project-icon">🧵</div>
                    </div>
                    <h3>Al-Nisa</h3>
                    <span class="tag">E-commerce</span>
                    <p>Premium knitting fabrics e-commerce platform blending traditional Kashmiri artistry with contemporary fashion for luxury textiles.</p>
                    <div class="tech-stack">
                        <span>Next.js</span>
                        <span>Node.js</span>
                        <span>MongoDB</span>
                        <span>Razorpay</span>
                    </div>
                    <a href="https://alnisa.devmatrix.org/" target="_blank" class="project-link">View Live →</a>
                </div>

                <div class="project-card">
                    <div class="project-header">
                        <div class="project-icon">🎨</div>
                    </div>
                    <h3>Royal Paper Mache</h3>
                    <span class="tag">Cultural Heritage</span>
                    <p>Digital showcase for traditional Kashmiri paper mache crafts, bringing centuries-old artistry to modern e-commerce.</p>
                    <div class="tech-stack">
                        <span>React</span>
                        <span>Node.js</span>
                        <span>MongoDB</span>
                        <span>Stripe</span>
                    </div>
                    <a href="https://royalpapermache.in/" target="_blank" class="project-link">View Live →</a>
                </div>

                <div class="project-card">
                    <div class="project-header">
                        <div class="project-icon">💧</div>
                    </div>
                    <h3>Home Basics</h3>
                    <span class="tag">Service Platform</span>
                    <p>Trusted water purification and water heater installation services platform with booking system and service tracking.</p>
                    <div class="tech-stack">
                        <span>React</span>
                        <span>Node.js</span>
                        <span>MongoDB</span>
                    </div>
                    <a href="https://homebasics.onrender.com/" target="_blank" class="project-link">View Live →</a>
                </div>

                <div class="project-card">
                    <div class="project-header">
                        <div class="project-icon">✈️</div>
                    </div>
                    <h3>M.M Tour and Travels</h3>
                    <span class="tag">Tourism</span>
                    <p>Comprehensive travel platform offering custom tour packages, expert guides, and 24/7 support for memorable journeys.</p>
                    <div class="tech-stack">
                        <span>Next.js</span>
                        <span>Node.js</span>
                        <span>PostgreSQL</span>
                    </div>
                    <a href="https://mmtourandtravels.in/" target="_blank" class="project-link">View Live →</a>
                </div>

                <div class="project-card">
                    <div class="project-header">
                        <div class="project-icon">🏔️</div>
                    </div>
                    <h3>One Call Kashmir</h3>
                    <span class="tag">Tourism Agency</span>
                    <p>Premier Kashmir tourism platform providing seamless tour bookings, shikara rides, and adventure experiences in the valley.</p>
                    <div class="tech-stack">
                        <span>React</span>
                        <span>Node.js</span>
                        <span>MongoDB</span>
                    </div>
                    <a href="https://onecallkashmir.com/" target="_blank" class="project-link">View Live →</a>
                </div>
            </div>
        </div>
    </section>

    <!-- Skills Section -->
    <section id="skills">
        <div class="container">
            <h2 class="section-title">🛠️ Technical Arsenal</h2>
            <div class="skills-grid">
                <div class="skill-category">
                    <h3>Languages & Frameworks</h3>
                    <div class="skill-tags">
                        <span>TypeScript</span>
                        <span>JavaScript</span>
                        <span>Node.js</span>
                        <span>Next.js</span>
                        <span>React.js</span>
                        <span>Python</span>
                        <span>Django</span>
                        <span>FastAPI</span>
                    </div>
                </div>

                <div class="skill-category">
                    <h3>Databases & Cloud</h3>
                    <div class="skill-tags">
                        <span>PostgreSQL</span>
                        <span>MongoDB</span>
                        <span>Redis</span>
                        <span>Azure</span>
                        <span>AWS</span>
                        <span>Render</span>
                    </div>
                </div>

                <div class="skill-category">
                    <h3>Tools & Technologies</h3>
                    <div class="skill-tags">
                        <span>Git/GitHub</span>
                        <span>Docker</span>
                        <span>Postman</span>
                        <span>Shadcn/ui</span>
                        <span>TailwindCSS</span>
                        <span>Linux</span>
                        <span>Socket.io</span>
                        <span>REST APIs</span>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <p>✨ Built with passion by Abrar Hussain Dar • Building solutions that scale, perform, and create impact</p>
            <p style="margin-top: 1rem; color: #667eea;">💡 Open to collaborations and exciting opportunities</p>
        </div>
    </footer>
</body>
</html>
