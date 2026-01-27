<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Кибергигиена: Полный гайд</title>
    <style>
        :root {
            --bg-primary: #0f172a;
            --bg-secondary: #1e293b;
            --text-primary: #e2e8f0;
            --text-secondary: #94a3b8;
            --accent: #38bdf8;
            --accent-glow: rgba(56, 189, 248, 0.15);
            --danger: #f43f5e;
            --success: #10b981;
            --warning: #f59e0b;
            --border: #334155;
            --font-main: 'Segoe UI', system-ui, -apple-system, sans-serif;
            --max-width: 740px;
        }

        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }

        html {
            scroll-behavior: smooth;
        }

        body {
            background-color: var(--bg-primary);
            color: var(--text-primary);
            font-family: var(--font-main);
            line-height: 1.7;
            font-size: 18px;
            overflow-x: hidden;
        }

        /* Reading Progress Bar */
        .progress-container {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 4px;
            background: transparent;
            z-index: 1000;
        }

        .progress-bar {
            height: 100%;
            background: linear-gradient(90deg, var(--accent), #818cf8);
            width: 0%;
            transition: width 0.1s;
        }

        /* Layout */
        .container {
            max-width: var(--max-width);
            margin: 0 auto;
            padding: 2rem 1.5rem;
        }

        header {
            padding: 4rem 0 2rem;
            border-bottom: 1px solid var(--border);
            margin-bottom: 3rem;
        }

        .tag {
            display: inline-block;
            background: var(--accent-glow);
            color: var(--accent);
            padding: 0.3rem 0.8rem;
            border-radius: 50px;
            font-size: 0.85rem;
            font-weight: 600;
            margin-bottom: 1rem;
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        h1 {
            font-size: 2.5rem;
            line-height: 1.2;
            margin-bottom: 1rem;
            background: linear-gradient(to right, #fff, #94a3b8);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        .meta {
            color: var(--text-secondary);
            font-size: 0.95rem;
            display: flex;
            align-items: center;
            gap: 1rem;
        }

        /* Content Styling */
        article p {
            margin-bottom: 1.5rem;
            color: #cbd5e1;
        }

        h2 {
            font-size: 1.8rem;
            margin: 3rem 0 1rem;
            color: var(--text-primary);
            display: flex;
            align-items: center;
            gap: 0.5rem;
        }

        h3 {
            font-size: 1.3rem;
            margin: 2rem 0 1rem;
            color: var(--accent);
        }

        ul {
            margin-bottom: 1.5rem;
            list-style: none;
        }

        li {
            margin-bottom: 0.8rem;
            padding-left: 1.5rem;
            position: relative;
        }

        li::before {
            content: "•";
            color: var(--accent);
            position: absolute;
            left: 0;
            font-weight: bold;
        }

        /* Feature Blocks */
        .highlight-box {
            background: var(--bg-secondary);
            border-left: 4px solid var(--accent);
            padding: 1.5rem;
            margin: 2rem 0;
            border-radius: 0 8px 8px 0;
        }

        .highlight-box.danger {
            border-left-color: var(--danger);
            background: rgba(244, 63, 94, 0.05);
        }

        .highlight-box.warning {
            border-left-color: var(--warning);
            background: rgba(245, 158, 11, 0.05);
        }

        .highlight-title {
            display: block;
            font-weight: 700;
            margin-bottom: 0.5rem;
            color: var(--text-primary);
        }

        .stat-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 1rem;
            margin: 2rem 0;
        }

        .stat-card {
            background: var(--bg-secondary);
            padding: 1.5rem;
            border-radius: 12px;
            text-align: center;
            border: 1px solid var(--border);
        }

        .stat-number {
            display: block;
            font-size: 2rem;
            font-weight: 800;
            color: var(--accent);
            margin-bottom: 0.5rem;
        }

        .stat-label {
            font-size: 0.85rem;
            color: var(--text-secondary);
        }

        /* Interactive Elements */
        .password-checker {
            background: var(--bg-secondary);
            padding: 1.5rem;
            border-radius: 12px;
            margin: 2rem 0;
            border: 1px solid var(--border);
        }

        .example-input {
            width: 100%;
            padding: 0.8rem;
            background: var(--bg-primary);
            border: 1px solid var(--border);
            color: var(--text-primary);
            border-radius: 6px;
            margin-top: 0.5rem;
            font-family: monospace;
        }

        /* Footer */
        footer {
            margin-top: 4rem;
            padding-top: 2rem;
            border-top: 1px solid var(--border);
            text-align: center;
            color: var(--text-secondary);
            font-size: 0.9rem;
        }

        /* Floating Navigation (Desktop) */
        .toc {
            position: fixed;
            left: 2rem;
            top: 50%;
            transform: translateY(-50%);
            width: 200px;
            display: none;
        }

        .toc-title {
            font-size: 0.8rem;
            text-transform: uppercase;
            color: var(--text-secondary);
            margin-bottom: 1rem;
            letter-spacing: 1px;
        }

        .toc ul {
            border-left: 2px solid var(--border);
        }

        .toc li {
            padding-left: 0;
            margin-bottom: 0;
        }

        .toc li::before { content: none; }

        .toc a {
            display: block;
            padding: 0.5rem 0 0.5rem 1rem;
            color: var(--text-secondary);
            text-decoration: none;
            font-size: 0.9rem;
            border-left: 2px solid transparent;
            margin-left: -2px;
            transition: all 0.2s;
        }

        .toc a:hover, .toc a.active {
            color: var(--accent);
            border-left-color: var(--accent);
        }

        @media (min-width: 1200px) {
            .toc { display: block; }
        }

        @media (max-width: 600px) {
            h1 { font-size: 1.8rem; }
            body { font-size: 16px; }
            .container { padding: 1rem; }
        }
    </style>
</head>
<body>

    <div class="progress-container">
        <div class="progress-bar" id="progressBar"></div>
    </div>

    <!-- Table of Contents (Desktop) -->
    <nav class="toc">
        <div class="toc-title">Содержание</div>
        <ul>
            <li><a href="#intro">Введение</a></li>
            <li><a href="#digital-footprint">Цифровой след</a></li>
            <li><a href="#passwords">Безопасность аккаунта</a></li>
            <li><a href="#social-engineering">Социальная инженерия</a></li>
            <li><a href="#doxing">Доксинг и Буллинг</a></li>
            <li><a href="#conclusion">Итоги</a></li>
        </ul>
    </nav>

    <div class="container">
        <header>
            <span class="tag">Digital Safety 2026</span>
            <h1>Твой цифровой щит: Как выжить в интернете и не потерять себя</h1>
            <div class="meta">
                <span>⏱️ Время чтения: 7 минут</span>
                <span>📅 Обновлено: Январь 2026</span>
            </div>
        </header>

        <article>
            <div id="intro">
                <p>Интернет — это не просто место для мемов, игр и общения. Это полноценное измерение нашей жизни, где действуют свои законы физики и уголовного права. Мы живем в эпоху, где потерять аккаунт в Steam или Telegram может быть больнее, чем потерять кошелек.</p>
                <p>Ты вырос с телефоном в руках, поэтому тебе кажется, что ты знаешь всё. Но хакеры, мошенники и корпорации знают немного больше. В этой статье мы разберем не скучные правила "не сиди долго за компом", а реальные механики защиты твоей личной жизни и репутации.</p>
            </div>

            <div class="stat-grid">
                <div class="stat-card">
                    <span class="stat-number">81%</span>
                    <span class="stat-label">Взломов происходят из-за слабых паролей</span>
                </div>
                <div class="stat-card">
                    <span class="stat-number">∞</span>
                    <span class="stat-label">Время хранения твоих фото в сети</span>
                </div>
            </div>

            <h2 id="digital-footprint">👣 Цифровой след: Интернет помнит всё</h2>
            <p>Представь, что ты идешь по снегу. За тобой остаются следы. В интернете "снег" никогда не тает. Твой цифровой след — это всё, что ты лайкнул, запостил, прокомментировал или даже просто посмотрел.</p>
            
            <div class="highlight-box warning">
                <span class="highlight-title">⚠️ Почему это важно?</span>
                Через 5-10 лет, когда ты будешь устраиваться на работу мечты или поступать в зарубежный вуз, HR-менеджер "пробьет" твои соцсети. Агрессивные комментарии, фото с алкоголем или сомнительные посты 2024 года могут закрыть перед тобой двери в 2030 году.
            </div>

            <h3>Что делать?</h3>
            <ul>
                <li><strong>Принцип билборда:</strong> Прежде чем отправить сообщение или фото, представь, что это повесили на огромный рекламный щит в центре твоего города, где его видят твои родители и учителя. Если тебе стыдно — не отправляй.</li>
                <li><strong>Закрытый профиль:</strong> Это не паранойя, а гигиена. В Instagram, VK и TikTok держи профиль закрытым для незнакомцев.</li>
                <li><strong>Чистка:</strong> Раз в полгода просматривай свои старые посты и удаляй то, что потеряло актуальность или выглядит глупо.</li>
            </ul>

            <h2 id="passwords">🔐 Крепость для аккаунта</h2>
            <p>Самая большая ложь, в которую мы верим: "Да кому я нужен, чтобы меня ломать?". Ты нужен. Твой аккаунт — это спам-база, это доступ к друзьям (чтобы занять у них денег от твоего имени), это игровые ценности.</p>

            <div class="highlight-box">
                <span class="highlight-title">💡 Формула идеального пароля</span>
                Забудь про <code>Masha2008</code> или <code>QWERTY</code>. Длина важнее сложности.
                <br><br>
                <strong>Плохо:</strong> <code>Tr0ub4dor&3</code> (Сложно запомнить, легко взломать перебором)
                <br>
                <strong>Хорошо:</strong> <code>Purple-Elephant-Eating-Pizza-On-Mars</code> (Легко запомнить, компьютеру потребуется миллион лет на взлом)
            </div>

            <h3>Двухфакторная аутентификация (2FA)</h3>
            <p>Пароль могут украсть. Но если включена 2FA, хакеру нужен еще и твой телефон. Включи это везде: VK, Telegram, Google, Steam, Discord. Лучше использовать приложения (Google Authenticator), чем СМС.</p>

            <h2 id="social-engineering">🎣 Социальная инженерия: Взлом человека</h2>
            <p>Хакеры редко "ломают код". Они ломают людей. Социальная инженерия — это манипуляция твоими чувствами: страхом, жадностью или любопытством.</p>

            <div class="highlight-box danger">
                <span class="highlight-title">🚩 Красные флаги фишинга</span>
                <ul>
                    <li><strong>Срочность:</strong> "Ваш аккаунт будет удален через 24 часа! Нажмите сюда!"</li>
                    <li><strong>Халява:</strong> "Ты выиграл iPhone / Получи бесплатные скины / Nitro бесплатно".</li>
                    <li><strong>Авторитет:</strong> Сообщение якобы от "Администрации Telegram" или "Службы поддержки Steam".</li>
                </ul>
            </div>

            <p><strong>Золотое правило:</strong> Никогда не вводи логин и пароль, перейдя по ссылке из сообщения. Хочешь зайти в Steam? Открой браузер, вбей <code>steamcommunity.com</code> руками и зайди. Не кликай.</p>

            <h2 id="doxing">🕵️ Доксинг и Кибербуллинг</h2>
            <p>Доксинг — это сбор и публикация твоих личных данных (адрес, телефон, школа) без твоего согласия. Часто это используют для шантажа или травли.</p>

            <h3>Как защититься от доксинга?</h3>
            <ul>
                <li><strong>Никнеймы:</strong> Не используй один и тот же никнейм везде. Если твой ник в игре совпадает с ником в Инстаграме, найти твое лицо и школу — дело 5 минут.</li>
                <li><strong>Фотографии:</strong> Не выкладывай фото из окна (вид дома), фото билетов, грамот с адресом школы. Геотеги ставь только после того, как ушел из этого места.</li>
                <li><strong>Очистка метаданных:</strong> Фотографии содержат скрытые данные (EXIF), где может быть записана точная GPS-координата съемки. Мессенджеры часто это стирают, а вот отправка "файлом" — нет.</li>
            </ul>

            <div class="highlight-box warning">
                <span class="highlight-title">🛡️ Если тебя травят (Кибербуллинг)</span>
                <p>1. <strong>Не отвечай.</strong> Троллю нужна твоя реакция. Гнев, слезы, оправдания — это его топливо.<br>
                2. <strong>Сохрани доказательства.</strong> Делай скриншоты переписок.<br>
                3. <strong>Блокируй и жалуйся.</strong> Используй кнопку Report беспощадно.<br>
                4. <strong>Расскажи.</strong> Родителям или старшему брату/сестре. Это не стукачество, это привлечение союзников в войне.</p>
            </div>

            <h2 id="conclusion">🚀 Итоги</h2>
            <p>Цифровая безопасность — это не паранойя и шапочка из фольги. Это просто ремень безопасности в машине. Он не мешает ехать, но спасает жизнь при аварии.</p>
            <p>Интернет — потрясающее место. Учись, развлекайся, общайся. Просто помни: твои данные — это валюта 21 века. Не разбрасывайся ими.</p>

        </article>
        
        <footer>
            <p>© 2026 Создано с заботой о твоем цифровом будущем. <br>Данный материал носит образовательный характер.</p>
        </footer>
    </div>

    <script>
        // Progress Bar Logic
        window.onscroll = function() {
            let winScroll = document.body.scrollTop || document.documentElement.scrollTop;
            let height = document.documentElement.scrollHeight - document.documentElement.clientHeight;
            let scrolled = (winScroll / height) * 100;
            document.getElementById("progressBar").style.width = scrolled + "%";

            // Active TOC link logic
            let sections = document.querySelectorAll('h2, div[id="intro"]');
            let navLinks = document.querySelectorAll('.toc a');
            
            sections.forEach(sec => {
                let top = window.scrollY;
                let offset = sec.offsetTop - 150;
                let height = sec.offsetHeight;
                let id = sec.getAttribute('id');

                if(top >= offset && top < offset + height + 200) {
                    navLinks.forEach(links => {
                        links.classList.remove('active');
                        document.querySelector('.toc a[href*=' + id + ']').classList.add('active');
                    });
                }
            });
        };
    </script>
</body>
</html>
