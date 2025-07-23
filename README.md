<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My GitHub Profile</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --primary: #24292e;
            --secondary: #0366d6;
            --light: #f6f8fa;
            --dark: #1f2328;
            --gray: #6e7781;
            --green: #2ea44f;
            --shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
        }
        
        body {
            background-color: var(--light);
            color: var(--dark);
            line-height: 1.6;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        header {
            background-color: white;
            box-shadow: var(--shadow);
            padding: 20px 0;
            position: sticky;
            top: 0;
            z-index: 100;
        }
        
        .header-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .logo {
            font-size: 24px;
            font-weight: 700;
            color: var(--primary);
            text-decoration: none;
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        .logo i {
            color: var(--secondary);
        }
        
        nav ul {
            display: flex;
            list-style: none;
            gap: 20px;
        }
        
        nav a {
            text-decoration: none;
            color: var(--dark);
            font-weight: 500;
            transition: color 0.3s;
        }
        
        nav a:hover {
            color: var(--secondary);
        }
        
        .hero {
            padding: 80px 0;
            text-align: center;
            background: linear-gradient(135deg, #f5f7fa 0%, #c3cfe2 100%);
        }
        
        .hero img {
            width: 150px;
            height: 150px;
            border-radius: 50%;
            object-fit: cover;
            border: 5px solid white;
            box-shadow: var(--shadow);
            margin-bottom: 20px;
        }
        
        .hero h1 {
            font-size: 2.5rem;
            margin-bottom: 10px;
            color: var(--primary);
        }
        
        .hero p {
            font-size: 1.2rem;
            color: var(--gray);
            max-width: 600px;
            margin: 0 auto 20px;
        }
        
        .social-links {
            display: flex;
            justify-content: center;
            gap: 15px;
            margin-top: 20px;
        }
        
        .social-links a {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            width: 40px;
            height: 40px;
            border-radius: 50%;
            background-color: var(--primary);
            color: white;
            text-decoration: none;
            transition: all 0.3s;
        }
        
        .social-links a:hover {
            background-color: var(--secondary);
            transform: translateY(-3px);
        }
        
        .section {
            padding: 60px 0;
        }
        
        .section-title {
            text-align: center;
            margin-bottom: 40px;
            font-size: 2rem;
            color: var(--primary);
        }
        
        .about-content {
            display: flex;
            gap: 40px;
            align-items: center;
        }
        
        .about-text {
            flex: 1;
        }
        
        .about-text h3 {
            margin-bottom: 20px;
            font-size: 1.5rem;
            color: var(--dark);
        }
        
        .about-text p {
            margin-bottom: 15px;
            color: var(--gray);
        }
        
        .skills {
            flex: 1;
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(120px, 1fr));
            gap: 15px;
        }
        
        .skill-item {
            background-color: white;
            padding: 15px;
            border-radius: 5px;
            text-align: center;
            box-shadow: var(--shadow);
            transition: transform 0.3s;
        }
        
        .skill-item:hover {
            transform: translateY(-5px);
        }
        
        .skill-item i {
            font-size: 2rem;
            margin-bottom: 10px;
            color: var(--secondary);
        }
        
        .projects {
            background-color: #f6f8fa;
        }
        
        .project-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 30px;
        }
        
        .project-card {
            background-color: white;
            border-radius: 8px;
            overflow: hidden;
            box-shadow: var(--shadow);
            transition: all 0.3s;
        }
        
        .project-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.1);
        }
        
        .project-image {
            height: 200px;
            overflow: hidden;
        }
        
        .project-image img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.5s;
        }
        
        .project-card:hover .project-image img {
            transform: scale(1.05);
        }
        
        .project-info {
            padding: 20px;
        }
        
        .project-info h3 {
            margin-bottom: 10px;
            color: var(--primary);
        }
        
        .project-info p {
            color: var(--gray);
            margin-bottom: 15px;
        }
        
        .project-links {
            display: flex;
            gap: 10px;
        }
        
        .project-links a {
            padding: 8px 15px;
            border-radius: 5px;
            text-decoration: none;
            font-size: 0.9rem;
            font-weight: 500;
            transition: all 0.3s;
        }
        
        .code-link {
            background-color: var(--primary);
            color: white;
        }
        
        .code-link:hover {
            background-color: var(--secondary);
        }
        
        .live-link {
            background-color: var(--light);
            color: var(--dark);
            border: 1px solid var(--gray);
        }
        
        .live-link:hover {
            background-color: white;
            border-color: var(--secondary);
            color: var(--secondary);
        }
        
        .contact {
            text-align: center;
        }
        
        .contact-form {
            max-width: 600px;
            margin: 0 auto;
            padding: 30px;
            background-color: white;
            border-radius: 8px;
            box-shadow: var(--shadow);
        }
        
        .form-group {
            margin-bottom: 20px;
            text-align: left;
        }
        
        .form-group label {
            display: block;
            margin-bottom: 8px;
            color: var(--dark);
            font-weight: 500;
        }
        
        .form-group input,
        .form-group textarea {
            width: 100%;
            padding: 12px;
            border: 1px solid #ddd;
            border-radius: 5px;
            font-size: 1rem;
            transition: border-color 0.3s;
        }
        
        .form-group input:focus,
        .form-group textarea:focus {
            outline: none;
            border-color: var(--secondary);
        }
        
        .submit-btn {
            background-color: var(--secondary);
            color: white;
            border: none;
            padding: 12px 25px;
            font-size: 1rem;
            font-weight: 500;
            border-radius: 5px;
            cursor: pointer;
            transition: background-color 0.3s;
        }
        
        .submit-btn:hover {
            background-color: var(--primary);
        }
        
        footer {
            background-color: var(--primary);
            color: white;
            text-align: center;
            padding: 20px 0;
            margin-top: 60px;
        }
        
        @media (max-width: 768px) {
            .header-content {
                flex-direction: column;
                gap: 20px;
            }
            
            nav ul {
                flex-direction: column;
                align-items: center;
                gap: 10px;
            }
            
            .about-content {
                flex-direction: column;
            }
            
            .hero h1 {
                font-size: 2rem;
            }
            
            .hero p {
                font-size: 1rem;
            }
            
            .section {
                padding: 40px 0;
            }
            
            .section-title {
                font-size: 1.8rem;
                margin-bottom: 30px;
            }
        }
    </style>
