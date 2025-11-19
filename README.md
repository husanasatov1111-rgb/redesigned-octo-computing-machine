<!DOCTYPE html>
<html lang="uz">
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Mening To‘liq Saytim</title>
    <style>
        body {
            margin: 0;
            font-family: Arial, sans-serif;
            background: #E9F0FF;
            color: #333;
        }
        header {
            background: linear-gradient(90deg, #005CFF, #003EB0);
            padding: 25px;
            text-align: center;
            color: white;
            font-size: 30px;
            font-weight: bold;
        }
        header img {
            width:70px; height:70px; border-radius:50%; vertical-align:middle; margin-right:10px;
        }
        nav {
            background: #ffffffcc;
            padding: 12px;
            text-align: center;
            position: sticky;
            top: 0;
            backdrop-filter: blur(10px);
            animation: fadeDown 0.6s ease-out;
        }
        nav a {
            margin: 0 15px;
            text-decoration: none;
            color: #005CFF;
            font-weight: bold;
        }
        nav a:hover { text-decoration: underline; }
        @keyframes fadeDown {
            from { opacity: 0; transform: translateY(-20px); }
            to { opacity: 1; transform: translateY(0); }
        }
        :root {
            --asosiy: #005CFF;
            --asosiy-2: #003EB0;
            --fon: #E9F0FF;
        }
        .hero { position:relative; overflow:hidden; height:350px; }
        .hero img { width:100%; height:100%; object-fit:cover; filter:brightness(60%); }
        .hero div { position:absolute; width:100%; text-align:center; color:white; font-size:40px; font-weight:bold; top:50%; transform:translateY(-50%); z-index:2; }
        .container { max-width:900px; margin:auto; padding:20px; }
        .card { background:white; padding:20px; margin:15px 0; border-radius:12px; box-shadow:0 0 10px rgba(0,0,0,0.1); transition:.3s; }
        .card:hover { transform: scale(1.01); }
        button { background: #005CFF; color:white; padding:10px 20px; border:none; border-radius:8px; cursor:pointer; font-size:16px; }
        button:hover { background:#003EB0; }
        footer { background:#333; color:white; text-align:center; padding:15px; margin-top:20px; }
        @media (max-width:600px){.hero { height:250px; }.hero div { font-size:28px; } img { width:98% !important; }}
    </style>
</head>
<body>

<header><img src="https://picsum.photos/120/120" alt="Logo">Mening To‘liq Professional Saytim</header>

<nav>
    <a href="#home">Bosh sahifa</a>
    <a href="#about">Men haqimda</a>
    <a href="#gallery">Rasmlar</a>
    <a href="#portfolio">Portfolio</a>
    <a href="#blog">Blog</a>
    <a href="#contact">Aloqa</a>
</nav>

<button id="themeToggle" style="position:fixed; right:20px; bottom:20px; z-index:1000; padding:12px 18px; border-radius:10px; border:none; background:#222; color:white;">Dark / Light</button>

<div class="hero" id="home">
    <div id="sliderText">Xush kelibsiz!</div>
    <img id="sliderImg" src="https://picsum.photos/1200/400">
</div>

<div class="container">
    <div class="card" id="about">
        <h2>Men haqimda</h2>
        <p>Bu bo‘limga o‘zingiz haqingizda ma’lumot yozishingiz mumkin. Sayt to‘liq interaktiv va zamonaviy dizaynga ega.</p>
    </div>

    <div class="card" id="gallery">
        <h2>Rasmlar Galereyasi</h2>
        <img src="https://picsum.photos/400" style="width:48%; border-radius:10px; margin:1%;">
        <img src="https://picsum.photos/401" style="width:48%; border-radius:10px; margin:1%;">
    </div>

    <div class="card" id="portfolio">
        <h2>Portfolio</h2>
        <div style="display:flex; flex-wrap:wrap; gap:15px;">
            <div style="background:#f9f9f9; width:46%; border-radius:12px; padding:15px; box-shadow:0 0 8px rgba(0,0,0,0.1);">
                <img src="https://picsum.photos/300" style="width:100%; border-radius:10px;">
                <h3>Loyiha 1</h3>
                <p>Kichik tavsif yoziladi.</p>
            </div>
            <div style="background:#f9f9f9; width:46%; border-radius:12px; padding:15px; box-shadow:0 0 8px rgba(0,0,0,0.1);">
                <img src="https://picsum.photos/301" style="width:100%; border-radius:10px;">
                <h3>Loyiha 2</h3>
                <p>Kichik tavsif yoziladi.</p>
            </div>
        </div>
    </div>

    <div class="card" id="blog">
        <h2>Blog</h2>
        <div style="display:flex; flex-direction:column; gap:15px;">
            <div style="background:#fafafa; padding:15px; border-radius:10px; box-shadow:0 0 8px rgba(0,0,0,0.1);">
                <h3>1-maqola</h3>
                <p>Bu yerda qisqa matn joylashadi...</p>
                <button>Batafsil</button>
            </div>
            <div style="background:#fafafa; padding:15px; border-radius:10px; box-shadow:0 0 8px rgba(0,0,0,0.1);">
                <h3>2-maqola</h3>
                <p>Bu yerda qisqa matn joylashadi...</p>
                <button>Batafsil</button>
            </div>
        </div>
    </div>

    <div class="card" id="contact">
        <h2>Aloqa</h2>
        <form id="contactForm">
            <label>Ismingiz:</label>
            <input type="text" id="name" style="width:100%; padding:10px; margin:5px 0; border-radius:8px; border:1px solid #ccc;">
            <label>Telefon:</label>
            <input type="text" id="phone" style="width:100%; padding:10px; margin:5px 0; border-radius:8px; border:1px solid #ccc;">
            <label>Xabar:</label>
            <textarea id="msg" style="width:100%; padding:10px; margin:5px 0; border-radius:8px; border:1px solid #ccc; height:100px;"></textarea>
            <button type="button" onclick="sendMessage()">Yuborish</button>
        </form>
        <p id="status"></p>
    </div>
</div>

<footer>© 2025 Mening Saytim — Barcha huquqlar himoyalangan</footer>

<script>
// Dark / Light mode
let dark = false;
document.getElementById('themeToggle').onclick = () => {
    dark = !dark;
    if(dark){ document.body.style.background = '#111'; document.body.style.color = '#fff'; }
    else{ document.body.style.background = ''; document.body.style.color = ''; }
};

// Simple slider
let imgs = ['https://picsum.photos/1200/400?random=1','https://picsum.photos/1200/400?random=2','https://picsum.photos/1200/400?random=3'];
let texts = ['Xush kelibsiz!', 'Bizning loyihalar', 'Eng yaxshi xizmatlar'];
let idx = 0;
setInterval(()=>{ idx=(idx+1)%imgs.length; document.getElementById('sliderImg').src=imgs[idx]; document.getElementById('sliderText').innerText=texts[idx]; },3000);

//Telegram bot API integratsiya
function sendMessage(){
    let name=document.getElementById('name').value;
    let phone=document.getElementById('phone').value;
    let msg=document.getElementById('msg').value;
    if(!name||!phone||!msg){ document.getElementById('status').innerText='Iltimos barcha maydonlarni to‘ldiring!'; return; }
    let token='BOT_TOKENNI_BU_YERGA_QOYING';
    let chatId='CHAT_ID_BU_YERGA_QOYING';
    let text=`Yangi xabar:%0AIsm: ${name}%0ATelefon: ${phone}%0AXabar: ${msg}`;
    fetch(`https://api.telegram.org/bot${token}/sendMessage?chat_id=${chatId}&text=${text}`)
    .then(r=>{ document.getElementById('status').innerText='Xabar yuborildi!'; document.getElementById('contactForm').reset(); })
    .catch(()=>{ document.getElementById('status').innerText='Xatolik yuz berdi!'; });
}
</script>

</body>
</html>

