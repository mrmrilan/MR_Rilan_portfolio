:root{
  --bg:#070a12;
  --text:#eef2ff;
  --muted:rgba(238,242,255,.72);
  --border:rgba(255,255,255,.10);

  --accent:#7c5cff;
  --accent2:#22c55e;
  --accent3:#00d4ff;

  --shadow: 0 18px 70px rgba(0,0,0,.62);
  --radius:22px;
}

*{box-sizing:border-box}
html,body{height:100%}
html{scroll-behavior:smooth}
body{
  margin:0;
  font-family:Inter, system-ui, -apple-system, Segoe UI, Roboto, Arial, sans-serif;
  color:var(--text);
  background:var(--bg);
  line-height:1.6;
  overflow-x:hidden;
}

a{color:inherit}
.container{width:min(1120px, 92vw); margin-inline:auto}
.sr-only{
  position:absolute;width:1px;height:1px;padding:0;margin:-1px;overflow:hidden;
  clip:rect(0,0,0,0);white-space:nowrap;border:0;
}

/* Top progress bar */
.progress{
  position:fixed; top:0; left:0; height:3px; width:0%;
  background:linear-gradient(90deg,var(--accent),var(--accent2),var(--accent3));
  z-index:9999;
  box-shadow:0 10px 20px rgba(124,92,255,.25);
}

