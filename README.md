<!DOCTYPE html>
<html lang="ar">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>RWL | POLICE MOD</title>
<style>
    body {
        margin: 0;
        padding: 0;
        font-family: Cairo, Arial, sans-serif;
        background: #0a0a0a;
        color: #f1c40f;
        text-align: center;
    }
    header {
        padding: 40px 20px;
    }
    img.logo {
        width: 200px;
        border: 4px solid #f1c40f;
        border-radius: 12px;
        margin-bottom: 20px;
    }
    h1 {
        font-size: 44px;
        margin: 10px 0;
        letter-spacing: 2px;
    }
    .section {
        margin: 40px auto;
        max-width: 800px;
        padding: 0 20px;
    }
    .section h2 {
        font-size: 32px;
        margin-bottom: 15px;
        border-bottom: 2px solid #f1c40f;
        display: inline-block;
        padding-bottom: 5px;
    }
    p {
        font-size: 19px;
        line-height: 1.7;
        color: #e0e0e0;
    }
    .btn {
        display: inline-block;
        padding: 14px 30px;
        margin: 15px 8px;
        background: #f1c40f;
        color: #0a0a0a;
        text-decoration: none;
        font-size: 20px;
        font-weight: bold;
        border-radius: 8px;
        transition: 0.3s;
        cursor: pointer;
    }
    .btn:hover {
        background: #d4a017;
        transform: scale(1.05);
    }
    .rules-list {
        text-align: right;
        direction: rtl;
        margin-top: 15px;
        list-style: none;
        padding: 0;
    }
    .rules-list li {
        background: #1a1a1a;
        margin: 8px 0;
        padding: 10px 15px;
        border-radius: 6px;
        font-size: 18px;
        color: #f1c40f;
    }
    footer {
        margin: 60px 0 20px;
        font-size: 15px;
        color: #ccc;
    }
</style>
</head>
<body>

<header>
    <img class="logo" src="https://cdn.discordapp.com/attachments/1461797385557508288/1474504963282436358/7afb93643be699e0.gif" alt="لوغو RWL | POLICE MOD">
    <h1>RWL | POLICE MOD</h1>
    <p>أهلاً بك في سيرفر الشرطة <strong>RWL Police Mod</strong> على FiveM! 🚓🔥</p>
</header>

<div class="section">
    <h2>📌 معلومات السيرفر</h2>
    <p>
        ➤ نظام لعب **شرطة واقعي** داخل FiveM.  
        ➤ انضم الآن للعبة عبر العنوان التالي:
    </p>
    <p style="font-size: 24px; font-weight: bold; color: #f1c40f;">
        ➤ <code id="server-ip">connect dag6oj</code>
    </p>
    <button class="btn" onclick="copyIP()">📋 نسخ IP السيرفر</button>
    <a class="btn" href="https://discord.gg/rwl" target="_blank">🔗 انضم للديسكورد</a>
</div>

<div class="section">
    <h2>🚀 طريقة الانضمام</h2>
    <p>
        1. افتح لعبة **GTA V** على جهازك.  
        2. حمّل برنامج **FiveM** إذا ما كان عندك.  
        3. بمجرد دخولك لـ FiveM، افتح قائمة السيرفرات.  
        4. في خانة الـ IP اكتب أو الصق: <strong>connect dag6oj</strong>  
        5. انضم والعب مع فريق الشرطة داخل المجتمع!
    </p>
</div>

<div class="section">
    <h2>📜 قوانين السيرفر</h2>
    <ul class="rules-list">
        <li>🛑 ممنوع الإساءة أو الشتائم لأي لاعب.</li>
        <li>🚨 الالتزام بدورك كشرطي وعدم التعرض للاعبين بدون سبب.</li>
        <li>🔇 لا تستخدم أي برامج غش أو تعديلات غير مسموح بها.</li>
        <li>🎙️ احترم أعضاء الطاقم والتعليمات الصادرة منهم.</li>
        <li>📢 ممنوع نشر الإعلانات داخل السيرفر بدون إذن.</li>
    </ul>
</div>

<footer>
    © 2026 RWL | POLICE MOD
</footer>

<script>
function copyIP() {
    const ipText = document.getElementById("server-ip").innerText;
    navigator.clipboard.writeText(ipText).then(() => {
        alert("تم نسخ IP السيرفر 🟡\n" + ipText);
    }).catch(() => {
        alert("فشل النسخ، حاول مرة أخرى.");
    });
}
</script>

</body>
</html>
