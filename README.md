# nnk
<!DOCTYPE html>
<html lang="ru">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>NNkey — AI система роста</title>

<style>
@import url('https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&display=swap');

*{
margin:0;
padding:0;
box-sizing:border-box;
font-family:Inter,sans-serif;
}

body{
background:radial-gradient(circle at top,#0b0c18,#05050a);
color:white;
overflow-x:hidden;
}

.bg{
position:fixed;
inset:0;
background:
radial-gradient(circle at 15% 20%,rgba(123,97,255,0.25),transparent 45%),
radial-gradient(circle at 80% 70%,rgba(76,201,240,0.18),transparent 45%);
}

.container{
max-width:1100px;
margin:auto;
padding:110px 24px;
position:relative;
z-index:2;
}

nav{
display:flex;
justify-content:space-between;
align-items:center;
margin-bottom:60px;
}

.logo-3d{
display:flex;
align-items:center;
gap:14px;
perspective:800px;
}

.logo-wrap{
display:flex;
align-items:center;
gap:10px;
animation:spin 6s linear infinite;
transform-style:preserve-3d;
filter:drop-shadow(0 0 15px rgba(123,97,255,0.8))
       drop-shadow(0 0 30px rgba(76,201,240,0.4));
}

@keyframes spin{
0%{transform:rotateY(0deg) rotateX(10deg);}
100%{transform:rotateY(360deg) rotateX(10deg);}
}

.nn{
font-size:34px;
font-weight:800;
letter-spacing:6px;
background:linear-gradient(180deg,#fff,#b9a7ff,#7B61FF);
-webkit-background-clip:text;
-webkit-text-fill-color:transparent;
}

.ai-dot{
font-size:12px;
animation:pulse 2s infinite;
}

@keyframes pulse{
0%,100%{opacity:0.5;transform:scale(1);}
50%{opacity:1;transform:scale(1.2);}
}

.key-icon{
width:28px;
height:14px;
position:relative;
}

.key-icon::before{
content:"";
position:absolute;
width:20px;
height:4px;
background:#cfcfff;
top:5px;
box-shadow:0 0 15px #7B61FF;
}

.key-icon::after{
content:"";
position:absolute;
width:10px;
height:10px;
border:2px solid #cfcfff;
border-radius:50%;
right:0;
box-shadow:0 0 15px #4cc9f0;
}

h1{font-size:58px;}

h1 span{
background:linear-gradient(90deg,#7B61FF,#4cc9f0);
-webkit-background-clip:text;
-webkit-text-fill-color:transparent;
}

/* GRID */
.grid{
margin-top:60px;
display:grid;
grid-template-columns:repeat(auto-fit,minmax(240px,1fr));
gap:16px;
}

.card{
background:rgba(255,255,255,0.03);
border:1px solid rgba(255,255,255,0.08);
padding:18px;
border-radius:14px;
backdrop-filter:blur(12px);
}

/* CHAT */
.chat{
margin-top:60px;
background:rgba(255,255,255,0.04);
border-radius:14px;
padding:15px;
}

.messages{
height:260px;
overflow-y:auto;
font-size:14px;
}

.input{
display:flex;
gap:10px;
margin-top:10px;
}

.input input{
flex:1;
padding:10px;
border-radius:10px;
border:none;
}

.input button{
background:#7B61FF;
border:none;
color:white;
padding:10px 14px;
border-radius:10px;
}

.cta{
margin-top:10px;
width:100%;
padding:12px;
border-radius:10px;
background:linear-gradient(90deg,#7B61FF,#4cc9f0);
border:none;
color:white;
cursor:pointer;
}

/* PATH */
.path{
margin-top:60px;
padding:20px;
background:rgba(255,255,255,0.03);
border:1px solid rgba(255,255,255,0.08);
border-radius:14px;
backdrop-filter:blur(12px);
}

.path-title{
font-size:18px;
margin-bottom:12px;
font-weight:600;
}

.steps{
display:grid;
grid-template-columns:repeat(auto-fit,minmax(220px,1fr));
gap:10px;
}

.step{
padding:12px;
border-radius:10px;
background:rgba(123,97,255,0.12);
border:1px solid rgba(123,97,255,0.3);
cursor:pointer;
transition:0.2s;
}

.step:hover{
transform:scale(1.03);
}

.active-path{
margin-top:15px;
padding:12px;
border-radius:10px;
background:rgba(76,201,240,0.1);
border:1px solid rgba(76,201,240,0.3);
display:none;
}

/* SMALL TABS */
.small-tab{
position:fixed;
bottom:20px;
left:20px;
background:linear-gradient(90deg,#7B61FF,#4cc9f0);
padding:10px 14px;
border-radius:12px;
cursor:pointer;
font-size:13px;
z-index:20;
box-shadow:0 0 20px rgba(123,97,255,0.4);
}

.brand-modal{
position:fixed;
inset:0;
background:rgba(0,0,0,0.6);
display:none;
align-items:center;
justify-content:center;
z-index:50;
}

.brand-box{
background:#0f1020;
padding:22px;
border-radius:16px;
max-width:520px;
width:90%;
border:1px solid rgba(255,255,255,0.08);
backdrop-filter:blur(12px);
}

.brand-list{
margin-top:10px;
line-height:1.6;
opacity:0.9;
}

.close-btn{
margin-top:12px;
background:#7B61FF;
border:none;
color:#fff;
padding:10px 14px;
border-radius:10px;
cursor:pointer;
}
</style>
</head>

<body>

<div class="bg"></div>

<div class="container">

<nav>
<div class="logo-3d">
<div class="logo-wrap">
<span class="nn">NN</span>
<span class="ai-dot">AI</span>
</div>
<div class="key-icon"></div>
</div>
</nav>

<h1>Next<span>Node</span>key</h1>

<p style="margin-top:10px; opacity:0.85;">
NNkey — система роста бизнеса через стратегический бренд, точный маркетинг и управляемое привлечение клиентов
</p>

<!-- SERVICES GRID -->
<div class="grid">
<div class="card"><b>🎯 Брендинг</b><br>Айдентика и позиционирование</div>
<div class="card"><b>📈 Маркетинг</b><br>Реклама и рост клиентов</div>
<div class="card"><b>🤖 AI-консультант</b><br>Навигация и стратегия</div>
<div class="card"><b>👥 Менторство</b><br>Сопровождение бизнеса</div>
</div>

<!-- PATH -->
<div class="path">
  <div class="path-title">🎯 Выбери путь своего бизнеса</div>

  <div class="steps">
    <div class="step" onclick="choose('start')">🚀 Хочу запустить бизнес</div>
    <div class="step" onclick="choose('grow')">📈 Уже есть бизнес, хочу рост</div>
    <div class="step" onclick="choose('brand')">🎯 Хочу сильный бренд</div>
    <div class="step" onclick="choose('mentor')">👥 Нужен ментор / сопровождение</div>
  </div>

  <div class="active-path" id="pathBox"></div>
</div>

<!-- CHAT -->
<div class="chat">

<div class="messages" id="messages">
🤖 NNkey: Я превращаю бизнес в систему роста
</div>

<div class="input">
<input id="msg">
<button onclick="send()">→</button>
</div>

<button class="cta" onclick="openForm()">Оставить заявку</button>

<div id="form" style="display:none;margin-top:10px;">
<input id="name" placeholder="Имя" style="width:100%;margin-bottom:8px;padding:10px;">
<input id="contact" placeholder="Контакт" style="width:100%;margin-bottom:8px;padding:10px;">
<button class="cta" onclick="submitLead()">Отправить</button>
</div>

</div>
</div>

<!-- TABS -->
<div class="small-tab" onclick="openBrand()">О бренде</div>
<div class="small-tab" style="left:140px;background:linear-gradient(90deg,#4cc9f0,#7B61FF);" onclick="openServices()">Услуги</div>

<!-- BRAND MODAL -->
<div class="brand-modal" id="brandModal" onclick="closeModal(event)">
<div class="brand-box">

<h3>NNkey — система роста</h3>

<p style="margin-top:10px;">
NNkey — это команда специалистов по маркетингу, дизайну и стратегии, которая выстраивает для бизнеса систему роста: от упаковки бренда до стабильного привлечения клиентов.

Мы не продаём “рекламу” или отдельные услуги.
Мы создаём структуру, которая начинает работать как механизм:

бренд → позиционирование → маркетинг → поток заявок

Для ускорения процессов мы используем современные AI-инструменты, но стратегию, креатив и результат создают живые специалисты..
</p>

<p style="margin-top:10px;">
Наша фишка — глубокий анализ ниши, упаковка бизнеса и создание стратегии роста, которая работает как система.
</p>

<p style="margin-top:10px;">
 Поэтому с нами растут быстрее, стабильнее и дороже.
</p>

<div style="margin-top:15px;">
<b>Основатель:</b><br>
Радченко Вероника Дмитриевна
</div>

<div style="margin-top:10px;">
<b>Контакт:</b><br>
veroniradchenko@yandex.ru
</div>

</div>
</div>

<!-- SERVICES MODAL -->
<div class="brand-modal" id="servicesModal" onclick="closeModal(event)">
<div class="brand-box">

<h3>Наши услуги</h3>

<div class="brand-list">

<b>🔥 Маркетологи</b><br>
— таргетированная реклама<br>
— воронки продаж<br>
— стратегия роста<br><br>

<b>📣 PR-специалисты</b><br>
— продвижение бренда<br>
— личный бренд<br>
— медиа и охваты<br><br>

<b>🎨 Дизайнеры</b><br>
— фирменный стиль<br>
— упаковка бизнеса<br>
— визуальные системы<br>

</div>

<button class="close-btn" onclick="document.getElementById('servicesModal').style.display='none'">
Закрыть
</button>

</div>
</div>

<script>

let step = 0;
let lead = { name:"", contact:"", goal:"" };

function send(){
const input = document.getElementById("msg");
const box = document.getElementById("messages");

if(!input.value) return;

const text = input.value.trim();
box.innerHTML += `<div>👤 ${text}</div>`;
input.value = "";

if(step === 0){
box.innerHTML += `<div>🤖 Привет! У тебя уже есть бизнес или ты только начинаешь?</div>`;
step = 1;
return;
}

if(step === 1){
lead.goal = text;
box.innerHTML += `<div>🤖 Что важнее: клиенты, бренд или масштаб?</div>`;
step = 2;
return;
}

if(step === 2){
box.innerHTML += `<div>🤖 Как тебя зовут?</div>`;
step = 3;
return;
}

if(step === 3){
lead.name = text;
box.innerHTML += `<div>🤖 Оставь контакт</div>`;
step = 4;
return;
}

if(step === 4){
lead.contact = text;

fetch("https://script.google.com/macros/s/AKfycbzkcT3993_G9FWJabJRA7NKLazJUqV4hsAxaBtqu7CbXibsNR43uJOB_d8Tv_PhuneVCw/exec",{
method:"POST",
body:JSON.stringify(lead)
});

step = 0;
lead = { name:"", contact:"", goal:"" };
}
}

/* PATH */
function choose(type){
const box = document.getElementById("pathBox");
box.style.display="block";

let text="";

if(type==="start") text="🚀 Запуск → Брендинг → Маркетинг → Рост";
if(type==="grow") text="📈 Анализ → Реклама → Масштаб";
if(type==="brand") text="🎯 Бренд → Упаковка → Стратегия";
if(type==="mentor") text="👥 Менторство → Полное сопровождение";

box.innerText=text;
}

/* MODALS */
function openBrand(){
document.getElementById("brandModal").style.display="flex";
}

function openServices(){
document.getElementById("servicesModal").style.display="flex";
}

function closeModal(e){
if(e.target.classList.contains("brand-modal")){
e.target.style.display="none";
}
}
/* FORM */
function openForm() {
  document.getElementById("form").style.display = "block";
}

/* GOOGLE SHEETS */
async function submitLead() {
  const name = document.getElementById("name").value;
  const contact = document.getElementById("contact").value;

  if (!name || !contact) {
    alert("Заполни поля");
    return;
  }

  await fetch("https://script.google.com/macros/s/AKfycbzkcT3993_G9FWJabJRA7NKLazJUqV4hsAxaBtqu7CbXibsNR43uJOB_d8Tv_PhuneVCw/exec", {
    method: "POST",
    body: JSON.stringify({ name, contact })
  });

  alert("Заявка отправлена");
}
</script>

</body>
</html>
