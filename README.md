# Valentine-s-Day-

<!DOCTYPE html>
<html lang="de">
<head>
    <meta charset="UTF-8">
    <title>💖 Valentinstag 💖</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #ffe6f0;
            text-align: center;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
        }

        .container {
            background: white;
            padding: 30px;
            border-radius: 20px;
            box-shadow: 0 10px 20px rgba(0,0,0,0.2);
        }

        button {
            font-size: 20px;
            padding: 10px 25px;
            margin: 10px;
            border-radius: 10px;
            border: none;
            cursor: pointer;
        }

        #yesBtn {
            background-color: #ff4d6d;
            color: white;
        }

        #noBtn {
            background-color: #cccccc;
        }

        img {
            width: 250px;
            margin-top: 20px;
        }
    </style>
</head>
<body>

<div class="container" id="content">
    <h1>💘 Willst du mein Valentin sein? 💘</h1>
    <p id="message"></p>
    <button id="yesBtn" onclick="yesClicked()">Ja 💖</button>
    <button id="noBtn" onclick="noClicked()">Nein 😢</button>
</div>

<script>
    let noClickCount = 0;
    const messages = [
        "Bist du dir sicher? 🥺",
        "Versuch es nochmal 😭",
        "Noch eine Chance? 💔",
        "Bitteee… 🥹",
        "Ich bin traurig… 😿"
    ];

    function noClicked() {
        const noBtn = document.getElementById("noBtn");
        const message = document.getElementById("message");

        if (noClickCount < messages.length) {
            message.textContent = messages[noClickCount];
        }

        // Button kleiner machen
        let scale = 1 - (noClickCount * 0.15);
        noBtn.style.transform = `scale(${scale})`;

        noClickCount++;
    }

    function yesClicked() {
        const content = document.getElementById("content");
        content.innerHTML = `
            <h1>Yaaaay! 💖🐱</h1>
            <p>I Liebe dich ljubavi moja!!!!! Ich freue mich so sehr auf unseren Valentinstag mit dir!</p>
            <img src="https://media.giphy.com/media/JIX9t2j0ZTN9S/giphy.gif" alt="Süße Katze">
        `;
    }
</script>

</body>
</html>
