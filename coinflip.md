<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Coin Flip Game</title>
    <style>
        #coin {
            width: 100px;
            height: 100px;
            background-image: url('https://upload.wikimedia.org/wikipedia/commons/6/6f/6i_cropped.png');
            background-size: cover;
            cursor: pointer;
        }
    </style>
</head>
<body>
    <h1>Coin Flip Game</h1>
    <p>Click the coin to flip it!</p>
    <div id="coin"></div>
    <p id="result"></p>
    <button onclick="flipCoin()">Flip Coin</button>

    <script>
        function flipCoin() {
            const coin = document.getElementById('coin');
            const result = document.getElementById('result');

            // Randomly choose heads or tails
            const randomNumber = Math.random();
            const resultText = randomNumber < 0.5 ? 'Heads' : 'Tails';

            // Rotate the coin to simulate the flip
            coin.style.transition = 'transform 0.5s';
            setTimeout(() => {
                coin.style.transform = 'rotateY(180deg)';
                setTimeout(() => {
                    // Update the coin image after the flip animation
                    coin.style.backgroundImage = `url('${resultText === 'Heads' ? 'https://upload.wikimedia.org/wikipedia/commons/6/6f/6i_cropped.png' : 'https://upload.wikimedia.org/wikipedia/commons/thumb/d/d7/10i_cropped.png/106px-10i_cropped.png'}')`;
                    setTimeout(() => {
                        // Display the result
                        result.textContent = `Result: ${resultText}`;
                        coin.style.transform = 'rotateY(0deg)';
                        coin.style.transition = 'none';
                    }, 500);
                }, 250);
            }, 100);

            // Clear the previous result
            result.textContent = '';
        }
    </script>
</body>
</html>
