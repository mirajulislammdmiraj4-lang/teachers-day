<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Happy Teachers' Day 💖</title>
    <style>
        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }

        body {
            background: linear-gradient(135deg, #ffe6f0 0%, #fff0f5 100%);
            font-family: 'Poppins', sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            overflow: hidden;
            position: relative;
        }

        .container {
            text-align: center;
            position: relative;
            width: 100%;
            max-width: 400px;
            z-index: 10;
        }

        /* Header Text */
        h1 {
            color: #ff4081;
            font-size: 26px;
            margin-bottom: 20px;
            text-shadow: 1px 1px 2px rgba(0,0,0,0.05);
        }

        .heart {
            color: #ff1744;
            display: inline-block;
            animation: pulse 0.8s infinite alternate;
        }

        @keyframes pulse {
            0% { transform: scale(1); }
            100% { transform: scale(1.25); }
        }

        /* Cake Wrapper - মার্জিন বাড়িয়ে মোমবাতিকে লেখা থেকে নিচে নামানো হয়েছে */
        .cake-wrapper {
            position: relative;
            margin: 100px auto 20px; 
            width: 220px;
        }

        .cake-base {
            position: relative;
            width: 220px;
            height: 120px;
            background: linear-gradient(to bottom, #ffb74d 0%, #f48fb1 40%, #f06292 100%);
            border-radius: 20px 20px 15px 15px;
            box-shadow: 0 12px 25px rgba(240, 98, 146, 0.3), inset 0 -5px 10px rgba(0,0,0,0.1);
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
        }

        /* Cream Frosting & Drips */
        .cream-top {
            position: absolute;
            top: -15px;
            left: 0;
            width: 100%;
            height: 35px;
            background: #ffffff;
            border-radius: 20px 20px 10px 10px;
            box-shadow: 0 4px 6px rgba(0,0,0,0.05);
        }

        .cream-drips {
            position: absolute;
            top: 15px;
            left: 0;
            width: 100%;
            display: flex;
            justify-content: space-around;
        }

        .drip {
            width: 20px;
            height: 18px;
            background: #ffffff;
            border-radius: 0 0 10px 10px;
        }

        /* Cherries on Cake */
        .cherries {
            position: absolute;
            top: -28px;
            width: 100%;
            display: flex;
            justify-content: space-between;
            padding: 0 15px;
            box-sizing: border-box;
        }

        .cherry {
            width: 16px;
            height: 16px;
            background: #d50000;
            border-radius: 50%;
            box-shadow: inset -2px -2px 4px rgba(0,0,0,0.3);
        }

        .cake-text {
            color: #ffffff;
            font-weight: 700;
            font-size: 16px;
            text-shadow: 1px 2px 4px rgba(216, 27, 96, 0.5);
            margin-top: 15px;
            z-index: 2;
            letter-spacing: 0.5px;
        }

        /* Candles Style */
        .candles {
            position: absolute;
            top: -55px;
            width: 100%;
            display: flex;
            justify-content: center;
            gap: 35px;
            z-index: 5;
        }

        .candle {
            width: 12px;
            height: 42px;
            background: repeating-linear-gradient(45deg, #ba68c8, #ba68c8 5px, #ffffff 5px, #ffffff 10px);
            border-radius: 4px;
            position: relative;
            cursor: pointer;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
        }

        /* Candle Flame */
        .flame {
            width: 12px;
            height: 20px;
            background: linear-gradient(to top, #ff9800, #ffeb3b);
            border-radius: 50% 50% 20% 20%;
            position: absolute;
            top: -20px;
            box-shadow: 0 0 12px #ffeb3b, 0 0 22px #ff9800;
            animation: flicker 0.5s infinite alternate ease-in-out;
        }

        @keyframes flicker {
            0% { transform: scale(1) rotate(-3deg); opacity: 0.95; }
            100% { transform: scale(1.15) rotate(3deg); opacity: 1; }
        }

        .flame.off {
            display: none;
        }

        .instruction {
            color: #ec407a;
            font-size: 14px;
            margin-top: 25px;
            font-weight: 600;
        }

        /* Sparkle Confetti */
        .sparkle {
            position: absolute;
            width: 10px;
            height: 10px;
            border-radius: 50%;
            pointer-events: none;
            z-index: 99;
            animation: burst 1.2s ease-out forwards;
        }

        @keyframes burst {
            0% { opacity: 1; transform: translate(0, 0) scale(1); }
            100% { opacity: 0; transform: translate(var(--dx), var(--dy)) scale(0.2); }
        }

        /* Message Card */
        .card {
            display: none;
            width: 320px;
            background: rgba(255, 255, 255, 0.95);
            backdrop-filter: blur(5px);
            padding: 28px 22px;
            border-radius: 20px;
            box-shadow: 0 15px 35px rgba(240, 98, 146, 0.25);
            text-align: center;
            margin: 0 auto;
            border: 2px solid #f8bbd0;
            opacity: 0;
            transform: scale(0.2) rotate(-10deg);
            transition: all 0.8s cubic-bezier(0.175, 0.885, 0.32, 1.275);
        }

        .card.show {
            display: block;
            opacity: 1;
            transform: scale(1) rotate(0deg);
        }

        .card h2 {
            color: #d81b60;
            font-size: 21px;
            margin-bottom: 15px;
        }

        .card p {
            color: #444;
            font-size: 14px;
            line-height: 1.6;
        }
    </style>
</head>
<body>

    <div class="container">
        <!-- Screen 1: Cute Cake Screen -->
        <div id="cakeScreen">
            <h1>Happy Teachers' Day <span class="heart">❤️</span></h1>
            
            <div class="cake-wrapper">
                <!-- Candles -->
                <div class="candles">
                    <div class="candle" onclick="extinguish(this)"><div class="flame"></div></div>
                    <div class="candle" onclick="extinguish(this)"><div class="flame"></div></div>
                    <div class="candle" onclick="extinguish(this)"><div class="flame"></div></div>
                </div>

                <!-- Cherries -->
                <div class="cherries">
                    <div class="cherry"></div>
                    <div class="cherry"></div>
                    <div class="cherry"></div>
                </div>

                <!-- Cake Body -->
                <div class="cake-base">
                    <div class="cream-top"></div>
                    <div class="cream-drips">
                        <div class="drip"></div>
                        <div class="drip"></div>
                        <div class="drip"></div>
                        <div class="drip"></div>
                    </div>
                    <span class="cake-text">Happy Teachers' Day</span>
                </div>
            </div>

            <p class="instruction">✨ Tap each candle to blow it out! ✨</p>
        </div>

        <!-- Screen 2: Message Card -->
        <div id="letterCard" class="card">
            <h2>Happy Teachers' Day, Ma’am! 🌸💐</h2>
            <p>
                You are not just a teacher, but a wonderful mentor and an inspiration to us. Thank you for your guidance, kindness, and for always believing in us. ❤️<br><br>
                Wishing you endless happiness and success. Happy Teachers' Day, Ma’am! 🌷
            </p>
        </div>
    </div>

    <script>
        let extinguishedCount = 0;

        function extinguish(candleElement) {
            const flame = candleElement.querySelector('.flame');
            if (flame && !flame.classList.contains('off')) {
                flame.classList.add('off');
                extinguishedCount++;
            }

            if (extinguishedCount === 3) {
                setTimeout(() => {
                    triggerSparkles();
                    document.getElementById('cakeScreen').style.display = 'none';
                    const card = document.getElementById('letterCard');
                    card.classList.add('show');
                }, 500);
            }
        }

        function triggerSparkles() {
            const colors = ['#ff4081', '#e040fb', '#ffeb3b', '#00e676', '#ff80ab', '#00bcd4'];
            
            for (let i = 0; i < 70; i++) {
                const sparkle = document.createElement('div');
                sparkle.className = 'sparkle';
                sparkle.style.backgroundColor = colors[Math.floor(Math.random() * colors.length)];
                sparkle.style.left = '50%';
                sparkle.style.top = '50%';

                const angle = Math.random() * Math.PI * 2;
                const velocity = 120 + Math.random() * 220;
                const dx = Math.cos(angle) * velocity + 'px';
                const dy = Math.sin(angle) * velocity + 'px';

                sparkle.style.setProperty('--dx', dx);
                sparkle.style.setProperty('--dy', dy);

                document.body.appendChild(sparkle);
                setTimeout(() => sparkle.remove(), 1200);
            }
        }
    </script>
</body>
</html>
