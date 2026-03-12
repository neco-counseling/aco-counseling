# aco-counseling
<!DOCTYPE html>

<html lang="ja">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0">
<meta name="theme-color" content="#faf7f2">
<title>こころの相談室 — あなたの悩みに寄り添います</title>
<link href="https://fonts.googleapis.com/css2?family=Noto+Serif+JP:wght@300;400;600&family=Zen+Kaku+Gothic+New:wght@300;400;700&display=swap" rel="stylesheet">
<style>
  :root {
    --cream: #f5f0e8;
    --warm-white: #faf7f2;
    --sage: #8ba888;
    --sage-dark: #5f7a5c;
    --terracotta: #c47a5a;
    --dusty-rose: #d4a0a0;
    --charcoal: #2d2d2d;
    --muted: #4a4644;
    --light-sage: #d4e0d2;
    --parchment: #e8dfc8;
  }

- { margin: 0; padding: 0; box-sizing: border-box; }

html { scroll-behavior: smooth; }

body {
font-family: ‘Noto Serif JP’, serif;
background: var(–warm-white);
color: var(–charcoal);
overflow-x: hidden;
}

/* Organic background texture */
body::before {
content: ‘’;
position: fixed;
inset: 0;
background-image:
radial-gradient(ellipse 80% 60% at 20% 10%, rgba(139,168,136,0.08) 0%, transparent 60%),
radial-gradient(ellipse 60% 80% at 80% 90%, rgba(196,122,90,0.06) 0%, transparent 60%),
radial-gradient(ellipse 100% 100% at 50% 50%, rgba(212,224,210,0.1) 0%, transparent 70%);
pointer-events: none;
z-index: 0;
}

/* NAV */
nav {
position: fixed;
top: 0;
width: 100%;
padding: 1.2rem 3rem;
display: flex;
justify-content: space-between;
align-items: center;
background: rgba(250,247,242,0.92);
backdrop-filter: blur(12px);
border-bottom: 1px solid rgba(139,168,136,0.2);
z-index: 100;
}

.nav-logo {
font-family: ‘Noto Serif JP’, serif;
font-weight: 600;
font-size: 1.1rem;
color: var(–sage-dark);
letter-spacing: 0.15em;
}

.nav-links {
display: flex;
gap: 2.5rem;
list-style: none;
}

.nav-links a {
font-family: ‘Zen Kaku Gothic New’, sans-serif;
font-weight: 300;
font-size: 0.85rem;
color: var(–muted);
text-decoration: none;
letter-spacing: 0.08em;
transition: color 0.3s;
}

.nav-links a:hover { color: var(–sage-dark); }

.nav-cta {
background: var(–sage);
color: white !important;
padding: 0.5rem 1.4rem;
border-radius: 2rem;
transition: background 0.3s !important;
}

.nav-cta:hover { background: var(–sage-dark) !important; color: white !important; }

/* HERO */
.hero {
position: relative;
min-height: 100vh;
display: grid;
grid-template-columns: 1fr 1fr;
align-items: center;
padding: 8rem 5rem 4rem;
gap: 4rem;
z-index: 1;
}

.hero-text { animation: fadeInLeft 1s ease forwards; }

.hero-label {
font-family: ‘Zen Kaku Gothic New’, sans-serif;
font-weight: 300;
font-size: 0.8rem;
letter-spacing: 0.25em;
color: var(–terracotta);
text-transform: uppercase;
margin-bottom: 1.5rem;
display: flex;
align-items: center;
gap: 1rem;
}

.hero-label::before {
content: ‘’;
display: block;
width: 2rem;
height: 1px;
background: var(–terracotta);
}

h1 {
font-size: clamp(2.4rem, 4vw, 3.8rem);
font-weight: 300;
line-height: 1.6;
letter-spacing: 0.05em;
color: var(–charcoal);
margin-bottom: 2rem;
}

h1 span {
color: var(–sage-dark);
font-weight: 600;
}

.hero-desc {
font-family: ‘Zen Kaku Gothic New’, sans-serif;
font-weight: 400;
font-size: 1rem;
line-height: 2;
color: #3a3634;
margin-bottom: 3rem;
max-width: 440px;
}

.hero-buttons {
display: flex;
gap: 1rem;
flex-wrap: wrap;
}

.btn-primary {
background: var(–sage-dark);
color: white;
padding: 1rem 2.5rem;
border: none;
border-radius: 3rem;
font-family: ‘Zen Kaku Gothic New’, sans-serif;
font-size: 0.9rem;
letter-spacing: 0.08em;
cursor: pointer;
text-decoration: none;
display: inline-block;
transition: all 0.3s;
box-shadow: 0 4px 20px rgba(95,122,92,0.25);
}

