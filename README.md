<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>About Me | Обо мне</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            padding: 20px;
        }

        .container {
            background: white;
            border-radius: 20px;
            box-shadow: 0 20px 60px rgba(0, 0, 0, 0.3);
            max-width: 800px;
            width: 100%;
            overflow: hidden;
        }

        .header {
            background: linear-gradient(135deg, #2c3e50 0%, #3498db 100%);
            color: white;
            padding: 40px;
            text-align: center;
        }

        .header h1 {
            font-size: 2.5em;
            margin-bottom: 10px;
        }

        .header p {
            font-size: 1.2em;
            opacity: 0.9;
        }

        .lang-switch {
            display: flex;
            justify-content: center;
            gap: 10px;
            margin-top: 20px;
        }

        .lang-btn {
            padding: 10px 25px;
            border: 2px solid white;
            background: transparent;
            color: white;
            border-radius: 25px;
            cursor: pointer;
            font-size: 1em;
            transition: all 0.3s ease;
        }

        .lang-btn:hover {
            background: white;
            color: #2c3e50;
        }

        .lang-btn.active {
            background: white;
            color: #2c3e50;
        }

        .content {
            padding: 40px;
        }

        .section {
            margin-bottom: 30px;
        }

        .section h2 {
            color: #2c3e50;
            font-size: 1.5em;
            margin-bottom: 15px;
            border-bottom: 3px solid #3498db;
            padding-bottom: 10px;
            display: inline-block;
        }

        .section p {
            color: #555;
            line-height: 1.8;
            font-size: 1.1em;
        }

        .tech-stack {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
            margin-top: 15px;
        }

        .tech-badge {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            padding: 8px 16px;
            border-radius: 20px;
            font-size: 0.9em;
        }

        .repo-section {
            background: linear-gradient(135deg, #f5f7fa 0%, #c3cfe2 100%);
            border-radius: 15px;
            padding: 25px;
            margin-top: 20px;
        }

        .repo-card {
            background: white;
            border-radius: 10px;
            padding: 20px;
            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }

        .repo-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 8px 25px rgba(0, 0, 0, 0.15);
        }

        .repo-name {
            font-size: 1.3em;
            color: #2c3e50;
            margin-bottom: 10px;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .repo-name svg {
            width: 24px;
            height: 24px;
            fill: #2c3e50;
        }

        .repo-description {
            color: #555;
            line-height: 1.6;
            margin-bottom: 15px;
        }

        .repo-stats {
            display: flex;
            gap: 20px;
            flex-wrap: wrap;
        }

        .stat-item {
            display: flex;
            align-items: center;
            gap: 5px;
            color: #666;
            font-size: 0.9em;
        }

        .stat-item svg {
            width: 18px;
            height: 18px;
            fill: #666;
        }

        .stats-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
            gap: 20px;
            margin-top: 20px;
        }

        .stat-card {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            padding: 25px;
            border-radius: 15px;
            text-align: center;
            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.2);
            transition: transform 0.3s ease;
        }

        .stat-card:hover {
            transform: scale(1.05);
        }

        .stat-number {
            font-size: 2.5em;
            font-weight: bold;
            margin-bottom: 5px;
        }

        .stat-label {
            font-size: 0.9em;
            opacity: 0.9;
        }

        .btn-link {
            display: inline-block;
            background: #2c3e50;
            color: white;
            padding: 10px 20px;
            border-radius: 8px;
            text-decoration: none;
            margin-top: 15px;
            transition: background 0.3s ease;
        }

        .btn-link:hover {
            background: #34495e;
        }

        .contact-links {
            display: flex;
            gap: 15px;
            margin-top: 15px;
        }

        .contact-link {
            background: #3498db;
            color: white;
            padding: 10px 20px;
            border-radius: 8px;
            text-decoration: none;
            transition: background 0.3s ease;
        }

        .contact-link:hover {
            background: #2980b9;
        }

        .hidden {
            display: none;
        }

        @media (max-width: 600px) {
            .header h1 {
                font-size: 1.8em;
            }

            .content {
                padding: 20px;
            }

            .contact-links {
                flex-direction: column;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="header">
            <h1 id="name">Welcome!</h1>
            <p id="title">Frontend Developer</p>
            <div class="lang-switch">
                <button class="lang-btn active" onclick="switchLang('en')">English</button>
                <button class="lang-btn" onclick="switchLang('ru')">Русский</button>
            </div>
        </div>

        <div class="content">
            <!-- English Content -->
            <div id="en-content">
                <div class="section">
                    <h2>About Me</h2>
                    <p>
                        Hello! I'm a passionate Frontend Developer with expertise in modern web technologies. 
                        I love creating beautiful, responsive, and user-friendly websites and applications. 
                        My goal is to deliver high-quality code and exceptional user experiences.
                    </p>
                </div>

                <div class="section">
                    <h2>Tech Stack</h2>
                    <div class="tech-stack">
                        <span class="tech-badge">HTML5</span>
                        <span class="tech-badge">CSS3</span>
                        <span class="tech-badge">JavaScript</span>
                        <span class="tech-badge">TypeScript</span>
                        <span class="tech-badge">Vue.js</span>
                        <span class="tech-badge">Nuxt</span>
                        <span class="tech-badge">React.js</span>
                        <span class="tech-badge">Next.js</span>
                        <span class="tech-badge">TailwindCSS</span>
                        <span class="tech-badge">Sass</span>
                        <span class="tech-badge">Vite</span>
                        <span class="tech-badge">Git</span>
                    </div>
                </div>

                <div class="section">
                    <h2>Contact</h2>
                    <p>I'm always open to new opportunities and collaborations. Feel free to reach out!</p>
                    <div class="contact-links">
                        <a href="mailto:your.email@example.com" class="contact-link">Email</a>
                        <a href="https://github.com/yourusername" class="contact-link" target="_blank">GitHub</a>
                        <a href="https://linkedin.com/in/yourusername" class="contact-link" target="_blank">LinkedIn</a>
                    </div>
                </div>
            </div>

            <!-- Russian Content -->
            <div id="ru-content" class="hidden">
                <div class="section">
                    <h2>Обо мне</h2>
                    <p>
                        Привет! Я увлечённый Frontend-разработчик с экспертизой в современных веб-технологиях. 
                        Я люблю создавать красивые, адаптивные и удобные сайты и приложения. 
                        Моя цель — писать качественный код и обеспечивать превосходный пользовательский опыт.
                    </p>
                </div>

                <div class="section">
                    <h2>Технологии</h2>
                    <div class="tech-stack">
                        <span class="tech-badge">HTML5</span>
                        <span class="tech-badge">CSS3</span>
                        <span class="tech-badge">JavaScript</span>
                        <span class="tech-badge">TypeScript</span>
                        <span class="tech-badge">Vue.js</span>
                        <span class="tech-badge">Nuxt</span>
                        <span class="tech-badge">React.js</span>
                        <span class="tech-badge">Next.js</span>
                        <span class="tech-badge">TailwindCSS</span>
                        <span class="tech-badge">Sass</span>
                        <span class="tech-badge">Vite</span>
                        <span class="tech-badge">Git</span>
                    </div>
                </div>

                <div class="section">
                    <h2>Контакты</h2>
                    <p>Я всегда открыт для новых возможностей и сотрудничества. Не стесняйтесь связаться со мной!</p>
                    <div class="contact-links">
                        <a href="mailto:your.email@example.com" class="contact-link">Email</a>
                        <a href="https://github.com/yourusername" class="contact-link" target="_blank">GitHub</a>
                        <a href="https://linkedin.com/in/yourusername" class="contact-link" target="_blank">LinkedIn</a>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <script>
        function switchLang(lang) {
            const enContent = document.getElementById('en-content');
            const ruContent = document.getElementById('ru-content');
            const buttons = document.querySelectorAll('.lang-btn');
            const name = document.getElementById('name');
            const title = document.getElementById('title');

            if (lang === 'en') {
                enContent.classList.remove('hidden');
                ruContent.classList.add('hidden');
                buttons[0].classList.add('active');
                buttons[1].classList.remove('active');
                name.textContent = 'Welcome!';
                title.textContent = 'Frontend Developer';
            } else {
                enContent.classList.add('hidden');
                ruContent.classList.remove('hidden');
                buttons[0].classList.remove('active');
                buttons[1].classList.add('active');
                name.textContent = 'Добро пожаловать!';
                title.textContent = 'Frontend Разработчик';
            }
        }
    </script>
</body>
</html>
