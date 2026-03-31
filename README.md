<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Ruslan | Animated Portfolio</title>

<style>
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: 'Segoe UI', sans-serif;
}

body {
    background: #020617;
    color: white;
    overflow-x: hidden;
}

/* Background animated gradient */
body::before {
    content: "";
    position: fixed;
    width: 200%;
    height: 200%;
    background: linear-gradient(45deg, #00f2fe, #4facfe, #00ff87, #60efff);
    animation: bgMove 10s infinite linear;
    z-index: -1;
    opacity: 0.15;
}

@keyframes bgMove {
    0% { transform: translate(0,0); }
    50% { transform: translate(-25%, -25%); }
    100% { transform: translate(0,0); }
}

/* Header */
header {
    text-align: center;
    padding: 100px 20px;
    animation: fadeIn 2s ease;
}

h1 {
    font-size: 60px;
    background: linear-gradient(90deg, #00f2fe, #4facfe);
    -webkit-background-clip: text;
    color: transparent;
    transition: 0.3s;
}

h1:hover {
    letter-spacing: 5px;
}

/* Sections */
section {
    padding: 50px;
    text-align: center;
}

/* Cards */
.card {
    display: inline-block;
    margin: 20px;
    padding: 30px;
    background: rgba(255,255,255,0.05);
    border-radius: 20px;
    backdrop-filter: blur(10px);
    transition: 0.4s;
    cursor: pointer;
}

/* Hover animation */
.card:hover {
    transform: translateY(-10px) scale(1.1) rotate(2deg);
    box-shadow: 0 0 25px #00f2fe;
}

/* Button */
button {
    margin-top: 20px;
    padding: 12px 25px;
    border: none;
    border-radius: 30px;
    background: linear-gradient(90deg, #00f2fe, #4facfe);
    color: black;
    font-weight: bold;
    cursor: pointer;
    transition: 0.3s;
}

button:hover {
    transform: scale(1.1);
    box-shadow: 0 0 20px #00f2fe;
}

/* Cursor glow effect */
.cursor {
    position: fixed;
    width: 20px;
    height: 20px;
    background: #00f2fe;
    border-radius: 50%;
    pointer-events: none;
    mix-blend-mode: difference;
    transition: transform 0.1s;
}

/* Fade animation */
@keyframes fadeIn {
    from { opacity: 0; transform: translateY(50px);}
    to { opacity: 1; transform: translateY(0);}
}

footer {
    padding: 20px;
    text-align: center;
    opacity: 0.7;
}
</style>

</head>
<body>

<div class="cursor" id="cursor"></div>

<header>
    <h1>🚀 Ruslan</h1>
    <p>Animated Developer Portfolio</p>
    <button onclick="showMsg()">Click Me</button>
</header>

<section>
    <h2>🛠 Skills</h2>
    <div class="card">HTML</div>
    <div class="card">CSS</div>
    <div class="card">JavaScript</div>
</section>

<section>
    <h2>📂 Projects</h2>
    <div class="card">Coming soon...</div>
</section>

<footer>
    <p>© 2026 Ruslan</p>
</footer>

<script>
function showMsg() {
    alert("🔥 Welcome to my animated site!");
}

/* Cursor animation */
const cursor = document.getElementById("cursor");

document.addEventListener("mousemove", e => {
    cursor.style.top = e.clientY + "px";
    cursor.style.left = e.clientX + "px";
});
</script>

</body>
</html>