.btn-primary:hover {
background: var(–sage);
transform: translateY(-2px);
box-shadow: 0 8px 30px rgba(95,122,92,0.3);
}

.btn-secondary {
background: transparent;
color: var(–charcoal);
padding: 1rem 2rem;
border: 1.5px solid var(–parchment);
border-radius: 3rem;
font-family: ‘Zen Kaku Gothic New’, sans-serif;
font-size: 0.9rem;
letter-spacing: 0.08em;
cursor: pointer;
text-decoration: none;
display: inline-block;
transition: all 0.3s;
}

.btn-secondary:hover {
border-color: var(–sage);
color: var(–sage-dark);
}

/* Hero visual */
.hero-visual {
position: relative;
height: 500px;
animation: fadeInRight 1s ease forwards;
}

.circle-large {
position: absolute;
top: 50%;
left: 50%;
transform: translate(-50%, -50%);
width: 380px;
height: 380px;
border-radius: 50%;
background: radial-gradient(circle at 35% 35%, var(–light-sage), var(–parchment));
animation: breathe 6s ease-in-out infinite;
}

.circle-accent {
position: absolute;
top: 10%;
right: 10%;
width: 100px;
height: 100px;
border-radius: 50%;
background: rgba(196,122,90,0.2);
animation: float1 5s ease-in-out infinite;
}

.circle-small {
position: absolute;
bottom: 15%;
left: 10%;
width: 60px;
height: 60px;
border-radius: 50%;
background: rgba(139,168,136,0.35);
animation: float2 7s ease-in-out infinite;
}

.hero-card {
position: absolute;
top: 50%;
left: 50%;
transform: translate(-50%, -50%);
text-align: center;
z-index: 2;
}

.hero-icon {
font-size: 5rem;
display: block;
margin-bottom: 1rem;
animation: pulse 3s ease-in-out infinite;
}

.hero-card-text {
font-family: ‘Noto Serif JP’, serif;
font-size: 1rem;
color: var(–sage-dark);
letter-spacing: 0.1em;
}

/* STATS */
.stats {
position: relative;
z-index: 1;
padding: 3rem 5rem;
display: flex;
justify-content: center;
gap: 4rem;
background: var(–cream);
border-top: 1px solid rgba(139,168,136,0.2);
border-bottom: 1px solid rgba(139,168,136,0.2);
}

.stat-item { text-align: center; }

.stat-num {
font-size: 2.2rem;
font-weight: 600;
color: var(–sage-dark);
letter-spacing: 0.05em;
}

.stat-label {
font-family: ‘Zen Kaku Gothic New’, sans-serif;
font-weight: 300;
font-size: 0.8rem;
color: var(–muted);
letter-spacing: 0.1em;
margin-top: 0.3rem;
}

/* SECTION COMMON */
section {
position: relative;
z-index: 1;
padding: 6rem 5rem;
}

.section-label {
font-family: ‘Zen Kaku Gothic New’, sans-serif;
font-size: 0.75rem;
letter-spacing: 0.3em;
color: var(–terracotta);
text-transform: uppercase;
display: flex;
align-items: center;
gap: 1rem;
margin-bottom: 1rem;
}

.section-label::before {
content: ‘’;
width: 1.5rem;
height: 1px;
background: var(–terracotta);
}

h2 {
font-size: clamp(1.8rem, 3vw, 2.8rem);
font-weight: 300;
line-height: 1.5;
letter-spacing: 0.05em;
margin-bottom: 1rem;
}

.section-sub {
font-family: ‘Zen Kaku Gothic New’, sans-serif;
font-weight: 400;
color: #4a4644;
font-size: 0.95rem;
line-height: 2;
margin-bottom: 4rem;
max-width: 500px;
}

/* WORRIES GRID */
.worries-section { background: var(–warm-white); }

.worries-grid {
display: grid;
grid-template-columns: repeat(3, 1fr);
gap: 1.5rem;
}

.worry-card {
background: var(–cream);
border-radius: 1.5rem;
padding: 2rem;
border: 1px solid rgba(139,168,136,0.2);
transition: all 0.4s;
cursor: default;
position: relative;
overflow: hidden;
}

.worry-card::after {
content: ‘’;
position: absolute;
bottom: 0;
left: 0;
width: 100%;
height: 3px;
background: linear-gradient(90deg, var(–sage), var(–terracotta));
transform: scaleX(0);
transition: transform 0.4s;
transform-origin: left;
}

