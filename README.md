<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>GitHub Profile README</title>
    <style>
        :root {
            --primary-color: #2d4cc8;
            --secondary-color: #6e40c9;
            --accent-color: #ff4f7e;
            --text-color: #24292e;
            --bg-color: #ffffff;
            --card-bg: #f6f8fa;
            --shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        body {
            background-color: #f0f0f0;
            color: var(--text-color);
            line-height: 1.6;
            padding: 20px;
            max-width: 1200px;
            margin: 0 auto;
        }

        .github-profile {
            background: linear-gradient(135deg, var(--primary-color), var(--secondary-color));
            border-radius: 12px;
            padding: 30px;
            color: white;
            margin-bottom: 25px;
            box-shadow: var(--shadow);
            position: relative;
            overflow: hidden;
        }

        .github-profile::before {
            content: '';
            position: absolute;
            top: -50%;
            right: -50%;
            width: 100%;
            height: 200%;
            background: rgba(255, 255, 255, 0.1);
            transform: rotate(30deg);
        }

        .profile-header {
            display: flex;
            align-items: center;
            position: relative;
            z-index: 2;
        }

        .profile-image {
            width: 120px;
            height: 120px;
            border-radius: 50%;
            border: 4px solid rgba(255, 255, 255, 0.3);
            margin-right: 25px;
            object-fit: cover;
        }

        .profile-info h1 {
            font-size: 2.5rem;
            margin-bottom: 5px;
            font-weight: 700;
        }

        .profile-info p {
            font-size: 1.2rem;
            opacity: 0.9;
            margin-bottom: 15px;
        }

        .social-links {
            display: flex;
            gap: 15px;
            margin-top: 10px;
        }

        .social-links a {
            color: white;
            text-decoration: none;
            background: rgba(255, 255, 255, 0.2);
            padding: 8px 15px;
            border-radius: 20px;
            font-size: 0.9rem;
            transition: all 0.3s ease;
        }

        .social-links a:hover {
            background: rgba(255, 255, 255, 0.3);
            transform: translateY(-2px);
        }

        .stats-container {
            display: flex;
            gap: 20px;
            margin: 30px 0;
            flex-wrap: wrap;
        }

        .stat-card {
            background: var(--bg-color);
            border-radius: 10px;
            padding: 20px;
            flex: 1;
            min-width: 200px;
            box-shadow: var(--shadow);
            transition: transform 0.3s ease;
        }

        .stat-card:hover {
            transform: translateY(-5px);
        }

        .stat-card h3 {
            color: var(--primary-color);
            margin-bottom: 10px;
            font-size: 1.2rem;
        }

        .stat-card p {
            color: var(--text-color);
            font-size: 1.8rem;
            font-weight: bold;
        }

        .section-title {
            font-size: 1.8rem;
            margin: 40px 0 20px;
            color: var(--primary-color);
            position: relative;
            padding-bottom: 10px;
        }

        .section-title::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 60px;
            height: 4px;
            background: linear-gradient(to right, var(--primary-color), var(--accent-color));
            border-radius: 2px;
        }

        .skills-container {
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
            margin-bottom: 30px;
        }

        .skill {
            background: linear-gradient(to right, var(--primary-color), var(--secondary-color));
            color: white;
            padding: 8px 18px;
            border-radius: 20px;
            font-size: 0.9rem;
        }

        .projects-container {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 25px;
            margin-bottom: 40px;
        }

        .project-card {
            background: var(--bg-color);
            border-radius: 12px;
            overflow: hidden;
            box-shadow: var(--shadow);
            transition: transform 0.3s ease;
        }

        .project-card:hover {
            transform: translateY(-5px);
        }

        .project-image {
            width: 100%;
            height: 180px;
            object-fit: cover;
        }

        .project-content {
            padding: 20px;
        }

        .project-content h3 {
            margin-bottom: 10px;
            color: var(--primary-color);
        }

        .project-content p {
            color: var(--text-color);
            margin-bottom: 15px;
            font-size: 0.95rem;
        }

        .project-tags {
            display: flex;
            flex-wrap: wrap;
            gap: 8px;
            margin-bottom: 15px;
        }

        .tag {
            background: var(--card-bg);
            padding: 4px 10px;
            border-radius: 15px;
            font-size: 0.8rem;
            color: var(--secondary-color);
        }

        .project-link {
            display: inline-block;
            color: var(--primary-color);
            text-decoration: none;
            font-weight: 600;
            font-size: 0.9rem;
        }

        .project-link:hover {
            text-decoration: underline;
        }

        .contact-container {
            background: linear-gradient(135deg, var(--primary-color), var(--secondary-color));
            border-radius: 12px;
            padding: 30px;
            color: white;
            margin-bottom: 40px;
            box-shadow: var(--shadow);
        }

        .contact-container h2 {
            margin-bottom: 20px;
            font-size: 1.8rem;
        }

        .contact-links {
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
        }

        .contact-link {
            background: rgba(255, 255, 255, 0.2);
            color: white;
            text-decoration: none;
            padding: 12px 25px;
            border-radius: 8px;
            display: flex;
            align-items: center;
            gap: 10px;
            transition: all 0.3s ease;
        }

        .contact-link:hover {
            background: rgba(255, 255, 255, 0.3);
            transform: translateY(-3px);
        }

        footer {
            text-align: center;
            padding: 20px;
            color: var(--text-color);
            opacity: 0.7;
            font-size: 0.9rem;
        }

        @media (max-width: 768px) {
            .profile-header {
                flex-direction: column;
                text-align: center;
            }
            
            .profile-image {
                margin-right: 0;
                margin-bottom: 20px;
            }
            
            .social-links {
                justify-content: center;
            }
            
            .stats-container {
                flex-direction: column;
            }
        }
    </style>
