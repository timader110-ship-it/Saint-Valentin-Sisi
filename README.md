<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <title>Saint Valentin 💘</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background: linear-gradient(135deg, #ff9a9e, #fad0c4);
            height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            margin: 0;
        }

        .container {
            background: white;
            padding: 40px;
            border-radius: 20px;
            text-align: center;
            box-shadow: 0 10px 30px rgba(0,0,0,0.2);
        }

        h1 {
            margin-bottom: 30px;
        }

        button {
            padding: 15px 30px;
            font-size: 18px;
            border: none;
            border-radius: 10px;
            cursor: pointer;
            margin: 10px;
        }

        #yes {
            background-color: #ff4d6d;
            color: white;
        }

        #no {
            background-color: #ccc;
            position: absolute;
        }

        #result {
            display: none;
            margin-top: 30px;
        }

        img {
            width: 250px;
            border-radius: 15px;
        }
    </style>
</head>
<body>

<div class="container" id="question">
    <h1>Veux-tu être ma Valentine ? 💖</h1>
    <button id="yes">OUI 😍</button>
    <button id="no">NON 🙄</button>
</div>

<div class="container" id="result">
    <h1>YES !!! 💘💘💘</h1>
    <p>Je savais que tu dirais oui 😏</p>
    <img src="https://media.giphy.com/media/l0MYt5jPR6QX5pnqM/giphy.gif" alt="love gif">
</div>

<script>
    const noBtn = document.getElementById("no");
    const yesBtn = document.getElementById("yes");
    const question = document.getElementById("question");
    const result = document.getElementById("result");

    noBtn.addEventListener("mouseover", () => {
        const x = Math.random() * (window.innerWidth - noBtn.offsetWidth);
        const y = Math.random() * (window.innerHeight - noBtn.offsetHeight);
        noBtn.style.left = `${x}px`;
        noBtn.style.top = `${y}px`;
    });

    yesBtn.addEventListener("click", () => {
        question.style.display = "none";
        result.style.display = "block";
    });
</script>

</body>
</html>