.worry-card:hover {
transform: translateY(-4px);
box-shadow: 0 12px 40px rgba(95,122,92,0.12);
}

.worry-card:hover::after { transform: scaleX(1); }

.worry-emoji {
font-size: 2rem;
display: block;
margin-bottom: 1rem;
}

.worry-title {
font-size: 1.05rem;
font-weight: 600;
letter-spacing: 0.05em;
margin-bottom: 0.8rem;
color: var(–charcoal);
}

.worry-desc {
font-family: ‘Zen Kaku Gothic New’, sans-serif;
font-weight: 300;
font-size: 0.85rem;
color: var(–muted);
line-height: 1.9;
}

/* HOW IT WORKS */
.process-section {
background: var(–cream);
}

.process-steps {
display: grid;
grid-template-columns: repeat(4, 1fr);
gap: 2rem;
position: relative;
}

.process-steps::before {
content: ‘’;
position: absolute;
top: 2.5rem;
left: 10%;
width: 80%;
height: 1px;
background: linear-gradient(90deg, transparent, var(–sage), var(–terracotta), transparent);
}

.step {
text-align: center;
padding: 1rem;
}

.step-num {
width: 5rem;
height: 5rem;
border-radius: 50%;
background: var(–warm-white);
border: 2px solid var(–sage);
display: flex;
align-items: center;
justify-content: center;
margin: 0 auto 1.5rem;
font-size: 1.5rem;
font-weight: 600;
color: var(–sage-dark);
position: relative;
z-index: 1;
}

.step-title {
font-size: 1rem;
font-weight: 600;
letter-spacing: 0.05em;
margin-bottom: 0.8rem;
}

.step-desc {
font-family: ‘Zen Kaku Gothic New’, sans-serif;
font-weight: 300;
font-size: 0.82rem;
color: var(–muted);
line-height: 2;
}

/* COUNSELORS */
.counselors-section { background: var(–warm-white); }

.counselors-grid {
display: grid;
grid-template-columns: repeat(3, 1fr);
gap: 2rem;
}

.counselor-card {
background: var(–cream);
border-radius: 2rem;
padding: 2.5rem 2rem;
text-align: center;
border: 1px solid rgba(139,168,136,0.15);
transition: all 0.4s;
}

.counselor-card:hover {
transform: translateY(-6px);
box-shadow: 0 16px 48px rgba(95,122,92,0.12);
}

.counselor-avatar {
width: 90px;
height: 90px;
border-radius: 50%;
margin: 0 auto 1.5rem;
display: flex;
align-items: center;
justify-content: center;
font-size: 2.5rem;
border: 3px solid var(–light-sage);
}

.counselor-avatar.rose { background: rgba(212,160,160,0.3); }
.counselor-avatar.sage { background: rgba(139,168,136,0.3); }
.counselor-avatar.terra { background: rgba(196,122,90,0.2); }

.counselor-name {
font-size: 1.15rem;
font-weight: 600;
letter-spacing: 0.05em;
margin-bottom: 0.3rem;
}

.counselor-role {
font-family: ‘Zen Kaku Gothic New’, sans-serif;
font-size: 0.8rem;
color: var(–terracotta);
letter-spacing: 0.1em;
margin-bottom: 1rem;
}

.counselor-bio {
font-family: ‘Zen Kaku Gothic New’, sans-serif;
font-weight: 400;
font-size: 0.85rem;
color: #3a3634;
line-height: 2;
margin-bottom: 1.5rem;
}

.counselor-tags {
display: flex;
flex-wrap: wrap;
gap: 0.5rem;
justify-content: center;
}

.tag {
background: var(–light-sage);
color: var(–sage-dark);
padding: 0.3rem 0.9rem;
border-radius: 2rem;
font-family: ‘Zen Kaku Gothic New’, sans-serif;
font-size: 0.75rem;
letter-spacing: 0.05em;
}

/* TESTIMONIALS */
.testimonials-section {
background: var(–sage-dark);
color: white;
}

.testimonials-section .section-label { color: var(–light-sage); }
.testimonials-section .section-label::before { background: var(–light-sage); }
.testimonials-section h2 { color: white; }

.testimonials-grid {
display: grid;
grid-template-columns: repeat(3, 1fr);
gap: 2rem;
}

.testimonial-card {
background: rgba(255,255,255,0.08);
border: 1px solid rgba(255,255,255,0.15);
border-radius: 1.5rem;
padding: 2rem;
backdrop-filter: blur(10px);
transition: all 0.3s;
}

