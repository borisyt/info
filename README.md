<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Borisonchik · docs</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, sans-serif;
            background: #f8f9fc;
            color: #1e293b;
            line-height: 1.6;
            height: 100vh;
            display: flex;
        }

        /* === НАВИГАЦИЯ СЛЕВА (как в документации) === */
        .sidebar {
            width: 260px;
            background: #ffffff;
            border-right: 1px solid #e4e7ec;
            padding: 32px 16px;
            display: flex;
            flex-direction: column;
            box-shadow: 2px 0 12px rgba(0,0,0,0.02);
        }

        .logo {
            font-weight: 600;
            font-size: 1.5rem;
            letter-spacing: -0.5px;
            padding: 0 12px 24px 12px;
            border-bottom: 1px solid #edf0f5;
            margin-bottom: 24px;
            color: #0f1829;
        }

        .logo span {
            color: #2563eb;
            background: #e8f0fe;
            padding: 2px 8px;
            border-radius: 20px;
            font-size: 0.9rem;
            margin-left: 8px;
        }

        .nav-menu {
            display: flex;
            flex-direction: column;
            gap: 4px;
        }

        .nav-item {
            padding: 10px 14px;
            border-radius: 8px;
            font-size: 0.95rem;
            font-weight: 500;
            color: #475569;
            cursor: pointer;
            transition: all 0.1s;
            border: none;
            background: none;
            text-align: left;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .nav-item:hover {
            background: #f1f5f9;
            color: #1e293b;
        }

        .nav-item.active {
            background: #e8f0fe;
            color: #2563eb;
            font-weight: 500;
        }

        .nav-icon {
            font-size: 1.2rem;
            width: 24px;
            display: inline-block;
            color: #5f6b7a;
        }

        .nav-item.active .nav-icon {
            color: #2563eb;
        }

        /* === ОСНОВНОЙ КОНТЕНТ === */
        .content {
            flex: 1;
            padding: 40px 48px;
            overflow-y: auto;
            background: #ffffff;
        }

        .page {
            max-width: 800px;
            margin: 0 auto;
            display: none;
        }

        .page.active-page {
            display: block;
        }

        h1 {
            font-size: 2.2rem;
            font-weight: 600;
            letter-spacing: -0.02em;
            margin-bottom: 1rem;
            color: #0b1b33;
        }

        h2 {
            font-size: 1.5rem;
            font-weight: 600;
            margin: 2rem 0 1rem;
            padding-bottom: 0.5rem;
            border-bottom: 1px solid #e9edf2;
        }

        .lead {
            font-size: 1.2rem;
            color: #3a4b62;
            background: #f8fafd;
            padding: 16px 20px;
            border-radius: 12px;
            border-left: 4px solid #2563eb;
            margin: 24px 0;
        }

        .card-grid {
            display: flex;
            flex-direction: column;
            gap: 12px;
            margin: 20px 0;
        }

        .social-link {
            display: flex;
            align-items: center;
            gap: 16px;
            padding: 14px 18px;
            background: #f9fbfe;
            border-radius: 10px;
            text-decoration: none;
            color: #1e293b;
            border: 1px solid #eef2f6;
            transition: 0.1s;
            font-size: 1.05rem;
        }

        .social-link:hover {
            background: #eff6ff;
            border-color: #b9d3f8;
        }

        .social-icon {
            font-size: 1.5rem;
            width: 32px;
            text-align: center;
        }

        .link-arrow {
            margin-left: auto;
            color: #8a99b0;
            font-size: 1.2rem;
        }

        .video-list {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(240px, 1fr));
            gap: 16px;
            margin: 24px 0;
        }

        .video-card {
            border: 1px solid #eef2f6;
            border-radius: 10px;
            padding: 16px;
            background: #fafcff;
        }

        .video-card strong {
            display: block;
            font-size: 1rem;
            margin-bottom: 6px;
        }

        .video-card .date {
            font-size: 0.85rem;
            color: #6b7b90;
        }

        .footer-docs {
            margin-top: 48px;
            padding-top: 24px;
            border-top: 1px solid #eef2f6;
            color: #6b7b90;
            font-size: 0.9rem;
        }
    </style>
