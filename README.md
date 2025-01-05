<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Do You Love Me?</title>
    <style>
        body {
            font-family: 'Comic Sans MS', cursive, sans-serif;
            background-color: #fff0f5;
            color: #4b0082;
            text-align: center;
            padding: 20px;
        }
        h1 {
            color: #ff1493;
            font-size: 2.5rem;
        }
        .gif-container {
            margin: 20px 0;
        }
        button {
            padding: 10px 20px;
            font-size: 18px;
            color: white;
            background-color: #ff1493;
            border: none;
            border-radius: 10px;
            cursor: pointer;
            margin: 10px;
            transition: transform 0.3s, background-color 0.3s;
        }
        button:hover {
            background-color: #ff69b4;
            transform: scale(1.1);
        }
        #noo-button {
            position: relative;
        }
    </style>
    <script>
        let nooClickCount = 0;

        function handleYes() {
            document.body.innerHTML = `
                <h1>Love you too! 😘😘</h1>
                <div class="gif-container">
                    <img src="https://media.giphy.com/media/Z21HJj2kz9uBG/giphy.gif" alt="Kissing Cats GIF" width="300">
                </div>
            `;
        }

        function handleNo() {
            nooClickCount++;
            if (nooClickCount === 1) {
                document.body.innerHTML = `
                    <h1>Please yess press kar do naaa 😢</h1>
                    <div class="gif-container">
                        <img src="https://media.giphy.com/media/L95W4wv8nnb9K/giphy.gif" alt="Sad Cat GIF" width="300">
                    </div>
                    <button onclick="handleYes()">Yess</button>
                    <button id="noo-button" onclick="handleNo()">Noo</button>
                `;
            } else if (nooClickCount === 2) {
                document.body.innerHTML = `
                    <h1>Pls baby maan jao naaa 🥺💕</h1>
                    <div class="gif-container">
                        <img src="https://media.giphy.com/media/MDJ9IbxxvDUQM/giphy.gif" alt="Cute Cat Love GIF" width="300">
                    </div>
                    <button onclick="handleYes()">Yess</button>
                    <button id="noo-button" onclick="handleNo()">Noo</button>
                `;
            } else {
                const nooButton = document.getElementById('noo-button');
                nooButton.style.position = 'absolute';
                nooButton.style.top = `${Math.random() * 80 + 10}%`;
                nooButton.style.left = `${Math.random() * 80 + 10}%`;
            }
        }

        function finalYes() {
            document.body.innerHTML = `
                <h1>Mujhe pata tha tum maan jaogi! Love youu too baby ❤️🫂</h1>
                <div class="gif-container">
                    <img src="https://media.giphy.com/media/Z21HJj2kz9uBG/giphy.gif" alt="Kissing Cats GIF" width="300">
                </div>
                <div class="gif-container">
                    <img src="https://media.giphy.com/media/MDJ9IbxxvDUQM/giphy.gif" alt="Happy Cat GIF" width="300">
                </div>
            `;
        }
    </script>
</head>
<body>
    <h1>Do You Love Me? 🥰</h1>
   
    <button onclick="handleYes()">Yess</button>
    <button id="noo-button" onclick="handleNo()">Noo</button>
</body>
</html>