.testimonial-card:hover {
background: rgba(255,255,255,0.13);
transform: translateY(-3px);
}

.testimonial-quote {
font-size: 2.5rem;
color: rgba(255,255,255,0.25);
margin-bottom: 0.5rem;
line-height: 1;
}

.testimonial-text {
font-family: ‘Zen Kaku Gothic New’, sans-serif;
font-weight: 300;
font-size: 0.9rem;
line-height: 2;
color: rgba(255,255,255,0.85);
margin-bottom: 1.5rem;
}

.testimonial-author {
font-size: 0.85rem;
font-weight: 600;
color: var(–light-sage);
letter-spacing: 0.08em;
}

.testimonial-detail {
font-family: ‘Zen Kaku Gothic New’, sans-serif;
font-size: 0.75rem;
color: rgba(255,255,255,0.5);
letter-spacing: 0.05em;
}

/* CONTACT */
.contact-section {
background: var(–cream);
text-align: center;
}

.contact-section h2 { color: var(–charcoal); }

.contact-card {
max-width: 680px;
margin: 0 auto;
background: var(–warm-white);
border-radius: 2rem;
padding: 3.5rem;
border: 1px solid rgba(139,168,136,0.25);
box-shadow: 0 8px 40px rgba(95,122,92,0.08);
}

.form-group {
margin-bottom: 1.5rem;
text-align: left;
}

label {
display: block;
font-family: ‘Zen Kaku Gothic New’, sans-serif;
font-weight: 400;
font-size: 0.85rem;
color: var(–charcoal);
letter-spacing: 0.05em;
margin-bottom: 0.6rem;
}

label span {
color: var(–terracotta);
font-size: 0.75rem;
margin-left: 0.3rem;
}

input, select, textarea {
width: 100%;
padding: 0.9rem 1.2rem;
border: 1.5px solid var(–parchment);
border-radius: 0.8rem;
font-family: ‘Zen Kaku Gothic New’, sans-serif;
font-size: 0.9rem;
background: var(–warm-white);
color: var(–charcoal);
transition: border-color 0.3s;
outline: none;
}

input:focus, select:focus, textarea:focus {
border-color: var(–sage);
box-shadow: 0 0 0 3px rgba(139,168,136,0.1);
}

textarea { min-height: 120px; resize: vertical; }

.form-grid {
display: grid;
grid-template-columns: 1fr 1fr;
gap: 1rem;
}

.submit-btn {
width: 100%;
padding: 1.1rem;
background: var(–sage-dark);
color: white;
border: none;
border-radius: 3rem;
font-family: ‘Zen Kaku Gothic New’, sans-serif;
font-size: 1rem;
letter-spacing: 0.12em;
cursor: pointer;
margin-top: 1rem;
transition: all 0.3s;
box-shadow: 0 4px 20px rgba(95,122,92,0.25);
}

.submit-btn:hover {
background: var(–sage);
transform: translateY(-2px);
box-shadow: 0 8px 30px rgba(95,122,92,0.3);
}

.privacy-note {
font-family: ‘Zen Kaku Gothic New’, sans-serif;
font-size: 0.75rem;
color: var(–muted);
margin-top: 1rem;
letter-spacing: 0.03em;
}

/* FOOTER */
footer {
position: relative;
z-index: 1;
background: var(–charcoal);
color: rgba(255,255,255,0.6);
padding: 4rem 5rem 2rem;
}

.footer-grid {
display: grid;
grid-template-columns: 2fr 1fr 1fr 1fr;
gap: 3rem;
margin-bottom: 3rem;
}

.footer-brand h3 {
font-size: 1.15rem;
font-weight: 600;
color: white;
letter-spacing: 0.12em;
margin-bottom: 1rem;
}

.footer-brand p {
font-family: ‘Zen Kaku Gothic New’, sans-serif;
font-weight: 300;
font-size: 0.82rem;
line-height: 2;
}

.footer-col h4 {
font-size: 0.85rem;
font-weight: 600;
color: white;
letter-spacing: 0.1em;
margin-bottom: 1rem;
}

.footer-col ul {
list-style: none;
}

.footer-col ul li {
margin-bottom: 0.6rem;
}

.footer-col ul li a {
font-family: ‘Zen Kaku Gothic New’, sans-serif;
font-weight: 300;
font-size: 0.82rem;
color: rgba(255,255,255,0.5);
text-decoration: none;
letter-spacing: 0.05em;
transition: color 0.3s;
}