</head>
<body>
    <!-- НАВИГАЦИЯ (СЛЕВА) -->
    <div class="sidebar">
        <div class="logo">
            Borisonchik<span>docs</span>
        </div>
        <div class="nav-menu">
            <button class="nav-item active" data-page="home">
                <span class="nav-icon">📄</span> Главная
            </button>
            <button class="nav-item" data-page="info">
                <span class="nav-icon">ℹ️</span> Информация
            </button>
            <button class="nav-item" data-page="social">
                <span class="nav-icon">🌐</span> Социальные сети
            </button>
            <button class="nav-item" data-page="walkthroughs">
                <span class="nav-icon">🎮</span> Прохождения
            </button>
        </div>
        <div style="margin-top: auto; font-size: 0.85rem; color: #94a3b8; padding: 16px 12px 0; border-top: 1px solid #edf2f7; margin-top: 24px;">
            v1.0 · официально
        </div>
    </div>

    <!-- КОНТЕНТ (меняется) -->
    <div class="content">
        <!-- Страница: Главная -->
        <div id="home" class="page active-page">
            <h1>Главная</h1>
            <div class="lead">
                Borisonchik Official — документация и ссылки.
            </div>
            <p>Добро пожаловать. Здесь собраны все официальные ресурсы, социальные сети и список прохождений. Используй навигацию слева для перехода между разделами.</p>
            <h2>Быстрые ссылки</h2>
            <div class="card-grid">
                <a href="#" class="social-link" target="_blank">
                    <span class="social-icon">📺</span> YouTube
                    <span class="link-arrow">↗</span>
                </a>
                <a href="#" class="social-link" target="_blank">
                    <span class="social-icon">💬</span> Discord
                    <span class="link-arrow">↗</span>
                </a>
                <a href="#" class="social-link" target="_blank">
                    <span class="social-icon">📘</span> Facebook
                    <span class="link-arrow">↗</span>
                </a>
            </div>
            <div class="footer-docs">
                ⚡ кратко · основное
            </div>
        </div>

        <!-- Страница: Информация -->
        <div id="info" class="page">
            <h1>Информация</h1>
            <p>Здесь может быть описание канала, контакты для связи и прочее.</p>
            <div style="background: #f1f6fd; padding: 20px; border-radius: 12px; margin: 24px 0;">
                <p style="margin-bottom: 8px;"><strong>📌 О проекте:</strong></p>
                <p>Игровые прохождения, обзоры и стримы. Контент выходит регулярно.</p>
                <p style="margin-top: 16px;"><strong>📬 Контакт:</strong> borisonchik@example.com</p>
            </div>
        </div>

        <!-- Страница: Социальные сети (только они) -->
        <div id="social" class="page">
            <h1>Социальные сети</h1>
            <p style="color: #4a5b73;">Все официальные площадки Borisonchik:</p>
            <div class="card-grid" style="margin-top: 24px;">
                <a href="#" class="social-link" target="_blank">
                    <span class="social-icon">📺</span> YouTube (подпишись)
                    <span class="link-arrow">↗</span>
                </a>
                <a href="#" class="social-link" target="_blank">
                    <span class="social-icon">🎮</span> Twitch
                    <span class="link-arrow">↗</span>
                </a>
                <a href="#" class="social-link" target="_blank">
                    <span class="social-icon">💬</span> Discord сервер
                    <span class="link-arrow">↗</span>
                </a>
                <a href="#" class="social-link" target="_blank">
                    <span class="social-icon">📘</span> Facebook
                    <span class="link-arrow">↗</span>
                </a>
                <a href="#" class="social-link" target="_blank">
                    <span class="social-icon">📷</span> Instagram
                    <span class="link-arrow">↗</span>
                </a>
                <a href="#" class="social-link" target="_blank">
                    <span class="social-icon">🎵</span> TikTok
                    <span class="link-arrow">↗</span>
                </a>
                <a href="#" class="social-link" target="_blank">
                    <span class="social-icon">💬</span> Telegram
                    <span class="link-arrow">↗</span>
                </a>
            </div>
        </div>

        <!-- Страница: Прохождения -->
        <div id="walkthroughs" class="page">
            <h1>Все мои прохождения</h1>
            <div class="video-list">
                <div class="video-card">
                    <strong>🔴 Half-Life 2</strong>
                    <span class="date">полное прохождение · 12 видео</span>
                </div>
                <div class="video-card">
                    <strong>🔵 Portal 2</strong>
                    <span class="date">кооператив · 8 видео</span>
                </div>
                <div class="video-card">
                    <strong>🟣 Cyberpunk 2077</strong>
                    <span class="date">патч 2.0 · 20 видео</span>
                </div>
                <div class="video-card">
                    <strong>🟢 The Witcher 3</strong>
                    <span class="date">DLC · 15 видео</span>
                </div>
                <div class="video-card">
                    <strong>⚫ Dark Souls 3</strong>
                    <span class="date">все боссы · 14 видео</span>
                </div>
                <div class="video-card">
                    <strong>🟡 Minecraft</strong>
                    <span class="date">хардкор · 6 видео</span>
                </div>
            </div>
            <p style="margin-top: 24px; background: #f0f4fe; padding: 12px 16px; border-radius: 8px;">
                ⚡ Плейлисты добавляются по мере выхода. Подпишись на уведомления!
            </p>
        </div>
    </div>

    <!-- Простой JS для переключения страниц (как в документации) -->
    <script>
        (function() {
            const navItems = document.querySelectorAll('.nav-item');
            const pages = document.querySelectorAll('.page');

            function switchPage(pageId) {
                // Скрыть все страницы
                pages.forEach(page => {
                    page.classList.remove('active-page');
                });
                // Показать нужную
                const activePage = document.getElementById(pageId);
                if (activePage) {
                    activePage.classList.add('active-page');
                }
                // Обновить активный класс в меню
                navItems.forEach(item => {
                    item.classList.remove('active');
                    if (item.getAttribute('data-page') === pageId) {
                        item.classList.add('active');
                    }
                });
            }

            // Навесить обработчики на пункты меню
            navItems.forEach(item => {
                item.addEventListener('click', function(e) {
                    e.preventDefault();
                    const pageId = this.getAttribute('data-page');
                    if (pageId) {
                        switchPage(pageId);
                        // меняем URL hash (необязательно, но красиво)
                        window.location.hash = pageId;
                    }
                });
            });

            // При загрузке проверить hash
            if (window.location.hash) {
                const hash = window.location.hash.substring(1); // убираем #
                const validPages = ['home', 'info', 'social', 'walkthroughs'];
                if (validPages.includes(hash)) {
                    switchPage(hash);
                } else {
                    switchPage('home');
                }
            } else {
                switchPage('home');
            }
        })();
    </script>
</body>
</html>
