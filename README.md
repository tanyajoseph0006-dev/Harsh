<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>For You ❤️</title>
<style>
    body {
        margin: 0;
        height: 100vh;
        background: linear-gradient(135deg, #ffdde1, #ee9ca7);
        display: flex;
        justify-content: center;
        align-items: center;
        font-family: 'Georgia', serif;
        overflow: hidden;
    }

    .card {
        background: rgba(255,255,255,0.9);
        padding: 40px;
        border-radius: 20px;
        text-align: center;
        box-shadow: 0 20px 40px rgba(0,0,0,0.2);
        max-width: 350px;
        animation: fadeIn 2s ease;
    }

    h1 {
        color: #c2185b;
        margin-bottom: 10px;
    }

    p {
        color: #444;
        font-size: 16px;
        line-height: 1.6;
    }

    .bouquet {
        margin: 30px auto;
        width: 120px;
        height: 160px;
        position: relative;
    }

    .flower {
        width: 30px;
        height: 30px;
        background: #fff;
        border-radius: 50%;
        position: absolute;
        animation: bloom 3s infinite alternate;
    }

    .flower::before,
    .flower::after {
        content: '';
        width: 30px;
        height: 30px;
        background: #fff;
        border-radius: 50%;
        position: absolute;
    }

    .flower::before {
        left: -15px;
    }

    .flower::after {
        right: -15px;
    }

    .f1 { top: 0; left: 45px; }
    .f2 { top: 25px; left: 20px; }
    .f3 { top: 25px; right: 20px; }

    .stem {
        width: 6px;
        height: 80px;
        background: #2e7d32;
        margin: auto;
        border-radius: 3px;
    }

    .heart {
        position: absolute;
        color: #e91e63;
        font-size: 18px;
        animation: float 6s infinite;
    }

    @keyframes fadeIn {
        from { opacity: 0; transform: translateY(20px); }
        to { opacity: 1; transform: translateY(0); }
    }

    @keyframes bloom {
        from { transform: scale(1); }
        to { transform: scale(1.1); }
    }

    @keyframes float {
        0% { transform: translateY(0); opacity: 1; }
        100% { transform: translateY(-600px); opacity: 0; }
    }
</style>
</head>
<body>

<div class="card">
    <h1>I love you, Harsh 🤍</h1>
    <p>
        You are the most amazing person in my life.<br>
        I am happiest knowing you are in my life.<br>
        This little piece of code carries<br>
        all the feelings I don’t always say out loud.
    </p>

    <div class="bouquet">
        <div class="flower f1"></div>
        <div class="flower f2"></div>
        <div class="flower f3"></div>
        <div class="stem"></div>
    </div>

    <p style="font-size:14px;color:#777;">
        — Made with love, just for you 🌸
    </p>
</div>

<script>
    for(let i=0;i<20;i++){
        let heart = document.createElement("div");
        heart.className = "heart";
        heart.innerHTML = "❤";
        heart.style.left = Math.random() * 100 + "vw";
        heart.style.bottom = "-20px";
        heart.style.animationDuration = (4 + Math.random() * 4) + "s";
        document.body.appendChild(heart);
    }
</script>

</body>
</html>