.footer-col ul li a:hover { color: var(–light-sage); }

.footer-bottom {
border-top: 1px solid rgba(255,255,255,0.1);
padding-top: 2rem;
display: flex;
justify-content: space-between;
align-items: center;
font-family: ‘Zen Kaku Gothic New’, sans-serif;
font-size: 0.78rem;
letter-spacing: 0.05em;
}

/* ANIMATIONS */
@keyframes fadeInLeft {
from { opacity: 0; transform: translateX(-30px); }
to { opacity: 1; transform: translateX(0); }
}

@keyframes fadeInRight {
from { opacity: 0; transform: translateX(30px); }
to { opacity: 1; transform: translateX(0); }
}

@keyframes breathe {
0%, 100% { transform: translate(-50%, -50%) scale(1); }
50% { transform: translate(-50%, -50%) scale(1.05); }
}

@keyframes float1 {
0%, 100% { transform: translateY(0) rotate(0deg); }
50% { transform: translateY(-15px) rotate(10deg); }
}

@keyframes float2 {
0%, 100% { transform: translateY(0) rotate(0deg); }
50% { transform: translateY(12px) rotate(-8deg); }
}

@keyframes pulse {
0%, 100% { transform: scale(1); }
50% { transform: scale(1.08); }
}

/* Scroll reveal */
.reveal {
opacity: 0;
transform: translateY(24px);
transition: opacity 0.7s ease, transform 0.7s ease;
}

.reveal.visible {
opacity: 1;
transform: translateY(0);
}

/* Mobile-first responsive */
@media (max-width: 640px) {
nav { padding: 1rem 1.2rem; }
.nav-links { display: none; }

```
.hero {
  grid-template-columns: 1fr !important;
  padding: 5rem 1.4rem 3rem !important;
  gap: 1.5rem !important;
  min-height: auto !important;
}
.hero-visual { display: none !important; }
h1 { font-size: 1.9rem !important; }
.hero-desc { font-size: 0.88rem !important; max-width: 100% !important; }

section { padding: 3.5rem 1.4rem; }
h2 { font-size: 1.7rem; }
.counselors-grid { grid-template-columns: 1fr; }
.contact-card { padding: 1.6rem 1.2rem; }
.form-grid { grid-template-columns: 1fr; }
```

}
</style>

</head>
<body>

<!-- NAV -->

<nav>
  <div class="nav-logo">
    こころの相談室
    <div style="font-family:'Zen Kaku Gothic New',sans-serif; font-weight:300; font-size:0.65rem; letter-spacing:0.18em; color:var(--muted); margin-top:0.1rem;">思考の根本改善</div>
  </div>
  <ul class="nav-links">
    <li><a href="#worries">コース</a></li>
    <li><a href="#counselors">カウンセラー</a></li>
    <li><a href="#testimonials">お客様の声</a></li>
    <li><a href="https://lin.ee/MCWLE3V" target="_blank" class="nav-cta">お申し込み</a></li>
  </ul>
</nav>

<!-- HERO -->

<section class="hero">
  <div class="hero-text">
    <div class="hero-label">安心・安全・秘密厳守</div>
    <h1>
      あなたの悩みを<br>
      <span>一人で</span>抱えないで
    </h1>
    <p class="hero-desc">
      悩み。<br>
      それは思考の誤りにより発生しています。<br><br>
      考え方、捉え方を変えれば選択が広がり見えてきます。<br>
      不透明な未来の視点から今に向けて、自分の人生を自分で切り拓きましょう。<br><br>
      そのお手伝い、きっかけとなるのが私の役目です。
    </p>
    <div class="hero-buttons">
      <a href="https://lin.ee/MCWLE3V" target="_blank" class="btn-primary">お申し込みはこちら</a>
    </div>
  </div>
  <div class="hero-visual">
    <div class="circle-large"></div>
    <div class="circle-accent"></div>
    <div class="circle-small"></div>
    <div class="hero-card">
      <span class="hero-icon">🌿</span>
      <p class="hero-card-text">あなたのペースで</p>
    </div>
  </div>
</section>

<!-- COURSES -->

<section id="worries" class="worries-section">
  <div class="section-label">コース・料金</div>
  <h2>2つのコースから<br>お選びください</h2>
  <p class="section-sub">チャットで気軽に。あなたのペースで思考を変えていきます。</p>

  <div style="display:flex; flex-direction:column; gap:1.6rem; max-width:480px; margin:0 auto;">

