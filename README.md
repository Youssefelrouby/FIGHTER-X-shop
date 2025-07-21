<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>FIGHTER X shop</title>
<style>
body {
    margin: 0;
    font-family: Arial, sans-serif;
    background: #fff;
    background-image: url('boxer-holding-wrap.jpg');
    background-size: cover;
    background-attachment: fixed;
    background-position: center top;
    transition: background-image 0.8s ease-in-out;
}
header.top-bar {
    background: rgba(51, 51, 51, 0.8);
    color: white;
    padding: 10px;
    font-weight: bold;
    font-size: 20px;
    text-align: center;
}
header.nav-bar {
    background: rgba(51, 51, 51, 0.8);
    display: flex;
    justify-content: center;
    gap: 20px;
    padding: 10px;
}
header.nav-bar a {
    color: white;
    text-decoration: none;
    font-size: 14px;
    cursor: pointer;
}
header.nav-bar a:hover {
    text-decoration: underline;
}
section {
    padding: 20px;
    max-width: 800px;
    margin: auto;
    line-height: 1.6;
    background: rgba(255, 255, 255, 0.9);
    border-radius: 10px;
    transition: transform 0.5s;
}
section:hover {
    transform: scale(1.02);
}
h2 {
    color: #333;
    margin-top: 30px;
}
p, li {
    margin-bottom: 10px;
}
.wraps-container {
    display: flex;
    justify-content: center;
    gap: 30px;
    flex-wrap: wrap;
    margin-top: 20px;
}
.wrap-box {
    text-align: center;
    transition: transform 0.4s;
}
.wrap-box:hover {
    transform: translateY(-5px);
}
.wrap-box img {
    width: 150px;
    height: 200px;
    border: 2px solid #333;
    object-fit: cover;
    background: #eee;
    border-radius: 8px;
}
.country {
    color: #333;
    font-weight: bold;
    margin-top: 5px;
}
.price {
    color: #ff9900;
    font-weight: bold;
    font-size: 18px;
}
.vote-container {
    text-align: center;
    margin: 30px 0;
}
.vote-question {
    font-size: 18px;
    font-weight: bold;
    margin-bottom: 15px;
    color: #333;
}
.vote-button {
    background: #f0f0f0;
    border: none;
    padding: 10px 20px;
    font-size: 16px;
    cursor: pointer;
    margin: 10px;
    border-radius: 5px;
    transition: background 0.3s, transform 0.3s;
}
.vote-button:hover {
    background: #d9d9d9;
    transform: scale(1.05);
}
.vote-button.active {
    background: #333;
    color: white;
}
footer {
    background: rgba(51, 51, 51, 0.8);
    color: #ff9900;
    font-weight: bold;
    font-size: 14px;
    padding: 10px;
    text-align: center;
    border-radius: 5px;
}
</style>
<script>
function scrollToSection(id) {
    document.getElementById(id).scrollIntoView({ behavior: 'smooth' });
    if (id !== 'info') {
        document.body.style.backgroundImage = "url('boxer-punching-wrap.jpg')";
    } else {
        document.body.style.backgroundImage = "url('boxer-holding-wrap.jpg')";
    }
}
function vote(button) {
    let buttons = document.querySelectorAll('.vote-button');
    buttons.forEach(btn => btn.classList.remove('active'));
    button.classList.add('active');
}
</script>
</head>
<body>
<header class="top-bar">FIGHTER X shop</header>
<header class="nav-bar">
    <a onclick="scrollToSection('info')">Information</a>
    <a onclick="scrollToSection('pictures')">Pictures</a>
    <a onclick="scrollToSection('price')">Price</a>
    <a onclick="scrollToSection('contact')">Communication</a>
</header>
<section id="info">
    <h2>About Hand Wraps</h2>
    <p>Hand wraps are long strips of cloth used by boxers and martial artists to protect their hands and wrists during training and competition. They help stabilize the wrist and knuckles, reducing the risk of injuries from repeated impacts while providing comfort inside the gloves.</p>
    <h2>Types and Usage</h2>
    <p>There are traditional cloth wraps, elastic wraps for a tighter fit, and gel wraps for quick protection. To use, wrap around the wrist, knuckles, thumb, and secure with Velcro.</p>
</section>
<section id="pictures">
    <div class="wraps-container">
        <div class="wrap-box">
            <img src="c:\Users\somart\Desktop\WhatsApp Image 2025-07-21 at 00.48.24_c7904a77.jpg"="Thailand Boxing Hand Wraps">
            <p class="country">Thailand - $7</p>
        </div>
        <div class="wrap-box">
            <img src="egypt-wrap.jpg" alt="Egyptian Boxing Hand Wraps">
            <p class="country">Egypt - $6</p>
        </div>
        <div class="wrap-box">
            <img src="c:\Users\somart\Desktop\WhatsApp Image 2025-07-21 at 00.48.23_21ad3a05.jpg" alt="French Boxing Hand Wraps">
            <p class="country">France - $7</p>
        </div>
    </div>
</section>
<section id="price">
    <div class="vote-container">
        <div class="vote-question">Do you want your next hand wraps to be Ukrainian or Russian?</div>
        <button class="vote-button" onclick="vote(this)">Ukrainian</button>
        <button class="vote-button" onclick="vote(this)">Russian</button>
    </div>
</section>
<section id="contact">
    <footer>
        Telephone: 01553502805 | Email: youssefelmalthy@gmail.com
    </footer>
</section>
</body>
</html>
