
<html lang="en"> 
 <head> 
  <meta charset="UTF-8"> 
  <meta name="viewport" content="width=device-width, initial-scale=1.0"> 
  <title>Eid Mubarak Greetings</title> 
  <link href="https://fonts.googleapis.com/css2?family=Dancing+Script:wght@700&amp;family=Great+Vibes&amp;family=Roboto:wght@400;700&amp;display=swap" rel="stylesheet"> 
  <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            background: linear-gradient(135deg, #2c5f2d, #e3c08d);
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            font-family: 'Roboto', sans-serif;
            overflow: hidden;
            text-align: center;
            padding: 20px;
            position: relative;
        }

        .container {
            background: rgba(255, 255, 255, 0.9);
            padding: 2rem;
            border-radius: 15px;
            box-shadow: 0 0 20px rgba(255, 215, 0, 0.5);
            max-width: 600px;
            width: 90%;
            animation: slideIn 1s forwards, glowBorder 2s infinite alternate;
            border: 3px solid #ffdd44;
            position: relative;
            z-index: 2;
        }

        @keyframes glowBorder {
            0% {
                box-shadow: 0 0 10px #ffdd44, 0 0 20px #ffcc00;
            }
            100% {
                box-shadow: 0 0 15px #ffdd44, 0 0 25px #ffcc00;
            }
        }

        h1 {
            font-family: 'Great Vibes', cursive;
            font-size: 3rem;
            color: #2c5f2d;
            margin-bottom: 1rem;
            text-shadow: 0 0 10px #fff, 0 0 25px #ffdd44;
            animation: glow 2s infinite alternate;
        }

        @keyframes glow {
            0% {
                text-shadow: 0 0 10px #fff, 0 0 25px #ffdd44;
            }
            100% {
                text-shadow: 0 0 15px #fff, 0 0 30px #ffcc00;
            }
        }

        .message {
            font-size: 1.2rem;
            font-family: 'Dancing Script', cursive;
            color: #333;
            line-height: 1.6;
            overflow: hidden;
            display: inline-block;
            white-space: normal;
            text-align: center;
            width: 100%;
            text-shadow: 0 0 5px #ffdd44, 0 0 10px #ffcc00;
        }

        @keyframes slideIn {
            from {
                transform: translateY(-50%);
                opacity: 0;
            }
            to {
                transform: translateY(0);
                opacity: 1;
            }
        }

        /* Floating Moon */
        .moon {
            position: absolute;
            top: 10%;
            left: 50%;
            transform: translateX(-50%);
            font-size: 5rem;
            animation: float 4s infinite ease-in-out;
        }

        @keyframes float {
            0%, 100% {
                transform: translateX(-50%) translateY(0);
            }
            50% {
                transform: translateX(-50%) translateY(-15px);
            }
        }

        /* Floating Stars */
        .stars span {
            position: absolute;
            font-size: 1.5rem;
            opacity: 0.8;
            animation: twinkle 2s infinite alternate;
        }

        @keyframes twinkle {
            0% { opacity: 0.5; transform: scale(1); }
            100% { opacity: 1; transform: scale(1.2); }
        }

        @media (max-width: 768px) {
            h1 {
                font-size: 2.5rem;
            }
            .message {
                font-size: 1.1rem;
            }
        }
    </style> 
 </head> 
 <body> <!-- Floating Decorations --> 
  <div class="decorations"> 
   <div class="moon">
    🌙
   </div> 
   <div class="stars"> <span style="top: 10%; left: 10%">✨</span> <span style="top: 20%; right: 15%">⭐</span> <span style="bottom: 25%; left: 30%">🌟</span> <span style="top: 50%; right: 10%">✨</span> <span style="bottom: 40%; left: 50%">⭐</span> <span style="top: 70%; right: 30%">🌟</span> 
   </div> 
  </div> <!-- Main Content --> 
  <div class="container"> 
   <h1>Eid Mubarak</h1> 
   <p class="message" id="eidMessage"></p> 
  </div> 
  <script>
        const messageText = `On this blessed occasion of Eid, may your heart be filled with joy, your home be filled with peace, and your life be blessed with endless happiness.\n
        May Allah’s divine light guide your path, His mercy surround you, and His love uplift your spirit. \n
        Let this Eid be a reminder to cherish every moment, spread kindness, and embrace gratitude. Wishing you a day filled with laughter, love, and countless blessings!\n
        
        ✨ Eid Mubarak! ✨`;
        
        let i = 0;
        function typeEffect() {
            if (i < messageText.length) {
                document.getElementById("eidMessage").textContent += messageText.charAt(i);
                i++;
                setTimeout(typeEffect, 40);
            }
        }

        window.addEventListener('load', typeEffect);

        function addStars() {
            const starsContainer = document.querySelector('.stars');
            for (let i = 0; i < 6; i++) {
                const star = document.createElement('span');
                star.style.top = Math.random() * 100 + '%';
                star.style.left = Math.random() * 100 + '%';
                star.textContent = Math.random() > 0.5 ? '✨' : '⭐';
                star.style.animationDuration = Math.random() * 3 + 1 + 's';
                starsContainer.appendChild(star);
            }
        }

        window.addEventListener('load', addStars);
    </script> 
 </body>
</html>
