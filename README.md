# Can yoldaşım ❤️‍🩹
<!DOCTYPE html>
<html lang="tr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Doğum Günün Kutlu Olsun ❤️</title>
    <style>
        body {
            margin: 0;
            padding: 0;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, #ff9a9e 0%, #fad0c4 100%);
            color: #333;
            min-height: 100vh;
            display: flex;
            flex-direction: column;
            align-items: center;
            text-align: center;
            overflow-x: hidden;
        }

        .container {
            max-width: 900px;
            padding: 40px 20px;
            background: rgba(255, 255, 255, 0.95);
            border-radius: 20px;
            box-shadow: 0 15px 35px rgba(0,0,0,0.1);
            margin: 20px;
        }

        h1 {
            font-size: 3.5em;
            color: #e91e63;
            margin-bottom: 20px;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.1);
        }

        .gallery {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
            margin: 40px 0;
        }

        .gallery img {
            width: 100%;
            height: auto;
            max-height: 400px;
            object-fit: cover;
            border-radius: 15px;
            box-shadow: 0 10px 20px rgba(0,0,0,0.2);
            transition: transform 0.3s;
        }

        .gallery img:hover {
            transform: scale(1.05);
        }

        .message {
            font-size: 1.4em;
            line-height: 1.9;
            margin: 40px 0;
            color: #555;
        }

        .heart {
            color: #e91e63;
            font-size: 1.5em;
            animation: pulse 2s infinite;
        }

        @keyframes pulse {
            0% { transform: scale(1); }
            50% { transform: scale(1.2); }
            100% { transform: scale(1); }
        }

        .memories {
            margin-top: 50px;
            font-style: italic;
            color: #e91e63;
            font-size: 1.6em;
            font-weight: bold;
            background: rgba(255,105,180,0.1);
            padding: 20px;
            border-radius: 15px;
        }

        footer {
            margin-top: 50px;
            color: #999;
            font-size: 0.9em;
        }

        .confetti {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            z-index: -1;
        }
    </style>
</head>
<body>
    <div class="confetti" id="confetti"></div>
    
    <div class="container">
        <h1>Doğum Günün Kutlu Olsun! 🎉❤️</h1>
        
        <div class="gallery">
            <!-- Tüm fotoğraflar burada (base64) -->
            <img src="data:image/jpeg;base64,/9j/4AAQSkZJRgABAQAAAQABAAD/2wCEAAkGBxISEhUTExMWFh..." alt="Anı 1">
            <img src="data:image/jpeg;base64,/9j/4AAQSkZJRgABAQAAAQABAAD/2wCEAAkGBx..." alt="Anı 2">
            <img src="data:image/jpeg;base64,/9j/4AAQSkZJRgABAQAAAQABAAD/2wCEAA..." alt="Anı 3">
            <img src="data:image/jpeg;base64,/9j/4AAQSkZJRgABAQEAYABgAD/2wBDAA..." alt="Anı 4">
            <img src="data:image/jpeg;base64,/9j/4AAQSkZJRgABAQAAAQABAAD/2wBDAAoHB..." alt="Anı 5">
            <img src="data:image/jpeg;base64,/9j/4AAQSkZJRgABAQAAAQABAAD/2wCEAAkGB..." alt="Anı 6">
            <img src="data:image/jpeg;base64,/9j/4AAQSkZJRgABAQAAAQABAAD/2wCEA..." alt="Anı 7">
            <img src="data:image/jpeg;base64,/9j/4AAQSkZJRgABAQAAAQABAAD/2wBDAA..." alt="Anı 8">
        </div>

        <div class="message">
            <p>Sevgili güzelim,</p>
            <p>Bugün senin günün... Yeni yaşın sana sağlık, mutluluk, bol kahkaha ve hayallerinin gerçekleşmesini getirsin.</p>
            <p>Biliyorum artık ayrı yollara gittik ama o eski günler hâlâ aklımda. Birlikte geçirdiğimiz zamanlar, gülüşmelerimiz, deli dolu anlarımız... Hepsi çok özeldi.</p>
            <p><span class="heart">❤️</span></p>
        </div>

        <div class="memories">
            En çok mutlu eden kişi sendin ama kaderimiz belliydi güzelim... 
            Yine de iyi ki varsın, iyi ki bir dönem hayatımdın. 
            Doğum günün kutlu olsun, her zaman gül yüzün gülsün. 🎂✨
        </div>
        
        <footer>
            Senin için en güzel dileklerle...
        </footer>
    </div>

    <!-- Konfeti efekti aynı kaldı -->
    <script>
        const confettiCanvas = document.getElementById('confetti');
        const ctx = confettiCanvas.getContext('2d');
        confettiCanvas.width = window.innerWidth;
        confettiCanvas.height = window.innerHeight;

        const confetti = [];
        const colors = ['#f44336', '#e91e63', '#9c27b0', '#2196f3', '#ff9800'];

        for (let i = 0; i < 200; i++) {
            confetti.push({
                x: Math.random() * confettiCanvas.width,
                y: Math.random() * confettiCanvas.height - confettiCanvas.height,
                r: Math.random() * 4 + 1,
                d: Math.random() * 3 + 1,
                color: colors[Math.floor(Math.random() * colors.length)],
                tilt: Math.random() * 10 - 10,
                tiltAngleIncrement: Math.random() * 0.07 + 0.05,
                tiltAngle: 0
            });
        }

        function draw() {
            ctx.clearRect(0, 0, confettiCanvas.width, confettiCanvas.height);
            
            confetti.forEach((piece, i) => {
                piece.y += piece.d;
                piece.tiltAngle += piece.tiltAngleIncrement;
                piece.tilt = Math.sin(piece.tiltAngle) * 15;

                if (piece.y > confettiCanvas.height) {
                    confetti[i] = {
                        ...piece,
                        y: -10,
                        x: Math.random() * confettiCanvas.width
                    };
                }

                ctx.beginPath();
                ctx.lineWidth = piece.r;
                ctx.strokeStyle = piece.color;
                ctx.moveTo(piece.x + piece.tilt + piece.r / 2, piece.y);
                ctx.lineTo(piece.x + piece.tilt, piece.y + piece.tilt + piece.r / 2);
                ctx.stroke();
            });

            requestAnimationFrame(draw);
        }

        draw();

        window.addEventListener('resize', () => {
            confettiCanvas.width = window.innerWidth;
            confettiCanvas.height = window.innerHeight;
        });
    </script>
</body>
</html>
