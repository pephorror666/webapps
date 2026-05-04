<html lang="es">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>IARANN | We Forge Heavy Code</title>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500&family=Outfit:wght@300;600;800&display=swap"
        rel="stylesheet">
    <style>
        :root {
            --bg: #050505;
            --surface: #121214;
            --surface-hover: #1c1c1f;
            --text: #ffffff;
            --text-muted: #8e8e93;
            --primary: #a855f7;
            --border: rgba(255, 255, 255, 0.06);
            --font-main: 'Inter', sans-serif;
            --font-heading: 'Outfit', sans-serif;
        }

        h1 {opacity: 0.0;}
        
        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
            -webkit-tap-highlight-color: transparent;
        }

        body {
            font-family: var(--font-main);
            background-color: var(--bg);
            color: var(--text);
            line-height: 1.4;
            padding-bottom: 40px;
        }

        /* Fondo sutil */
        .glow {
            position: fixed;
            top: 0;
            left: 50%;
            transform: translateX(-50%);
            width: 100%;
            height: 300px;
            background: radial-gradient(circle, rgba(168, 85, 247, 0.08) 0%, transparent 70%);
            z-index: -1;
            pointer-events: none;
        }

        .container {
            max-width: 600px;
            margin: 0 auto;
            padding: 20px;
        }

        header {
            text-align: center;
            padding: 40px 0 30px 0;
        }

        .logo {
            font-family: var(--font-heading);
            font-size: 2.8rem;
            font-weight: 800;
            letter-spacing: -1px;
            color: #fff;
            margin-bottom: 4px;
        }

        .tagline {
            font-family: var(--font-heading);
            font-size: 0.85rem;
            color: var(--text-muted);
            text-transform: uppercase;
            letter-spacing: 4px;
            font-weight: 300;
            border-left: 1px solid #333;
            padding-left: 15px;
            margin-left: 15px;
            display: inline-block;
        }

        .section-title {
            font-family: var(--font-heading);
            font-size: 1.1rem;
            font-weight: 600;
            color: var(--text);
            margin: 30px 0 15px 5px;
            display: flex;
            align-items: center;
            opacity: 0.9;
        }

        .app-list {
            display: flex;
            flex-direction: column;
            gap: 2px;
            /* Espacio mínimo entre filas */
            background: var(--surface);
            border-radius: 18px;
            overflow: hidden;
            border: 1px solid var(--border);
        }

        .app-item {
            display: flex;
            align-items: center;
            padding: 14px 16px;
            text-decoration: none;
            color: inherit;
            transition: background 0.2s ease;
            position: relative;
        }

        .app-item:not(:last-child)::after {
            content: '';
            position: absolute;
            bottom: 0;
            right: 0;
            left: 70px;
            /* Alineado con el inicio del texto */
            height: 1px;
            background: var(--border);
        }

        .app-item:active {
            background-color: var(--surface-hover);
        }

        @media (hover: hover) {
            .app-item:hover {
                background-color: var(--surface-hover);
            }
        }

        .app-icon {
            width: 42px;
            height: 42px;
            background: rgba(255, 255, 255, 0.03);
            border: 1px solid rgba(255, 255, 255, 0.05);
            border-radius: 10px;
            display: flex;
            align-items: center;
            justify-content: center;
            color: var(--primary);
            margin-right: 14px;
            flex-shrink: 0;
        }

        .app-content {
            flex-grow: 1;
            min-width: 0;
            /* Para truncado de texto si fuera necesario */
        }

        .app-content h4 {
            font-family: var(--font-heading);
            font-size: 1.05rem;
            font-weight: 600;
            margin-bottom: 2px;
            color: #fff;
        }

        .app-content p {
            font-size: 0.85rem;
            color: var(--text-muted);
            white-space: nowrap;
            overflow: hidden;
            text-overflow: ellipsis;
        }

        .chevron {
            color: #3a3a3c;
            margin-left: 10px;
        }

        footer {
            text-align: center;
            padding: 50px 0 20px;
            color: #444;
            font-size: 0.75rem;
            font-family: var(--font-heading);
            letter-spacing: 1px;
        }

        /* Ajustes para móviles muy pequeños */
        @media (max-width: 370px) {
            .logo {
                font-size: 2.2rem;
            }

            .app-content p {
                display: none;
            }

            /* Ocultar descripción en pantallas mínimas */
        }
    </style>
</head>