/* Background */
.bg{position:fixed; inset:0; z-index:-2}
.bg__grid{
  position:absolute; inset:0;
  background-image:
    linear-gradient(to right, rgba(255,255,255,.06) 1px, transparent 1px),
    linear-gradient(to bottom, rgba(255,255,255,.06) 1px, transparent 1px);
  background-size: 70px 70px;
  opacity:.14;
  mask-image: radial-gradient(700px 650px at 50% 10%, #000 38%, transparent 74%);
}
.bg__blob{
  position:absolute; width:580px; height:580px; border-radius:999px;
  filter: blur(95px);
  opacity:.38;
  animation: floaty 10s ease-in-out infinite;
}
.bg__blob--a{left:-220px; top:-170px; background:radial-gradient(circle at 30% 30%, var(--accent), transparent 60%)}
.bg__blob--b{right:-240px; top:20px; background:radial-gradient(circle at 30% 30%, var(--accent2), transparent 60%); animation-delay:-2.7s}
@keyframes floaty{0%,100%{transform:translateY(0)} 50%{transform:translateY(20px)}}

/* Subtle particles */
.particles{
  position:fixed; inset:0; pointer-events:none; z-index:-1;
  opacity:.55;
}

/* Header */
.header{
  position:sticky; top:0; z-index:50;
  backdrop-filter: blur(16px);
  background: rgba(7,10,18,.62);
  border-bottom: 1px solid rgba(255,255,255,.08);
}
.header__inner{
  display:flex; align-items:center; justify-content:space-between;
  padding:14px 0;
}
.brand{
  display:flex; align-items:center; gap:10px;
  text-decoration:none;
  font-weight:950;
}
.brand__mark{
  width:14px; height:14px; border-radius:6px;
  background: linear-gradient(135deg, var(--accent), #a78bfa);
  box-shadow: 0 0 0 6px rgba(124,92,255,.14);
}
.brand__name{letter-spacing:.2px}

/* Nav */
.nav__menu{
  display:flex; align-items:center; gap:14px;
  list-style:none; margin:0; padding:0;
}
.nav__menu a{
  text-decoration:none;
  color:var(--muted);
  font-weight:900;
  font-size:14px;
  padding:10px 12px;
  border-radius:14px;
  transition: background .2s ease, color .2s ease;
}
.nav__menu a:hover{background:rgba(255,255,255,.06); color:var(--text)}

.nav__toggle{
  display:none;
  border:1px solid rgba(255,255,255,.10);
  background:rgba(255,255,255,.05);
  border-radius:14px;
  padding:10px 12px;
}
.nav__bars{width:18px; height:2px; background:var(--text); display:block; position:relative}
.nav__bars::before,.nav__bars::after{content:""; position:absolute; left:0; width:18px; height:2px; background:var(--text)}
.nav__bars::before{top:-6px}
.nav__bars::after{top:6px}

/* Buttons */
.btn{
  display:inline-flex; align-items:center; justify-content:center;
  border-radius:16px;
  padding:12px 16px;
  border:1px solid rgba(124,92,255,.45);
  background: linear-gradient(135deg, rgba(124,92,255,.95), rgba(124,92,255,.70));
  color:white;
  font-weight:950;
  text-decoration:none;
  box-shadow: 0 16px 40px rgba(124,92,255,.18);
  transition: transform .15s ease, filter .15s ease;
}
.btn:hover{filter:brightness(1.06); transform: translateY(-1px)}
.btn--ghost{
  background:rgba(255,255,255,.05);
  border:1px solid rgba(255,255,255,.10);
  box-shadow:none;
}
.btn--small{padding:10px 12px; font-size:13px}

/* Hero */
.hero{padding:56px 0 34px}
.hero__grid{display:grid; grid-template-columns: 1.15fr .85fr; gap:18px; align-items:start}
.pill{
  display:inline-flex; align-items:center; gap:10px;
  border:1px solid rgba(255,255,255,.12);
  background:rgba(255,255,255,.04);
  padding:8px 12px;
  border-radius:999px;
  font-size:13px;
  color:var(--muted);
  font-weight:900;
}
.pill__dot{
  width:10px; height:10px; border-radius:999px;
  background:linear-gradient(135deg, var(--accent), var(--accent2));
  box-shadow:0 0 0 5px rgba(34,197,94,.10);
}
.hero__title{
  margin:14px 0 10px;
  font-size:48px;
  line-height:1.05;
  letter-spacing:-.8px;
}
.accent{
  background:linear-gradient(135deg, var(--accent), #a78bfa, var(--accent3));
  -webkit-background-clip:text;
  background-clip:text;
  color:transparent;
}
.hero__subtitle{color:var(--muted); max-width:62ch; font-size:16px; font-weight:750}
.hero__cta{display:flex; gap:12px; margin:18px 0 14px; flex-wrap:wrap}

.hero__stats{display:grid; grid-template-columns: repeat(3, minmax(0,1fr)); gap:12px}
.statCard{
  background:rgba(255,255,255,.04);
  border:1px solid rgba(255,255,255,.10);
  border-radius:18px;
  padding:12px;
}
.statCard__k{color:rgba(238,242,255,.55); font-size:12px; font-weight:950; text-transform:uppercase; letter-spacing:.6px}
.statCard__v{display:block; margin-top:4px; font-weight:950; text-decoration:none; color:var(--text)}

/* Premium gradient border cards */
.card{
  position:relative;
  border-radius: var(--radius);
  padding:18px;
  box-shadow: var(--shadow);
  background: rgba(255,255,255,.035);
  border:1px solid rgba(255,255,255,.10);
  overflow:hidden;
  transform-style: preserve-3d;
  transition: transform .18s ease;
}
.card::before{
  content:"";
  position:absolute; inset:-2px;
  background: conic-gradient(from 180deg,
    rgba(124,92,255,.0),
    rgba(124,92,255,.45),
    rgba(34,197,94,.35),
    rgba(0,212,255,.30),
    rgba(124,92,255,.0)
  );
  filter: blur(14px);
  opacity:.35;
  pointer-events:none;
}
.card::after{
  content:"";
  position:absolute; inset:1px;
  border-radius: calc(var(--radius) - 2px);
  background: linear-gradient(180deg, rgba(255,255,255,.07), rgba(255,255,255,.03));
  pointer-events:none;
}
.card > *{position:relative; z-index:1}

.card__head{display:flex; align-items:center; justify-content:space-between; gap:10px}
.card__title{margin:0; font-size:18px}
.card__footer{display:flex; gap:10px; margin-top:14px; flex-wrap:wrap}

.chip{
  font-size:12px; font-weight:980;
  padding:7px 10px;
  border-radius:999px;
  border:1px solid rgba(34,197,94,.35);
  background:rgba(34,197,94,.12);
  color:#caffdd;
}

/* Lists */
.featureList{list-style:none; padding:0; margin:14px 0 0; display:grid; gap:12px}
.featureList li{
  display:flex; gap:12px; align-items:flex-start;
  padding:12px;
  background:rgba(0,0,0,.18);
  border:1px solid rgba(255,255,255,.10);
  border-radius:16px;
}
.featureList__icon{font-size:18px}
.featureList__title{font-weight:980}
.featureList__desc{color:var(--muted); font-weight:800; font-size:13px}

/* Sections */
.section{padding:44px 0}
.section__head h2{margin:0; font-size:30px; letter-spacing:-.3px}
.section__head p{margin:6px 0 0; color:var(--muted); font-weight:800}
.grid{display:grid; gap:16px; margin-top:16px}
.grid--2{grid-template-columns:repeat(2, minmax(0,1fr))}
.grid--3{grid-template-columns:repeat(3, minmax(0,1fr))}
.grid--4{grid-template-columns:repeat(4, minmax(0,1fr))}
h3{margin:0 0 8px}
.muted{color:var(--muted); font-weight:800}
.tiny{font-size:12px}

/* tags */
.tags{display:flex; gap:10px; flex-wrap:wrap; margin-top:12px}
.tag{
  border:1px solid rgba(124,92,255,.22);
  background:rgba(124,92,255,.12);
  color:var(--text);
  padding:8px 10px;
  border-radius:999px;
  font-size:12px;
  font-weight:980;
}

/* timeline */
.timeline{list-style:none; padding:0; margin:0}
.timeline li{padding:12px 0; border-bottom:1px solid rgba(255,255,255,.10)}
.timeline li:last-child{border-bottom:none}
.timeline__title{font-weight:980}
.timeline__meta{color:var(--muted); font-weight:880; font-size:13px}

/* pill row */
.pillRow{display:flex; flex-wrap:wrap; gap:10px}
.pillRow span{
  border:1px solid rgba(255,255,255,.12);
  background:rgba(0,0,0,.18);
  padding:8px 10px;
  border-radius:999px;
  font-size:12px;
  font-weight:980;
  color:var(--muted);
}

/* Projects */
.project__top{display:flex; align-items:flex-start; justify-content:space-between; gap:12px}
.badge{
  border:1px solid rgba(255,255,255,.12);
  background:rgba(255,255,255,.05);
  color:var(--muted);
  font-size:12px;
  font-weight:980;
  padding:7px 10px;
  border-radius:999px;
}
.project__desc{color:var(--muted); font-weight:850}
.project__actions{display:flex; gap:10px; margin-top:14px; flex-wrap:wrap}

/* Certificates */
.certGrid{display:grid; gap:12px}
.certItem{
  display:flex; align-items:center; justify-content:space-between; gap:12px;
  padding:14px;
  border:1px solid rgba(255,255,255,.12);
  background:rgba(0,0,0,.18);
  border-radius:18px;
}

/* Gallery */
.photoCard{
  border:1px solid rgba(255,255,255,.12);
  background:rgba(0,0,0,.18);
  border-radius:18px;
  overflow:hidden;
}
.photoCard img{
  width:100%; height:180px; object-fit:cover; display:block;
  transition: transform .35s ease;
}
.photoCard:hover img{transform:scale(1.06)}
.photoCard figcaption{padding:12px 12px 14px; display:grid; gap:4px}
.photoCard figcaption b{font-weight:980}
.photoCard figcaption span{color:var(--muted); font-weight:850; font-size:13px}

/* Contact */
.contact{display:grid; gap:12px; margin-top:10px}
.contact__row{
  display:grid; grid-template-columns: 28px 70px 1fr;
  gap:10px; align-items:center;
  padding:12px;
  border:1px solid rgba(255,255,255,.12);
  background:rgba(0,0,0,.18);
  border-radius:18px;
  text-decoration:none;
}
.contact__row:hover{background:rgba(255,255,255,.06)}
.contact__row b{justify-self:end}

.form{display:grid; gap:12px}
label{display:grid; gap:6px; font-weight:980}
input,textarea{
  width:100%; padding:12px 12px;
  border-radius:16px;
  border:1px solid rgba(255,255,255,.12);
  background:rgba(0,0,0,.18);
  color:var(--text);
  outline:none;
  font-family:inherit;
  font-weight:850;
}
input:focus,textarea:focus{
  border-color:rgba(124,92,255,.55);
  box-shadow:0 0 0 4px rgba(124,92,255,.15);
}
.whatsapp-btn{
  display:inline-flex;
  align-items:center;
  gap:8px;
}

.whatsapp-btn img{
  width:18px;
  height:18px;
}


/* Footer */
.footer{
  border-top:1px solid rgba(255,255,255,.10);
  padding:18px 0;
  background: rgba(7,10,18,.55);
}
.footer__inner{
  display:flex; align-items:center; justify-content:space-between; gap:12px;
  color:var(--muted);
  font-weight:900;
}

/* Reveal */
.reveal{opacity:0; transform:translateY(16px); transition:opacity .75s ease, transform .75s ease}
.reveal.is-visible{opacity:1; transform:translateY(0)}

/* Mobile */
@media (max-width: 980px){
  .hero__grid{grid-template-columns:1fr}
  .hero__stats{grid-template-columns:1fr}
  .grid--4{grid-template-columns:repeat(2, minmax(0,1fr))}
  .hero__title{font-size:40px}
}
@media (max-width: 820px){
  .grid--2,.grid--3{grid-template-columns:1fr}
  .grid--4{grid-template-columns:1fr}
  .nav__toggle{display:inline-flex}
  .nav__menu{
    position:absolute; right:4vw; top:62px;
    display:none; flex-direction:column; gap:8px;
    padding:10px;
    background: rgba(7,10,18,.92);
    border:1px solid rgba(255,255,255,.12);
    border-radius:18px;
    width:min(280px, 92vw);
  }
  .nav__menu.open{display:flex}
  .contact__row b{justify-self:start}
}

/* Reduced motion */
@media (prefers-reduced-motion: reduce){
  html{scroll-behavior:auto}
  .bg__blob{animation:none}
  .reveal{transition:none; opacity:1; transform:none}
  .btn,.card,.photoCard img{transition:none}
}
/* Fix long email/links overflowing into other cards */
.statCard,
.metaCard {
  min-width: 0;          /* important for grid items */
  overflow: hidden;      /* prevents spilling into next card */
}

.statCard__v,
.metaCard__value {
  overflow-wrap: anywhere;  /* wraps long emails */
  word-break: break-word;
}
