<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8"/>
<meta name="viewport" content="width=device-width,initial-scale=1.0"/>
<title>Ad/Pulse — Lead Conversion Predictor</title>
<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700;800&display=swap" rel="stylesheet"/>
<script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
<script src="https://cdn.jsdelivr.net/npm/xlsx/dist/xlsx.full.min.js"></script>
<style>
:root{
  --bg:#04040f;
  --navy:#080820;
  --card:#0d0d2b;
  --purple:#7c3aed;
  --violet:#a855f7;
  --pink:#ec4899;
  --cyan:#06b6d4;
  --teal:#14b8a6;
  --green:#10b981;
  --yellow:#f59e0b;
  --red:#ef4444;
  --white:#ffffff;
  --muted:#94a3b8;
  --border:rgba(124,58,237,0.25);
}
*{margin:0;padding:0;box-sizing:border-box}
html{scroll-behavior:smooth}
body{
  font-family:'Poppins',sans-serif;
  background:var(--bg);
  color:var(--white);
  overflow-x:hidden;
  min-height:100vh;
}

/* ---- NOISE OVERLAY ---- */
body::before{
  content:'';position:fixed;inset:0;
  background-image:url("data:image/svg+xml,%3Csvg viewBox='0 0 256 256' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='n'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.9' numOctaves='4' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23n)' opacity='0.04'/%3E%3C/svg%3E");
  pointer-events:none;z-index:0;opacity:.4;
}

/* ---- NAV ---- */
nav{
  position:fixed;top:0;left:0;right:0;z-index:999;
  display:flex;align-items:center;justify-content:space-between;
  padding:1rem 2.5rem;
  background:rgba(4,4,15,0.85);
  backdrop-filter:blur(20px);
  border-bottom:1px solid rgba(124,58,237,0.15);
}
.nav-logo{
  font-family:'Poppins',sans-serif;font-weight:800;font-size:1.5rem;
  background:linear-gradient(135deg,var(--violet),var(--cyan));
  -webkit-background-clip:text;-webkit-text-fill-color:transparent;
}
.nav-links{display:flex;gap:2rem;list-style:none}
.nav-links a{color:var(--muted);text-decoration:none;font-size:.9rem;font-weight:500;transition:.2s}
.nav-links a:hover{color:var(--white)}
.nav-cta{
  padding:.55rem 1.4rem;border-radius:50px;
  background:linear-gradient(135deg,var(--purple),var(--pink));
  color:#fff;font-weight:600;font-size:.875rem;text-decoration:none;
  box-shadow:0 0 20px rgba(168,85,247,.35);
  transition:box-shadow .3s;
}
.nav-cta:hover{box-shadow:0 0 35px rgba(168,85,247,.6)}

/* ---- HERO ---- */
.hero{
  min-height:100vh;display:flex;flex-direction:column;
  align-items:center;justify-content:center;text-align:center;
  padding:8rem 2rem 4rem;
  position:relative;overflow:hidden;
}
.hero-glow{
  position:absolute;width:700px;height:700px;border-radius:50%;
  background:radial-gradient(circle,rgba(124,58,237,.18) 0%,transparent 70%);
  top:50%;left:50%;transform:translate(-50%,-50%);pointer-events:none;
}
.hero-badge{
  display:inline-flex;align-items:center;gap:.5rem;
  padding:.4rem 1.1rem;border-radius:50px;
  border:1px solid rgba(168,85,247,.4);
  background:rgba(124,58,237,.12);
  font-size:.8rem;color:var(--violet);font-weight:600;
  margin-bottom:1.5rem;letter-spacing:.05em;
}
.hero-title{
  font-family:'Poppins',sans-serif;font-size:clamp(3.5rem,9vw,7rem);
  font-weight:800;line-height:.95;
  background:linear-gradient(135deg,var(--violet) 0%,var(--pink) 45%,var(--cyan) 100%);
  -webkit-background-clip:text;-webkit-text-fill-color:transparent;
  margin-bottom:.5rem;
}
.hero-sub{font-size:1.25rem;color:var(--white);font-weight:300;letter-spacing:.1em;margin-bottom:.75rem}
.hero-desc{max-width:560px;color:var(--muted);line-height:1.7;margin-bottom:2.5rem}
.hero-btns{display:flex;gap:1rem;flex-wrap:wrap;justify-content:center}
.btn-primary{
  padding:.8rem 2rem;border-radius:50px;
  background:linear-gradient(135deg,var(--purple),var(--pink));
  color:#fff;font-weight:700;font-size:1rem;border:none;cursor:pointer;
  box-shadow:0 0 25px rgba(168,85,247,.45);transition:.3s;text-decoration:none;
}
.btn-primary:hover{box-shadow:0 0 45px rgba(168,85,247,.7);transform:translateY(-2px)}
.btn-secondary{
  padding:.8rem 2rem;border-radius:50px;
  border:1px solid rgba(168,85,247,.4);background:transparent;
  color:var(--violet);font-weight:600;font-size:1rem;cursor:pointer;transition:.3s;text-decoration:none;
}
.btn-secondary:hover{background:rgba(124,58,237,.15);border-color:var(--violet)}

/* ---- SECTION BASE ---- */
section{padding:5rem 2rem;position:relative;z-index:1}
.container{max-width:1100px;margin:0 auto}
.section-tag{
  display:inline-block;font-size:.75rem;font-weight:700;letter-spacing:.12em;
  text-transform:uppercase;padding:.35rem .9rem;border-radius:50px;margin-bottom:1rem;
}
.section-title{
  font-family:'Poppins',sans-serif;font-size:clamp(1.8rem,4vw,2.8rem);
  font-weight:800;margin-bottom:.75rem;line-height:1.15;
}
.section-desc{color:var(--muted);max-width:550px;line-height:1.7;margin-bottom:2.5rem}

/* ---- CARDS ---- */
.card{
  background:var(--card);border-radius:1.25rem;padding:2rem;
  border:1px solid var(--border);position:relative;overflow:hidden;
  transition:box-shadow .3s,transform .3s;
}
.card:hover{transform:translateY(-3px)}
.card::before{
  content:'';position:absolute;inset:0;border-radius:1.25rem;
  background:linear-gradient(135deg,rgba(124,58,237,.06),transparent);
  pointer-events:none;
}

/* ---- PURPLE CARD ---- */
.card-purple{border-color:rgba(168,85,247,.3)}
.card-purple:hover{box-shadow:0 0 40px rgba(168,85,247,.2)}
/* ---- CYAN CARD ---- */
.card-cyan{border-color:rgba(6,182,212,.3)}
.card-cyan:hover{box-shadow:0 0 40px rgba(6,182,212,.2)}
/* ---- PINK CARD ---- */
.card-pink{border-color:rgba(236,72,153,.3)}
.card-pink:hover{box-shadow:0 0 40px rgba(236,72,153,.2)}
/* ---- GREEN CARD ---- */
.card-green{border-color:rgba(16,185,129,.3)}
.card-green:hover{box-shadow:0 0 40px rgba(16,185,129,.2)}

