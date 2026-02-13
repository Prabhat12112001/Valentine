<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Miku's Love Quiz 💖</title>
    <style>
        * { margin: 0; padding: 0; box-sizing: border-box; }
        
        body {
            height: 100vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            background: linear-gradient(-45deg, #ee7752, #e73c7e, #23a6d5, #23d5ab);
            background-size: 400% 400%;
            font-family: Arial, sans-serif;
            overflow: hidden;
            color: white;
            animation: gradientShift 15s ease infinite;
        }

        @keyframes gradientShift {
            0% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
            100% { background-position: 0% 50%; }
        }

        .stars, .hearts, .final-explosion {
            position: fixed; top: 0; left: 0; width: 100%; height: 100%;
            pointer-events: none;
        }
        .stars { z-index: 1; }
        .hearts { z-index: 5; }
        .final-explosion { z-index: 50; }

        .star {
            position: absolute; width: 2px; height: 2px; background: white;
            border-radius: 50%; animation: twinkle 2s infinite;
        }
        @keyframes twinkle { 0%,100%{opacity:.3;transform:scale(1);} 50%{opacity:1;transform:scale(1.5);} }

        .heart {
            position: absolute; font-size: 20px;
            animation: floatUp 6s linear forwards;
        }
        @keyframes floatUp {
            0% { transform: translateY(100vh) translateX(0) rotate(0deg) scale(0); opacity: 1; }
            20% { transform: translateY(80vh) translateX(20%) rotate(90deg) scale(1); }
            50% { transform: translateY(50vh) translateX(-10%) rotate(180deg) scale(1.2); }
            80% { transform: translateY(20vh) translateX(30%) rotate(270deg) scale(1); }
            100% { transform: translateY(-100px) translateX(-20%) rotate(360deg) scale(0); opacity: 0; }
        }

        .sparkle {
            position: absolute; width: 3px; height: 3px; background: #ffd700;
            border-radius: 50%; animation: sparkleBurst 3s infinite;
        }
        @keyframes sparkleBurst {
            0%, 100% { transform: scale(0) rotate(0deg); opacity: 0; }
            50% { transform: scale(1.5) rotate(180deg); opacity: 1; }
        }

        /* SPECIAL POPUPS */
        .special-message, .warning-message {
            position: fixed; top: 50%; left: 50%; transform: translate(-50%, -50%);
            color: #fff; padding: 30px; border-radius: 25px; text-align: center;
            display: none; backdrop-filter: blur(15px); z-index: 1000;
            font-size: clamp(1.1em, 4vw, 1.4em); line-height: 1.4; max-width: 85vw;
        }
        .special-message {
            background: linear-gradient(135deg, rgba(255,193,7,0.95), rgba(255,152,0,0.9));
            box-shadow: 0 20px 60px rgba(255,193,7,0.5); border: 2px solid #ffd700;
            animation: specialPop 0.5s ease-out;
        }
        .warning-message {
            background: rgba(255, 0, 0, 0.9);
            box-shadow: 0 0 40px rgba(255,0,0,0.6); border: 2px solid white;
            animation: specialPop 0.3s ease-out;
        }
        @keyframes specialPop {
            0% { transform: translate(-50%, -50%) scale(0.5); opacity: 0; }
            100% { transform: translate(-50%, -50%) scale(1); opacity: 1; }
        }

        .container {
            text-align: center; max-width: 90vw; width: 100%; z-index: 10; padding: 20px;
        }
        .title {
            font-size: clamp(1.5em, 5vw, 2em); margin-bottom: 15px;
            background: linear-gradient(45deg, #ffd700, #ff6b9d);
            -webkit-background-clip: text; -webkit-text-fill-color: transparent;
            animation: glow 2s ease-in-out infinite alternate;
        }
        @keyframes glow { from { filter: drop-shadow(0 0 5px #ffd700); } to { filter: drop-shadow(0 0 20px #ff6b9d); } }

        .question {
            font-size: clamp(1.6em, 6vw, 2.2em); margin-bottom: 35px; 
            text-shadow: 2px 2px 4px rgba(0,0,0,0.4); line-height: 1.3;
            animation: heartbeat 2s infinite;
        }
        @keyframes heartbeat { 0%,100% { transform: scale(1); } 50% { transform: scale(1.05); } }

        .progress { display: flex; justify-content: center; gap: 8px; margin-bottom: 25px; }
        .progress-dot {
            width: 14px; height: 14px; border-radius: 50%; background: rgba(255,255,255,0.4);
            transition: all 0.4s ease;
        }
        .progress-dot.active { background: #ffd700; transform: scale(1.3); box-shadow: 0 0 12px #ffd700; }
        .progress-dot.completed { background: #ff6b9d; box-shadow: 0 0 12px #ff6b9d; }

        .buttons { display: flex; gap: 15px; justify-content: center; flex-wrap: wrap; }
        button {
            padding: 15px 25px; font-size: clamp(1em, 3.5vw, 1.3em); 
            border: none; border-radius: 35px; cursor: pointer; font-weight: bold;
            box-shadow: 0 8px 25px rgba(0,0,0,0.3); position: relative; z-index: 20;
            min-height: 55px; touch-action: manipulation; flex: 1; max-width: 200px;
        }
        .yes {
            background: linear-gradient(45deg, #00d4ff, #0099cc); color: white;
        }
        .yes:hover, .yes:active { 
            transform: scale(1.05); box-shadow: 0 12px 35px rgba(0,212,255,0.6); 
        }
        .no {
            background: linear-gradient(45deg, #ff4757, #ff3838); color: white; 
        }
        .final-yes {
            background: linear-gradient(45deg, #ffd700, #ffed4e); color: #c44569;
            font-size: clamp(1.1em, 4vw, 1.5em); padding: 18px 35px;
            animation: pulse 1.5s infinite;
        }
        @keyframes pulse {
            0% { box-shadow: 0 0 0 0 rgba(255,215,0,0.7); }
            70% { box-shadow: 0 0 0 20px rgba(255,215,0,0); }
            100% { box-shadow: 0 0 0 0 rgba(255,215,0,0); }
        }

        .message {
            position: fixed; top: 50%; left: 50%; transform: translate(-50%, -50%);
            background: linear-gradient(135deg, rgba(255,255,255,0.95), rgba(255,245,245,0.98));
            color: #c44569; padding: clamp(30px, 10vw, 70px); border-radius: 30px;
            text-align: center; line-height: 1.4; box-shadow: 0 30px 80px rgba(0,0,0,0.6);
            max-width: 90vw; width: 90%; display: none; backdrop-filter: blur(20px); z-index: 100;
            border: 2px solid rgba(255,215,0,0.4); animation: messagePop 1.5s ease-out;
            max-height: 85vh; overflow-y: auto;
        }
        @keyframes messagePop {
            0% { transform: translate(-50%, -50%) scale(0.7); opacity: 0; }
            50% { transform: translate(-50%, -50%) scale(1.02); opacity: 0.9; }
            100% { transform: translate(-50%, -50%) scale(1); opacity: 1; }
        }

        .message h1 {
            font-size: clamp(2em, 8vw, 4em); margin-bottom: 20px;
            background: linear-gradient(45deg, #ff6b9d, #ffd700, #ff1493);
            -webkit-background-clip: text; -webkit-text-fill-color: transparent;
            animation: titleBounce 2s infinite;
        }
        .message h2 {
            font-size: clamp(1.8em, 6vw, 2.8em); margin-bottom: 25px; color: #ff6b9d;
            animation: heartbeatGlow 2s infinite; line-height: 1.2;
        }
        .love-line {
            font-size: clamp(1.1em, 4vw, 1.4em); margin: 18px 0; opacity: 0;
            animation: fadeInUp 1s ease forwards;
        }
        .love-line:nth-child(3) { animation-delay: 0.3s; }
        .love-line:nth-child(4) { animation-delay: 0.6s; }
        .love-line:nth-child(5) { animation-delay: 0.9s; }
        @keyframes fadeInUp {
            0% { opacity: 0; transform: translateY(25px); }
            100% { opacity: 1; transform: translateY(0); }
        }
        .signature {
            font-size: clamp(1.1em, 4vw, 1.5em); margin-top: 30px; color: #00d4ff;
            animation: rainbow 3s infinite; font-weight: bold;
        }
        @keyframes rainbow { 0% { filter: hue-rotate(0deg); } 100% { filter: hue-rotate(360deg); } }
    </style>
</head>
<body>
    <div class="stars" id="stars"></div>
    <div class="hearts" id="hearts"></div>
    <div class="final-explosion" id="finalExplosion"></div>
    
    <div class="warning-message" id="warningMsg">btau abhi😒</div>
    
    <div class="special-message" id="specialMessage">
        Tu chahti toh baby wale pe bhi click kr skti thi 🥲<br>
        Nvm I lovee youuu h na baby ❤️
    </div>
    
    <div class="container" id="quizContainer">
        <div class="title">Miku's Love Quiz 💝</div>
        <div class="progress" id="progress">
            <div class="progress-dot active"></div><div class="progress-dot"></div><div class="progress-dot"></div>
            <div class="progress-dot"></div><div class="progress-dot"></div>
        </div>
        <div class="question" id="question">Do you love me more than McDonald's? 🍔😍</div>
        <div class="buttons">
            <button class="yes" id="yesBtn" onclick="nextQuestion()">Yes I do</button>
            <button class="no" id="noButton">Nope</button>
        </div>
    </div>
    
    <div class="message" id="message">
        <h1>🎉 PERFECT 5/5! 🎉</h1>
        <h2>Miku, you're my FOREVER! 💍</h2>
        <div class="love-line">You're not just my girlfriend, you're my <strong>sunshine 🌞</strong></div>
        <div class="love-line">you're my <strong>heartbeat 💓</strong> and <strong>adventure 🏔️</strong></div>
        <div class="love-line"><em>Every laugh with you feels like magic ✨</em></div>
        <div class="signature">Made with ∞ love for my Miku ❤️</div>
    </div>

    <script>
        const questions = [
            "Do you love me more than McDonald's? 🍔😍",
            "Do you smile when you see my name pop up? 📱🥰",
            "Prabhat is your favourite distraction?",
            "Who is the best person you have ever met in your life?",
            "Miku, will you be my Valentine? 💝❤️"
        ];
        
        const yesLabels = ["Yes I do", "Yes I do", "Yes he is", "Prabhat", "YES! I WILL! 💍"];
        let currentQuestion = 0;
        let nopeClickCount = 0;
        
        document.addEventListener('DOMContentLoaded', () => {
            setupLogic();
            createStars();
        });

        function moveButton() {
            if (currentQuestion !== 3) {
                const noBtn = document.getElementById('noButton');
                const x = Math.random() * (window.innerWidth - 150);
                const y = Math.random() * (window.innerHeight - 100);
                noBtn.style.position = 'fixed';
                noBtn.style.left = x + 'px';
                noBtn.style.top = y + 'px';
                noBtn.style.zIndex = '1000';
            }
        }
        
        function setupLogic() {
            const noBtn = document.getElementById('noButton');
            noBtn.style.position = 'relative';
            noBtn.style.left = '0';
            noBtn.style.top = '0';

            if (currentQuestion === 3) {
                noBtn.textContent = "It's you baby 💋";
                noBtn.onmouseenter = null; 
                noBtn.ontouchstart = null;
                noBtn.onclick = () => { currentQuestion++; updateQuestion(); };
            } else {
                noBtn.textContent = "Nope";
                noBtn.onmouseenter = moveButton;
                noBtn.ontouchstart = (e) => { e.preventDefault(); moveButton(); };
                noBtn.onclick = () => {
                    if (currentQuestion < 3) {
                        nopeClickCount++;
                        if (nopeClickCount >= 2) {
                            showWarning();
                            nopeClickCount = 0; 
                        }
                    }
                };
            }
        }

        function showWarning() {
            const w = document.getElementById('warningMsg');
            w.style.display = 'block';
            document.body.style.pointerEvents = 'none'; // Freeze screen
            setTimeout(() => {
                w.style.display = 'none';
                document.body.style.pointerEvents = 'auto'; // Resume
            }, 2000);
        }
        
        function nextQuestion() {
            if (currentQuestion === 3) {
                document.getElementById('specialMessage').style.display = 'block';
                document.body.style.pointerEvents = 'none';
                setTimeout(() => {
                    document.getElementById('specialMessage').style.display = 'none';
                    document.body.style.pointerEvents = 'auto';
                    currentQuestion++;
                    updateQuestion();
                }, 3500);
            } else {
                currentQuestion++;
                updateQuestion();
            }
        }
        
        function updateQuestion() {
            const dots = document.querySelectorAll('.progress-dot');
            if (dots[currentQuestion]) dots[currentQuestion].classList.add('active');
            if (dots[currentQuestion-1]) dots[currentQuestion-1].classList.add('completed');
            
            if (currentQuestion < questions.length) {
                document.getElementById('question').textContent = questions[currentQuestion];
                document.getElementById('yesBtn').textContent = yesLabels[currentQuestion];
                if (currentQuestion === 4) document.getElementById('yesBtn').classList.add('final-yes');
                setupLogic();
                createHearts(15);
            } else {
                showFinalMessage();
            }
        }

        function createStars() {
            const starsContainer = document.getElementById('stars');
            for (let i = 0; i < 80; i++) {
                const star = document.createElement('div');
                star.className = 'star';
                star.style.left = Math.random() * 100 + '%';
                star.style.top = Math.random() * 100 + '%';
                star.style.animationDelay = Math.random() * 2 + 's';
                starsContainer.appendChild(star);
            }
        }

        function createHearts(count) {
            const heartsContainer = document.getElementById('hearts');
            for (let i = 0; i < count; i++) {
                setTimeout(() => {
                    const heart = document.createElement('div');
                    heart.className = 'heart';
                    heart.innerHTML = '💖';
                    heart.style.left = Math.random() * 100 + '%';
                    heart.style.animationDuration = (3 + Math.random() * 3) + 's';
                    heartsContainer.appendChild(heart);
                    setTimeout(() => heart.remove(), 7000);
                }, i * 25);
            }
        }

        function showFinalMessage() {
            document.getElementById('quizContainer').style.display = 'none';
            document.getElementById('message').style.display = 'block';
            const explosionContainer = document.getElementById('finalExplosion');
            setInterval(() => {
                const sparkle = document.createElement('div');
                sparkle.className = 'sparkle';
                sparkle.style.left = Math.random() * 100 + '%';
                sparkle.style.top = Math.random() * 100 + '%';
                explosionContainer.appendChild(sparkle);
                setTimeout(() => sparkle.remove(), 3000);
            }, 500);
            createHearts(80);
        }
 </script>     
</body>
</html>
