<!DOCTYPE html>
<html lang="hi">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>Bihar Voice Chat</title>
<style>
body{margin:0;font-family:Arial;background:#101426;color:white;text-align:center}
header{background:#7028d9;padding:22px;font-size:25px;font-weight:bold}
.card{background:#202943;margin:15px;padding:18px;border-radius:15px}
button{background:#813df0;color:white;border:0;padding:12px 18px;margin:5px;border-radius:9px;font-size:16px}
input{padding:12px;width:75%;border-radius:8px;border:0;margin:6px}
.coin{color:#ffd447;font-size:22px}
</style>
</head>
<body>
<header>🎙️ Bihar Voice Chat</header>
<div class="card">
<h2>आपका स्वागत है!</h2>
<p>दोस्तों से मिलें और पार्टी रूम का आनंद लें।</p>
<input id="name" placeholder="अपना नाम लिखें">
<button onclick="login()">लॉगिन करें</button>
<p id="welcome"></p>
</div>
<div class="card">
<h2>🪙 आपका वॉलेट</h2>
<p class="coin">कॉइन: <span id="coins">1000</span></p>
<button onclick="addCoins()">फ्री कॉइन लें (+100)</button>
</div>
<div class="card">
<h2>🎤 वॉइस पार्टी रूम</h2>
<button onclick="room()">पार्टी रूम खोलें</button>
<p id="room">अभी कोई लाइव वॉइस कनेक्शन नहीं है।</p>
</div>
<div class="card">
<h2>🎲 नंबर गेम</h2>
<button onclick="game()">गेम खेलें</button>
<p id="game"></p>
</div>
<script>
let coins=1000;
function login(){
let n=document.getElementById('name').value.trim();
document.getElementById('welcome').textContent=n?'नमस्ते '+n+'!':'पहले अपना नाम लिखें।';
}
function addCoins(){
coins+=100;
document.getElementById('coins').textContent=coins;
}
function room(){
document.getElementById('room').textContent='यह डेमो रूम है। असली वॉइस चैट के लिए सर्वर जोड़ना होगा।';
}
function game(){
let n=Math.floor(Math.random()*6)+1;
document.getElementById('game').textContent='आपका नंबर: '+n;
}
</script>
</body>
</html>
