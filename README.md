<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Borisonchik Official</title>
    <style>
        /* Стили для красивого сайта */
        @import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;600;800&display=swap');

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Inter', sans-serif;
            background: linear-gradient(145deg, #0f0c1f 0%, #1a1533 100%);
            color: #f0eaff;
            min-height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            padding: 20px;
            line-height: 1.6;
        }

        .container {
            max-width: 900px;
            width: 100%;
            background: rgba(20, 15, 40, 0.6);
            backdrop-filter: blur(12px);
            -webkit-backdrop-filter: blur(12px);
            border: 1px solid rgba(140, 90, 255, 0.25);
            border-radius: 48px;
            padding: 40px 30px;
            box-shadow: 0 30px 60px rgba(0, 0, 0, 0.8), 0 0 0 1px rgba(170, 130, 255, 0.1) inset, 0 0 30px rgba(100, 70, 255, 0.3);
        }

        /* Шапка с аватаром */
        .profile {
            display: flex;
            flex-direction: column;
            align-items: center;
            margin-bottom: 30px;
        }

        .avatar {
            width: 120px;
            height: 120px;
            background: linear-gradient(135deg, #aa82ff, #5f3bdc);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 58px;
            font-weight: 800;
            color: white;
            text-shadow: 0 0 20px #ffffff;
            box-shadow: 0 15px 30px -8px #4a2bb3, 0 0 0 3px rgba(255, 255, 255, 0.15);
            margin-bottom: 20px;
            position: relative;
        }

        .avatar::after {
            content: '';
            position: absolute;
            width: 130px;
            height: 130px;
            border-radius: 50%;
            border: 2px solid rgba(210, 180, 255, 0.5);
            top: -5px;
            left: -5px;
            animation: pulse 2s infinite;
        }

        @keyframes pulse {
            0% { transform: scale(1); opacity: 0.6; }
            70% { transform: scale(1.1); opacity: 0; }
            100% { transform: scale(1); opacity: 0; }
        }

        h1 {
            font-size: 2.8rem;
            font-weight: 800;
            letter-spacing: 2px;
            background: linear-gradient(120deg, #ffffff, #e0c9ff);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            text-shadow: 0 0 15px #9f7aff;
            margin-bottom: 8px;
        }

        .badge {
            background: rgba(170, 130, 255, 0.2);
            border: 1px solid rgba(170, 130, 255, 0.5);
            border-radius: 60px;
            padding: 6px 18px;
            font-size: 0.9rem;
            color: #cbb9ff;
            backdrop-filter: blur(5px);
        }

        /* Кнопки соцсетей (первые три) */
        .buttons-primary {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 16px;
            margin: 30px 0 40px;
        }

        .btn {
            padding: 14px 32px;
            border-radius: 40px;
            font-weight: 600;
            text-decoration: none;
            display: inline-flex;
            align-items: center;
            gap: 12px;
            font-size: 1.1rem;
            transition: all 0.25s ease;
            border: 1px solid transparent;
            box-shadow: 0 8px 20px rgba(0, 0, 0, 0.5);
        }

        .btn-youtube {
            background: #ff1e3c;
            color: white;
            box-shadow: 0 0 20px #ff4d6d;
        }

        .btn-youtube:hover {
            background: #ff4d6d;
            transform: translateY(-4px);
            box-shadow: 0 15px 30px #ff1e3c;
        }

        .btn-discord {
            background: #5865f2;
            color: white;
            box-shadow: 0 0 20px #7983ff;
        }

        .btn-discord:hover {
            background: #7983ff;
            transform: translateY(-4px);
        }

        .btn-facebook {
            background: #1877f2;
            color: white;
            box-shadow: 0 0 20px #4c9aff;
        }

        .btn-facebook:hover {
            background: #4c9aff;
            transform: translateY(-4px);
        }

        /* Разделитель */
        .divider {
            text-align: center;
            margin: 40px 0 30px;
            position: relative;
        }

        .divider span {
            background: rgba(36, 28, 66, 0.8);
            padding: 8px 25px;
            border-radius: 60px;
            font-size: 1.2rem;
            font-weight: 600;
            letter-spacing: 1px;
            border: 1px solid #7a5fd0;
            backdrop-filter: blur(4px);
            color: #dacdff;
        }

        /* Социальные сети (все иконки) */
        .social-links {
            display: flex;
            flex-wrap: wrap;
            align-items: center;
            justify-content: center;
            gap: 25px;
            margin-bottom: 50px;
        }

        .social-item {
            background: rgba(255, 255, 255, 0.03);
            border: 1px solid rgba(170, 130, 255, 0.3);
            border-radius: 60px;
            padding: 10px 25px;
            display: flex;
            align-items: center;
            gap: 12px;
            text-decoration: none;
            color: #e0d0ff;
            font-weight: 500;
            transition: 0.2s;
            backdrop-filter: blur(4px);
        }

        .social-item:hover {
            background: rgba(170, 130, 255, 0.15);
            border-color: #aa82ff;
            transform: scale(1.05);
            color: white;
            box-shadow: 0 0 20px #9f7aff;
        }

        .social-item img, .social-item svg {
            width: 28px;
            height: 28px;
            filter: drop-shadow(0 0 5px #b89eff);
        }

        /* Видео секция */
        .walkthroughs {
            margin-top: 20px;
        }

        .walkthroughs h2 {
            font-size: 2rem;
            font-weight: 700;
            text-align: center;
            margin-bottom: 30px;
            background: linear-gradient(135deg, #f0eaff, #cfb3ff);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        .video-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
            gap: 25px;
        }

        .video-card {
            background: rgba(12, 8, 27, 0.7);
            border-radius: 30px;
            padding: 20px 15px 15px;
            border: 1px solid #3a2a70;
            backdrop-filter: blur(5px);
            transition: 0.3s;
            text-align: center;
        }

        .video-card:hover {
            border-color: #b28aff;
            box-shadow: 0 0 35px #5740a0;
            transform: translateY(-6px);
        }

        .video-thumb {
            width: 100%;
            aspect-ratio: 16 / 9;
            background: #2b2244;
            border-radius: 20px;
            display: flex;
            align-items: center;
            justify-content: center;
            margin-bottom: 15px;
            position: relative;
            overflow: hidden;
            border: 1px solid #5d4b9a;
        }

        .video-thumb svg {
            width: 60px;
            height: 60px;
            opacity: 0.8;
            transition: 0.2s;
        }

        .video-card:hover .video-thumb svg {
            opacity: 1;
            transform: scale(1.1);
            fill: #ff4d6d;
        }

        .video-card p {
            font-weight: 600;
            color: #f0e6ff;
        }

        .small-note {
            color: #8f81b3;
            font-size: 0.9rem;
            margin-top: 25px;
            text-align: center;
        }

        footer {
            text-align: center;
            margin-top: 40px;
            color: #6b5b95;
            font-size: 0.9rem;
        }

        /* Иконки (текстовые заглушки) */
        .icon-symbol {
            font-size: 24px;
            filter: drop-shadow(0 0 5px currentColor);
        }
    </style>
</head>
<body>
    <div class="container">
        <!-- Шапка профиля -->
        <div class="profile">
            <div class="avatar">B</div>
            <h1>Borisonchik</h1>
            <span class="badge">⚡ Официальный канал ⚡</span>
        </div>

        <!-- 1. Кнопки: YouTube, Discord, Facebook (как просил) -->
        <div class="buttons-primary">
            <a href="#" class="btn btn-youtube" target="_blank">
                <span class="icon-symbol">▶</span> YouTube
            </a>
            <a href="#" class="btn btn-discord" target="_blank">
                <span class="icon-symbol">💬</span> Discord
            </a>
            <a href="#" class="btn btn-facebook" target="_blank">
                <span class="icon-symbol">f</span> Фейсбук
            </a>
        </div>

        <!-- Разделитель "Социальные сети" -->
        <div class="divider">
            <span>🌐 СОЦИАЛЬНЫЕ СЕТИ 🌐</span>
        </div>

        <!-- 2. Блок "Социальные сети" (расширенный список) -->
        <div class="social-links">
            <!-- YouTube (повтор для комплекта) -->
            <a href="#" class="social-item" target="_blank">
                <span class="icon-symbol">📺</span> YouTube
            </a>
            <!-- Discord -->
            <a href="#" class="social-item" target="_blank">
                <span class="icon-symbol">🎧</span> Discord
            </a>
            <!-- Facebook -->
            <a href="#" class="social-item" target="_blank">
                <span class="icon-symbol">📘</span> Facebook
            </a>
            <!-- Instagram (добавил для красоты, можешь убрать) -->
            <a href="#" class="social-item" target="_blank">
                <span class="icon-symbol">📷</span> Instagram
            </a>
            <!-- TikTok (тоже для полноты) -->
            <a href="#" class="social-item" target="_blank">
                <span class="icon-symbol">🎵</span> TikTok
            </a>
            <!-- Twitch -->
            <a href="#" class="social-item" target="_blank">
                <span class="icon-symbol">🎮</span> Twitch
            </a>
            <!-- Telegram -->
            <a href="#" class="social-item" target="_blank">
                <span class="icon-symbol">📱</span> Telegram
            </a>
        </div>

        <!-- 3. Раздел "Все мои прохождения" -->
        <div class="walkthroughs">
            <h2>🎮 Все мои прохождения 🎮</h2>
            <div class="video-grid">
                <!-- Карточка видео 1 -->
                <div class="video-card">
                    <div class="video-thumb">
                        <!-- Символ плеера -->
                        <svg viewBox="0 0 24 24" width="50" height="50" fill="#aa82ff">
                            <path d="M8 5v14l11-7z"/>
                        </svg>
                    </div>
                    <p>🔴 Half-Life 2 (полное прохождение)</p>
                </div>
                <!-- Карточка видео 2 -->
                <div class="video-card">
                    <div class="video-thumb">
                        <svg viewBox="0 0 24 24" width="50" height="50" fill="#aa82ff">
                            <path d="M8 5v14l11-7z"/>
                        </svg>
                    </div>
                    <p>🔵 Portal 2 — кооператив</p>
                </div>
                <!-- Карточка видео 3 -->
                <div class="video-card">
                    <div class="video-thumb">
                        <svg viewBox="0 0 24 24" width="50" height="50" fill="#aa82ff">
                            <path d="M8 5v14l11-7z"/>
                        </svg>
                    </div>
                    <p>🟣 Cyberpunk 2077 (2.0 обновление)</p>
                </div>
                <!-- Карточка видео 4 -->
                <div class="video-card">
                    <div class="video-thumb">
                        <svg viewBox="0 0 24 24" width="50" height="50" fill="#aa82ff">
                            <path d="M8 5v14l11-7z"/>
                        </svg>
                    </div>
                    <p>🟢 The Witcher 3: все DLC</p>
                </div>
            </div>
            <p class="small-note">👆 скоро здесь появятся ссылки на ролики (подпишись, чтобы не пропустить)!</p>
        </div>

        <!-- Подвал -->
        <footer>
            Ⓒ 2025 Borisonchik Official. Все права защищены.
        </footer>
    </div>
</body>
</html>