<body>
    <div class="glow"></div>

    <div class="container">
        <header>
            <div class="logo">IARANN</div>
            <div class="tagline">We forge heavy code</div>
        </header>

        <div class="section-title">Tools & Utilities</div>
        <div class="app-list">
            <a href="./dathail/" target="_blank" class="app-item">
                <div class="app-icon">
                    <svg viewBox="0 0 24 24" width="22" height="22" fill="none" stroke="currentColor" stroke-width="2"
                        stroke-linecap="round" stroke-linejoin="round">
                        <path d="M12 22C6.477 22 2 17.523 2 12S6.477 2 12 2a10 10 0 0 1 10 10c0 1.1-.9 2-2 2h-2.15a1 1 0 0 0-.8.4 1 1 0 0 0-.2.83 1.5 1.5 0 0 1-1.45 1.77H12"></path>
                        <circle cx="7.5" cy="10.5" r=".5" fill="currentColor"></circle>
                        <circle cx="12" cy="7" r=".5" fill="currentColor"></circle>
                        <circle cx="16.5" cy="10.5" r=".5" fill="currentColor"></circle>
                    </svg>
                </div>
                <div class="app-content">
                    <h4>Dathail</h4>
                    <p>Minimalist color palette generator for crafting harmonious and accessible design schemes.</p>
                </div>
                <div class="chevron">
                    <svg width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
                        <path d="M9 18l6-6-6-6" />
                    </svg>
                </div>
            </a>
            
            <a href="./dictio/" target="_blank" class="app-item">
                <div class="app-icon">
                    <svg viewBox="0 0 24 24" width="22" height="22" fill="none" stroke="currentColor" stroke-width="2"
                        stroke-linecap="round" stroke-linejoin="round">
                        <path d="M4 19.5A2.5 2.5 0 0 1 6.5 17H20"></path>
                        <path d="M6.5 2H20v20H6.5A2.5 2.5 0 0 1 4 19.5v-15A2.5 2.5 0 0 1 6.5 2z"></path>
                    </svg>
                </div>
                <div class="app-content">
                    <h4>Dictio</h4>
                    <p>An English dictionary with synonyms and writing tools.</p>
                </div>
                <div class="chevron">
                    <svg width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
                        <path d="M9 18l6-6-6-6" />
                    </svg>
                </div>
            </a>

            <a href="./markdown-editor/" target="_blank" class="app-item">
                <div class="app-icon">
                    <svg viewBox="0 0 24 24" width="22" height="22" fill="none" stroke="currentColor" stroke-width="2"
                        stroke-linecap="round" stroke-linejoin="round">
                        <path d="M11 4H4a2 2 0 0 0-2 2v14a2 2 0 0 0 2 2h14a2 2 0 0 0 2-2v-7"></path>
                        <path d="M18.5 2.5a2.121 2.121 0 0 1 3 3L12 15l-4 1 1-4 9.5-9.5z"></path>
                    </svg>
                </div>
                <div class="app-content">
                    <h4>Markdown Studio</h4>
                    <p>Editor Markdown profesional con previsualización en tiempo real.</p>
                </div>
                <div class="chevron">
                    <svg width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
                        <path d="M9 18l6-6-6-6" />
                    </svg>
                </div>
            </a>

            <a href="./maths/" target="_blank" class="app-item">
                <div class="app-icon">
                    <svg viewBox="0 0 24 24" width="22" height="22" fill="none" stroke="currentColor" stroke-width="2"
                        stroke-linecap="round" stroke-linejoin="round">
                        <line x1="7" y1="12" x2="17" y2="12"></line>
                        <line x1="7" y1="16" x2="17" y2="16"></line>
                        <line x1="12" y1="7" x2="12" y2="17"></line>
                        <line x1="7" y1="7" x2="17" y2="17"></line>
                    </svg>
                </div>
                <div class="app-content">
                    <h4>Mathjs</h4>
                    <p>Computación numérica avanzada y operaciones de matrices.</p>
                </div>
                <div class="chevron">
                    <svg width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
                        <path d="M9 18l6-6-6-6" />
                    </svg>
                </div>
            </a>

            <a href="./notter/" target="_blank" class="app-item">
                <div class="app-icon">
                    <svg viewBox="0 0 24 24" width="22" height="22" fill="none" stroke="currentColor" stroke-width="2"
                        stroke-linecap="round" stroke-linejoin="round">
                        <path d="M21 15a2 2 0 0 1-2 2H7l-4 4V5a2 2 0 0 1 2-2h14a2 2 0 0 1 2 2z"></path>
                    </svg>
                </div>
                <div class="app-content">
                    <h4>Notter</h4>
                    <p>Micro-notas rápidas guardadas en almacenamiento local.</p>
                </div>
                <div class="chevron">
                    <svg width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
                        <path d="M9 18l6-6-6-6" />
                    </svg>
                </div>
            </a>
        </div>

        <div class="section-title">Music Experience</div>
        <div class="app-list">
            <a href="./ipod/" target="_blank" class="app-item">
                <div class="app-icon">
                    <svg viewBox="0 0 24 24" width="22" height="22" fill="none" stroke="currentColor" stroke-width="2"
                        stroke-linecap="round" stroke-linejoin="round">
                        <path d="M9 18V5l12-2v13"></path>
                        <circle cx="6" cy="18" r="3"></circle>
                        <circle cx="18" cy="16" r="3"></circle>
                    </svg>
                </div>
                <div class="app-content">
                    <h4>iPod Classic</h4>
                    <p>Reproductor retro con la mítica rueda de navegación.</p>
                </div>
                <div class="chevron">
                    <svg width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
                        <path d="M9 18l6-6-6-6" />
                    </svg>
                </div>
            </a>
        </div>

        <div class="section-title">Interactive Games</div>
        <div class="app-list">
            <a href="./games/surfer.html" target="_blank" class="app-item">
                <div class="app-icon">
                    <svg viewBox="0 0 24 24" width="22" height="22" fill="none" stroke="currentColor" stroke-width="2"
                        stroke-linecap="round" stroke-linejoin="round">
                        <path
                            d="M2 18c.6.5 1.2 1 2.5 1 2.5 0 2.5-2 5-2 2.5 0 2.5 2 5 2 2.5 0 2.5-2 5-2 1.3 0 1.9.5 2.5 1">
                        </path>
                        <path
                            d="M2 12c.6.5 1.2 1 2.5 1 2.5 0 2.5-2 5-2 2.5 0 2.5 2 5 2 2.5 0 2.5-2 5-2 1.3 0 1.9.5 2.5 1">
                        </path>
                    </svg>
                </div>
                <div class="app-content">
                    <h4>Surfer</h4>
                    <p>Esquiva criaturas marinas en este juego de surf retro.</p>
                </div>
                <div class="chevron">
                    <svg width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
                        <path d="M9 18l6-6-6-6" />
                    </svg>
                </div>
            </a>
        </div>

        <footer>
            &copy; 2026 IARANN<br>
        </footer>
    </div>
</body>

</html>