```
<!-- ① お試しコース -->
<div class="reveal" style="background:var(--warm-white); border-radius:1.8rem; border:1.5px solid rgba(139,168,136,0.3); overflow:hidden; box-shadow:0 4px 20px rgba(95,122,92,0.07); position:relative;">
  <div style="position:absolute; top:1.2rem; right:1.3rem; background:var(--terracotta); color:white; font-family:'Zen Kaku Gothic New',sans-serif; font-size:0.68rem; font-weight:700; letter-spacing:0.1em; padding:0.25rem 0.85rem; border-radius:2rem;">毎月3名限定</div>
  <div style="background:var(--cream); padding:1.6rem 1.8rem 1.2rem;">
    <div style="font-family:'Zen Kaku Gothic New',sans-serif; font-size:0.7rem; letter-spacing:0.22em; color:var(--terracotta); margin-bottom:0.5rem; text-transform:uppercase;">お試しコース</div>
    <div style="display:flex; align-items:flex-end; gap:0.4rem; margin-bottom:0.2rem;">
      <span style="font-size:2.2rem; font-weight:600; color:var(--charcoal); line-height:1;">¥1,980</span>
      <span style="font-family:'Zen Kaku Gothic New',sans-serif; font-size:0.76rem; color:var(--muted); padding-bottom:0.25rem;">税込</span>
    </div>
    <div style="font-family:'Zen Kaku Gothic New',sans-serif; font-size:0.8rem; color:var(--muted);">まずは試してみたい方へ</div>
  </div>
  <div style="padding:1.4rem 1.8rem 1.8rem;">
    <div style="display:flex; flex-direction:column; gap:0.8rem; margin-bottom:1.6rem;">
      <div style="display:flex; align-items:center; gap:0.8rem;">
        <span style="width:1.5rem; height:1.5rem; background:var(--light-sage); border-radius:50%; display:flex; align-items:center; justify-content:center; font-size:0.7rem; flex-shrink:0;">💬</span>
        <span style="font-family:'Zen Kaku Gothic New',sans-serif; font-size:0.86rem; color:var(--charcoal);">チャット <strong>10分間</strong></span>
      </div>
      <div style="display:flex; align-items:center; gap:0.8rem;">
        <span style="width:1.5rem; height:1.5rem; background:var(--light-sage); border-radius:50%; display:flex; align-items:center; justify-content:center; font-size:0.7rem; flex-shrink:0;">📅</span>
        <span style="font-family:'Zen Kaku Gothic New',sans-serif; font-size:0.86rem; color:var(--charcoal);">毎週日曜日対応</span>
      </div>
      <div style="display:flex; align-items:center; gap:0.8rem;">
        <span style="width:1.5rem; height:1.5rem; background:rgba(196,122,90,0.15); border-radius:50%; display:flex; align-items:center; justify-content:center; font-size:0.7rem; flex-shrink:0;">🌸</span>
        <span style="font-family:'Zen Kaku Gothic New',sans-serif; font-size:0.86rem; color:var(--terracotta); font-weight:600;">毎月3名限定</span>
      </div>
    </div>
    <a href="https://lin.ee/MCWLE3V" target="_blank" class="btn-secondary" style="display:block; text-align:center; padding:0.85rem;">このコースで申し込む</a>
  </div>
</div>

<!-- ② 思考根本改善コース（ミディアム高級感） -->
<div class="reveal" style="background:linear-gradient(150deg,#4a5c48 0%,#5e7058 55%,#635848 100%); border-radius:1.8rem; border:1px solid rgba(220,200,155,0.2); overflow:hidden; box-shadow:0 8px 36px rgba(0,0,0,0.1), 0 1px 6px rgba(210,180,100,0.04); position:relative;">
  <div style="position:absolute; top:0; left:0; right:0; height:1px; background:linear-gradient(90deg,transparent,rgba(220,200,150,0.3),transparent);"></div>
  <div style="position:absolute; top:1.3rem; right:1.3rem; background:rgba(210,190,140,0.15); border:1px solid rgba(210,190,140,0.28); color:rgba(230,215,175,0.85); font-family:'Zen Kaku Gothic New',sans-serif; font-size:0.68rem; font-weight:600; letter-spacing:0.12em; padding:0.25rem 0.8rem; border-radius:2rem;">おすすめ</div>
  <div style="padding:1.6rem 1.8rem 1.2rem;">
    <div style="font-family:'Zen Kaku Gothic New',sans-serif; font-size:0.7rem; letter-spacing:0.22em; color:rgba(220,200,155,0.7); margin-bottom:0.5rem; text-transform:uppercase;">思考根本改善コース</div>
    <div style="display:flex; align-items:flex-end; gap:0.4rem; margin-bottom:0.2rem;">
      <span style="font-size:2.2rem; font-weight:600; color:rgba(240,225,185,0.9); line-height:1;">¥8,000</span>
      <span style="font-family:'Zen Kaku Gothic New',sans-serif; font-size:0.76rem; color:rgba(220,200,155,0.5); padding-bottom:0.25rem;">1回 / 税込</span>
    </div>
    <div style="font-family:'Zen Kaku Gothic New',sans-serif; font-size:0.8rem; color:rgba(210,195,155,0.6);">本格的に変わりたい方へ</div>
  </div>
  <div style="margin:0 1.8rem; height:1px; background:linear-gradient(90deg,transparent,rgba(210,190,140,0.15),transparent);"></div>
  <div style="padding:1.4rem 1.8rem 1.8rem;">
    <div style="display:flex; flex-direction:column; gap:0.8rem; margin-bottom:1.6rem;">
      <div style="display:flex; align-items:center; gap:0.8rem;">
        <span style="width:1.5rem; height:1.5rem; background:rgba(200,175,110,0.12); border:1px solid rgba(200,175,110,0.22); border-radius:50%; display:flex; align-items:center; justify-content:center; font-size:0.7rem; flex-shrink:0;">💬</span>
        <span style="font-family:'Zen Kaku Gothic New',sans-serif; font-size:0.86rem; color:rgba(235,220,185,0.85);">チャット <strong style="color:rgba(240,225,185,0.95);">30分間</strong></span>
      </div>
      <div style="display:flex; align-items:center; gap:0.8rem;">
        <span style="width:1.5rem; height:1.5rem; background:rgba(200,175,110,0.12); border:1px solid rgba(200,175,110,0.22); border-radius:50%; display:flex; align-items:center; justify-content:center; font-size:0.7rem; flex-shrink:0;">📅</span>
        <span style="font-family:'Zen Kaku Gothic New',sans-serif; font-size:0.86rem; color:rgba(235,220,185,0.85);">毎週日曜日対応</span>
      </div>
      <div style="display:flex; align-items:center; gap:0.8rem;">
        <span style="width:1.5rem; height:1.5rem; background:rgba(200,175,110,0.12); border:1px solid rgba(200,175,110,0.22); border-radius:50%; display:flex; align-items:center; justify-content:center; font-size:0.7rem; flex-shrink:0;">🌱</span>
        <span style="font-family:'Zen Kaku Gothic New',sans-serif; font-size:0.86rem; color:rgba(235,220,185,0.85);">思考パターンの根本改善</span>
      </div>
    </div>
    <a href="https://lin.ee/MCWLE3V" target="_blank" style="display:block; text-align:center; padding:0.85rem; background:linear-gradient(135deg,rgba(170,138,60,0.85),rgba(200,170,100,0.85)); color:#1e1a0e; border-radius:3rem; font-family:'Zen Kaku Gothic New',sans-serif; font-size:0.88rem; font-weight:700; letter-spacing:0.08em; text-decoration:none; box-shadow:0 3px 14px rgba(170,138,60,0.2);">このコースで申し込む</a>
  </div>
</div>
```

  </div>
