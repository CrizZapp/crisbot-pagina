<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>CrisBots - Multi-Sección</title>
<style>
    body {
        font-family: Arial, sans-serif;
        background: #121212;
        color: #fff;
        margin: 0;
        padding: 0;
    }
    header {
        background: #1f1f1f;
        padding: 20px;
        text-align: center;
    }
    header h1 { margin: 0; color: #00ffcc; }
    section {
        padding: 20px;
        max-width: 900px;
        margin: auto;
        display: none; /* ocultamos todas al inicio */
    }
    section.active { display: block; }
    h2 { color: #00ffcc; margin-bottom: 15px; }
    ul { list-style: none; padding: 0; }
    li {
        background: #2a2a2a;
        margin: 10px 0;
        padding: 15px;
        border-radius: 8px;
        transition: transform 0.3s, background 0.3s;
    }
    li.libre:hover { transform: scale(1.05); background: #00ffcc; color: #121212; }
    .ocupado { animation: parpadeo 1s infinite; }
    @keyframes parpadeo {
        0% { background: #2a2a2a; }
        50% { background: #ff4d4d; }
        100% { background: #2a2a2a; }
    }
    .btn {
        display: inline-block;
        padding: 15px 25px;
        background: #00ffcc;
        color: #121212;
        font-weight: bold;
        text-decoration: none;
        border-radius: 8px;
        transition: 0.3s;
        margin: 10px 5px 10px 0;
        cursor: pointer;
    }
    .btn:hover { background: #00e6b8; }
    .updates li { background: #2a2a2a; margin: 10px 0; padding: 10px; border-left: 4px solid #00ffcc; }
    .command-section { background: #1f1f1f; padding: 15px; margin: 10px 0; border-radius: 8px; }
    .command-section h3 { margin-top: 0; color: #00ffcc; }
    .command-section p { margin: 5px 0; }
    .comandos-bg { background: #222222; padding: 30px; border-radius: 10px; margin-top: 20px; }
</style>
</head>
<body>

<header>
    <h1>CrisBots</h1>
    <p>Tu colección de sub-bots</p>
</header>

<div style="text-align:center; margin:20px 0;">
    <span class="btn" onclick="showSection('subbots')">Sub-Bots</span>
    <span class="btn" onclick="showSection('comandos')">Comandos</span>
    <span class="btn" onclick="showSection('actualizaciones')">Actualizaciones</span>
</div>

<section id="subbots" class="active">
    <h2>Sub-Bots Disponibles</h2>
    <ul>
        <li class="libre">Bot 1 - Libre</li>
        <li class="libre">Bot 2 - Libre</li>
        <li class="libre">Bot 3 - Libre</li>
        <li class="libre">Bot 4 - Libre</li>
        <li class="ocupado">Bot 5 - Ocupado</li>
        <li class="libre">Bot 6 - Libre</li>
        <li class="libre">Bot 7 - Libre</li>
        <li class="libre">Bot 8 - Libre</li>
        <li class="libre">Bot 9 - Libre</li>
        <li class="libre">Bot 10 - Libre</li>
    </ul>
    <a class="btn" href="https://wa.me/+59898476523" target="_blank">Contactar por WhatsApp</a>
</section>

<section id="comandos" class="comandos-bg">
    <h2>Todos los Comandos de CrisBot</h2>
    <div class="command-section">
        <h3>Navidad</h3>
        <p>#navidad</p><p>#regalo</p><p>#santabot</p><p>#snow</p>
    </div>
    <div class="command-section">
        <h3>Básicos</h3>
        <p>#hi / #bye</p><p>#menu / #help</p><p>#ping</p><p>#hora</p>
        <p>#spam</p><p>#say</p><p>#miid</p><p>#owner / #creador</p>
    </div>
    <div class="command-section">
        <h3>Admin</h3>
        <p>#promote @user</p><p>#demote @user</p><p>#kick @user</p><p>#admin</p>
        <p>#todos</p><p>#aviso &lt;texto&gt;</p><p>#close / #open</p><p>#welcome / #welcome off</p>
        <p>#antilink / #antilink off</p><p>#baneargrupo</p><p>#desbaneargrupo</p><p>#exit</p>
        <p>#antidelete</p>
    </div>
    <div class="command-section">
        <h3>NSFW 🔞</h3>
        <p>#nsfw on/off</p><p>#ass</p><p>#boobs</p><p>#hentai</p>
    </div>
    <div class="command-section">
        <h3>Economía</h3>
        <p>#work / #daily / #fish / #ranking</p>
        <p>#slut / #double / #steal &lt;id&gt;</p>
        <p>#buyvip</p>
        <p>#tienda / #comprar / #gift / #giftoff / #apagargift</p>
    </div>
    <div class="command-section">
        <h3>Juegos</h3>
        <p>#ppt</p><p>#ahorcado</p><p>#letra</p><p>#contar</p><p>#veteranff</p>
    </div>
    <div class="command-section">
        <h3>Stickers & Imágenes</h3>
        <p>#sticker / #s</p><p>#brat</p><p>#emojimix</p><p>#waifu</p><p>#pfp</p><p>#ytimage</p>
    </div>
    <div class="command-section">
        <h3>Multimedia</h3>
        <p>#play</p><p>#yt</p><p>#ytaudio</p><p>#video</p><p>#tiktok / #tt</p>
        <p>#lyrics / #lyric / #cancion</p><p>#audio</p><p>#tts</p><p>#escopeta</p><p>#tralalerita</p>
    </div>
</section>

<section id="actualizaciones">
    <h2>Actualizaciones del Bot</h2>
    <ul class="updates">
        <li>v1.4 - CrisBot (Muchos mas comandos)</li>
        <li>v1.3 - Abrahaham Bot</li>
        <li>v1.2 - Nagatoro bot</li>
        <li>v1.1 - Primera version</li>
    </ul>
</section>

<script>
function showSection(sectionId) {
    document.querySelectorAll('section').forEach(s => s.classList.remove('active'));
    document.getElementById(sectionId).classList.add('active');
}
</script>

</body>
</html>
