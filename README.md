# troppertoxics.github.io
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Flip: Unleashed! - Epic Roblox Adventure</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Arial', sans-serif;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            overflow-x: hidden;
        }

        .container {
            max-width: 800px;
            margin: 0 auto;
            padding: 20px;
        }

        .header {
            text-align: center;
            margin-bottom: 30px;
            animation: fadeInDown 1s ease-out;
        }

        .game-title {
            font-size: 3.5rem;
            font-weight: bold;
            color: #fff;
            text-shadow: 0 4px 8px rgba(0,0,0,0.3);
            margin-bottom: 10px;
            animation: glow 2s ease-in-out infinite alternate;
        }

        .subtitle {
            font-size: 1.2rem;
            color: #f0f0f0;
            margin-bottom: 20px;
        }

        .update-badge {
            display: inline-block;
            background: linear-gradient(45deg, #ff6b6b, #ee5a24);
            color: white;
            padding: 8px 16px;
            border-radius: 25px;
            font-weight: bold;
            font-size: 0.9rem;
            animation: pulse 2s infinite;
            margin-bottom: 20px;
        }

        .features {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
            margin: 40px 0;
        }

        .feature-card {
            background: rgba(255,255,255,0.1);
            backdrop-filter: blur(10px);
            border-radius: 15px;
            padding: 25px;
            text-align: center;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            border: 1px solid rgba(255,255,255,0.2);
        }

        .feature-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 20px 40px rgba(0,0,0,0.2);
        }

        .feature-icon {
            font-size: 3rem;
            margin-bottom: 15px;
            display: block;
        }

        .feature-title {
            font-size: 1.3rem;
            color: #fff;
            margin-bottom: 10px;
            font-weight: bold;
        }

        .feature-description {
            color: #e0e0e0;
            line-height: 1.5;
        }

        .cta-section {
            text-align: center;
            margin: 50px 0;
            animation: fadeInUp 1s ease-out;
        }

        .play-button {
            display: inline-block;
            background: linear-gradient(45deg, #00c851, #007e33);
            color: white;
            font-size: 1.5rem;
            font-weight: bold;
            padding: 20px 40px;
            border-radius: 50px;
            text-decoration: none;
            transition: all 0.3s ease;
            box-shadow: 0 8px 25px rgba(0,200,81,0.3);
            animation: buttonFloat 3s ease-in-out infinite;
        }

        .play-button:hover {
            transform: translateY(-5px);
            box-shadow: 0 15px 35px rgba(0,200,81,0.4);
            background: linear-gradient(45deg, #00ff5f, #00c851);
        }

        .stats {
            display: flex;
            justify-content: center;
            gap: 40px;
            margin: 30px 0;
            flex-wrap: wrap;
        }

        .stat {
            text-align: center;
            color: #fff;
        }

        .stat-number {
            font-size: 2rem;
            font-weight: bold;
            display: block;
            animation: countUp 2s ease-out;
        }

        .stat-label {
            font-size: 0.9rem;
            color: #ccc;
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        .floating-shapes {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            z-index: -1;
        }

        .shape {
            position: absolute;
            opacity: 0.1;
            animation: float 6s ease-in-out infinite;
        }

        .shape:nth-child(1) { top: 20%; left: 10%; animation-delay: 0s; }
        .shape:nth-child(2) { top: 60%; right: 10%; animation-delay: 2s; }
        .shape:nth-child(3) { bottom: 20%; left: 20%; animation-delay: 4s; }

        @keyframes glow {
            from { text-shadow: 0 4px 8px rgba(0,0,0,0.3); }
            to { text-shadow: 0 4px 20px rgba(255,255,255,0.5); }
        }

        @keyframes pulse {
            0%, 100% { transform: scale(1); }
            50% { transform: scale(1.05); }
        }

        @keyframes fadeInDown {
            from { opacity: 0; transform: translateY(-50px); }
            to { opacity: 1; transform: translateY(0); }
        }

        @keyframes fadeInUp {
            from { opacity: 0; transform: translateY(50px); }
            to { opacity: 1; transform: translateY(0); }
        }

        @keyframes buttonFloat {
            0%, 100% { transform: translateY(0px); }
            50% { transform: translateY(-10px); }
        }

        @keyframes float {
            0%, 100% { transform: translateY(0px) rotate(0deg); }
            50% { transform: translateY(-20px) rotate(180deg); }
        }

        @keyframes countUp {
            from { opacity: 0; transform: scale(0.5); }
            to { opacity: 1; transform: scale(1); }
        }

        @media (max-width: 768px) {
            .game-title { font-size: 2.5rem; }
            .features { grid-template-columns: 1fr; }
            .stats { gap: 20px; }
        }
    </style>
</head>
<body>
    <div class="floating-shapes">
        <div class="shape" style="width: 80px; height: 80px; background: linear-gradient(45deg, #ff6b6b, #ee5a24); border-radius: 50%;"></div>
        <div class="shape" style="width: 60px; height: 60px; background: linear-gradient(45deg, #4ecdc4, #45b7aa); transform: rotate(45deg);"></div>
        <div class="shape" style="width: 100px; height: 100px; background: linear-gradient(45deg, #ffe66d, #ff8c42); clip-path: polygon(50% 0%, 0% 100%, 100% 100%);"></div>
    </div>

    <div class="container">
        <div class="header">
            <div class="update-badge">🔥 FRESH UPDATE!</div>
            <h1 class="game-title">FLIP: UNLEASHED!</h1>
            <p class="subtitle">Master the Ultimate Flipping Experience on Roblox</p>
        </div>

        <div class="features">
            <div class="feature-card">
                <span class="feature-icon">🚀</span>
                <h3 class="feature-title">Epic Flips</h3>
                <p class="feature-description">Experience mind-blowing flips and stunts that will leave you and your friends amazed!</p>
            </div>
            <div class="feature-card">
                <span class="feature-icon">⚡</span>
                <h3 class="feature-title">Lightning Fast</h3>
                <p class="feature-description">Smooth gameplay with zero lag. Jump in and start flipping instantly!</p>
            </div>
            <div class="feature-card">
                <span class="feature-icon">🏆</span>
                <h3 class="feature-title">Compete & Win</h3>
                <p class="feature-description">Challenge friends and climb the leaderboards to become the flip champion!</p>
            </div>
            <div class="feature-card">
                <span class="feature-icon">🎮</span>
                <h3 class="feature-title">Regular Updates</h3>
                <p class="feature-description">Fresh content added regularly with new features, flips, and challenges!</p>
            </div>
        </div>

        <div class="stats">
            <div class="stat">
                <span class="stat-number">1000+</span>
                <span class="stat-label">Players</span>
            </div>
            <div class="stat">
                <span class="stat-number">⭐⭐⭐⭐⭐</span>
                <span class="stat-label">Rating</span>
            </div>
            <div class="stat">
                <span class="stat-number">24/7</span>
                <span class="stat-label">Available</span>
            </div>
        </div>

        <div class="cta-section">
            <a href="https://www.roblox.com/games/15510488723/UPDATE-Flip-Unleashed" class="play-button">
                🎮 PLAY NOW - FREE!
            </a>
            <p style="color: #ccc; margin-top: 15px; font-size: 0.9rem;">
                Join thousands of players already flipping their way to victory!
            </p>
        </div>
    </div>

    <script>
        // Add some interactive elements
        document.addEventListener('mousemove', function(e) {
            const shapes = document.querySelectorAll('.shape');
            const x = e.clientX / window.innerWidth;
            const y = e.clientY / window.innerHeight;
            
            shapes.forEach((shape, index) => {
                const speed = (index + 1) * 0.5;
                shape.style.transform += ` translate(${x * speed}px, ${y * speed}px)`;
            });
        });

        // Animate stats on scroll
        const observerOptions = {
            threshold: 0.5,
            rootMargin: '0px 0px -50px 0px'
        };

        const observer = new IntersectionObserver(function(entries) {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.style.animation = 'countUp 2s ease-out';
                }
            });
        }, observerOptions);

        document.querySelectorAll('.stat-number').forEach(stat => {
            observer.observe(stat);
        });
    </script>
</body>
</html>
