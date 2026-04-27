<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<meta name="description" content="ZAxis Studio – Premium on-demand 3D printing. Custom prototypes, functional parts, artistic creations.">
<title>ZAxis Studio | Modern 3D Printing Studio</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Syne:wght@400;500;700;800&family=DM+Sans:ital,opsz,wght@0,9..40,300;0,9..40,400;0,9..40,500;1,9..40,300&display=swap" rel="stylesheet">
<style>
*,*::before,*::after{box-sizing:border-box;margin:0;padding:0}
:root{
  --bg:#09090A;
  --bg2:#111113;
  --bg3:#18181B;
  --surface:#1F1F23;
  --border:rgba(255,255,255,0.07);
  --border2:rgba(255,255,255,0.14);
  --text:#EDE8DF;
  --muted:#6B6760;
  --muted2:#9A9590;
  --accent:#FF5200;
  --accent2:#FF7A38;
}
html{scroll-behavior:smooth}
body{background:var(--bg);color:var(--text);font-family:'DM Sans',sans-serif;font-size:16px;line-height:1.6;overflow-x:hidden}
body::before{content:'';position:fixed;inset:0;background-image:radial-gradient(circle,rgba(255,255,255,0.032) 1px,transparent 1px);background-size:28px 28px;pointer-events:none;z-index:0}
section,nav,header,footer{position:relative;z-index:1}
::-webkit-scrollbar{width:3px}::-webkit-scrollbar-track{background:var(--bg)}::-webkit-scrollbar-thumb{background:var(--accent)}
#scrollProgress{position:fixed;top:0;left:0;height:2px;background:var(--accent);z-index:200;transition:width 0.08s linear;box-shadow:0 0 10px var(--accent)}
nav{position:fixed;top:0;left:0;right:0;z-index:100;display:flex;align-items:center;justify-content:space-between;padding:22px 48px;border-bottom:1px solid var(--border);background:rgba(9,9,10,0.88);backdrop-filter:blur(24px);-webkit-backdrop-filter:blur(24px)}
.logo{font-family:'Syne',sans-serif;font-weight:800;font-size:17px;letter-spacing:0.03em;color:var(--text);text-decoration:none;display:flex;align-items:center;gap:10px}
.logo-mark{width:28px;height:28px;border:1.5px solid var(--accent);border-radius:6px;display:flex;align-items:center;justify-content:center;position:relative;overflow:hidden}
.logo-mark::after{content:'';position:absolute;bottom:0;left:0;right:0;height:40%;background:var(--accent);animation:layer-build 2.2s ease-in-out infinite alternate}
@keyframes layer-build{0%{height:18%}100%{height:68%}}
.nav-links{display:flex;align-items:center;gap:36px;font-size:14px;color:var(--muted2)}
.nav-links a{color:inherit;text-decoration:none;transition:color 0.2s;letter-spacing:0.01em}
.nav-links a:hover{color:var(--text)}
.nav-cta{padding:10px 24px;background:var(--accent);color:#fff;font-size:13px;font-weight:500;letter-spacing:0.04em;border:none;border-radius:4px;cursor:pointer;text-decoration:none;transition:background 0.2s,transform 0.15s;white-space:nowrap}
.nav-cta:hover{background:var(--accent2);transform:translateY(-1px)}
.hamburger{display:none;background:none;border:none;color:var(--text);font-size:22px;cursor:pointer;padding:4px}
#mobileMenu{display:none;position:absolute;top:100%;left:0;right:0;background:var(--bg2);border-bottom:1px solid var(--border);padding:24px 48px}
#mobileMenu a{display:block;padding:12px 0;color:var(--muted2);text-decoration:none;border-bottom:1px solid var(--border);font-size:15px}
#mobileMenu a:last-child{border:none;color:var(--accent);font-weight:500}
#mobileMenu a:hover{color:var(--text)}
header{min-height:100svh;display:flex;flex-direction:column;justify-content:flex-end;padding:120px 48px 64px;overflow:hidden}
.hero-label{display:inline-flex;align-items:center;gap:8px;font-size:11px;letter-spacing:0.12em;font-weight:500;color:var(--muted);text-transform:uppercase;margin-bottom:32px}
.hero-label-dot{width:6px;height:6px;border-radius:50%;background:var(--accent);box-shadow:0 0 8px var(--accent);animation:blink 2s ease-in-out infinite}
@keyframes blink{0%,100%{opacity:1}50%{opacity:0.3}}
.hero-title{font-family:'Syne',sans-serif;font-weight:800;font-size:clamp(52px,9vw,128px);line-height:0.92;letter-spacing:-0.03em;color:var(--text);margin-bottom:48px;max-width:900px}
.hero-title em{font-style:normal;color:var(--accent)}
.hero-bottom{display:flex;align-items:flex-end;justify-content:space-between;gap:40px;flex-wrap:wrap}
.hero-desc{font-size:17px;color:var(--muted2);max-width:380px;line-height:1.7;font-weight:300}
.hero-actions{display:flex;flex-direction:column;gap:16px;align-items:flex-end}
.btn-primary{display:inline-flex;align-items:center;gap:12px;padding:16px 36px;background:var(--accent);color:#fff;font-size:14px;font-weight:500;letter-spacing:0.05em;text-decoration:none;border-radius:4px;transition:background 0.2s,transform 0.15s;text-transform:uppercase;white-space:nowrap}
.btn-primary:hover{background:var(--accent2);transform:translateY(-2px)}
.btn-primary svg{transition:transform 0.2s}
.btn-primary:hover svg{transform:translateX(4px)}
.btn-ghost{display:inline-flex;align-items:center;gap:8px;font-size:13px;color:var(--muted);text-decoration:none;letter-spacing:0.05em;text-transform:uppercase;transition:color 0.2s}
.btn-ghost:hover{color:var(--text)}
.hero-stats{display:flex;gap:48px}
.stat-item{border-left:1px solid var(--border2);padding-left:24px}
.stat-num{font-family:'Syne',sans-serif;font-size:28px;font-weight:700;color:var(--text);line-height:1}
.stat-label{font-size:12px;color:var(--muted);letter-spacing:0.06em;text-transform:uppercase;margin-top:4px}
.hero-visual{position:absolute;right:48px;top:50%;transform:translateY(-50%);width:min(400px,32vw);aspect-ratio:1;perspective:600px;display:flex;align-items:center;justify-content:center}
.print-cube{width:200px;height:200px;position:relative;transform-style:preserve-3d;animation:rotate-cube 18s linear infinite}
@keyframes rotate-cube{0%{transform:rotateX(22deg) rotateY(0deg)}100%{transform:rotateX(22deg) rotateY(360deg)}}
.cube-face{position:absolute;inset:0;border:1px solid rgba(255,82,0,0.32)}
.cube-face::after{content:'';position:absolute;left:0;right:0;bottom:0;height:40%;background:repeating-linear-gradient(0deg,rgba(255,82,0,0.14) 0px,rgba(255,82,0,0.14) 1px,transparent 1px,transparent 5px);animation:fill-up 3s ease-in-out infinite alternate}
@keyframes fill-up{0%{height:18%}100%{height:82%}}
.cube-front{transform:translateZ(100px)}
.cube-back{transform:translateZ(-100px) rotateY(180deg)}
.cube-left{transform:rotateY(-90deg) translateZ(100px)}
.cube-right{transform:rotateY(90deg) translateZ(100px)}
.cube-top{transform:rotateX(90deg) translateZ(100px)}
.cube-bottom{transform:rotateX(-90deg) translateZ(100px)}
.print-head{position:absolute;width:5px;height:5px;border-radius:50%;background:var(--accent);box-shadow:0 0 16px 4px var(--accent);animation:print-move 2.5s ease-in-out infinite alternate}
@keyframes print-move{0%{left:20%;top:30%}33%{left:72%;top:52%}66%{left:38%;top:74%}100%{left:78%;top:38%}}
.badge-live{position:absolute;top:20px;right:-16px;background:var(--bg3);border:1px solid var(--border2);border-radius:4px;padding:8px 14px;font-size:11px;letter-spacing:0.08em;color:var(--muted2);text-transform:uppercase;display:flex;align-items:center;gap:6px;white-space:nowrap}
.badge-live::before{content:'';width:5px;height:5px;border-radius:50%;background:var(--accent);animation:blink 2s ease-in-out infinite;flex-shrink:0}
.marquee-strip{border-top:1px solid var(--border);border-bottom:1px solid var(--border);padding:16px 0;overflow:hidden;background:var(--bg2)}
.marquee-inner{display:flex;gap:64px;animation:marquee 30s linear infinite;width:max-content}
.marquee-inner span{font-size:12px;letter-spacing:0.12em;color:var(--muted);text-transform:uppercase;white-space:nowrap;display:flex;align-items:center;gap:16px}
.marquee-inner span::before{content:'';width:4px;height:4px;border-radius:50%;background:var(--accent);opacity:0.6}
@keyframes marquee{0%{transform:translateX(0)}100%{transform:translateX(-50%)}}
.section-label{font-size:11px;letter-spacing:0.12em;text-transform:uppercase;color:var(--muted);margin-bottom:16px;display:block}
.section-title{font-family:'Syne',sans-serif;font-weight:700;font-size:clamp(36px,5vw,62px);letter-spacing:-0.025em;line-height:1.0;color:var(--text)}
.services-section{padding:120px 48px}
.services-header{display:flex;justify-content:space-between;align-items:flex-end;margin-bottom:56px;flex-wrap:wrap;gap:20px}
.services-grid{display:grid;grid-template-columns:repeat(3,1fr);border:1px solid var(--border)}
.service-card{padding:48px 40px;border-right:1px solid var(--border);transition:background 0.3s;position:relative;overflow:hidden}
.service-card:last-child{border-right:none}
.service-card::before{content:'';position:absolute;bottom:0;left:0;right:0;height:2px;background:var(--accent);transform:scaleX(0);transform-origin:left;transition:transform 0.35s ease}
.service-card:hover::before{transform:scaleX(1)}
.service-card:hover{background:rgba(255,82,0,0.028)}
.service-icon{width:44px;height:44px;border:1px solid var(--border2);border-radius:8px;margin-bottom:28px;display:flex;align-items:center;justify-content:center;transition:border-color 0.2s}
.service-card:hover .service-icon{border-color:var(--accent)}
.service-num{font-family:'Syne',sans-serif;font-size:11px;letter-spacing:0.1em;color:var(--muted);margin-bottom:12px}
.service-name{font-family:'Syne',sans-serif;font-size:22px;font-weight:700;color:var(--text);margin-bottom:14px}
.service-desc{font-size:14px;color:var(--muted2);line-height:1.7;margin-bottom:28px}
.service-price{font-size:13px;letter-spacing:0.06em;color:var(--accent);text-transform:uppercase}
.materials-section{padding:120px 48px;background:var(--bg2)}
.materials-header{display:flex;justify-content:space-between;align-items:flex-end;margin-bottom:56px;flex-wrap:wrap;gap:20px}
.materials-grid{display:grid;grid-template-columns:repeat(4,1fr);gap:1px;background:var(--border);border:1px solid var(--border)}
.mat-card{background:var(--bg2);padding:36px 32px;transition:background 0.25s}
.mat-card:hover{background:var(--bg3)}
.mat-swatch{width:36px;height:36px;border-radius:50%;margin-bottom:20px;border:2px solid rgba(255,255,255,0.08)}
.mat-name{font-family:'Syne',sans-serif;font-weight:700;font-size:16px;margin-bottom:6px;color:var(--text)}
.mat-note{font-size:13px;color:var(--muted2);line-height:1.55}
.mat-props{display:flex;flex-wrap:wrap;gap:6px;margin-top:16px}
.mat-tag{font-size:11px;letter-spacing:0.06em;background:var(--surface);color:var(--muted2);padding:3px 10px;border-radius:2px;text-transform:uppercase}
.process-section{padding:120px 48px}
.process-steps{display:grid;grid-template-columns:repeat(4,1fr);gap:1px;background:var(--border);border:1px solid var(--border);margin-top:64px}
.step{background:var(--bg);padding:44px 36px;position:relative}
.step-number{font-family:'Syne',sans-serif;font-size:64px;font-weight:800;color:rgba(255,82,0,0.1);line-height:1;margin-bottom:20px}
.step-title{font-family:'Syne',sans-serif;font-size:18px;font-weight:700;margin-bottom:10px;color:var(--text)}
.step-desc{font-size:14px;color:var(--muted2);line-height:1.65}
.step-arrow{position:absolute;right:-13px;top:50%;transform:translateY(-50%);width:24px;height:24px;background:var(--bg);border:1px solid var(--border2);border-radius:50%;z-index:2;display:flex;align-items:center;justify-content:center}
.step:last-child .step-arrow{display:none}
.quote-section{padding:120px 48px;background:var(--bg2);border-top:1px solid var(--border);border-bottom:1px solid var(--border)}
.quote-inner{display:grid;grid-template-columns:1fr 1fr;gap:80px;align-items:start;max-width:1100px;margin:0 auto}
.quote-form{background:var(--bg3);border:1px solid var(--border);padding:48px}
.form-group{margin-bottom:24px}
.form-group label{display:block;font-size:11px;letter-spacing:0.1em;text-transform:uppercase;color:var(--muted);margin-bottom:8px}
.form-group select,.form-group input{width:100%;background:var(--surface);border:1px solid var(--border2);color:var(--text);padding:14px 16px;font-family:'DM Sans',sans-serif;font-size:15px;border-radius:3px;outline:none;transition:border-color 0.2s;appearance:none;-webkit-appearance:none}
.form-group select:focus,.form-group input:focus{border-color:var(--accent)}
.form-group select option{background:var(--bg3)}
.form-row{display:grid;grid-template-columns:1fr 1fr;gap:20px}
.calc-btn{width:100%;padding:18px;background:var(--accent);color:#fff;font-family:'Syne',sans-serif;font-size:14px;font-weight:700;letter-spacing:0.08em;text-transform:uppercase;border:none;border-radius:3px;cursor:pointer;transition:background 0.2s,transform 0.15s}
.calc-btn:hover{background:var(--accent2);transform:translateY(-1px)}
#quoteResult{display:none;margin-top:32px;padding-top:32px;border-top:1px solid var(--border);text-align:center}
.result-label{font-size:11px;letter-spacing:0.1em;text-transform:uppercase;color:var(--muted);margin-bottom:8px}
.result-price{font-family:'Syne',sans-serif;font-size:72px;font-weight:800;color:var(--text);line-height:1}
.result-price sup{font-size:32px;vertical-align:top;margin-top:12px;display:inline-block}
.result-note{font-size:13px;color:var(--muted);margin-top:12px}
.quote-info{padding-top:8px}
.quote-promise{display:flex;align-items:flex-start;gap:16px;margin-bottom:32px;padding-bottom:32px;border-bottom:1px solid var(--border)}
.quote-promise:last-of-type{border:none;margin:0;padding:0}
.promise-icon{width:36px;height:36px;flex-shrink:0;border:1px solid var(--border2);border-radius:6px;display:flex;align-items:center;justify-content:center}
.promise-title{font-family:'Syne',sans-serif;font-weight:700;font-size:15px;margin-bottom:4px;color:var(--text)}
.promise-desc{font-size:13px;color:var(--muted2)}
.cta-banner{margin:120px 48px;padding:80px;background:var(--accent);position:relative;overflow:hidden}
.cta-banner::before{content:'';position:absolute;inset:0;background:repeating-linear-gradient(90deg,rgba(255,255,255,0.04) 0px,rgba(255,255,255,0.04) 1px,transparent 1px,transparent 60px)}
.cta-inner{position:relative;display:flex;justify-content:space-between;align-items:center;gap:40px;flex-wrap:wrap}
.cta-banner h2{font-family:'Syne',sans-serif;font-size:clamp(32px,4vw,56px);font-weight:800;letter-spacing:-0.02em;color:#fff;line-height:1.05}
.cta-banner h2 em{font-style:normal;opacity:0.65}
.btn-white{display:inline-flex;align-items:center;gap:12px;padding:18px 40px;background:#fff;color:var(--accent);font-family:'Syne',sans-serif;font-size:14px;font-weight:700;letter-spacing:0.06em;text-transform:uppercase;text-decoration:none;border-radius:3px;white-space:nowrap;transition:transform 0.2s;flex-shrink:0}
.btn-white:hover{transform:translateY(-2px)}
footer{padding:80px 48px 40px;background:var(--bg);border-top:1px solid var(--border)}
.footer-top{display:grid;grid-template-columns:2fr 1fr 1fr 1fr;gap:64px;margin-bottom:64px}
.footer-tagline{font-size:14px;color:var(--muted2);margin-top:16px;max-width:240px;line-height:1.7}
.footer-heading{font-family:'Syne',sans-serif;font-size:12px;letter-spacing:0.1em;text-transform:uppercase;color:var(--muted);margin-bottom:20px}
.footer-links{list-style:none}
.footer-links li{margin-bottom:12px}
.footer-links a{font-size:14px;color:var(--muted2);text-decoration:none;transition:color 0.2s}
.footer-links a:hover{color:var(--text)}
.footer-bottom{display:flex;justify-content:space-between;align-items:center;flex-wrap:wrap;gap:16px;padding-top:32px;border-top:1px solid var(--border)}
.footer-bottom p{font-size:12px;color:var(--muted);letter-spacing:0.04em}
.social-links{display:flex;gap:24px}
.social-links a{font-size:12px;letter-spacing:0.08em;text-transform:uppercase;color:var(--muted);text-decoration:none;transition:color 0.2s}
.social-links a:hover{color:var(--accent)}
.fade-up{opacity:0;transform:translateY(24px);transition:opacity 0.65s ease,transform 0.65s ease}
.fade-up.visible{opacity:1;transform:none}
@media(max-width:1100px){
  nav{padding:20px 24px}
  header{padding:100px 24px 48px}
  .hero-visual{display:none}
  .services-section,.process-section,.quote-section,.materials-section{padding:80px 24px}
  .services-grid,.process-steps,.materials-grid,.footer-top{grid-template-columns:1fr 1fr}
  .service-card:nth-child(2){border-right:none}
  .step:nth-child(2) .step-arrow,.step:nth-child(4) .step-arrow{display:none}
  .quote-inner{grid-template-columns:1fr;gap:48px}
  .cta-banner{margin:80px 24px;padding:48px}
  footer{padding:60px 24px 32px}
}
@media(max-width:640px){
  nav{padding:16px 20px}
  .nav-links{display:none}
  .hamburger{display:block}
  #mobileMenu{padding:20px}
  header{padding:90px 20px 36px}
  .hero-title{font-size:44px}
  .hero-bottom{flex-direction:column;align-items:flex-start}
  .hero-actions{align-items:flex-start}
  .hero-stats{flex-direction:column;gap:20px}
  .services-grid,.process-steps,.materials-grid{grid-template-columns:1fr}
  .service-card,.step,.mat-card{border-right:none}
  .form-row{grid-template-columns:1fr}
  .footer-top{grid-template-columns:1fr 1fr;gap:32px}
  .cta-banner{margin:60px 20px;padding:36px}
}
</style>
</head>
<body>

<div id="scrollProgress"></div>

<nav>
  <a href="#" class="logo">
    <div class="logo-mark"></div>
    ZAXIS STUDIO
  </a>
  <div class="nav-links">
    <a href="#services">Services</a>
    <a href="#materials">Materials</a>
    <a href="#process">Process</a>
    <a href="#quote">Quote</a>
  </div>
  <a href="#quote" class="nav-cta">Start a Project</a>
  <button class="hamburger" onclick="toggleMenu()" aria-label="Toggle menu">
    <svg width="22" height="22" viewBox="0 0 22 22" fill="none" stroke="currentColor" stroke-width="1.5" stroke-linecap="round">
      <line x1="3" y1="6" x2="19" y2="6"/><line x1="3" y1="11" x2="19" y2="11"/><line x1="3" y1="16" x2="19" y2="16"/>
    </svg>
  </button>
  <div id="mobileMenu">
    <a href="#services" onclick="toggleMenu()">Services</a>
    <a href="#materials" onclick="toggleMenu()">Materials</a>
    <a href="#process" onclick="toggleMenu()">Process</a>
    <a href="#quote" onclick="toggleMenu()">Quote</a>
    <a href="#quote" onclick="toggleMenu()">Start a Project →</a>
  </div>
</nav>

<header id="home">
  <div class="hero-visual" aria-hidden="true">
    <div style="position:relative;width:100%;height:100%">
      <div class="print-cube">
        <div class="cube-face cube-front"></div>
        <div class="cube-face cube-back"></div>
        <div class="cube-face cube-left"></div>
        <div class="cube-face cube-right"></div>
        <div class="cube-face cube-top"></div>
        <div class="cube-face cube-bottom"></div>
      </div>
      <div class="print-head"></div>
      <div class="badge-live">Live — printing now</div>
    </div>
  </div>

  <div class="hero-label">
    <div class="hero-label-dot"></div>
    On-demand 3D printing studio &nbsp;·&nbsp; San Diego, CA &nbsp;·&nbsp; Ships worldwide
  </div>

  <h1 class="hero-title">Your ideas,<br><em>printed</em><br>perfectly.</h1>

  <div class="hero-bottom">
    <p class="hero-desc">High-precision 3D printing for prototypes, functional parts, and artistic pieces. FDM · SLA · SLS · Carbon Fiber. Ready in record time.</p>
    <div class="hero-stats">
      <div class="stat-item"><div class="stat-num">1,284</div><div class="stat-label">Projects shipped</div></div>
      <div class="stat-item"><div class="stat-num">4.98</div><div class="stat-label">Average rating</div></div>
      <div class="stat-item"><div class="stat-num">48h</div><div class="stat-label">Avg. turnaround</div></div>
    </div>
    <div class="hero-actions">
      <a href="#quote" class="btn-primary">
        Start your project
        <svg width="16" height="16" viewBox="0 0 16 16" fill="none" stroke="currentColor" stroke-width="1.5"><line x1="2" y1="8" x2="14" y2="8"/><polyline points="9,3 14,8 9,13"/></svg>
      </a>
      <a href="#process" class="btn-ghost">
        How it works
        <svg width="12" height="12" viewBox="0 0 12 12" fill="none" stroke="currentColor" stroke-width="1.5"><polyline points="3,2 9,6 3,10"/></svg>
      </a>
    </div>
  </div>
</header>

<div class="marquee-strip" aria-hidden="true">
  <div class="marquee-inner">
    <span>Rapid Prototyping</span><span>FDM Printing</span><span>Resin SLA</span><span>Carbon Fiber</span><span>48-Hour Turnaround</span><span>Engineering Parts</span><span>Artistic Prints</span><span>Ships Worldwide</span><span>Tesla · NASA · IDEO</span><span>Free Design Review</span>
    <span>Rapid Prototyping</span><span>FDM Printing</span><span>Resin SLA</span><span>Carbon Fiber</span><span>48-Hour Turnaround</span><span>Engineering Parts</span><span>Artistic Prints</span><span>Ships Worldwide</span><span>Tesla · NASA · IDEO</span><span>Free Design Review</span>
  </div>
</div>

<section id="services" class="services-section">
  <div class="services-header fade-up">
    <div>
      <span class="section-label">Capabilities</span>
      <h2 class="section-title">What we print</h2>
    </div>
    <a href="#quote" style="font-size:13px;letter-spacing:0.06em;text-transform:uppercase;color:var(--muted);text-decoration:none;display:inline-flex;align-items:center;gap:8px;transition:color 0.2s" onmouseover="this.style.color='var(--text)'" onmouseout="this.style.color='var(--muted)'">Get a quote <svg width="14" height="14" viewBox="0 0 14 14" fill="none" stroke="currentColor" stroke-width="1.5"><line x1="2" y1="7" x2="12" y2="7"/><polyline points="7,2 12,7 7,12"/></svg></a>
  </div>
  <div class="services-grid fade-up">
    <div class="service-card">
      <div class="service-icon"><svg width="20" height="20" viewBox="0 0 20 20" fill="none" stroke="var(--accent)" stroke-width="1.5"><rect x="3" y="3" width="14" height="14" rx="1"/><line x1="3" y1="8" x2="17" y2="8"/><line x1="3" y1="13" x2="17" y2="13"/></svg></div>
      <div class="service-num">01</div>
      <div class="service-name">Rapid Prototyping</div>
      <p class="service-desc">From concept to functional part in under 48 hours. FDM, SLA, and SLS for any geometry and complexity level.</p>
      <div class="service-price">From $29 per part</div>
    </div>
    <div class="service-card">
      <div class="service-icon"><svg width="20" height="20" viewBox="0 0 20 20" fill="none" stroke="var(--accent)" stroke-width="1.5"><polygon points="10,2 18,7 18,13 10,18 2,13 2,7"/><line x1="10" y1="2" x2="10" y2="18"/><line x1="2" y1="7" x2="18" y2="7"/><line x1="2" y1="13" x2="18" y2="13"/></svg></div>
      <div class="service-num">02</div>
      <div class="service-name">Engineering Parts</div>
      <p class="service-desc">Carbon fiber, PEEK, Nylon, and metal-infused filaments for structural, aerospace, and automotive applications.</p>
      <div class="service-price">From $89 per part</div>
    </div>
    <div class="service-card">
      <div class="service-icon"><svg width="20" height="20" viewBox="0 0 20 20" fill="none" stroke="var(--accent)" stroke-width="1.5"><circle cx="10" cy="10" r="7"/><path d="M10 3 C12 5 15 8 15 10 C15 12 12 15 10 17 C8 15 5 12 5 10 C5 8 8 5 10 3Z"/><line x1="3" y1="10" x2="17" y2="10"/></svg></div>
      <div class="service-num">03</div>
      <div class="service-name">Art &amp; Collectibles</div>
      <p class="service-desc">High-detail resin prints with full-color multi-jet and professional hand-painted or anodized finishes.</p>
      <div class="service-price">From $15 per piece</div>
    </div>
  </div>
</section>

<section id="materials" class="materials-section">
  <div class="materials-header fade-up">
    <div>
      <span class="section-label">Materials</span>
      <h2 class="section-title">Chosen for performance</h2>
    </div>
    <p style="font-size:14px;color:var(--muted2);max-width:280px;line-height:1.7">12 materials in stock. Free sample kit for qualifying orders.</p>
  </div>
  <div class="materials-grid fade-up">
    <div class="mat-card">
      <div class="mat-swatch" style="background:#E8E0D0"></div>
      <div class="mat-name">PLA+</div>
      <p class="mat-note">Best for models, display parts, early prototypes.</p>
      <div class="mat-props"><span class="mat-tag">Biodegradable</span><span class="mat-tag">24 colors</span><span class="mat-tag">From $29</span></div>
    </div>
    <div class="mat-card">
      <div class="mat-swatch" style="background:#C4D4E0"></div>
      <div class="mat-name">PETG</div>
      <p class="mat-note">Best for functional parts, food-safe containers.</p>
      <div class="mat-props"><span class="mat-tag">Impact resistant</span><span class="mat-tag">Clear option</span><span class="mat-tag">From $49</span></div>
    </div>
    <div class="mat-card">
      <div class="mat-swatch" style="background:#2E2C29"></div>
      <div class="mat-name">Carbon Fiber Nylon</div>
      <p class="mat-note">Best for structural brackets, aerospace, motorsport.</p>
      <div class="mat-props"><span class="mat-tag">High stiffness</span><span class="mat-tag">Lightweight</span><span class="mat-tag">From $89</span></div>
    </div>
    <div class="mat-card">
      <div class="mat-swatch" style="background:#F0C080"></div>
      <div class="mat-name">Resin (SLA)</div>
      <p class="mat-note">Best for jewelry, miniatures, dental models.</p>
      <div class="mat-props"><span class="mat-tag">25µm layers</span><span class="mat-tag">Ultra-fine</span><span class="mat-tag">From $59</span></div>
    </div>
  </div>
</section>

<section id="process" class="process-section">
  <div class="fade-up" style="max-width:600px;margin-bottom:0">
    <span class="section-label">How it works</span>
    <h2 class="section-title">Four steps from file to doorstep</h2>
  </div>
  <div class="process-steps fade-up">
    <div class="step">
      <div class="step-number">01</div>
      <div class="step-title">Upload your file</div>
      <p class="step-desc">Drop your STL, OBJ, or STEP file. Our system auto-checks for printability and flags issues instantly.</p>
      <div class="step-arrow"><svg width="10" height="10" viewBox="0 0 10 10" fill="none" stroke="var(--muted)" stroke-width="1.5"><polyline points="3,2 7,5 3,8"/></svg></div>
    </div>
    <div class="step">
      <div class="step-number">02</div>
      <div class="step-title">Choose material</div>
      <p class="step-desc">Select from 12 materials and finishes. Our engineers review every order before printing begins.</p>
      <div class="step-arrow"><svg width="10" height="10" viewBox="0 0 10 10" fill="none" stroke="var(--muted)" stroke-width="1.5"><polyline points="3,2 7,5 3,8"/></svg></div>
    </div>
    <div class="step">
      <div class="step-number">03</div>
      <div class="step-title">We print &amp; inspect</div>
      <p class="step-desc">Precision-calibrated machines with layer-by-layer quality monitoring. Every part is dimensionally verified.</p>
      <div class="step-arrow"><svg width="10" height="10" viewBox="0 0 10 10" fill="none" stroke="var(--muted)" stroke-width="1.5"><polyline points="3,2 7,5 3,8"/></svg></div>
    </div>
    <div class="step">
      <div class="step-number">04</div>
      <div class="step-title">Ships to you</div>
      <p class="step-desc">Packed and shipped within 48 hours. Track your order in real-time with our live dashboard.</p>
    </div>
  </div>
</section>

<section id="quote" class="quote-section">
  <div class="quote-inner">
    <div class="quote-form fade-up">
      <span class="section-label">Instant estimate</span>
      <h2 style="font-family:'Syne',sans-serif;font-size:32px;font-weight:700;letter-spacing:-0.02em;margin-bottom:36px;color:var(--text)">Get your price<br>in seconds</h2>
      <div class="form-group">
        <label>Material</label>
        <select id="material">
          <option value="50">PLA+ — entry grade</option>
          <option value="80">PETG — functional grade</option>
          <option value="130">Carbon Fiber Nylon — structural</option>
          <option value="200">Resin SLA — ultra-fine detail</option>
          <option value="340">PEEK — aerospace grade</option>
        </select>
      </div>
      <div class="form-row">
        <div class="form-group"><label>Volume (cm³)</label><input id="volume" type="number" value="120" min="1" step="1"></div>
        <div class="form-group"><label>Quantity</label><input id="quantity" type="number" value="1" min="1" step="1"></div>
      </div>
      <div class="form-group">
        <label>Finish</label>
        <select id="finish">
          <option value="1.0">As-printed</option>
          <option value="1.18">Sanded smooth</option>
          <option value="1.35">Painted / custom color</option>
        </select>
      </div>
      <button class="calc-btn" onclick="calculateQuote()">Calculate estimate</button>
      <div id="quoteResult">
        <div class="result-label">Estimated total</div>
        <div class="result-price"><sup>$</sup><span id="priceDisplay">—</span></div>
        <div class="result-note" id="resultNote"></div>
        <a href="mailto:hello@zaxis-studio.com" class="btn-primary" style="margin-top:24px;display:inline-flex;justify-content:center;width:100%">
          Request exact quote
          <svg width="16" height="16" viewBox="0 0 16 16" fill="none" stroke="currentColor" stroke-width="1.5"><line x1="2" y1="8" x2="14" y2="8"/><polyline points="9,3 14,8 9,13"/></svg>
        </a>
      </div>
    </div>
    <div class="quote-info fade-up">
      <div class="quote-promise">
        <div class="promise-icon"><svg width="18" height="18" viewBox="0 0 18 18" fill="none" stroke="var(--accent)" stroke-width="1.5"><polyline points="2,9 7,14 16,4"/></svg></div>
        <div><div class="promise-title">Free design review</div><p class="promise-desc">Our engineers check every file for printability before charging you a cent.</p></div>
      </div>
      <div class="quote-promise">
        <div class="promise-icon"><svg width="18" height="18" viewBox="0 0 18 18" fill="none" stroke="var(--accent)" stroke-width="1.5"><circle cx="9" cy="9" r="7"/><polyline points="9,5 9,9 12,11"/></svg></div>
        <div><div class="promise-title">48-hour turnaround</div><p class="promise-desc">Most orders ship within two business days. Rush options available for urgent projects.</p></div>
      </div>
      <div class="quote-promise">
        <div class="promise-icon"><svg width="18" height="18" viewBox="0 0 18 18" fill="none" stroke="var(--accent)" stroke-width="1.5"><path d="M9 2L11 7H16L12 10L14 15L9 12L4 15L6 10L2 7H7Z"/></svg></div>
        <div><div class="promise-title">Quality guarantee</div><p class="promise-desc">Not happy with your print? We reprint or refund. No questions asked, no hassle.</p></div>
      </div>
      <div style="margin-top:48px;padding:28px;background:var(--bg3);border:1px solid var(--border)">
        <p style="font-size:12px;color:var(--muted);letter-spacing:0.08em;text-transform:uppercase;margin-bottom:12px">Trusted by</p>
        <p style="font-family:'Syne',sans-serif;font-size:14px;color:var(--muted2);line-height:2.2;letter-spacing:0.04em">Tesla &nbsp;·&nbsp; NASA JPL &nbsp;·&nbsp; IDEO &nbsp;·&nbsp; Intuitive Surgical &nbsp;·&nbsp; General Atomics</p>
      </div>
    </div>
  </div>
</section>

<div class="cta-banner fade-up" style="position:relative;z-index:1">
  <div class="cta-inner">
    <h2>Ready to bring<br><em>your idea</em> to life?</h2>
    <a href="mailto:hello@zaxis-studio.com" class="btn-white">
      Email us your file
      <svg width="16" height="16" viewBox="0 0 16 16" fill="none" stroke="currentColor" stroke-width="1.5"><line x1="2" y1="8" x2="14" y2="8"/><polyline points="9,3 14,8 9,13"/></svg>
    </a>
  </div>
</div>

<footer>
  <div class="footer-top">
    <div>
      <a href="#" class="logo" style="display:inline-flex"><div class="logo-mark"></div>ZAXIS STUDIO</a>
      <p class="footer-tagline">Premium on-demand 3D printing. San Diego · Los Angeles · Worldwide shipping.</p>
      <p style="font-size:13px;color:var(--muted);margin-top:24px;line-height:1.8">hello@zaxis-studio.com<br>(858) 555-0147</p>
    </div>
    <div>
      <p class="footer-heading">Company</p>
      <ul class="footer-links"><li><a href="#">About us</a></li><li><a href="#">Careers</a></li><li><a href="#">Sustainability</a></li><li><a href="#">Press kit</a></li></ul>
    </div>
    <div>
      <p class="footer-heading">Resources</p>
      <ul class="footer-links"><li><a href="#">3D Printing 101</a></li><li><a href="#">Material guide</a></li><li><a href="#">File prep tips</a></li><li><a href="#">Blog</a></li></ul>
    </div>
    <div>
      <p class="footer-heading">Services</p>
      <ul class="footer-links"><li><a href="#">Rapid prototyping</a></li><li><a href="#">Engineering parts</a></li><li><a href="#">Art &amp; collectibles</a></li><li><a href="#">Bulk orders</a></li></ul>
    </div>
  </div>
  <div class="footer-bottom">
    <p>© 2026 ZAxis Studio. All rights reserved.</p>
    <div class="social-links"><a href="#">Twitter / X</a><a href="#">Instagram</a><a href="#">LinkedIn</a></div>
  </div>
</footer>

<script>
function toggleMenu(){
  var m=document.getElementById('mobileMenu');
  m.style.display=m.style.display==='block'?'none':'block';
}
function calculateQuote(){
  var base=parseFloat(document.getElementById('material').value);
  var vol=Math.max(1,parseFloat(document.getElementById('volume').value)||120);
  var qty=Math.max(1,parseFloat(document.getElementById('quantity').value)||1);
  var finish=parseFloat(document.getElementById('finish').value);
  var unitPrice=base*(vol/100)*finish;
  var total=Math.round(unitPrice*qty);
  document.getElementById('priceDisplay').textContent=total.toLocaleString();
  var note=qty>1?('$'+Math.round(unitPrice)+' per part · '+qty+' parts · includes free design review'):'Includes free design review · ships within 48h';
  document.getElementById('resultNote').textContent=note;
  var r=document.getElementById('quoteResult');
  r.style.display='block';
  r.style.opacity='0';r.style.transform='translateY(8px)';
  r.style.transition='opacity 0.4s,transform 0.4s';
  setTimeout(function(){r.style.opacity='1';r.style.transform='none'},10);
}
window.addEventListener('scroll',function(){
  var s=document.documentElement.scrollTop;
  var h=document.documentElement.scrollHeight-document.documentElement.clientHeight;
  document.getElementById('scrollProgress').style.width=(s/h*100)+'%';
});
var observer=new IntersectionObserver(function(entries){
  entries.forEach(function(e){if(e.isIntersecting)e.target.classList.add('visible')});
},{threshold:0.1});
document.querySelectorAll('.fade-up').forEach(function(el){observer.observe(el)});
</script>
</body>
</html>