</head>
<body>
    <header>
        <div class="container header-content">
            <a href="#" class="logo">
                <i class="fab fa-github"></i>
                <span>MyGitHub</span>
            </a>
            <nav>
                <ul>
                    <li><a href="#home">Home</a></li>
                    <li><a href="#about">About</a></li>
                    <li><a href="#skills">Skills</a></li>
                    <li><a href="#projects">Projects</a></li>
                    <li><a href="#contact">Contact</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <section class="hero" id="home">
        <div class="container">
            <img src="fotoku.jpg" alt="Profile photo of a professional software developer standing in front of a computer workspace">
            <h1>Halo, Saya [Saufika1211]</h1>
            <p>Seorang Developer yang berfokus pada pembuatan solusi digital yang indah dan fungsional.</p>
            <div class="social-links">
                <a href="#"><i class="fab fa-github"></i></a>
                <a href="#"><i class="fab fa-linkedin-in"></i></a>
                <a href="#"><i class="fab fa-twitter"></i></a>
                <a href="#"><i class="fab fa-instagram"></i></a>
            </div>
        </div>
    </section>

    <section class="section" id="about">
        <div class="container">
            <h2 class="section-title">Tentang Saya</h2>
            <div class="about-content">
                <div class="about-text">
                    <h3>Perkenalkan diri Anda disini</h3>
                    <p>Saya adalah seorang developer yang passionate dengan teknologi dan selalu ingin mempelajari hal baru. Saya telah bekerja di industri ini selama beberapa tahun dan telah menyelesaikan berbagai proyek menarik.</p>
                    <p>Ketika tidak coding, saya suka membaca buku, menonton film, atau menjelajahi tempat-tempat baru.</p>
                    <p>Saya juga aktif berkontribusi di berbagai proyek open source dan senang berbagi pengetahuan dengan komunitas developer.</p>
                </div>
                <div class="skills">
                    <div class="skill-item">
                        <i class="fab fa-html5"></i>
                        <p>HTML5</p>
                    </div>
                    <div class="skill-item">
                        <i class="fab fa-css3-alt"></i>
                        <p>CSS3</p>
                    </div>
                    <div class="skill-item">
                        <i class="fab fa-js"></i>
                        <p>JavaScript</p>
                    </div>
                    <div class="skill-item">
                        <i class="fab fa-react"></i>
                        <p>React</p>
                    </div>
                    <div class="skill-item">
                        <i class="fab fa-node-js"></i>
                        <p>Node.js</p>
                    </div>
                    <div class="skill-item">
                        <i class="fab fa-git-alt"></i>
                        <p>Git</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <section class="section projects" id="projects">
        <div class="container">
            <h2 class="section-title">Proyek Terbaru</h2>
            <div class="project-grid">
                <div class="project-card">
                    <div class="project-image">
                        <img src="fotoku.jpg" alt="Screenshot of E-commerce website with modern design and product showcase">
                    </div>
                    <div class="project-info">
                        <h3>Website E-commerce</h3>
                        <p>Sebuah platform e-commerce dengan fitur lengkap termasuk keranjang belanja, sistem pembayaran, dan manajemen produk.</p>
                        <div class="project-links">
                            <a href="#" class="code-link">Source Code</a>
                            <a href="#" class="live-link">Live Demo</a>
                        </div>
                    </div>
                </div>
                
                <div class="project-card">
                    <div class="project-image">
                        <img src="https://placehold.co/600x400" alt="Dashboard analytics interface with charts and data visualization">
                    </div>
                    <div class="project-info">
                        <h3>Dashboard Analytics</h3>
                        <p>Sistem dashboard untuk memvisualisasikan data dengan berbagai chart dan laporan interaktif.</p>
                        <div class="project-links">
                            <a href="#" class="code-link">Source Code</a>
                            <a href="#" class="live-link">Live Demo</a>
                        </div>
                    </div>
                </div>
                
                <div class="project-card">
                    <div class="project-image">
                        <img src="https://placehold.co/600x400" alt="Mobile application screenshot showing social media feed interface">
                    </div>
                    <div class="project-info">
                        <h3>Aplikasi Mobile</h3>
                        <p>Aplikasi sosial media dengan fitur posting, komentar, dan sistem notifikasi real-time.</p>
                        <div class="project-links">
                            <a href="#" class="code-link">Source Code</a>
                            <a href="#" class="live-link">Live Demo</a>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <section class="section contact" id="contact">
        <div class="container">
            <h2 class="section-title">Hubungi Saya</h2>
            <div class="contact-form">
                <form id="contactForm">
                    <div class="form-group">
                        <label for="name">Nama</label>
                        <input type="text" id="name" name="name" required>
                    </div>
                    <div class="form-group">
                        <label for="email">Email</label>
                        <input type="email" id="email" name="email" required>
                    </div>
                    <div class="form-group">
                        <label for="message">Pesan</label>
                        <textarea id="message" name="message" rows="5" required></textarea>
                    </div>
                    <button type="submit" class="submit-btn">Kirim Pesan</button>
                </form>
            </div>
        </div>
    </section>

    <footer>
        <div class="container">
            <p>&copy; 2023 MyGitHub Profile. All rights reserved.</p>
        </div>
    </footer>

    <script>
        // Smooth scrolling for navigation links
        document.querySelectorAll('nav a').forEach(anchor => {
            anchor.addEventListener('click', function(e) {
                e.preventDefault();
                
                const targetId = this.getAttribute('href');
                const targetElement = document.querySelector(targetId);
                
                window.scrollTo({
                    top: targetElement.offsetTop - 80,
                    behavior: 'smooth'
                });
            });
        });
        
        // Form submission handling
        const contactForm = document.getElementById('contactForm');
        contactForm.addEventListener('submit', function(e) {
            e.preventDefault();
            
            const name = document.getElementById('name').value;
            const email = document.getElementById('email').value;
            const message = document.getElementById('message').value;
            
            // Here you would normally send the form data to a server
            console.log('Form submitted:', { name, email, message });
            
            alert('Terima kasih! Pesan Anda telah terkirim. Saya akan segera menghubungi Anda.');
            contactForm.reset();
        });
    </script>
</body>
</html>
