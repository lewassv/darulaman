<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=yes, viewport-fit=cover">
    <meta name="apple-mobile-web-app-capable" content="yes">
    <meta name="apple-mobile-web-app-status-bar-style" content="black-translucent">
    <title>Darul Aman | Backend Developer</title>
    <!-- Google Fonts & Font Awesome -->
    <link href="https://fonts.googleapis.com/css2?family=Inter:opsz,wght@14..32,300;14..32,400;14..32,600;14..32,700;14..32,800&family=JetBrains+Mono:wght@400;500;600;700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            -webkit-tap-highlight-color: transparent;
        }

        body {
            font-family: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Helvetica, sans-serif;
            background: #0a0e17;
            color: #d4e1ed;
            scroll-behavior: smooth;
            overflow-x: hidden;
            -webkit-font-smoothing: antialiased;
        }

        ::-webkit-scrollbar {
            width: 6px;
        }
        ::-webkit-scrollbar-track {
            background: #1a2332;
            border-radius: 10px;
        }
        ::-webkit-scrollbar-thumb {
            background: #00d4ff;
            border-radius: 10px;
        }

        .container {
            max-width: 1280px;
            margin: 0 auto;
            padding: 0 1.5rem;
        }

        section {
            padding: 4rem 0;
        }

        .section-title {
            font-size: 2.2rem;
            font-weight: 800;
            margin-bottom: 1rem;
            background: linear-gradient(135deg, #00d4ff, #7b2ffc);
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
            letter-spacing: -0.5px;
        }

        .section-subtitle {
            font-size: 1rem;
            color: #8ba0c7;
            margin-bottom: 2.5rem;
            border-left: 4px solid #00d4ff;
            padding-left: 1rem;
        }

        /* Navbar */
        .navbar {
            position: sticky;
            top: 0;
            background: rgba(10, 14, 23, 0.96);
            backdrop-filter: blur(18px);
            -webkit-backdrop-filter: blur(18px);
            z-index: 1000;
            padding: 0.9rem 0;
            border-bottom: 1px solid rgba(0, 212, 255, 0.15);
        }

        .nav-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
            flex-wrap: wrap;
        }

        .logo {
            font-weight: 800;
            font-size: 1.7rem;
            background: linear-gradient(120deg, #00d4ff, #7b2ffc);
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
            letter-spacing: -0.5px;
        }
        .logo i {
            color: #00d4ff;
            margin-right: 6px;
        }
        .logo span {
            color: #7b2ffc;
        }

        .nav-links {
            display: flex;
            gap: 1.6rem;
            list-style: none;
        }

        .nav-links a {
            text-decoration: none;
            font-weight: 600;
            color: #8ba0c7;
            transition: 0.3s;
            font-size: 0.95rem;
            padding: 6px 0;
            position: relative;
        }

        .nav-links a::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 0;
            height: 2px;
            background: linear-gradient(90deg, #00d4ff, #7b2ffc);
            transition: width 0.3s;
        }

        .nav-links a:hover::after,
        .nav-links a:active::after {
            width: 100%;
        }

        .nav-links a:hover {
            color: #00d4ff;
        }

        /* Hero */
        .hero {
            padding: 2rem 0 3rem 0;
            display: flex;
            flex-wrap: wrap;
            align-items: center;
            justify-content: space-between;
            gap: 1.8rem;
        }

        .hero-content {
            flex: 1;
        }

        .hero-badge {
            background: rgba(0, 212, 255, 0.15);
            color: #00d4ff;
            padding: 0.3rem 1.2rem;
            border-radius: 40px;
            display: inline-block;
            font-size: 0.8rem;
            font-weight: 600;
            margin-bottom: 1rem;
            border: 1px solid rgba(0, 212, 255, 0.2);
            font-family: 'JetBrains Mono', monospace;
        }

        .hero-content h1 {
            font-size: 2.6rem;
            font-weight: 800;
            line-height: 1.2;
            margin-bottom: 0.8rem;
            color: #e8f0fe;
        }

        .hero-highlight {
            background: linear-gradient(120deg, #00d4ff, #7b2ffc);
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
        }

        .hero-desc {
            font-size: 1.05rem;
            color: #8ba0c7;
            margin: 1.2rem 0;
            max-width: 100%;
            line-height: 1.6;
        }

        .tech-stack {
            display: flex;
            gap: 0.8rem;
            flex-wrap: wrap;
            margin: 1.5rem 0;
        }

        .tech-tag {
            background: rgba(0, 212, 255, 0.08);
            color: #00d4ff;
            padding: 0.4rem 1rem;
            border-radius: 30px;
            font-size: 0.75rem;
            font-weight: 600;
            font-family: 'JetBrains Mono', monospace;
            border: 1px solid rgba(0, 212, 255, 0.15);
        }

        .btn-group {
            display: flex;
            gap: 0.9rem;
            flex-wrap: wrap;
        }

        .btn-primary, .btn-outline {
            padding: 0.7rem 1.8rem;
            border-radius: 50px;
            font-weight: 600;
            font-size: 0.9rem;
            transition: 0.3s;
            text-decoration: none;
            display: inline-block;
            text-align: center;
        }

        .btn-primary {
            background: linear-gradient(135deg, #00d4ff, #7b2ffc);
            color: white;
            border: none;
            box-shadow: 0 6px 20px rgba(0, 212, 255, 0.25);
        }

        .btn-primary:hover {
            transform: translateY(-2px);
            box-shadow: 0 8px 30px rgba(0, 212, 255, 0.35);
        }

        .btn-primary:active {
            transform: scale(0.97);
        }

        .btn-outline {
            background: transparent;
            border: 2px solid #00d4ff;
            color: #00d4ff;
        }

        .btn-outline:hover {
            background: rgba(0, 212, 255, 0.1);
            transform: translateY(-2px);
        }

        .btn-outline:active {
            transform: scale(0.97);
        }

        .hero-image {
            flex: 1;
            text-align: center;
        }

        /* Style untuk foto profil */
        .profile-photo {
            width: 280px;
            height: 280px;
            border-radius: 50%;
            object-fit: cover;
            border: 4px solid #00d4ff;
            box-shadow: 0 0 40px rgba(0, 212, 255, 0.2), 0 0 80px rgba(0, 212, 255, 0.1);
            transition: all 0.3s ease;
        }

        .profile-photo:hover {
            transform: scale(1.02);
            box-shadow: 0 0 60px rgba(0, 212, 255, 0.3), 0 0 100px rgba(0, 212, 255, 0.15);
        }

        .code-float {
            font-family: 'JetBrains Mono', monospace;
            font-size: 0.8rem;
            color: #7b2ffc;
            opacity: 0.6;
            margin-top: 1rem;
        }

        .terminal-text {
            font-family: 'JetBrains Mono', monospace;
            color: #00d4ff;
            font-size: 0.85rem;
            opacity: 0.7;
            margin-top: 0.5rem;
        }

        /* Stats */
        .stats-row {
            display: flex;
            gap: 2rem;
            flex-wrap: wrap;
            margin-top: 1.8rem;
        }

        .stat-item {
            display: flex;
            align-items: center;
            gap: 0.5rem;
            color: #8ba0c7;
        }

        .stat-item i {
            color: #00d4ff;
        }

        .stat-item strong {
            color: #e8f0fe;
            font-size: 1.2rem;
        }

        /* Skills Grid */
        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
            gap: 1.5rem;
            margin-top: 1.8rem;
        }

        .skill-card {
            background: rgba(26, 35, 50, 0.6);
            border-radius: 1.8rem;
            padding: 1.8rem 1.2rem;
            transition: all 0.3s ease;
            border: 1px solid rgba(0, 212, 255, 0.08);
            text-align: center;
            backdrop-filter: blur(10px);
        }

        .skill-card:hover {
            transform: translateY(-4px);
            border-color: rgba(0, 212, 255, 0.2);
            box-shadow: 0 12px 30px rgba(0, 0, 0, 0.3);
        }

        .skill-card:active {
            transform: scale(0.98);
        }

        .skill-icon {
            font-size: 2.5rem;
            color: #00d4ff;
            margin-bottom: 1rem;
        }

        .skill-card h3 {
            font-size: 1.2rem;
            margin-bottom: 0.6rem;
            color: #e8f0fe;
            font-weight: 700;
        }

        .skill-card p {
            font-size: 0.9rem;
            color: #8ba0c7;
            line-height: 1.5;
        }

        .skill-level {
            margin-top: 0.8rem;
            height: 4px;
            background: #1a2332;
            border-radius: 4px;
            overflow: hidden;
        }

        .skill-level-bar {
            height: 100%;
            background: linear-gradient(90deg, #00d4ff, #7b2ffc);
            border-radius: 4px;
            transition: width 1s ease;
        }

        /* Portfolio */
        .portfolio-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 1.5rem;
            margin-top: 1.8rem;
        }

        .portfolio-item {
            background: rgba(26, 35, 50, 0.6);
            border-radius: 1.8rem;
            overflow: hidden;
            transition: 0.3s;
            border: 1px solid rgba(0, 212, 255, 0.08);
            backdrop-filter: blur(10px);
        }

        .portfolio-item:hover {
            transform: translateY(-4px);
            border-color: rgba(0, 212, 255, 0.2);
        }

        .portfolio-header {
            padding: 1.5rem 1.5rem 0.5rem;
            display: flex;
            justify-content: space-between;
            align-items: flex-start;
        }

        .portfolio-header .project-icon {
            font-size: 2rem;
            color: #00d4ff;
        }

        .portfolio-tag {
            background: rgba(123, 47, 252, 0.2);
            color: #7b2ffc;
            padding: 0.25rem 1rem;
            border-radius: 30px;
            font-size: 0.7rem;
            font-weight: 600;
            font-family: 'JetBrains Mono', monospace;
        }

        .portfolio-info {
            padding: 0 1.5rem 1.5rem;
        }

        .portfolio-info h3 {
            font-size: 1.2rem;
            margin-bottom: 0.4rem;
            color: #e8f0fe;
        }

        .portfolio-info p {
            font-size: 0.85rem;
            color: #8ba0c7;
            line-height: 1.5;
        }

        .portfolio-tech {
            display: flex;
            gap: 0.5rem;
            flex-wrap: wrap;
            margin-top: 0.8rem;
        }

        .portfolio-tech span {
            background: rgba(0, 212, 255, 0.08);
            color: #00d4ff;
            padding: 0.2rem 0.8rem;
            border-radius: 20px;
            font-size: 0.7rem;
            font-family: 'JetBrains Mono', monospace;
        }

        /* Testimonial */
        .testimonial-card {
            background: rgba(26, 35, 50, 0.6);
            border-radius: 1.8rem;
            padding: 1.5rem;
            margin: 0.5rem 0;
            border: 1px solid rgba(0, 212, 255, 0.08);
            backdrop-filter: blur(10px);
        }

        .testimonial-card p {
            font-size: 0.9rem;
            line-height: 1.6;
            color: #d4e1ed;
        }

        .testimonial-card h4 {
            margin-top: 0.8rem;
            font-size: 0.9rem;
            color: #00d4ff;
        }

        .testimonial-card .role {
            font-size: 0.75rem;
            color: #8ba0c7;
        }

        /* Contact */
        .contact-flex {
            display: flex;
            flex-wrap: wrap;
            gap: 2rem;
            background: rgba(26, 35, 50, 0.6);
            border-radius: 2rem;
            padding: 2rem;
            border: 1px solid rgba(0, 212, 255, 0.08);
            backdrop-filter: blur(10px);
        }

        .contact-info {
            flex: 1;
        }

        .contact-info h3 {
            font-size: 1.5rem;
            margin-bottom: 0.8rem;
            color: #e8f0fe;
        }

        .contact-info > p {
            color: #8ba0c7;
            margin-bottom: 1.5rem;
        }

        .contact-detail {
            display: flex;
            align-items: center;
            gap: 0.8rem;
            margin: 1rem 0;
            flex-wrap: wrap;
            color: #d4e1ed;
        }

        .contact-detail i {
            font-size: 1.3rem;
            color: #00d4ff;
            width: 36px;
        }

        .contact-detail a {
            color: #d4e1ed;
            text-decoration: none;
            transition: 0.3s;
        }

        .contact-detail a:hover {
            color: #00d4ff;
        }

        .contact-form {
            flex: 1;
        }

        .input-group {
            margin-bottom: 1rem;
        }

        input, textarea {
            width: 100%;
            padding: 0.85rem 1rem;
            border: 1px solid rgba(0, 212, 255, 0.15);
            border-radius: 1.2rem;
            font-family: inherit;
            font-size: 0.95rem;
            transition: 0.3s;
            background: rgba(10, 14, 23, 0.6);
            color: #e8f0fe;
            appearance: none;
        }

        input::placeholder, textarea::placeholder {
            color: #4a5a7a;
        }

        input:focus, textarea:focus {
            outline: none;
            border-color: #00d4ff;
            box-shadow: 0 0 0 3px rgba(0, 212, 255, 0.1);
        }

        button[type="submit"] {
            background: linear-gradient(135deg, #00d4ff, #7b2ffc);
            color: white;
            border: none;
            padding: 0.85rem 1.5rem;
            border-radius: 2rem;
            font-weight: 700;
            cursor: pointer;
            width: 100%;
            font-size: 1rem;
            transition: 0.3s;
        }

        button[type="submit"]:hover {
            transform: translateY(-2px);
            box-shadow: 0 8px 30px rgba(0, 212, 255, 0.3);
        }

        button[type="submit"]:active {
            transform: scale(0.98);
        }

        /* Footer */
        footer {
            background: #060a12;
            color: #4a5a7a;
            padding: 1.8rem 0;
            text-align: center;
            margin-top: 1.5rem;
            font-size: 0.8rem;
            border-top: 1px solid rgba(0, 212, 255, 0.05);
        }

        footer .heart {
            color: #00d4ff;
        }

        /* Responsive */
        @media (max-width: 640px) {
            .container {
                padding: 0 1.2rem;
            }
            section {
                padding: 2.8rem 0;
            }
            .nav-container {
                flex-direction: column;
                gap: 0.7rem;
            }
            .nav-links {
                gap: 1.2rem;
            }
            .nav-links a {
                font-size: 0.85rem;
            }
            .hero {
                flex-direction: column-reverse;
                text-align: center;
                padding: 1rem 0 2rem;
            }
            .hero-content h1 {
                font-size: 2rem;
            }
            .hero-desc {
                font-size: 0.95rem;
            }
            .btn-group {
                justify-content: center;
            }
            .tech-stack {
                justify-content: center;
            }
            .stats-row {
                justify-content: center;
            }
            .section-title {
                font-size: 1.9rem;
            }
            .profile-photo {
                width: 200px;
                height: 200px;
            }
            .skills-grid, .portfolio-grid {
                gap: 1rem;
            }
            .skill-card {
                padding: 1.2rem;
            }
            .contact-flex {
                padding: 1.2rem;
                gap: 1.5rem;
            }
            .contact-detail {
                gap: 0.6rem;
            }
            .contact-detail i {
                font-size: 1.1rem;
                width: 28px;
            }
            input, textarea {
                padding: 0.7rem 0.9rem;
                font-size: 0.9rem;
            }
        }

        @media (max-width: 380px) {
            .hero-content h1 {
                font-size: 1.7rem;
            }
            .logo {
                font-size: 1.4rem;
            }
            .nav-links a {
                font-size: 0.75rem;
            }
            .section-title {
                font-size: 1.7rem;
            }
            .skill-icon {
                font-size: 2rem;
            }
            .btn-primary, .btn-outline {
                padding: 0.55rem 1rem;
                font-size: 0.8rem;
            }
            .profile-photo {
                width: 160px;
                height: 160px;
            }
        }

        input, select, textarea, button {
            border-radius: 12px;
        }
        button, a, .skill-card, .portfolio-item {
            cursor: pointer;
        }
    </style>
</head>
<body>
    <nav class="navbar">
        <div class="container nav-container">
            <div class="logo">
                <i class="fas fa-terminal"></i>lewassv<span>.Dev</span>
            </div>
            <ul class="nav-links">
                <li><a href="#home">Beranda</a></li>
                <li><a href="#keahlian">Keahlian</a></li>
                <li><a href="#portofolio">Proyek</a></li>
                <li><a href="#kontak">Kontak</a></li>
            </ul>
        </div>
    </nav>

    <main>
        <!-- Hero Section -->
        <section id="home">
            <div class="container hero">
                <div class="hero-content">
                    <div class="hero-badge">
                        <i class="fas fa-code"></i> Backend Developer
                    </div>
                    <h1>Hi, I'm <span class="hero-highlight">Darul Aman</span></h1>
                    <p class="hero-desc">
                        Backend Developer dengan pengalaman membangun sistem yang scalable, aman, dan performant. 
                        Spesialisasi di <strong>Arsitektur Microservices, API Design, dan Database Optimization</strong>.
                    </p>
                    <div class="tech-stack">
                        <span class="tech-tag"><i class="fab fa-php"></i> PHP (Laravel)</span>
                        <span class="tech-tag"><i class="fab fa-node"></i> Node.js</span>
                        <span class="tech-tag"><i class="fas fa-database"></i> PostgreSQL</span>
                        <span class="tech-tag"><i class="fas fa-cloud"></i> AWS</span>
                        <span class="tech-tag"><i class="fas fa-code-branch"></i> Docker</span>
                    </div>
                    <div class="btn-group">
                        <a href="#portofolio" class="btn-primary"><i class="fas fa-folder-open"></i> Lihat Proyek</a>
                        <a href="#kontak" class="btn-outline"><i class="fas fa-paper-plane"></i> Hubungi Saya</a>
                    </div>
                    <div class="stats-row">
                        <span class="stat-item"><i class="fas fa-check-circle"></i> <strong>53+</strong> Proyek Selesai</span>
                        <span class="stat-item"><i class="fas fa-users"></i> <strong>30+</strong> Followers</span>
                        <span class="stat-item"><i class="fas fa-code-branch"></i> <strong>2+</strong> Tahun Pengalaman</span>
                    </div>
                </div>
                <div class="hero-image">
                    <!-- Ganti src="foto-saya.jpg" dengan nama file foto Anda -->
                    <img src="lewassv7.JPEG" alt="Foto Darul Aman" class="profile-photo">
                    <div class="code-float">
                       
                    </div>
                    <div class="terminal-text">
                        
                    </div>
                </div>
            </div>
        </section>

        <!-- Keahlian -->
        <section id="keahlian" style="background: rgba(10, 14, 23, 0.5);">
            <div class="container">
                <h2 class="section-title">Tech Stack &amp; Keahlian</h2>
                <div class="section-subtitle">Tools dan teknologi yang saya kuasai untuk membangun solusi backend</div>
                <div class="skills-grid">
                    <div class="skill-card">
                        <div class="skill-icon"><i class="fas fa-server"></i></div>
                        <h3>Backend Development</h3>
                        <p>Laravel, Node.js, Express.js, RESTful API, GraphQL, Microservices Architecture</p>
                        <div class="skill-level">
                            <div class="skill-level-bar" style="width: 90%;"></div>
                        </div>
                    </div>
                    <div class="skill-card">
                        <div class="skill-icon"><i class="fas fa-database"></i></div>
                        <h3>Database &amp; Cache</h3>
                        <p>PostgreSQL, MySQL, MongoDB, Redis, Query Optimization, Database Design</p>
                        <div class="skill-level">
                            <div class="skill-level-bar" style="width: 85%;"></div>
                        </div>
                    </div>
                    <div class="skill-card">
                        <div class="skill-icon"><i class="fas fa-cloud"></i></div>
                        <h3>Cloud &amp; DevOps</h3>
                        <p>AWS (EC2, S3, RDS), Docker, CI/CD, Nginx, Linux Server Management</p>
                        <div class="skill-level">
                            <div class="skill-level-bar" style="width: 80%;"></div>
                        </div>
                    </div>
                    <div class="skill-card">
                        <div class="skill-icon"><i class="fas fa-shield-alt"></i></div>
                        <h3>Security &amp; Performance</h3>
                        <p>Authentication (JWT, OAuth), Encryption, API Security, Caching, Load Balancing</p>
                        <div class="skill-level">
                            <div class="skill-level-bar" style="width: 75%;"></div>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- Portofolio -->
        <section id="portofolio">
            <div class="container">
                <h2 class="section-title">Proyek Unggulan</h2>
                <div class="section-subtitle">Portofolio proyek backend yang telah saya kerjakan</div>
                <div class="portfolio-grid">
                    <div class="portfolio-item">
                        <div class="portfolio-header">
                            <span class="project-icon"><i class="fas fa-shopping-cart"></i></span>
                            <span class="portfolio-tag">E-Commerce</span>
                        </div>
                        <div class="portfolio-info">
                            <h3>Marketplace API</h3>
                            <p>Backend API untuk marketplace dengan fitur payment gateway, real-time inventory, dan order management.</p>
                            <div class="portfolio-tech">
                                <span>Laravel</span>
                                <span>MySQL</span>
                                <span>Redis</span>
                                <span>Midtrans</span>
                            </div>
                        </div>
                    </div>

                    <div class="portfolio-item">
                        <div class="portfolio-header">
                            <span class="project-icon"><i class="fas fa-chart-line"></i></span>
                            <span class="portfolio-tag">Analytics</span>
                        </div>
                        <div class="portfolio-info">
                            <h3>Analytics Dashboard</h3>
                            <p>Sistem analitik real-time untuk monitoring data bisnis dengan WebSocket dan visualisasi data.</p>
                            <div class="portfolio-tech">
                                <span>Node.js</span>
                                <span>PostgreSQL</span>
                                <span>Socket.io</span>
                                <span>Docker</span>
                            </div>
                        </div>
                    </div>

                    <div class="portfolio-item">
                        <div class="portfolio-header">
                            <span class="project-icon"><i class="fas fa-heartbeat"></i></span>
                            <span class="portfolio-tag">Healthcare</span>
                        </div>
                        <div class="portfolio-info">
                            <h3>E-Health Platform</h3>
                            <p>Platform telemedicine dengan fitur appointment, rekam medis digital, dan integrasi dengan sistem laboratorium.</p>
                            <div class="portfolio-tech">
                                <span>Laravel</span>
                                <span>PostgreSQL</span>
                                <span>AWS</span>
                                <span>JWT</span>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- Testimonial -->
        <section style="background: rgba(10, 14, 23, 0.5);">
            <div class="container">
                <h2 class="section-title">Testimoni Klien</h2>
                <div class="section-subtitle">Apa kata mereka tentang kolaborasi dengan saya</div>
                <div class="skills-grid" style="grid-template-columns: repeat(auto-fit, minmax(280px,1fr));">
                    <div class="testimonial-card">
                        <i class="fas fa-quote-left" style="font-size: 1.6rem; color:#00d4ff; opacity:0.5"></i>
                        <p style="margin: 0.8rem 0;">"Darul sangat profesional dan cepat dalam menyelesaikan proyek API. Dokumentasi yang diberikan juga sangat lengkap dan mudah dipahami."</p>
                        <h4>— Andi Pratama</h4>
                        <span class="role">CTO, TechSolution.id</span>
                    </div>
                    <div class="testimonial-card">
                        <i class="fas fa-quote-left" style="font-size: 1.6rem; color:#00d4ff; opacity:0.5"></i>
                        <p style="margin: 0.8rem 0;">"Tim kami sangat terbantu dengan arsitektur microservices yang dibangun. Sistem jadi lebih scalable dan maintenance jadi lebih mudah."</p>
                        <h4>— Sarah Wijaya</h4>
                        <span class="role">Lead Developer, FinPro</span>
                    </div>
                    <div class="testimonial-card">
                        <i class="fas fa-quote-left" style="font-size: 1.6rem; color:#00d4ff; opacity:0.5"></i>
                        <p style="margin: 0.8rem 0;">"Kualitas kode yang dihasilkan sangat bersih dan mengikuti best practice. Database query yang dioptimasi membuat performa aplikasi meningkat drastis."</p>
                        <h4>— Budi Santoso</h4>
                        <span class="role">CEO, EduTech</span>
                    </div>
                </div>
            </div>
        </section>

        <!-- Kontak -->
        <section id="kontak">
            <div class="container">
                <h2 class="section-title">Hubungi Saya</h2>
                <div class="section-subtitle">Tertarik berkolaborasi atau punya pertanyaan? Mari terhubung</div>
                <div class="contact-flex">
                    <div class="contact-info">
                        <h3>Let's Build Something Great</h3>
                        <p>Saya siap membantu Anda membangun solusi backend yang handal dan scalable.</p>
                        <div class="contact-detail">
                            <i class="fas fa-envelope"></i>
                            <a href="mailto:darul.aman@email.com">darul.aman@email.com</a>
                        </div>
                        <div class="contact-detail">
                            <i class="fab fa-github"></i>
                            <a href="#">github.com/darulaman</a>
                        </div>
                        <div class="contact-detail">
                            <i class="fab fa-linkedin"></i>
                            <a href="#">linkedin.com/in/darulaman</a>
                        </div>
                        <div class="contact-detail">
                            <i class="fab fa-twitter"></i>
                            <a href="#">@darulaman_dev</a>
                        </div>
                    </div>
                    <div class="contact-form">
                        <form id="contactForm">
                            <div class="input-group">
                                <input type="text" id="name" placeholder="Nama lengkap" required>
                            </div>
                            <div class="input-group">
                                <input type="email" id="email" placeholder="Email aktif" required>
                            </div>
                            <div class="input-group">
                                <textarea rows="4" id="message" placeholder="Deskripsikan kebutuhan proyek Anda..." required></textarea>
                            </div>
                            <button type="submit"><i class="fas fa-paper-plane"></i> Kirim Pesan</button>
                            <p id="formFeedback" style="margin-top: 1rem; font-size: 0.8rem; text-align:center; color: #00d4ff;"></p>
                        </form>
                    </div>
                </div>
            </div>
        </section>
    </main>

    <footer>
        <div class="container">
            <p><i class="fas fa-code heart"></i> Build with precision, deploy with confidence</p>
            <p style="margin-top: 0.5rem; font-size: 0.75rem; color: #3a4a6a;">
                &lt;?php echo "Made with Time by Darul Aman"; ?&gt;
            </p>
        </div>
    </footer>

    <script>
        // Smooth Scrolling
        document.querySelectorAll('.nav-links a, .btn-primary, .btn-outline').forEach(anchor => {
            anchor.addEventListener('click', function(e) {
                const hash = this.getAttribute('href');
                if (hash && hash.startsWith('#')) {
                    e.preventDefault();
                    const target = document.querySelector(hash);
                    if (target) {
                        target.scrollIntoView({ behavior: 'smooth', block: 'start' });
                    }
                }
            });
        });

        // Contact Form
        const contactForm = document.getElementById('contactForm');
        const feedback = document.getElementById('formFeedback');

        contactForm.addEventListener('submit', (e) => {
            e.preventDefault();
            const name = document.getElementById('name').value.trim();
            const email = document.getElementById('email').value.trim();
            const message = document.getElementById('message').value.trim();

            if(!name || !email || !message) {
                feedback.innerHTML = '⚠️ Semua bidang harus diisi.';
                feedback.style.color = '#ff6b6b';
                return;
            }
            if(!email.includes('@')) {
                feedback.innerHTML = '📧 Masukkan email valid.';
                feedback.style.color = '#ff6b6b';
                return;
            }

            feedback.innerHTML = '✅ Terima kasih, ' + name + '! Pesan Anda telah terkirim. Saya akan membalas dalam 1x24 jam.';
            feedback.style.color = '#00d4ff';
            contactForm.reset();
            setTimeout(() => {
                feedback.innerHTML = '';
            }, 5000);
        });
    </script>
</body>
</html>