/* ---- FORM ELEMENTS ---- */
label{display:block;font-size:.82rem;font-weight:600;color:var(--muted);margin-bottom:.45rem;letter-spacing:.04em}
input[type=text],input[type=email],input[type=number],select,textarea{
  width:100%;padding:.75rem 1rem;border-radius:.7rem;
  background:rgba(255,255,255,.04);border:1px solid rgba(255,255,255,.1);
  color:var(--white);font-family:'Poppins',sans-serif;font-size:.95rem;
  outline:none;transition:.2s;
}
input:focus,select:focus,textarea:focus{border-color:var(--violet);box-shadow:0 0 0 3px rgba(168,85,247,.12)}
select option{background:#1a1a3e;color:#fff}
textarea{resize:vertical;min-height:120px}

/* GRID */
.grid-2{display:grid;grid-template-columns:1fr 1fr;gap:1.25rem}
.grid-3{display:grid;grid-template-columns:repeat(3,1fr);gap:1.5rem}
.grid-4{display:grid;grid-template-columns:repeat(4,1fr);gap:1.25rem}

/* ---- TOGGLE BUTTONS ---- */
.toggle-group{display:flex;gap:.5rem}
.toggle-btn{
  padding:.6rem 1.4rem;border-radius:50px;
  border:1px solid rgba(255,255,255,.15);background:transparent;
  color:var(--muted);font-weight:600;font-size:.875rem;cursor:pointer;transition:.2s;
}
.toggle-btn.active{
  background:linear-gradient(135deg,var(--purple),var(--pink));
  border-color:transparent;color:#fff;
  box-shadow:0 0 18px rgba(168,85,247,.35);
}

/* ---- RANGE SLIDER ---- */
.slider-wrap{position:relative}
input[type=range]{
  -webkit-appearance:none;width:100%;height:6px;border-radius:3px;
  background:linear-gradient(to right,var(--violet) 0%,var(--cyan) 100%);
  outline:none;border:none;padding:0;cursor:pointer;
}
input[type=range]::-webkit-slider-thumb{
  -webkit-appearance:none;width:18px;height:18px;border-radius:50%;
  background:var(--white);box-shadow:0 0 10px rgba(168,85,247,.6);cursor:pointer;
}
.slider-val{
  position:absolute;right:0;top:-1.6rem;
  font-size:.8rem;font-weight:700;color:var(--cyan);
}

/* ---- TIMER ---- */
.timer-display{
  font-family:'Poppins',sans-serif;font-size:2.5rem;font-weight:800;
  text-align:center;padding:1rem;
  background:rgba(124,58,237,.08);border-radius:.75rem;
  border:1px solid rgba(124,58,237,.2);
  color:var(--violet);letter-spacing:.08em;
  margin-bottom:.75rem;
}
.timer-controls{display:flex;gap:.75rem;justify-content:center;margin-bottom:1rem}
.timer-btn{
  padding:.55rem 1.3rem;border-radius:50px;border:none;cursor:pointer;
  font-weight:700;font-size:.85rem;transition:.2s;
}
.timer-start{background:linear-gradient(135deg,var(--green),var(--teal));color:#fff}
.timer-stop{background:linear-gradient(135deg,var(--red),var(--pink));color:#fff}
.timer-reset{background:rgba(255,255,255,.08);color:var(--muted)}
.timer-manual{display:flex;gap:.5rem;align-items:center;justify-content:center;margin-bottom:.5rem}
.timer-manual input{width:70px;text-align:center;font-size:1rem;font-weight:700;padding:.5rem}
.timer-manual span{color:var(--muted);font-weight:700}

/* ---- PREDICT BUTTON ---- */
.btn-predict{
  width:100%;padding:1.1rem;border-radius:1rem;border:none;cursor:pointer;
  font-family:'Poppins',sans-serif;font-size:1.1rem;font-weight:800;color:#fff;
  background:linear-gradient(135deg,var(--purple),var(--pink),var(--cyan));
  background-size:200%;
  box-shadow:0 0 30px rgba(168,85,247,.45);
  transition:.4s;letter-spacing:.03em;
  animation:gradShift 4s ease infinite;
}
@keyframes gradShift{
  0%{background-position:0% 50%}
  50%{background-position:100% 50%}
  100%{background-position:0% 50%}
}
.btn-predict:hover{box-shadow:0 0 55px rgba(168,85,247,.7);transform:translateY(-2px)}

/* ---- RESULT BADGE ---- */
.result-badge{
  display:none;padding:1.5rem;border-radius:1rem;margin-top:1.5rem;text-align:center;
  animation:fadeInUp .4s ease;
}
@keyframes fadeInUp{from{opacity:0;transform:translateY(15px)}to{opacity:1;transform:translateY(0)}}
.result-badge.show{display:block}
.result-badge.high{background:rgba(16,185,129,.1);border:1px solid rgba(16,185,129,.4);box-shadow:0 0 30px rgba(16,185,129,.15)}
.result-badge.medium{background:rgba(245,158,11,.1);border:1px solid rgba(245,158,11,.4);box-shadow:0 0 30px rgba(245,158,11,.15)}
.result-badge.low{background:rgba(239,68,68,.1);border:1px solid rgba(239,68,68,.4);box-shadow:0 0 30px rgba(239,68,68,.15)}
.result-emoji{font-size:2.5rem;margin-bottom:.5rem}
.result-label{font-family:'Poppins',sans-serif;font-size:1.4rem;font-weight:800;margin-bottom:.5rem}
.result-label.high{color:var(--green)}
.result-label.medium{color:var(--yellow)}
.result-label.low{color:var(--red)}
.result-msg{color:var(--muted);line-height:1.6}

/* ---- DASHBOARD ---- */
.stat-cards{display:grid;grid-template-columns:repeat(4,1fr);gap:1rem;margin-bottom:2rem}
.stat-card{
  padding:1.5rem;border-radius:1rem;text-align:center;
  background:var(--card);border:1px solid;
}
.stat-card.total{border-color:rgba(168,85,247,.4);box-shadow:0 0 20px rgba(168,85,247,.1)}
.stat-card.high-c{border-color:rgba(16,185,129,.4);box-shadow:0 0 20px rgba(16,185,129,.1)}
.stat-card.med-c{border-color:rgba(245,158,11,.4);box-shadow:0 0 20px rgba(245,158,11,.1)}
.stat-card.low-c{border-color:rgba(239,68,68,.4);box-shadow:0 0 20px rgba(239,68,68,.1)}
.stat-num{font-family:'Poppins',sans-serif;font-size:2.2rem;font-weight:800}
.stat-num.total{color:var(--violet)}
.stat-num.high-c{color:var(--green)}
.stat-num.med-c{color:var(--yellow)}
.stat-num.low-c{color:var(--red)}
.stat-label{font-size:.8rem;color:var(--muted);margin-top:.25rem;font-weight:500}

/* ---- TABLE ---- */
.lead-table{width:100%;border-collapse:collapse;margin-top:2rem}
.lead-table th{
  padding:.75rem 1rem;text-align:left;font-size:.75rem;
  color:var(--muted);font-weight:600;letter-spacing:.08em;text-transform:uppercase;
  border-bottom:1px solid rgba(255,255,255,.08);
}
.lead-table td{
  padding:.8rem 1rem;font-size:.875rem;
  border-bottom:1px solid rgba(255,255,255,.04);color:var(--white);
}
.lead-table tr:hover td{background:rgba(255,255,255,.02)}
.badge-high{padding:.25rem .75rem;border-radius:50px;background:rgba(16,185,129,.15);color:var(--green);font-size:.75rem;font-weight:700;border:1px solid rgba(16,185,129,.3)}
.badge-med{padding:.25rem .75rem;border-radius:50px;background:rgba(245,158,11,.15);color:var(--yellow);font-size:.75rem;font-weight:700;border:1px solid rgba(245,158,11,.3)}
.badge-low{padding:.25rem .75rem;border-radius:50px;background:rgba(239,68,68,.15);color:var(--red);font-size:.75rem;font-weight:700;border:1px solid rgba(239,68,68,.3)}
.chart-wrap{max-width:380px;margin:2rem auto 0}

/* ---- BULK UPLOAD ---- */
.upload-zone{
  border:2px dashed rgba(168,85,247,.35);border-radius:1.25rem;
  padding:3rem;text-align:center;cursor:pointer;transition:.3s;
  background:rgba(124,58,237,.04);position:relative;
}
.upload-zone:hover,.upload-zone.drag{
  border-color:var(--violet);background:rgba(124,58,237,.08);
  box-shadow:0 0 30px rgba(168,85,247,.15);
}
.upload-icon{font-size:3rem;margin-bottom:1rem}
.upload-title{font-family:'Poppins',sans-serif;font-size:1.2rem;font-weight:700;margin-bottom:.5rem}
.upload-sub{color:var(--muted);font-size:.875rem;margin-bottom:1rem}
.upload-hint{font-size:.78rem;color:rgba(168,85,247,.6);margin-top:.75rem}
#fileInput{position:absolute;inset:0;opacity:0;cursor:pointer}
.template-hint{
  margin-top:1rem;padding:.75rem 1.25rem;border-radius:.75rem;
  background:rgba(6,182,212,.06);border:1px solid rgba(6,182,212,.2);
  font-size:.8rem;color:var(--cyan);
}
.bulk-results{margin-top:2rem;display:none}
.bulk-results.show{display:block}
.bulk-summary{display:grid;grid-template-columns:repeat(3,1fr);gap:1rem;margin-bottom:2rem}
.bulk-insights-grid{display:grid;grid-template-columns:1fr 1fr;gap:1.25rem;margin-top:2rem}

/* ---- INSIGHTS ---- */
.insight-card{
  padding:1.5rem;border-radius:1rem;background:var(--card);
  border:1px solid rgba(168,85,247,.2);transition:.3s;
}
.insight-card:hover{box-shadow:0 0 25px rgba(168,85,247,.15);border-color:rgba(168,85,247,.4)}
.insight-icon{font-size:1.5rem;margin-bottom:.75rem}
.insight-title{font-family:'Poppins',sans-serif;font-size:1rem;font-weight:700;margin-bottom:.5rem}
.insight-text{font-size:.875rem;color:var(--muted);line-height:1.7}

/* ---- SERVICES ---- */
.services-grid{display:grid;grid-template-columns:repeat(2,1fr);gap:1.5rem}
.service-card{
  padding:2rem;border-radius:1.25rem;background:var(--card);
  position:relative;overflow:hidden;transition:.3s;
}
.service-card::after{
  content:'';position:absolute;top:0;left:0;right:0;height:2px;
}
.service-card.s1::after{background:linear-gradient(90deg,var(--violet),var(--pink))}
.service-card.s2::after{background:linear-gradient(90deg,var(--cyan),var(--violet))}
.service-card.s3::after{background:linear-gradient(90deg,var(--pink),var(--yellow))}
.service-card.s4::after{background:linear-gradient(90deg,var(--green),var(--cyan))}
.service-card:hover{transform:translateY(-4px);box-shadow:0 20px 50px rgba(0,0,0,.3)}
.service-num{font-family:'Poppins',sans-serif;font-size:.75rem;color:var(--muted);font-weight:700;letter-spacing:.12em;margin-bottom:.5rem}
.service-name{font-family:'Poppins',sans-serif;font-size:1.3rem;font-weight:800;margin-bottom:.75rem}
.service-desc{color:var(--muted);font-size:.875rem;line-height:1.7}

/* ---- CONTACT ---- */
.contact-grid{display:grid;grid-template-columns:1fr 1.5fr;gap:3rem;align-items:start}
.contact-perks{list-style:none;margin-top:1.5rem}
.contact-perks li{
  padding:.75rem 0;border-bottom:1px solid rgba(255,255,255,.06);
  display:flex;align-items:center;gap:.75rem;font-size:.9rem;color:var(--muted);
}
.contact-perks li span:first-child{font-size:1.1rem}
.btn-submit{
  width:100%;padding:1rem;border-radius:.75rem;border:none;cursor:pointer;
  font-family:'Poppins',sans-serif;font-size:1rem;font-weight:800;color:#fff;
  background:linear-gradient(135deg,var(--green),var(--cyan));
  box-shadow:0 0 25px rgba(16,185,129,.35);transition:.3s;
}
.btn-submit:hover{box-shadow:0 0 45px rgba(16,185,129,.55);transform:translateY(-2px)}

/* ---- FOOTER ---- */
footer{
  background:var(--navy);border-top:1px solid rgba(124,58,237,.15);
  padding:3rem 2rem;text-align:center;
}
.footer-logo{
  font-family:'Poppins',sans-serif;font-size:2rem;font-weight:800;
  background:linear-gradient(135deg,var(--violet),var(--cyan));
  -webkit-background-clip:text;-webkit-text-fill-color:transparent;
  margin-bottom:.5rem;
}
.footer-tagline{color:var(--muted);font-size:.875rem;margin-bottom:1.5rem}
.social-icons{display:flex;justify-content:center;gap:1rem;margin-bottom:1.5rem}
.social-icon{
  width:40px;height:40px;border-radius:50%;
  border:1px solid rgba(168,85,247,.3);display:flex;align-items:center;justify-content:center;
  font-size:1rem;color:var(--muted);transition:.2s;text-decoration:none;
}
.social-icon:hover{border-color:var(--violet);color:var(--violet)}
.footer-copy{font-size:.8rem;color:rgba(148,163,184,.5)}

/* ---- CHATBOT ---- */
#chatBtn{
  position:fixed;bottom:2rem;right:2rem;z-index:9999;
  width:60px;height:60px;border-radius:50%;border:none;cursor:pointer;
  background:linear-gradient(135deg,var(--purple),var(--pink));
  box-shadow:0 0 30px rgba(168,85,247,.5);font-size:1.5rem;
  transition:.3s;
}
#chatBtn:hover{box-shadow:0 0 50px rgba(168,85,247,.8);transform:scale(1.1)}
#chatPanel{
  position:fixed;bottom:6rem;right:2rem;z-index:9998;
  width:360px;max-height:520px;border-radius:1.25rem;
  background:#0d0d2b;border:1px solid rgba(168,85,247,.3);
  box-shadow:0 20px 60px rgba(0,0,0,.5);
  display:none;flex-direction:column;overflow:hidden;
}
#chatPanel.open{display:flex}
.chat-header{
  padding:1rem 1.25rem;background:linear-gradient(135deg,var(--purple),var(--pink));
  display:flex;justify-content:space-between;align-items:center;
}
.chat-header-title{font-family:'Poppins',sans-serif;font-weight:800;font-size:1rem}
.chat-close{background:none;border:none;color:#fff;cursor:pointer;font-size:1.2rem}
#chatMessages{flex:1;overflow-y:auto;padding:1rem;display:flex;flex-direction:column;gap:.75rem}
.chat-msg{padding:.7rem 1rem;border-radius:.9rem;max-width:85%;font-size:.875rem;line-height:1.5}
.chat-msg.bot{background:rgba(168,85,247,.15);border:1px solid rgba(168,85,247,.2);color:var(--white);align-self:flex-start}
.chat-msg.user{background:linear-gradient(135deg,var(--purple),var(--pink));color:#fff;align-self:flex-end}
.chat-suggestions{padding:.75rem;display:flex;flex-wrap:wrap;gap:.5rem;border-top:1px solid rgba(255,255,255,.06)}
.chat-sug{
  padding:.35rem .8rem;border-radius:50px;font-size:.75rem;
  border:1px solid rgba(168,85,247,.3);background:rgba(124,58,237,.1);
  color:var(--violet);cursor:pointer;transition:.2s;
}
.chat-sug:hover{background:rgba(124,58,237,.25);color:var(--white)}

/* ---- PROFILE SAVED BADGE ---- */
.profile-saved{
  display:none;align-items:center;gap:.75rem;
  margin-top:1rem;padding:.9rem 1.25rem;border-radius:.75rem;
  background:rgba(16,185,129,.1);border:1px solid rgba(16,185,129,.3);
  color:var(--green);font-weight:600;font-size:.9rem;
  animation:fadeInUp .4s ease;
}
.profile-saved.show{display:flex}
.dot-pulse{
  width:10px;height:10px;border-radius:50%;background:var(--green);
  animation:pulse 1.5s infinite;
}
@keyframes pulse{0%,100%{box-shadow:0 0 0 0 rgba(16,185,129,.5)}50%{box-shadow:0 0 0 8px rgba(16,185,129,0)}}

/* ---- SECTION COLORS ---- */
.tag-purple{background:rgba(168,85,247,.12);color:var(--violet);border:1px solid rgba(168,85,247,.25)}
.tag-cyan{background:rgba(6,182,212,.12);color:var(--cyan);border:1px solid rgba(6,182,212,.25)}
.tag-pink{background:rgba(236,72,153,.12);color:var(--pink);border:1px solid rgba(236,72,153,.25)}
.tag-green{background:rgba(16,185,129,.12);color:var(--green);border:1px solid rgba(16,185,129,.25)}
.tag-yellow{background:rgba(245,158,11,.12);color:var(--yellow);border:1px solid rgba(245,158,11,.25)}

/* ---- RESPONSIVE ---- */
@media(max-width:768px){
  nav{padding:1rem}
  .nav-links{display:none}
  .grid-2,.grid-3,.grid-4,.stat-cards,.services-grid,.contact-grid,.bulk-summary,.bulk-insights-grid{grid-template-columns:1fr}
  .hero-title{font-size:3rem}
  #chatPanel{width:calc(100vw - 2rem);right:1rem}
  .timer-manual{flex-wrap:wrap}
}

/* ---- DIVIDERS ---- */
.section-divider{height:1px;background:linear-gradient(90deg,transparent,rgba(124,58,237,.2),transparent);margin:0 2rem}

/* ---- PROGRESS BAR (bulk) ---- */
.progress-bar-wrap{height:6px;background:rgba(255,255,255,.06);border-radius:3px;margin:.5rem 0}
.progress-bar-fill{height:100%;border-radius:3px;transition:width .6s ease}

/* empty state */
.empty-state{text-align:center;padding:3rem;color:var(--muted)}
.empty-state .big-icon{font-size:3rem;margin-bottom:1rem;opacity:.4}

/* download btn */
.btn-download{
  padding:.65rem 1.5rem;border-radius:50px;border:none;cursor:pointer;
  background:linear-gradient(135deg,var(--cyan),var(--teal));
  color:#fff;font-weight:700;font-size:.875rem;
  box-shadow:0 0 15px rgba(6,182,212,.3);transition:.3s;
}
.btn-download:hover{box-shadow:0 0 30px rgba(6,182,212,.5)}
</style>
</head>
<body>

<!-- NAV -->
<nav>
  <div class="nav-logo">Ad/Pulse</div>
  <ul class="nav-links">
    <li><a href="#profile">Profile</a></li>
    <li><a href="#predictor">Predictor</a></li>
    <li><a href="#bulk">Bulk Upload</a></li>
    <li><a href="#dashboard">Dashboard</a></li>
    <li><a href="#insights">Insights</a></li>
    <li><a href="#services">Services</a></li>
  </ul>
  <a href="#contact" class="nav-cta">Start Growing →</a>
</nav>

<!-- HERO -->
<section class="hero">
  <div class="hero-glow"></div>
  <div class="hero-badge">✦ AI-Powered Lead Intelligence</div>
  <div class="hero-title">Ad/Pulse</div>
  <div class="hero-sub">Lead Conversion Predictor</div>
  <p class="hero-desc">Identify high-value leads before your competition does. Combine behavioral signals to score intent — then act with precision.</p>
  <div class="hero-btns">
    <a href="#predictor" class="btn-primary">Analyze a Lead →</a>
    <a href="#bulk" class="btn-secondary">Bulk Upload Excel</a>
  </div>
</section>

<div class="section-divider"></div>

<!-- SECTION 1: COMPANY PROFILE -->
<section id="profile">
  <div class="container">
    <span class="section-tag tag-purple">01 — Company Profile</span>
    <h2 class="section-title">Tell Us About Your Business</h2>
    <p class="section-desc">Set your profile once — all predictions and insights become personalized to your industry and model.</p>

    <div class="card card-purple">
      <div class="grid-2" style="gap:1.5rem">
        <div>
          <label>Company Name</label>
          <input type="text" id="companyName" placeholder="e.g. Nexora Digital"/>
        </div>
        <div>
          <label>Industry / Sector</label>
          <select id="industry">
            <option value="">Select Industry</option>
            <option>E-commerce</option>
            <option>SaaS/Software</option>
            <option>Education</option>
            <option>Healthcare</option>
            <option>Real Estate</option>
            <option>Digital Marketing</option>
            <option>Retail</option>
            <option>Finance</option>
            <option>Other</option>
          </select>
        </div>
        <div>
          <label>Business Type</label>
          <div class="toggle-group" id="bizTypeGroup">
            <button class="toggle-btn" onclick="selectToggle('bizTypeGroup',this,'B2B')">B2B</button>
            <button class="toggle-btn" onclick="selectToggle('bizTypeGroup',this,'B2C')">B2C</button>
            <button class="toggle-btn" onclick="selectToggle('bizTypeGroup',this,'Both')">Both</button>
          </div>
        </div>
        <div>
          <label>Company Size</label>
          <select id="companySize">
            <option value="">Select Size</option>
            <option>1–10 employees</option>
            <option>11–50 employees</option>
            <option>51–200 employees</option>
            <option>200+ employees</option>
          </select>
        </div>
        <div>
          <label>What You Sell</label>
          <select id="sellType">
            <option value="">Select Type</option>
            <option>Product</option>
            <option>Service</option>
            <option>Course</option>
            <option>Subscription</option>
            <option>Multiple</option>
          </select>
        </div>
        <div style="display:flex;align-items:flex-end">
          <button class="btn-primary" onclick="saveProfile()" style="width:100%">💾 Save Profile</button>
        </div>
      </div>
      <div class="profile-saved" id="profileSaved">
        <div class="dot-pulse"></div>
        <span>Profile Saved — predictions are now personalized.</span>
      </div>
    </div>
  </div>
</section>

<div class="section-divider"></div>

<!-- SECTION 2: PREDICTOR -->
<section id="predictor">
  <div class="container">
    <span class="section-tag tag-purple">02 — Lead Predictor</span>
    <h2 class="section-title">Analyze Single Lead Intent</h2>
    <p class="section-desc">Enter behavioral data for one lead — time on site, visits, scroll depth, and clicks — to predict their purchase intent.</p>

    <div class="card card-purple">
      <!-- TIMER -->
      <div style="margin-bottom:1.5rem">
        <label>⏱ Time Spent on Website</label>
        <div class="timer-display" id="timerDisplay">0h 0m 0s</div>
        <div class="timer-controls">
          <button class="timer-btn timer-start" onclick="timerStart()">▶ Start</button>
          <button class="timer-btn timer-stop" onclick="timerStop()">⏸ Stop</button>
          <button class="timer-btn timer-reset" onclick="timerReset()">↺ Reset</button>
        </div>
        <p style="text-align:center;font-size:.8rem;color:var(--muted);margin-bottom:.75rem">— or type manually —</p>
        <div class="timer-manual">
          <input type="number" id="manH" placeholder="HH" min="0" max="99" onchange="manualTime()" style="width:75px;text-align:center"/>
          <span>h</span>
          <input type="number" id="manM" placeholder="MM" min="0" max="59" onchange="manualTime()" style="width:75px;text-align:center"/>
          <span>m</span>
          <input type="number" id="manS" placeholder="SS" min="0" max="59" onchange="manualTime()" style="width:75px;text-align:center"/>
          <span>s</span>
        </div>
      </div>

      <div class="grid-2" style="gap:1.5rem;margin-bottom:1.5rem">
        <div>
          <label>Total Visits</label>
          <input type="number" id="visits" placeholder="e.g. 4" min="0"/>
        </div>
        <div>
          <label>Number of Clicks</label>
          <input type="number" id="clicks" placeholder="e.g. 8" min="0"/>
        </div>
      </div>

      <div style="margin-bottom:2rem">
        <label>Scroll Depth — <span id="scrollLabel" style="color:var(--cyan);font-weight:700">50%</span></label>
        <div class="slider-wrap">
          <input type="range" id="scrollDepth" min="0" max="100" value="50" oninput="document.getElementById('scrollLabel').textContent=this.value+'%'"/>
        </div>
      </div>

      <button class="btn-predict" onclick="predict()">⚡ Predict Lead Intent</button>

      <div class="result-badge" id="resultBadge">
        <div class="result-emoji" id="resultEmoji"></div>
        <div class="result-label" id="resultLabel"></div>
        <div class="result-msg" id="resultMsg"></div>
      </div>
    </div>
  </div>
</section>

<div class="section-divider"></div>

<!-- SECTION 3: BULK UPLOAD -->
<section id="bulk">
  <div class="container">
    <span class="section-tag tag-cyan">03 — Bulk Company Analysis</span>
    <h2 class="section-title">Upload Excel to Analyze Multiple Companies</h2>
    <p class="section-desc">Upload a spreadsheet of prospective companies. Ad/Pulse will score each one and show you who's worth pursuing.</p>

    <div class="card card-cyan" style="margin-bottom:1.5rem">
      <div class="upload-zone" id="uploadZone">
        <input type="file" id="fileInput" accept=".xlsx,.xls,.csv" onchange="handleFile(this.files[0])"/>
        <div class="upload-icon">📊</div>
        <div class="upload-title">Drop your Excel file here</div>
        <div class="upload-sub">or click to browse — .xlsx, .xls, .csv accepted</div>
        <button class="btn-secondary" style="pointer-events:none">Choose File</button>
        <div class="upload-hint">Expected columns: Company, Industry, Time_Seconds, Visits, Scroll_Depth, Clicks</div>
      </div>

      <div class="template-hint">
        💡 <strong>Column Guide:</strong> Company Name | Industry | Time_Seconds (e.g. 180 = 3min) | Visits | Scroll_Depth (0-100) | Clicks
        &nbsp;·&nbsp; <a href="#" onclick="downloadTemplate(event)" style="color:var(--cyan);font-weight:700">Download Template ↓</a>
      </div>
    </div>

    <div class="bulk-results" id="bulkResults">
      <div style="display:flex;justify-content:space-between;align-items:center;margin-bottom:1.5rem;flex-wrap:wrap;gap:1rem">
        <h3 style="font-family:'Poppins',sans-serif;font-size:1.3rem;font-weight:800">Analysis Results</h3>
        <button class="btn-download" onclick="downloadBulkCSV()">⬇ Export Results CSV</button>
      </div>
      <div class="bulk-summary" id="bulkSummary"></div>
      <div style="display:grid;grid-template-columns:1.6fr 1fr;gap:2rem;align-items:start;margin-top:1.5rem">
        <div>
          <div id="bulkTable"></div>
        </div>
        <div>
          <canvas id="bulkChart" style="max-height:280px"></canvas>
        </div>
      </div>
      <div class="bulk-insights-grid" id="bulkInsights" style="margin-top:2rem"></div>
    </div>
  </div>
</section>

<div class="section-divider"></div>

<!-- SECTION 4: LIVE DASHBOARD -->
<section id="dashboard">
  <div class="container">
    <span class="section-tag tag-cyan">04 — Live Dashboard</span>
    <h2 class="section-title">Session Analytics</h2>
    <p class="section-desc">Every lead you analyze appears here in real-time. Track patterns, spot trends, and act fast.</p>

    <div class="stat-cards">
      <div class="stat-card total"><div class="stat-num total" id="statTotal">0</div><div class="stat-label">Total Analyzed</div></div>
      <div class="stat-card high-c"><div class="stat-num high-c" id="statHigh">0</div><div class="stat-label">High Interest</div></div>
      <div class="stat-card med-c"><div class="stat-num med-c" id="statMed">0</div><div class="stat-label">Medium Interest</div></div>
      <div class="stat-card low-c"><div class="stat-num low-c" id="statLow">0</div><div class="stat-label">Low Interest</div></div>
    </div>

    <div class="card card-cyan">
      <div id="tableWrap">
        <div class="empty-state"><div class="big-icon">📋</div><p>No leads analyzed yet. Use the predictor above.</p></div>
      </div>
      <div class="chart-wrap">
        <canvas id="donutChart"></canvas>
        <p style="text-align:center;font-size:.8rem;color:var(--muted);margin-top:.75rem">Lead Distribution</p>
      </div>
    </div>
  </div>
</section>

<div class="section-divider"></div>

<!-- SECTION 5: AI INSIGHTS -->
<section id="insights">
  <div class="container">
    <span class="section-tag tag-pink">05 — AI Insights</span>
    <h2 class="section-title">Personalized Action Intelligence</h2>
    <p class="section-desc">Based on your company profile and latest prediction — here's exactly what to do next.</p>
    <div id="insightCards" style="display:grid;grid-template-columns:repeat(3,1fr);gap:1.25rem">
      <div class="insight-card" style="grid-column:1/-1;text-align:center;padding:3rem;color:var(--muted)">
        <div style="font-size:2rem;margin-bottom:.75rem;opacity:.4">💡</div>
        <p>Run a prediction to unlock personalized AI insights based on your profile and lead data.</p>
      </div>
    </div>
  </div>
</section>

<div class="section-divider"></div>

<!-- SECTION 6: SERVICES -->
<section id="services">
  <div class="container">
    <span class="section-tag tag-green">06 — What We Do</span>
    <h2 class="section-title">Built for Modern Marketing</h2>
    <p class="section-desc">Four core pillars that turn engagement data into revenue-generating action.</p>
    <div class="services-grid">
      <div class="service-card s1">
        <div class="service-num">01</div>
        <div class="service-name">🎯 Lead Generation</div>
        <p class="service-desc">We build multi-channel funnels that attract qualified prospects — not just traffic. Every lead is tracked, scored, and ready for conversion from day one.</p>
      </div>
      <div class="service-card s2">
        <div class="service-num">02</div>
        <div class="service-name">⚡ Conversion Optimization</div>
        <p class="service-desc">A/B testing, landing page engineering, and behavioral triggers that turn visitors into buyers. We don't guess — we measure and iterate until results improve.</p>
      </div>
      <div class="service-card s3">
        <div class="service-num">03</div>
        <div class="service-name">📈 Campaign Analytics</div>
        <p class="service-desc">Real-time dashboards, attribution modeling, and cohort analysis. Know exactly which campaigns drive ROI — and kill the ones that don't.</p>
      </div>
      <div class="service-card s4">
        <div class="service-num">04</div>
        <div class="service-name">🚀 Personalized Ad Strategy</div>
        <p class="service-desc">AI-informed creative strategy tailored to your audience segments. Meta, Google, LinkedIn — we deploy where your buyers actually live.</p>
      </div>
    </div>
  </div>
</section>

<div class="section-divider"></div>

<!-- SECTION 7: CONTACT -->
<section id="contact">
  <div class="container">
    <div class="contact-grid">
      <div>
        <span class="section-tag tag-green">07 — Start Your Growth Journey</span>
        <h2 class="section-title">Let's Build Something That Converts</h2>
        <p class="section-desc">Tell us about your business and goals. We'll map out a custom growth plan — no fluff, no generic decks.</p>
        <ul class="contact-perks">
          <li><span>✅</span><span>Free 30-min strategy call</span></li>
          <li><span>✅</span><span>Custom campaign roadmap built for your industry</span></li>
          <li><span>✅</span><span>No long-term contracts — results first</span></li>
        </ul>
      </div>
      <div class="card card-green">
        <div class="grid-2" style="gap:1rem;margin-bottom:1rem">
          <div>
            <label>Full Name</label>
            <input type="text" placeholder="Sarah Chen"/>
          </div>
          <div>
            <label>Business Email</label>
            <input type="email" placeholder="sarah@company.com"/>
          </div>
          <div>
            <label>Company Name</label>
            <input type="text" placeholder="Nexora Inc."/>
          </div>
          <div>
            <label>Industry</label>
            <input type="text" placeholder="SaaS / E-commerce / etc."/>
          </div>
        </div>
        <div style="margin-bottom:1rem">
          <label>Your Goal</label>
          <select>
            <option>More Leads</option>
            <option>Better Conversions</option>
            <option>Brand Awareness</option>
            <option>Full Campaign Management</option>
          </select>
        </div>
        <div style="margin-bottom:1.5rem">
          <label>Tell Us About Your Business</label>
          <textarea placeholder="What are you selling, who's your audience, what's not working right now?"></textarea>
        </div>
        <button class="btn-submit" onclick="this.textContent='✅ Sent! We\'ll reach out within 24h'">Let's Grow Together →</button>
      </div>
    </div>
  </div>
</section>

<!-- FOOTER -->
<footer>
  <div class="footer-logo">Ad/Pulse</div>
  <p class="footer-tagline">Turning engagement into revenue — one lead at a time.</p>
  <div class="social-icons">
    <a class="social-icon" href="#">𝕏</a>
    <a class="social-icon" href="#">in</a>
    <a class="social-icon" href="#">f</a>
    <a class="social-icon" href="#">▶</a>
  </div>
  <p class="footer-copy">© 2026 Ad/Pulse. All rights reserved.</p>
</footer>

<!-- CHATBOT -->
<button id="chatBtn" onclick="toggleChat()">💬</button>
<div id="chatPanel">
  <div class="chat-header">
    <span class="chat-header-title">🤖 Pulse Assistant</span>
    <button class="chat-close" onclick="toggleChat()">✕</button>
  </div>
  <div id="chatMessages">
    <div class="chat-msg bot">Hey! 👋 I'm your Ad/Pulse marketing advisor. Ask me anything about leads, conversions, or how the platform works.</div>
  </div>
  <div class="chat-suggestions">
    <span class="chat-sug" onclick="chatAsk(this.textContent)">What is a high intent lead?</span>
    <span class="chat-sug" onclick="chatAsk(this.textContent)">How to improve conversion rate?</span>
    <span class="chat-sug" onclick="chatAsk(this.textContent)">What does scroll depth mean?</span>
    <span class="chat-sug" onclick="chatAsk(this.textContent)">Follow up with medium lead?</span>
    <span class="chat-sug" onclick="chatAsk(this.textContent)">Best converting industry?</span>
    <span class="chat-sug" onclick="chatAsk(this.textContent)">How does Ad/Pulse work?</span>
  </div>
</div>

<script>
/* ============================================================
   STATE
   ============================================================ */
let profile = {};
let timerSec = 0;
let timerRunning = false;
let timerInterval = null;
let leads = [];
let donutChartInst = null;
let bulkChartInst = null;
let bulkData = [];

/* ============================================================
   PROFILE
   ============================================================ */
function selectToggle(groupId, el, val) {
  document.querySelectorAll('#' + groupId + ' .toggle-btn').forEach(b => b.classList.remove('active'));
  el.classList.add('active');
  el.dataset.val = val;
}

function saveProfile() {
  const bizBtn = document.querySelector('#bizTypeGroup .toggle-btn.active');
  profile = {
    company: document.getElementById('companyName').value || 'Your Company',
    industry: document.getElementById('industry').value || 'Other',
    bizType: bizBtn ? bizBtn.dataset.val : 'B2B',
    size: document.getElementById('companySize').value || '11–50 employees',
    sell: document.getElementById('sellType').value || 'Service'
  };
  const saved = document.getElementById('profileSaved');
  saved.classList.add('show');
  setTimeout(() => saved.classList.remove('show'), 4000);
}

/* ============================================================
   TIMER
   ============================================================ */
function timerStart() {
  if (timerRunning) return;
  timerRunning = true;
  timerInterval = setInterval(() => {
    timerSec++;
    updateTimerDisplay(timerSec);
    syncManualFields(timerSec);
  }, 1000);
}
function timerStop() {
  timerRunning = false;
  clearInterval(timerInterval);
}
function timerReset() {
  timerStop();
  timerSec = 0;
  updateTimerDisplay(0);
  syncManualFields(0);
}
function updateTimerDisplay(s) {
  const h = Math.floor(s / 3600);
  const m = Math.floor((s % 3600) / 60);
  const sec = s % 60;
  document.getElementById('timerDisplay').textContent = `${h}h ${m}m ${sec}s`;
}
function syncManualFields(s) {
  document.getElementById('manH').value = Math.floor(s / 3600) || '';
  document.getElementById('manM').value = Math.floor((s % 3600) / 60) || '';
  document.getElementById('manS').value = s % 60 || '';
}
function manualTime() {
  const h = parseInt(document.getElementById('manH').value) || 0;
  const m = parseInt(document.getElementById('manM').value) || 0;
  const s = parseInt(document.getElementById('manS').value) || 0;
  timerSec = h * 3600 + m * 60 + s;
  updateTimerDisplay(timerSec);
}

/* ============================================================
   PREDICTION LOGIC
   ============================================================ */
function scoreLeadRaw(sec, scroll, clicks) {
  if (sec > 120 && scroll > 70 && clicks > 5) return 'high';
  if (sec > 60 || scroll > 40 || clicks > 3) return 'medium';
  return 'low';
}

function predict() {
  const visits = parseInt(document.getElementById('visits').value) || 0;
  const clicks = parseInt(document.getElementById('clicks').value) || 0;
  const scroll = parseInt(document.getElementById('scrollDepth').value) || 0;
  const sec = timerSec;

  const level = scoreLeadRaw(sec, scroll, clicks);
  showResult(level);

  const h = Math.floor(sec / 3600), m = Math.floor((sec % 3600) / 60), s = sec % 60;
  const timeStr = `${h}h ${m}m ${s}s`;
  leads.push({ time: timeStr, visits, scroll, clicks, level });
  updateDashboard();
  updateInsights(level);
  document.getElementById('dashboard').scrollIntoView({ behavior: 'smooth', block: 'start' });
  setTimeout(() => document.getElementById('insights').scrollIntoView({ behavior: 'smooth', block: 'start' }), 800);
}

function showResult(level) {
  const badge = document.getElementById('resultBadge');
  const emoji = document.getElementById('resultEmoji');
  const label = document.getElementById('resultLabel');
  const msg = document.getElementById('resultMsg');

  badge.className = 'result-badge show ' + level;
  label.className = 'result-label ' + level;

  const data = {
    high: { emoji: '🟢', label: 'High Interest Lead', msg: 'Hot lead! Prioritize this prospect immediately. Strike while intent is high.' },
    medium: { emoji: '🟡', label: 'Medium Interest Lead', msg: 'Promising lead! A personalized follow-up campaign could push this lead to convert.' },
    low: { emoji: '🔴', label: 'Low Interest Lead', msg: 'This lead needs nurturing. Low engagement detected. Consider re-targeting campaigns.' }
  };
  emoji.textContent = data[level].emoji;
  label.textContent = data[level].label;
  msg.textContent = data[level].msg;
}

/* ============================================================
   DASHBOARD
   ============================================================ */
function updateDashboard() {
  const h = leads.filter(l => l.level === 'high').length;
  const m = leads.filter(l => l.level === 'medium').length;
  const lo = leads.filter(l => l.level === 'low').length;

  document.getElementById('statTotal').textContent = leads.length;
  document.getElementById('statHigh').textContent = h;
  document.getElementById('statMed').textContent = m;
  document.getElementById('statLow').textContent = lo;

  // Table
  const wrap = document.getElementById('tableWrap');
  if (!leads.length) {
    wrap.innerHTML = '<div class="empty-state"><div class="big-icon">📋</div><p>No leads yet.</p></div>';
  } else {
    let html = '<table class="lead-table"><thead><tr><th>#</th><th>Time</th><th>Visits</th><th>Scroll</th><th>Clicks</th><th>Result</th></tr></thead><tbody>';
    leads.forEach((l, i) => {
      const cls = l.level === 'high' ? 'badge-high' : l.level === 'medium' ? 'badge-med' : 'badge-low';
      const lbl = l.level.charAt(0).toUpperCase() + l.level.slice(1);
      html += `<tr><td>${i + 1}</td><td>${l.time}</td><td>${l.visits}</td><td>${l.scroll}%</td><td>${l.clicks}</td><td><span class="${cls}">${lbl}</span></td></tr>`;
    });
    html += '</tbody></table>';
    wrap.innerHTML = html;
  }

  // Donut
  const ctx = document.getElementById('donutChart').getContext('2d');
  if (donutChartInst) donutChartInst.destroy();
  if (leads.length) {
    donutChartInst = new Chart(ctx, {
      type: 'doughnut',
      data: {
        labels: ['High', 'Medium', 'Low'],
        datasets: [{ data: [h, m, lo], backgroundColor: ['#10b981', '#f59e0b', '#ef4444'], borderWidth: 0, hoverOffset: 8 }]
      },
      options: {
        plugins: {
          legend: { labels: { color: '#94a3b8', font: { family: 'Poppins', size: 12 }, padding: 16 } }
        },
        cutout: '68%',
        animation: { animateRotate: true, duration: 800 }
      }
    });
  }
}

/* ============================================================
   INSIGHTS
   ============================================================ */
function updateInsights(level) {
  const ind = profile.industry || 'General';
  const biz = profile.bizType || 'B2B';
  const sell = profile.sell || 'Service';

  const insightMap = {
    high: {
      'SaaS/Software': [
        { icon: '🎯', title: 'Send a Demo Invite NOW', text: 'This B2B SaaS lead has evaluated your product deeply. Reach out with a personalized demo invite within the next 2 hours. Decision-makers move fast.' },
        { icon: '💼', title: 'Prepare a ROI Pitch', text: 'High-intent SaaS leads respond to value quantification. Show them a 3-month ROI projection based on their company size and use case.' },
        { icon: '📞', title: 'Direct Sales Outreach', text: 'Skip the nurture sequence — this lead deserves a direct call. Pair it with a one-pager tailored to their industry segment.' }
      ],
      'Healthcare': [
        { icon: '⚡', title: 'Respond Within 1 Hour', text: 'High-intent healthcare leads are rare and extremely valuable. Trust is everything — speed of response signals reliability and seriousness.' },
        { icon: '🛡️', title: 'Lead with Compliance', text: 'Healthcare buyers care about security and compliance first. Lead your outreach with HIPAA readiness and case studies from similar providers.' },
        { icon: '📊', title: 'Case Study Deck', text: 'Share a success story from a similar healthcare client. Peer proof is the fastest trust-builder in this vertical.' }
      ],
      'E-commerce': [
        { icon: '🛒', title: 'Exclusive Access Offer', text: 'This is a purchase-ready lead. Send an exclusive early access offer or limited-time bundle. Urgency converts high-intent retail shoppers.' },
        { icon: '🔁', title: 'Retargeting Sequence', text: 'Deploy personalized retargeting ads showing the exact products they browsed. Match the ad creative to their scroll depth behavior.' },
        { icon: '💌', title: 'Abandoned Cart Trigger', text: 'If this is a returning visitor with high scroll, trigger a cart-recovery email with free shipping. Convert before they find a competitor.' }
      ],
      default: [
        { icon: '🔥', title: 'Strike While Intent Is Hot', text: 'This is your highest-priority lead right now. Assign to your best sales rep and initiate contact within the next 3 hours.' },
        { icon: '🎁', title: 'Offer Immediate Value', text: 'High-intent leads convert faster when given a small win upfront. Consider a free audit, trial, or custom proposal as a hook.' },
        { icon: '📅', title: 'Book a Discovery Call', text: 'Use Calendly or a direct invite to book a 20-minute discovery call. Frame it as understanding their goals — not selling.' }
      ]
    },
    medium: {
      'E-commerce': [
        { icon: '🏷️', title: 'Trigger a Discount Offer', text: 'Medium intent on e-commerce often signals price hesitation. Deploy a 10–15% discount email or a free shipping offer with a 48-hour expiry.' },
        { icon: '📧', title: 'Nurture Email Sequence', text: 'Start a 5-email behavioral nurture sequence: value → social proof → objection handling → offer → urgency. Spread over 10 days.' },
        { icon: '🧲', title: 'Retarget with Social Proof', text: 'Show them UGC ads featuring real customer reviews. Medium-intent buyers need social validation before committing.' }
      ],
      'Education': [
        { icon: '🎓', title: 'Offer a Free Sample Lesson', text: 'Medium-intent education leads often face content doubt. A free lesson or mini-quiz reactivates curiosity and builds commitment.' },
        { icon: '📹', title: 'Instructor Intro Video', text: 'Send a short personal video from the course creator. Human connection dramatically increases conversion in the education space.' },
        { icon: '💬', title: 'Community Sneak Peek', text: 'Invite them to a free live Q&A or community Slack. Let them experience the learning environment before buying.' }
      ],
      default: [
        { icon: '📬', title: 'Personalized Follow-Up', text: 'This lead is considering — they just need a push. Send a personalized message referencing their specific behavior and use case.' },
        { icon: '🧪', title: 'A/B Test Your CTA', text: 'Test two different value propositions in your outreach. Medium leads are comparing options — show clear differentiation.' },
        { icon: '⏰', title: 'Create Urgency', text: 'Add a time-limited incentive to your next touchpoint. "This offer expires in 72 hours" moves fence-sitters into action.' }
      ]
    },
    low: {
      'Education': [
        { icon: '🎯', title: 'Content Mismatch Fix', text: 'Low engagement often means your content isn\'t matching their learning goal. Survey this segment and redesign the top-of-funnel content.' },
        { icon: '🔄', title: 'Re-engagement Quiz', text: 'A short quiz ("What kind of learner are you?") creates personalized re-engagement and moves leads deeper into the funnel.' },
        { icon: '💡', title: 'Lower the Barrier', text: 'Offer a completely free micro-course or downloadable guide. Get them experiencing value before asking for anything.' }
      ],
      default: [
        { icon: '🌱', title: 'Long-Term Nurture', text: 'This lead isn\'t ready now — but they could be in 30–60 days. Add to a long-term nurture sequence with educational content.' },
        { icon: '📉', title: 'Audit Your Landing Page', text: 'Low engagement often reflects a message-market mismatch. Review your headline, offer, and CTA for this traffic source.' },
        { icon: '🎯', title: 'Re-targeting Campaign', text: 'Launch a retargeting ad campaign with fresh creative. Test a video ad — video retargeting outperforms static by 3x for cold audiences.' }
      ]
    }
  };

  const levelMap = insightMap[level];
  const cards = levelMap[ind] || levelMap['default'];
  const container = document.getElementById('insightCards');
  container.innerHTML = cards.map(c => `
    <div class="insight-card">
      <div class="insight-icon">${c.icon}</div>
      <div class="insight-title">${c.title}</div>
      <p class="insight-text">${c.text}</p>
    </div>
  `).join('');
}

/* ============================================================
   BULK UPLOAD
   ============================================================ */
const uploadZone = document.getElementById('uploadZone');
uploadZone.addEventListener('dragover', e => { e.preventDefault(); uploadZone.classList.add('drag'); });
uploadZone.addEventListener('dragleave', () => uploadZone.classList.remove('drag'));
uploadZone.addEventListener('drop', e => {
  e.preventDefault();
  uploadZone.classList.remove('drag');
  if (e.dataTransfer.files[0]) handleFile(e.dataTransfer.files[0]);
});

function handleFile(file) {
  if (!file) return;
  const ext = file.name.split('.').pop().toLowerCase();
  const reader = new FileReader();
  reader.onload = e => {
    const data = new Uint8Array(e.target.result);
    const wb = XLSX.read(data, { type: 'array' });
    const ws = wb.Sheets[wb.SheetNames[0]];
    const rows = XLSX.utils.sheet_to_json(ws, { defval: '' });
    processBulk(rows, file.name);
  };
  reader.readAsArrayBuffer(file);
}

function processBulk(rows, fname) {
  bulkData = rows.map((r, i) => {
    const sec = parseInt(r['Time_Seconds'] || r['time_seconds'] || r['Time'] || 0);
    const scroll = parseFloat(r['Scroll_Depth'] || r['scroll_depth'] || r['Scroll'] || 0);
    const clicks = parseInt(r['Clicks'] || r['clicks'] || 0);
    const visits = parseInt(r['Visits'] || r['visits'] || 0);
    const company = r['Company'] || r['company'] || r['Company Name'] || `Company ${i + 1}`;
    const industry = r['Industry'] || r['industry'] || '—';
    const level = scoreLeadRaw(sec, scroll, clicks);
    const h = Math.floor(sec / 3600), m = Math.floor((sec % 3600) / 60), s = sec % 60;
    return { company, industry, time: `${h}h ${m}m ${s}s`, sec, visits, scroll, clicks, level };
  });

  renderBulkResults(fname);
}

function renderBulkResults(fname) {
  const h = bulkData.filter(d => d.level === 'high').length;
  const m = bulkData.filter(d => d.level === 'medium').length;
  const lo = bulkData.filter(d => d.level === 'low').length;

  // Summary cards
  document.getElementById('bulkSummary').innerHTML = `
    <div class="stat-card high-c"><div class="stat-num high-c">${h}</div><div class="stat-label">High Interest</div></div>
    <div class="stat-card med-c"><div class="stat-num med-c">${m}</div><div class="stat-label">Medium Interest</div></div>
    <div class="stat-card low-c"><div class="stat-num low-c">${lo}</div><div class="stat-label">Low Interest</div></div>
  `;

  // Table
  let tableHtml = `<table class="lead-table" style="width:100%">
    <thead><tr><th>#</th><th>Company</th><th>Industry</th><th>Time</th><th>Scroll</th><th>Clicks</th><th>Result</th></tr></thead><tbody>`;
  bulkData.forEach((d, i) => {
    const cls = d.level === 'high' ? 'badge-high' : d.level === 'medium' ? 'badge-med' : 'badge-low';
    const lbl = d.level.charAt(0).toUpperCase() + d.level.slice(1);
    tableHtml += `<tr><td>${i + 1}</td><td style="font-weight:600">${d.company}</td><td>${d.industry}</td><td>${d.time}</td><td>${d.scroll}%</td><td>${d.clicks}</td><td><span class="${cls}">${lbl}</span></td></tr>`;
  });
  tableHtml += '</tbody></table>';
  document.getElementById('bulkTable').innerHTML = tableHtml;

  // Chart
  const ctx = document.getElementById('bulkChart').getContext('2d');
  if (bulkChartInst) bulkChartInst.destroy();
  bulkChartInst = new Chart(ctx, {
    type: 'doughnut',
    data: {
      labels: [`High (${h})`, `Medium (${m})`, `Low (${lo})`],
      datasets: [{ data: [h, m, lo], backgroundColor: ['#10b981', '#f59e0b', '#ef4444'], borderWidth: 0, hoverOffset: 8 }]
    },
    options: {
      plugins: {
        legend: { labels: { color: '#94a3b8', font: { family: 'Poppins', size: 12 }, padding: 16 } }
      },
      cutout: '65%',
      animation: { animateRotate: true, duration: 900 }
    }
  });

  // Bulk insights
  const highCos = bulkData.filter(d => d.level === 'high').map(d => d.company).slice(0, 3).join(', ') || 'None';
  const medCos = bulkData.filter(d => d.level === 'medium').map(d => d.company).slice(0, 3).join(', ') || 'None';
  const dominantIndustry = (() => {
    const freq = {};
    bulkData.forEach(d => { freq[d.industry] = (freq[d.industry] || 0) + 1; });
    return Object.entries(freq).sort((a, b) => b[1] - a[1])[0]?.[0] || 'Mixed';
  })();

  document.getElementById('bulkInsights').innerHTML = `
    <div class="insight-card" style="border-color:rgba(16,185,129,.3)">
      <div class="insight-icon">🔥</div>
      <div class="insight-title">Priority Targets</div>
      <p class="insight-text"><strong style="color:var(--green)">${h} high-intent companies</strong> are ready for immediate outreach: <strong>${highCos}</strong>. Assign your best sales reps to these accounts today.</p>
    </div>
    <div class="insight-card" style="border-color:rgba(245,158,11,.3)">
      <div class="insight-icon">⏳</div>
      <div class="insight-title">Nurture Pipeline</div>
      <p class="insight-text"><strong style="color:var(--yellow)">${m} medium-intent companies</strong> (${medCos}) need a personalized follow-up sequence. Build a 3-touch drip campaign targeting their specific interest signals.</p>
    </div>
    <div class="insight-card" style="border-color:rgba(239,68,68,.3)">
      <div class="insight-icon">🌱</div>
      <div class="insight-title">Long-Term Nurture</div>
      <p class="insight-text"><strong style="color:var(--red)">${lo} low-intent companies</strong> aren't ready yet. Add them to a 60-day educational email sequence and re-score after a month of content engagement.</p>
    </div>
    <div class="insight-card" style="border-color:rgba(6,182,212,.3)">
      <div class="insight-icon">📊</div>
      <div class="insight-title">Industry Focus</div>
      <p class="insight-text">Your uploaded list is dominated by <strong style="color:var(--cyan)">${dominantIndustry}</strong> companies. Tailor your outreach copy and case studies to match their specific pain points and compliance needs.</p>
    </div>
  `;

  document.getElementById('bulkResults').classList.add('show');
  document.getElementById('bulkResults').scrollIntoView({ behavior: 'smooth' });
}

function downloadBulkCSV() {
  if (!bulkData.length) return;
  const headers = ['Company', 'Industry', 'Time', 'Visits', 'Scroll%', 'Clicks', 'Lead Level'];
  const rows = bulkData.map(d => [d.company, d.industry, d.time, d.visits, d.scroll, d.clicks, d.level]);
  const csv = [headers, ...rows].map(r => r.join(',')).join('\n');
  const a = document.createElement('a');
  a.href = 'data:text/csv;charset=utf-8,' + encodeURIComponent(csv);
  a.download = 'adpulse_bulk_results.csv';
  a.click();
}

function downloadTemplate(e) {
  e.preventDefault();
  const csv = 'Company,Industry,Time_Seconds,Visits,Scroll_Depth,Clicks\nAcme Corp,E-commerce,180,3,65,7\nTechStart Inc,SaaS/Software,45,1,20,2\nHealthPlus,Healthcare,240,5,85,12';
  const a = document.createElement('a');
  a.href = 'data:text/csv;charset=utf-8,' + encodeURIComponent(csv);
  a.download = 'adpulse_template.csv';
  a.click();
}

/* ============================================================
   CHATBOT
   ============================================================ */
const chatResponses = {
  'what is a high intent lead': '🔥 A high intent lead has spent more than 2 minutes on your site, scrolled past 70% of the page, AND clicked more than 5 times. These signals together show they\'re actively evaluating — not just browsing. Reach out within the hour.',
  'high interest lead': '🔥 A high interest lead has spent 2+ minutes on site, scrolled 70%+, and clicked 5+ times. This is your hottest prospect. Contact them immediately before they look elsewhere.',
  'how to improve conversion rate': '📈 Three proven moves: (1) Add social proof near your CTA — testimonials increase conversion by 34%. (2) Reduce form fields — every extra field loses 11% of conversions. (3) A/B test your headline — this single change can lift conversion by 50%+.',
  'conversion rate': '📈 To boost conversion: simplify your CTA, add social proof near the button, and A/B test headlines. Even a 1% lift in conversion rate can mean 2-3x more revenue.',
  'scroll depth': '📜 Scroll depth measures how far down your page a visitor has read. 0% = they bounced at the top. 100% = they read everything. 70%+ scroll depth tells us they\'re genuinely engaged with your content — a strong buying signal.',
  'what does scroll depth mean': '📜 Scroll depth tracks how far a visitor scrolls on your page. High scroll depth (70%+) means they\'re reading your full pitch — much more likely to convert than shallow scrollers.',
  'follow up with medium lead': '📧 Medium leads respond best to: a personalized email referencing something specific (their industry, their pain point), a time-limited incentive, and a clear single CTA. Don\'t send them a generic newsletter — make it feel 1:1.',
  'medium lead': '📧 For medium leads: send a personal email, add a 72-hour incentive, and give them one clear next step. Avoid overwhelming them with options.',
  'best converting industry': '🏆 Based on industry benchmarks: SaaS B2B typically converts at 5–8% with strong nurture. E-commerce averages 2–4%. Healthcare is low volume but extremely high value. Real Estate converts fast when intent signals are high. Context matters more than industry averages.',
  'which industry converts best': '🏆 SaaS and Professional Services tend to have the highest conversion rates with proper nurturing. But the best-converting industry is the one where your messaging matches buyer psychology perfectly.',
  'how does ad/pulse work': '⚡ Ad/Pulse scores leads using 4 behavioral signals: time on site, visit frequency, scroll depth, and click count. These are combined into a predictive model that classifies each lead as High, Medium, or Low intent — so you know exactly who to prioritize and how to follow up.',
  'how does adpulse work': '⚡ Ad/Pulse analyzes behavioral engagement data — time, scroll, clicks, visits — and uses a scoring algorithm to predict purchase intent. The output tells you who to contact now, who to nurture, and who to re-engage later.'
};

function toggleChat() {
  const panel = document.getElementById('chatPanel');
  panel.classList.toggle('open');
}

function chatAsk(q) {
  const msgs = document.getElementById('chatMessages');
  msgs.innerHTML += `<div class="chat-msg user">${q}</div>`;
  setTimeout(() => {
    const key = Object.keys(chatResponses).find(k => q.toLowerCase().includes(k));
    const reply = key ? chatResponses[key] : '🤔 Great question! That\'s a nuanced topic. The short answer: focus on behavioral intent signals — time, scroll, and clicks — rather than just demographics. Want to know more about a specific metric?';
    msgs.innerHTML += `<div class="chat-msg bot">${reply}</div>`;
    msgs.scrollTop = msgs.scrollHeight;
  }, 400);
  msgs.scrollTop = msgs.scrollHeight;
}
</script>
</body>
</html>