</section>

<!-- COUNSELORS -->

<section id="counselors" class="counselors-section">
  <div class="section-label">カウンセラー紹介</div>
  <h2>担当カウンセラー</h2>
  <p class="section-sub">思考改善を専門に、チャットで丁寧にサポートします。</p>
  <div style="display:flex; justify-content:center;">
    <div class="counselor-card reveal" style="max-width:420px; width:100%;">
      <div class="counselor-avatar sage" style="width:110px;height:110px;font-size:3rem;">🌿</div>
      <div class="counselor-name">Aco</div>
      <div class="counselor-role">思考改善カウンセラー</div>
      <p class="counselor-bio">現在の職場でも思考教育を行っています。ネガティブな思考のクセに寄り添い、より生きやすい考え方を一緒に育てます。チャット形式で、あなたのペースに合わせて丁寧にサポートします。</p>
      <div style="margin-top:1.2rem; padding:0.8rem 1.2rem; background:var(--light-sage); border-radius:0.8rem; display:inline-block;">
        <span style="font-family:'Zen Kaku Gothic New',sans-serif; font-size:0.82rem; color:var(--sage-dark); letter-spacing:0.08em;">📅 対応日：毎週日曜日のみ</span>
      </div>
      <div class="counselor-tags">
        <span class="tag">思考改善</span>
        <span class="tag">認知の歪み</span>
        <span class="tag">セルフケア</span>
        <span class="tag">自己肯定感</span>
      </div>
    </div>
  </div>