</head>
<body>
    <div class="github-profile">
        <div class="profile-header">
            <img src="https://via.placeholder.com/120" alt="Profile Image" class="profile-image">
            <div class="profile-info">
                <h1>Ismingiz Familiyangiz</h1>
                <p>💻 Dasturchi / Web Developer</p>
                <div class="social-links">
                    <a href="#">Twitter</a>
                    <a href="#">LinkedIn</a>
                    <a href="#">Instagram</a>
                    <a href="#">Portfolio</a>
                </div>
            </div>
        </div>
    </div>

    <div class="stats-container">
        <div class="stat-card">
            <h3>GitHub Stars</h3>
            <p>256</p>
        </div>
        <div class="stat-card">
            <h3>Followers</h3>
            <p>1.2K</p>
        </div>
        <div class="stat-card">
            <h3>Following</h3>
            <p>87</p>
        </div>
        <div class="stat-card">
            <h3>Repositories</h3>
            <p>42</p>
        </div>
    </div>

    <h2 class="section-title">Mening Ko'nikmalarim</h2>
    <div class="skills-container">
        <div class="skill">JavaScript</div>
        <div class="skill">React</div>
        <div class="skill">Node.js</div>
        <div class="skill">Python</div>
        <div class="skill">HTML/CSS</div>
        <div class="skill">MongoDB</div>
        <div class="skill">Git</div>
        <div class="skill">Docker</div>
        <div class="skill">UI/UX Design</div>
    </div>

    <h2 class="section-title">Mening Loyihalarim</h2>
    <div class="projects-container">
        <div class="project-card">
            <img src="https://via.placeholder.com/300x180" alt="Project Image" class="project-image">
            <div class="project-content">
                <h3>Loyiha Nomi</h3>
                <p>Bu loyiha haqida qisqacha tavsif. Loyihaning asosiy funksiyalari va qanday texnologiyalar qo'llanganligi haqida.</p>
                <div class="project-tags">
                    <span class="tag">React</span>
                    <span class="tag">Node.js</span>
                    <span class="tag">MongoDB</span>
                </div>
                <a href="#" class="project-link">Loyihani ko'rish →</a>
            </div>
        </div>
        <div class="project-card">
            <img src="https://via.placeholder.com/300x180" alt="Project Image" class="project-image">
            <div class="project-content">
                <h3>Loyiha Nomi</h3>
                <p>Bu loyiha haqida qisqacha tavsif. Loyihaning asosiy funksiyalari va qanday texnologiyalar qo'llanganligi haqida.</p>
                <div class="project-tags">
                    <span class="tag">Vue.js</span>
                    <span class="tag">Express</span>
                    <span class="tag">PostgreSQL</span>
                </div>
                <a href="#" class="project-link">Loyihani ko'rish →</a>
            </div>
        </div>
        <div class="project-card">
            <img src="https://via.placeholder.com/300x180" alt="Project Image" class="project-image">
            <div class="project-content">
                <h3>Loyiha Nomi</h3>
                <p>Bu loyiha haqida qisqacha tavsif. Loyihaning asosiy funksiyalari va qanday texnologiyalar qo'llanganligi haqida.</p>
                <div class="project-tags">
                    <span class="tag">Python</span>
                    <span class="tag">Django</span>
                    <span class="tag">SQLite</span>
                </div>
                <a href="#" class="project-link">Loyihani ko'rish →</a>
            </div>
        </div>
    </div>

    <div class="contact-container">
        <h2>Bog'lanish</h2>
        <div class="contact-links">
            <a href="mailto:your.email@example.com" class="contact-link">
                <span>✉️ Email</span>
            </a>
            <a href="https://t.me/yourusername" class="contact-link">
                <span>📱 Telegram</span>
            </a>
            <a href="https://linkedin.com/in/yourusername" class="contact-link">
                <span>💼 LinkedIn</span>
            </a>
            <a href="https://github.com/yourusername" class="contact-link">
                <span>🐙 GitHub</span>
            </a>
        </div>
    </div>

    <footer>
        <p>© 2023 Ismingiz Familiyangiz. Barcha huquqlar himoyalangan.</p>
    </footer>
</body>
</html>
