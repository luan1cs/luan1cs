
<!---<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Jogo de Clicar no Avião</title>
    <style>
        body {
            margin: 0;
            overflow: hidden;
        }
        canvas {
            display: block;
        }
    </style>
</head>
<body>
    <canvas id="gameCanvas"></canvas>
    <script>
        const canvas = document.getElementById('gameCanvas');
        const context = canvas.getContext('2d');
        canvas.width = window.innerWidth;
        canvas.height = window.innerHeight;

        let score = 0;

        class Airplane {
            constructor() {
                this.width = 60;
                this.height = 60;
                this.x = Math.random() * (canvas.width - this.width);
                this.y = Math.random() * (canvas.height - this.height);
                this.image = new Image();
                this.image.src = 'https://example.com/airplane.png'; // URL da imagem do avião
            }

            draw() {
                context.drawImage(this.image, this.x, this.y, this.width, this.height);
            }

            update() {
                this.x = Math.random() * (canvas.width - this.width);
                this.y = Math.random() * (canvas.height - this.height);
            }
        }

        const airplane = new Airplane();

        canvas.addEventListener('click', (event) => {
            const x = event.clientX;
            const y = event.clientY;

            if (x > airplane.x && x < airplane.x + airplane.width && y > airplane.y && y < airplane.y + airplane.height) {
                score++;
                airplane.update();
                alert(`Você clicou no avião! Pontuação: ${score}`);
            }
        });

        function gameLoop() {
            context.clearRect(0, 0, canvas.width, canvas.height);
            airplane.draw();
            requestAnimationFrame(gameLoop);
        }

        gameLoop();
    </script>
</body>
</html>

luan1cs/luan1cs is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
