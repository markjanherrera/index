<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
<title>Be My Valentine 💕</title>

<style>
/* Desktop block */
.desktop-warning {
    display: none;
}

/* Mobile only */
@media (min-width: 768px) {
    body * {
        display: none !important;
    }
    body {
        background: #ff758c;
    }
    .desktop-warning {
        display: flex !important;
        height: 100vh;
        justify-content: center;
        align-items: center;
        color: white;
        font-family: Comic Sans MS;
        text-align: center;
        font-size: 1.5em;
    }
}

body {
    margin: 0;
    height: 100vh;
    overflow: hidden;
    font-family: 'Comic Sans MS', cursive;
    background: linear-gradient(135deg, #ff758c, #ff7eb3);
    display: flex;
    justify-content: center;
    align-items: center;
}

.card {
    width: 90%;
    max-width: 360px;
    background: rgba(255,255,255,0.95);
    padding: 30px 20px;
    border-radius: 25px;
    text-align: center;
    box-shadow: 0 10px 25px rgba(0,0,0,0.25);
    z-index: 2;
}

h1 {
    color: #e6005c;
    font-size: 1.9em;
}

.buttons {
    margin-top: 25px;
    display: flex;
    justify-content: center;
    gap: 20px;
}

button {
    border: none;
    border-radius: 40px;
    padding: 14px 26px;
    font-size: 1.1em;
    cursor: pointer;
    transition: transform 0.3s ease;
}

#yes {
    background: #ff3366;
    color: white;
    transform: scale(1);
}

#no {
    background: #aaa;
    color: white;
    transform: scale(1);
}

/* Balloons */
.balloon {
    position: absolute;
    bottom: -120px;
    width: 50px;
    height: 70px;
    border-radius: 50%;
    animation: floatUp linear infinite;
}

.balloon::after {
    content: "";
    position: absolute;
    width: 2px;
    height: 35px;
    background: #555;
    bottom: -35px;
    left: 50%;
}

@keyframes floatUp {
    from { transform: translateY(0); opacity: 1; }
    to { transform: translateY(-120vh); opacity: 0; }
}

/* Hearts */
.heart {
    position: absolute;
    animation: floatHeart 6s linear infinite;
    color: rgba(255,0,100,0.3);
}

@keyframes floatHeart {
    from { transform: translateY(100vh); }
    to { transform: translateY(-10vh); }
}
</style>
</head>

<body>

<div class="desktop-warning">
    📱 Please open this on your phone 💕
</div>

<div class="card">
    <h1>crush mo ako no🧐</h1>
    <div class="buttons">
        <button id="yes" onclick="yesClick()">YES </button>
        <button id="no" onclick="noClick()">NO </button>
    </div>
</div>

<script>
let yesScale = 1;
let noScale = 1;

function noClick() {
    noScale -= 0.15;
    yesScale += 0.15;
    if (noScale < 0.2) noScale = 0.2;

    document.getElementById("no").style.transform = `scale(${noScale})`;
    document.getElementById("yes").style.transform = `scale(${yesScale})`;
}

function yesClick() {
    document.body.innerHTML = `
    <div style="
        height:100vh;
        display:flex;
        justify-content:center;
        align-items:center;
        text-align:center;
        font-family:Comic Sans MS;
        background:linear-gradient(135deg,#ff758c,#ff7eb3);
        color:white;
        padding:20px;">
        <h1>sabi ko na <br>crush mo pala ako bakla hahaah</h1>
    </div>`;
}

// Balloons
function createBalloon() {
    const b = document.createElement("div");
    b.className = "balloon";
    b.style.left = Math.random() * 100 + "vw";
    b.style.background = `hsl(${Math.random()*360},80%,70%)`;
    b.style.animationDuration = 7 + Math.random() * 5 + "s";
    document.body.appendChild(b);
    setTimeout(() => b.remove(), 13000);
}
setInterval(createBalloon, 800);

// Hearts
function createHeart() {
    const h = document.createElement("div");
    h.className = "heart";
    h.innerHTML = "❤️";
    h.style.left = Math.random() * 100 + "vw";
    h.style.fontSize = 14 + Math.random() * 18 + "px";
    document.body.appendChild(h);
    setTimeout(() => h.remove(), 6000);
}
setInterval(createHeart, 500);
</script>

</body>
</html>