</section>

<!-- CONTACT -->

<section id="contact" class="contact-section">
  <div class="section-label" style="justify-content:center">お申し込み</div>
  <h2 style="margin-bottom:0.5rem">LINEで<br>お申し込みください</h2>
  <p class="section-sub" style="margin: 0 auto 2.5rem; text-align:center">下のボタンから友だち追加して、ご希望のコースをメッセージしてください。日程・お支払い方法をご案内します。</p>

  <div style="max-width:400px; margin:0 auto; text-align:center;">
    <div style="background:var(--warm-white); border-radius:2rem; padding:2.5rem 2rem; border:1px solid rgba(139,168,136,0.2); box-shadow:0 8px 32px rgba(95,122,92,0.08);">
      <div style="font-size:3rem; margin-bottom:1rem;">💬</div>
      <p style="font-family:'Zen Kaku Gothic New',sans-serif; font-size:0.88rem; color:var(--muted); line-height:2; margin-bottom:2rem;">友だち追加後、<br>ご希望のコース名をお送りください。<br>Acoより折り返しご連絡します。</p>
      <a href="https://lin.ee/MCWLE3V" target="_blank" style="display:block; padding:1.1rem; background:#06C755; color:white; border-radius:3rem; font-family:'Zen Kaku Gothic New',sans-serif; font-size:1rem; font-weight:700; letter-spacing:0.1em; text-decoration:none; box-shadow:0 4px 20px rgba(6,199,85,0.3); transition:all 0.3s;">
        LINE で友だち追加する
      </a>
      <p style="font-family:'Zen Kaku Gothic New',sans-serif; font-size:0.75rem; color:var(--muted); margin-top:1.2rem; letter-spacing:0.03em;">🔒 秘密は厳守します</p>
    </div>
  </div>
</section>

<!-- FOOTER -->

<footer style="position:relative; z-index:1; background:var(--cream); border-top:1px solid rgba(139,168,136,0.2); padding:2rem 1.4rem; text-align:center;">
  <div style="font-family:'Noto Serif JP',serif; font-size:0.95rem; font-weight:600; color:var(--sage-dark); letter-spacing:0.12em; margin-bottom:0.3rem;">こころの相談室</div>
  <div style="font-family:'Zen Kaku Gothic New',sans-serif; font-size:0.72rem; color:var(--muted); letter-spacing:0.15em; margin-bottom:1.2rem;">思考の根本改善</div>
  <p style="font-family:'Zen Kaku Gothic New',sans-serif; font-size:0.75rem; color:var(--muted); letter-spacing:0.05em;">© 2025 こころの相談室. All rights reserved.</p>
</footer>

<script>
  // Scroll reveal
  const observer = new IntersectionObserver((entries) => {
    entries.forEach((entry, i) => {
      if (entry.isIntersecting) {
        setTimeout(() => {
          entry.target.classList.add('visible');
        }, 100);
        observer.unobserve(entry.target);
      }
    });
  }, { threshold: 0.1 });

  document.querySelectorAll('.reveal').forEach(el => observer.observe(el));

  // Form submit
  function handleSubmit() {
    const btn = document.querySelector('.submit-btn');
    btn.textContent = '✅ 送信完了！担当者よりご連絡いたします';
    btn.style.background = 'var(--sage)';
    btn.style.cursor = 'default';
    btn.onclick = null;
  }

  // Staggered reveal for grids
  document.querySelectorAll('.worries-grid .worry-card, .counselors-grid .counselor-card, .testimonials-grid .testimonial-card').forEach((el, i) => {
    el.style.transitionDelay = `${(i % 3) * 0.12}s`;
  });

  // Smooth nav highlight
  const sections = document.querySelectorAll('section[id]');
  window.addEventListener('scroll', () => {
    const scrollY = window.scrollY;
    sections.forEach(section => {
      const sectionTop = section.offsetTop - 100;
      const sectionHeight = section.offsetHeight;
      const id = section.getAttribute('id');
      const link = document.querySelector(`nav a[href="#${id}"]`);
      if (link && scrollY >= sectionTop && scrollY < sectionTop + sectionHeight) {
        link.style.color = 'var(--sage-dark)';
      } else if (link) {
        link.style.color = '';
      }
    });
  });
</script>

</body>
</html>
