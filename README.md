<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Sameera's Blessed Birthday</title>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Great+Vibes&family=Montserrat:wght@300;400;600&display=swap');

        :root {
            --deep-red: #a4161a;
            --soft-gold: #d4a373;
            --blush: #fff5f5;
            --dark-bg: #0b090a;
        }

        body {
            background: radial-gradient(circle at center, #2b0b0b 0%, #0b090a 100%);
            color: #f5f3f4;
            font-family: 'Montserrat', sans-serif;
            margin: 0;
            padding: 20px;
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            overflow-x: hidden;
        }

        .stars-container {
            position: fixed;
            top: 0; left: 0; width: 100%; height: 100%;
            z-index: -1;
        }

        .star {
            position: absolute;
            background: white;
            border-radius: 50%;
            opacity: 0.5;
            animation: twinkle var(--duration) infinite ease-in-out;
        }

        @keyframes twinkle {
            0%, 100% { opacity: 0.3; transform: scale(1); }
            50% { opacity: 1; transform: scale(1.2); }
        }

        .main-frame {
            border: 8px double var(--deep-red);
            background: rgba(255, 255, 255, 0.98);
            color: #333;
            padding: 40px;
            border-radius: 30px;
            max-width: 1000px;
            width: 100%;
            box-shadow: 0 0 50px rgba(164, 22, 26, 0.4);
            position: relative;
            animation: fadeIn 1.5s ease-in;
        }

        @keyframes fadeIn { from { opacity: 0; transform: translateY(20px); } to { opacity: 1; transform: translateY(0); } }

        .grid-container {
            display: grid;
            grid-template-columns: 1fr;
            gap: 25px;
            text-align: center;
        }

        @media (min-width: 768px) {
            .grid-container {
                grid-template-columns: repeat(3, 1fr);
                align-items: stretch;
            }
            .center-zone { grid-column: 2; grid-row: 1 / span 2; display: flex; flex-direction: column; justify-content: center; }
            .full-width { grid-column: 1 / span 3; }
        }

        .name-heading {
            font-family: 'Great Vibes', cursive;
            font-size: clamp(3rem, 10vw, 5rem);
            color: var(--deep-red);
            margin: 0;
            cursor: pointer;
            transition: transform 0.3s;
            background: linear-gradient(45deg, #a4161a, #660708, #a4161a);
            background-size: 200% auto;
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            animation: shine 3s linear infinite;
        }

        @keyframes shine { to { background-position: 200% center; } }
        .name-heading:hover { transform: scale(1.05); }

        .dua-card {
            background: #fff;
            border: 1px solid rgba(164, 22, 26, 0.2);
            border-left: 5px solid var(--deep-red);
            padding: 20px;
            border-radius: 12px;
            box-shadow: 0 4px 15px rgba(0,0,0,0.05);
            transition: all 0.4s ease;
            animation: float 4s ease-in-out infinite;
            animation-delay: var(--delay);
        }

        @keyframes float {
            0%, 100% { transform: translateY(0); }
            50% { transform: translateY(-10px); }
        }

        .dua-card:hover {
            transform: scale(1.02) translateY(-5px) !important;
            box-shadow: 0 8px 25px rgba(164, 22, 26, 0.15);
        }

        .arabic {
            display: block;
            font-size: 1.3rem;
            color: #660708;
            margin-bottom: 10px;
            font-weight: bold;
        }

        .translation { font-size: 0.9rem; color: #555; font-style: italic; }

        .birthday-message {
            background: var(--blush);
            border-top: 5px solid var(--deep-red);
            padding: 30px;
            border-radius: 15px;
            font-size: 1.1rem;
            line-height: 1.8;
            margin-top: 20px;
        }

        .particle {
            position: absolute;
            pointer-events: none;
            z-index: 999;
            animation: burst 1.2s ease-out forwards;
        }

        @keyframes burst {
            to { transform: translate(var(--x), var(--y)) rotate(360deg); opacity: 0; }
        }
    </style>
</head>
<body>

    <div class="stars-container" id="star-field"></div>

    <div class="main-frame">
        <div class="grid-container">
            
            <div class="dua-card" style="--delay: 0s">
                <span class="arabic">يَا مُقَلِّبَ الْقُلُوبِ ثَبِّتْ قَلْبِي</span>
                <div class="translation">"O Turner of hearts, keep my heart firm upon Your religion."</div>
            </div>

            <div class="dua-card" style="--delay: 0.5s">
                <span class="arabic">اللَّهُمَّ أَصْلِحْ لِي دِينِي</span>
                <div class="translation">"O Allah, set right for me my religion which is the safeguard of my affairs."</div>
            </div>

            <div class="center-zone">
                <h1 class="name-heading" onclick="celebrate(event)">Sameera</h1>
                <p style="color:var(--deep-red); font-weight:600; font-size: 0.8rem; letter-spacing: 2px;">BLESSED BIRTHDAY</p>
                <p style="color:#888; font-size: 0.7rem;">✨ Tap for a Surprise ✨</p>
            </div>

            <div class="dua-card" style="--delay: 1s">
                <span class="arabic">رَبِّ زِدْنِي عِلْمًا</span>
                <div class="translation">"My Lord, increase me in knowledge and wisdom."</div>
            </div>

            <div class="dua-card" style="--delay: 1.5s">
                <span class="arabic">رَبِّ اجْعَلْنِي مُقِيمَ الصَّلَاةِ</span>
                <div class="translation">"My Lord, make me an establisher of prayer."</div>
            </div>

            <div class="dua-card" style="--delay: 2s">
                <span class="arabic">رَبَّنَا آتِنَا فِي الدُّنْيَا حَسَنَةً</span>
                <div class="translation">"Our Lord, grant us good in this world and the Hereafter."</div>
            </div>

            <div class="dua-card" style="--delay: 2.5s">
                <span class="arabic">اللَّهُمَّ إِنِّي أَسْأَلُكَ عِلْمًا نَافِعًا</span>
                <div class="translation">"O Allah, I ask You for knowledge that is of benefit and a good provision."</div>
            </div>

            <div class="dua-card" style="--delay: 3s">
                <span class="arabic">اللَّهُمَّ بَارِكْ لَنَا فِيمَا رَزَقْتَنَا</span>
                <div class="translation">"O Allah, bless us in what You have provided for us."</div>
            </div>

            <div class="full-width birthday-message">
                <strong>Dearest Sameera,</strong><br>
                On this beautiful day, I pray that every step you take brings you closer to Allah's love. May your heart always be full of peace, your mind full of wisdom, and your life full of health and happiness. As you celebrate another year, may the light of the Quran guide your path and the love of the Almighty fill your heart with serenity. May this year open doors of immense <em>Barakah</em> and <em>Rahmah</em>. Wishing you a year as radiant as your soul.
                <br><br>
                <strong>Happy Birthday!</strong>
            </div>
        </div>
    </div>

    <script>
        // Stars Logic
        const starField = document.getElementById('star-field');
        for (let i = 0; i < 120; i++) {
            const star = document.createElement('div');
            star.className = 'star';
            const size = Math.random() * 3 + 'px';
            star.style.width = size;
            star.style.height = size;
            star.style.top = Math.random() * 100 + '%';
            star.style.left = Math.random() * 100 + '%';
            star.style.setProperty('--duration', (Math.random() * 3 + 2) + 's');
            starField.appendChild(star);
        }

        function celebrate(e) {
            const items = ['🌸', '✨', '⭐', '🌹', '💖', '🤲', '🌙'];
            for (let i = 0; i < 30; i++) {
                const p = document.createElement('div');
                p.classList.add('particle');
                p.textContent = items[Math.floor(Math.random() * items.length)];
                p.style.left = e.clientX + 'px';
                p.style.top = e.clientY + 'px';
                const x = (Math.random() - 0.5) * 600 + 'px';
                const y = (Math.random() - 0.5) * 600 + 'px';
                p.style.setProperty('--x', x);
                p.style.setProperty('--y', y);
                p.style.fontSize = Math.random() * 25 + 15 + 'px';
                document.body.appendChild(p);
                setTimeout(() => p.remove(), 1200);
            }
        }
    </script>
</body>
</html>
