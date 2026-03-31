<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Ruslan | Ultra Animation</title>

<style>
body {
    margin: 0;
    background: black;
    color: #00ffea;
    font-family: monospace;
    overflow-x: hidden;
}

/* Typing text */
.typing {
    font-size: 40px;
    text-align: center;
    margin-top: 100px;
    white-space: nowrap;
    overflow: hidden;
    border-right: 3px solid #00ffea;
    width: 0;
    animation: typing 4s steps(20) forwards, blink 0.7s infinite;
}

@keyframes typing {
    to { width: 300px; }
}

@keyframes blink {
    50% { border-color: transparent; }
}

/* Floating animation */
.float {
    text-align: center;
    margin-top: 50px;
    animation: float 3s ease-in-out infinite;
}

@keyframes float {
    0% { transform: translateY(0);}
    50% { transform: translateY(-20px);}
    100% { transform: translateY(0);}
}

/* Cards */
.card {
    margin: 40px auto;
    width: 200px;
    padding: 20px;
    text-align: center;
    border: 1px solid #00ffea;
    transition: 0.3s;
}

/* Hover glitch */
.card:hover {
    animation: glitch 0.3s infinite;
    background: #00ffea;
    color: black;
}

@keyframes glitch {
    0% { transform: translate(0);}
    20% { transform: translate(-2px,2px);}
    40% { transform: translate(2px,-2px);}
    60% { transform: translate(-2px,0);}
    80% { transform: translate(2px,2px);}
    100% { transform: translate(0);}
}

/* Cursor glow */
.cursor {
    position: fixed;
    width: 15px;
    height: 15px;
    background: #00ffea;
    border-radius: 50%;
    pointer-events: none;
}

</style>
</head>
<body>

<div class="cursor" id="cursor"></div>

<div class="typing">Hello, I'm Ruslan 🚀</div>

<div class="float">
    <h2>💻 Developer</h2>
</div>

<div class="card">HTML</div>
<div class="card">CSS</div>
<div class="card">JavaScript</div>

<script>
/* Cursor follow */
const cursor = document.getElementById("cursor");

document.addEventListener("mousemove", e => {
    cursor.style.top = e.clientY + "px";
    cursor.style.left = e.clientX + "px";
});
</script>

</body>
</html>
