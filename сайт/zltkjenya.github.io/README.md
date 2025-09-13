<!doctype html>
<html lang="en">
<head>
<meta charset="utf-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>Simple HTML Page</title>
<style>
:root{ --bg:#f7fafc; --card:#ffffff; --accent:#2563eb; --muted:#6b7280; }
body{ font-family:Inter, system-ui, -apple-system,Segoe UI, Roboto, "Helvetica Neue", Arial; margin:0; background:var(--bg); color:#111827; }
.container{ max-width:900px; margin:48px auto; padding:24px; }
header{ display:flex; align-items:center; justify-content:space-between; gap:16px; }
h1{ margin:0; font-size:1.5rem; }
nav a{ margin-left:12px; text-decoration:none; color:var(--muted); font-size:0.95rem }
.card{ background:var(--card); border-radius:12px; padding:18px; box-shadow:0 6px 18px rgba(16,24,40,0.06); }
.actions{ margin-top:16px; display:flex; gap:8px }
button{ border:0; padding:10px 14px; border-radius:8px; cursor:pointer; font-weight:600 }
.btn-primary{ background:var(--accent); color:#fff }
.btn-ghost{ background:transparent; color:var(--muted) }
footer{ margin-top:28px; text-align:center; color:var(--muted); font-size:0.9rem }
pre{ background:#0f172a; color:#e6eef8; padding:12px; border-radius:8px; overflow:auto }
</style>
</head>
<body>
<div class="container">
<header>
<h1>Збірна України з футболу</h1>
<nav>
<a href="#">Головна</a>
<a href="#Team">Команда</a>
<a href="#history">Історія</a>
</nav>
</header>

<main style="margin-top:18px">
<section class="card">
<h2 id="welcome">Ласкаво просимо на офіційний сайт збірної України!</h2>
<p style="color:var(--muted)">Тут ви знайдете інформацію про команду, історію клубу та останні новини.</p>
<div class="actions">
<button class="btn-primary" id="greetBtn">Greet me</button>
<button class="btn-ghost" id="showCode">Show HTML sample</button>
</div>
<div id="output" style="margin-top:14px"></div>
</section>

<section class="card" style="margin-top:18px">
<h3 id="history">Історія клубу</h3>
<p style="color:var(--muted)">Збірна України з футболу була створена у 1992 році після вступу Федерації футболу України (ФФУ) до УЄФА та ФІФА. Перший матч новостворена команда провела 29 квітня 1992 року в Ужгороді проти збірної Угорщини, який завершився поразкою 1:3, а перший гол в історії збірної забив Іван Гецко.</p>
</section>

<section class="card" style="margin-top:18px">
<h3 id="Team">Команда</h3>
<p style="color:var(--muted)">Воротарі
Андрій Лунін («Реал», Іспанія)
Анатолій Трубін («Бенфіка», Португалія)
Дмитро Різник («Шахтар»)
Захисники
Валерій Бондар («Шахтар»)
Микола Матвійенко («Шахтар»)
Юхим Конопля («Шахтар»)
Тарас Михавко («Динамо»)
Олександр Тимчик («Динамо»)
Ілля Забарний (ПСЖ, Франція)
Олександр Сваток («Остін», США)
Віталій Миколенко («Евертон», Англія)
Півзахисники
Олег Очеретько («Шахтар»)
Георгій Судаков («Шахтар»)
Артем Бондаренко («Шахтар»)
Олексій Гуцуляк («Полісся»)
Олександр Назаренко («Полісся»)
Олександр Зінченко («Арсенал», Англія)
Єгор Ярмолюк («Брентфорд», Англія)
Іван Калюжний («Металіст 1925»)
Микола Шапаренко («Динамо»)
Віктор Циганков («Жирона», Іспанія)
Олександр Зубков («Трабзонспор», Туреччина)
Нападники
Роман Яремчук («Олімпіакос», Греція)
Артем Довбик («Рома», Італія)
Владислав Ванат («Динамо»).</p>
<pre id="codePreview" style="display:none">&lt;!-- example: put your snippet here --&gt;&#10;&lt;p&gt;Hello world&lt;/p&gt;</pre>
</section>
</main>

<footer>
<small>Generated: <span id="now"></span></small>
</footer>
</div>

<script>
document.getElementById('now').textContent = new Date().toLocaleString();
document.getElementById('greetBtn').addEventListener('click', function(){
const out = document.getElementById('output');
out.innerHTML = '<strong>Hello!</strong> Nice to meet you. \n' +
'Try the "Show HTML sample" button to reveal a small snippet.';
});

document.getElementById('showCode').addEventListener('click', function(){
const pre = document.getElementById('codePreview');
pre.style.display = pre.style.display === 'none' ? 'block' : 'none';
});
</script>
</body>
</html>
