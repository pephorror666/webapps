<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=0.8">
    <title>IARANN | We Forge Heavy Code</title>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link
        href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600&family=Outfit:wght@300;600;800&display=swap"
        rel="stylesheet">
    <style>
        h1 {opacity: 0.0;}
        
        :root {
            --bg: #0a0a0c;
            --surface: #141417;
            --surface-hover: #1c1c21;
            --text: #f0f0f2;
            --text-muted: #9494a1;
            --primary: #8b5cf6;
            --primary-glow: rgba(139, 92, 246, 0.2);
            --accent: #06b6d4;
            --border: rgba(255, 255, 255, 0.08);
            --font-main: 'Inter', sans-serif;
            --font-heading: 'Outfit', sans-serif;
            --transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
        }

        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }

        body {
            font-family: var(--font-main);
            background-color: var(--bg);
            color: var(--text);
            line-height: 1.6;
            overflow-x: hidden;
        }

        /* Background effects */
        .glow-bg {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: -1;
            overflow: hidden;
            pointer-events: none;
        }

        .glow-1 {
            position: absolute;
            top: -10%;
            right: -10%;
            width: 50%;
            height: 50%;
            background: radial-gradient(circle, var(--primary-glow) 0%, transparent 70%);
            filter: blur(80px);
        }

        .glow-2 {
            position: absolute;
            bottom: -10%;
            left: -10%;
            width: 40%;
            height: 40%;
            background: radial-gradient(circle, rgba(6, 182, 212, 0.1) 0%, transparent 70%);
            filter: blur(80px);
        }

        .container {
            max-width: 1100px;
            margin: 0 auto;
            padding: 40px 20px;
        }

        header {
            margin-bottom: 80px;
            text-align: center;
        }

        .logo {
            font-family: var(--font-heading);
            font-size: 3.5rem;
            font-weight: 800;
            letter-spacing: -2px;
            background: linear-gradient(135deg, #fff 0%, #888 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            margin-bottom: 10px;
            display: inline-block;
        }

        .tagline {
            font-family: var(--font-heading);
            font-size: 1.2rem;
            color: var(--text-muted);
            text-transform: uppercase;
            letter-spacing: 4px;
            font-weight: 300;
        }

        .hero {
            margin-bottom: 100px;
            max-width: 800px;
            margin-left: auto;
            margin-right: auto;
            text-align: center;
        }

        .hero h3 {
            font-family: var(--font-heading);
            font-size: 2rem;
            margin-bottom: 20px;
            color: var(--text);
        }

        .hero p {
            font-size: 1.1rem;
            color: var(--text-muted);
            font-weight: 300;
            line-height: 1.8;
        }

        .section-title {
            font-family: var(--font-heading);
            font-size: 1.5rem;
            margin-bottom: 30px;
            display: flex;
            align-items: center;
            gap: 15px;
        }

        .section-title::after {
            content: '';
            height: 1px;
            flex-grow: 1;
            background: var(--border);
        }

        .grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(320px, 1fr));
            gap: 25px;
            margin-bottom: 60px;
        }

        .card {
            background-color: var(--surface);
            border: 1px solid var(--border);
            border-radius: 16px;
            padding: 30px;
            text-decoration: none;
            color: inherit;
            transition: var(--transition);
            display: flex;
            flex-direction: column;
            gap: 20px;
            position: relative;
            overflow: hidden;
        }

        .card:hover {
            transform: translateY(-5px);
            border-color: var(--primary);
            background-color: var(--surface-hover);
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.4);
        }

        .card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(135deg, var(--primary) 0%, transparent 100%);
            opacity: 0;
            transition: var(--transition);
            z-index: 0;
        }

        .card:hover::before {
            opacity: 0.05;
        }

        .card-icon {
            width: 50px;
            height: 50px;
            background: rgba(255, 255, 255, 0.03);
            border-radius: 12px;
            display: flex;
            align-items: center;
            justify-content: center;
            color: var(--primary);
            transition: var(--transition);
        }

        .card:hover .card-icon {
            background: var(--primary);
            color: #fff;
            transform: scale(1.1) rotate(5deg);
        }

        .card-content h4 {
            font-family: var(--font-heading);
            font-size: 1.4rem;
            margin-bottom: 8px;
            color: #fff;
        }

        .card-content p {
            font-size: 0.95rem;
            color: var(--text-muted);
            line-height: 1.5;
        }

        .card-arrow {
            margin-top: auto;
            display: flex;
            align-items: center;
            gap: 8px;
            font-size: 0.85rem;
            font-weight: 600;
            color: var(--primary);
            opacity: 0;
            transform: translateX(-10px);
            transition: var(--transition);
        }

        .card:hover .card-arrow {
            opacity: 1;
            transform: translateX(0);
        }

        footer {
            text-align: center;
            padding: 40px 0;
            border-top: 1px solid var(--border);
            color: var(--text-muted);
            font-size: 0.9rem;
            margin-top: 40px;
        }

        @media (max-width: 768px) {
            .logo {
                font-size: 2.5rem;
            }

            .grid {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>

<body>
    <div class="glow-bg">
        <div class="glow-1"></div>
        <div class="glow-2"></div>
    </div>

    <div class="container">
        <header>
            <div class="logo">IARANN</div>
            <div class="tagline">We forge heavy code</div>
        </header>

        <section class="hero">
            <h3>About</h3>
            <p>
                I build simple apps for fun—and to learn. This site is a small portfolio of those projects. I call it
                IARANN (a Scottish Gaelic word for “iron”) because I love programming, metal music, and Scotland.
                Friendly, useful tools—made by me, shared with you.
            </p>
        </section>

        <div class="section-title">Tools & Utilities</div>
        <div class="grid">
            <a href="./dictio/" target="_blank" rel="noopener noreferrer" class="card">
                <div class="card-icon">
                    <svg viewBox="0 0 24 24" width="24" height="24" fill="none" stroke="currentColor" stroke-width="2">
                        <path d="M4 19.5A2.5 2.5 0 0 1 6.5 17H20"></path>
                        <path d="M6.5 2H20v20H6.5A2.5 2.5 0 0 1 4 19.5v-15A2.5 2.5 0 0 1 6.5 2z"></path>
                    </svg>
                </div>
                <div class="card-content">
                    <h4>Dictio</h4>
                    <p>Advanced English dictionary with synonyms, antonyms, and writer's tools.</p>
                </div>
                <div class="card-arrow">Launch App &rarr;</div>
            </a>

            <a href="./markdown-editor/" target="_blank" rel="noopener noreferrer" class="card">
                <div class="card-icon">
                    <svg viewBox="0 0 24 24" width="24" height="24" fill="none" stroke="currentColor" stroke-width="2">
                        <path d="M11 4H4a2 2 0 0 0-2 2v14a2 2 0 0 0 2 2h14a2 2 0 0 0 2-2v-7"></path>
                        <path d="M18.5 2.5a2.121 2.121 0 0 1 3 3L12 15l-4 1 1-4 9.5-9.5z"></path>
                    </svg>
                </div>
                <div class="card-content">
                    <h4>Markdown Studio</h4>
                    <p>Create, edit, and save beautiful markdown documents with real-time preview.</p>
                </div>
                <div class="card-arrow">Launch App &rarr;</div>
            </a>

            <a href="./mathjs/" target="_blank" rel="noopener noreferrer" class="card">
                <div class="card-icon">
                    <svg viewBox="0 0 24 24" width="24" height="24" fill="none" stroke="currentColor" stroke-width="2">
                        <rect x="4" y="2" width="16" height="20" rx="2" ry="2"></rect>
                        <line x1="8" y1="6" x2="16" y2="6"></line>
                        <line x1="16" y1="14" x2="16" y2="18"></line>
                        <line x1="8" y1="14" x2="8" y2="18"></line>
                        <line x1="12" y1="14" x2="12" y2="18"></line>
                        <line x1="16" y1="10" x2="16" y2="10"></line>
                        <line x1="12" y1="10" x2="12" y2="10"></line>
                        <line x1="8" y1="10" x2="8" y2="10"></line>
                    </svg>
                </div>
                <div class="card-content">
                    <h4>Mathjs</h4>
                    <p>Powerful system for numeric computation, calculation, and matrix operations.</p>
                </div>
                <div class="card-arrow">Launch App &rarr;</div>
            </a>
        </div>

        <div class="section-title">Music Experience</div>
        <div class="grid">
            <a href="./ipod/" target="_blank" rel="noopener noreferrer" class="card">
                <div class="card-icon">
                    <svg viewBox="0 0 24 24" width="24" height="24" fill="none" stroke="currentColor" stroke-width="2">
                        <path d="M9 18V5l12-2v13"></path>
                        <circle cx="6" cy="18" r="3"></circle>
                        <circle cx="18" cy="16" r="3"></circle>
                    </svg>
                </div>
                <div class="card-content">
                    <h4>iPod Classic</h4>
                    <p>A retro-inspired music player that brings back the classic wheel experience.</p>
                </div>
                <div class="card-arrow">Launch App &rarr;</div>
            </a>
        </div>

        <div class="section-title">Interactive Games</div>
        <div class="grid">
            <a href="./games/surfer.html" target="_blank" rel="noopener noreferrer" class="card">
                <div class="card-icon">
                    <svg viewBox="0 0 24 24" width="24" height="24" fill="none" stroke="currentColor" stroke-width="2">
                        <path d="M2 6c.6.5 1.2 1 2.5 1C7 7 7 5 9.5 5c2.5 0 2.5 2 5 2 2.5 0 2.5-2 5-2 1.3 0 1.9.5 2.5 1">
                        </path>
                        <path
                            d="M2 12c.6.5 1.2 1 2.5 1 2.5 0 2.5-2 5-2 2.5 0 2.5 2 5 2 2.5 0 2.5-2 5-2 1.3 0 1.9.5 2.5 1">
                        </path>
                        <path
                            d="M2 18c.6.5 1.2 1 2.5 1 2.5 0 2.5-2 5-2 2.5 0 2.5 2 5 2 2.5 0 2.5-2 5-2 1.3 0 1.9.5 2.5 1">
                        </path>
                    </svg>
                </div>
                <div class="card-content">
                    <h4>Surfer</h4>
                    <p>Test your reflexes in this retro-styled surfing game. Survive the sea creatures!</p>
                </div>
                <div class="card-arrow">Launch App &rarr;</div>
            </a>
        </div>

        <footer>
            &copy; 2024 IARANN. Built with class and minimalism.
        </footer>
    </div>
</body>

</html>
