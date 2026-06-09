<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta name="description" content="FiestaMágica – Organizamos cumpleaños y fiestas infantiles temáticas únicas en Buenos Aires. Decoración, animación, candy bar y fotografía profesional. ¡Tu peque lo merece!">
  <meta name="keywords" content="fiestas infantiles, cumpleaños temáticos, animación infantil, organización eventos niños, decoración cumpleaños, Buenos Aires">
  <meta property="og:title" content="FiestaMágica | Fiestas Infantiles Únicas 🎉">
  <meta property="og:description" content="Hacemos realidad el cumpleaños que tu hijo siempre soñó.">
  <meta property="og:type" content="website">
  <title>FiestaMágica | Fiestas y Cumpleaños Infantiles 🎉</title>

  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Fredoka+One&family=Nunito:wght@400;600;700;800;900&display=swap" rel="stylesheet">

  <style>
    /* ══════════════════════════════════════
       TOKENS
    ══════════════════════════════════════ */
    :root {
      --coral:       #FF4785;
      --coral-dark:  #D93070;
      --coral-light: #FFE4EE;
      --yellow:      #FFD438;
      --yellow-dark: #F0B800;
      --yellow-light:#FFFCE8;
      --sky:         #38C9F0;
      --mint:        #3DD9A4;
      --purple:      #6B4EFF;
      --purple-dark: #2D1B69;
      --lavender:    #F0EBFF;
      --bg:          #FDFBFF;
      --text:        #1A1030;
      --muted:       #7264A3;
      --white:       #FFFFFF;
      --r-lg:        20px;
      --r-sm:        12px;
      --sh-sm:       0 4px 16px rgba(107,78,255,.10);
      --sh-md:       0 8px 32px rgba(107,78,255,.15);
      --sh-lg:       0 16px 48px rgba(107,78,255,.22);
      --ease:        cubic-bezier(.25,.46,.45,.94);
    }

    /* ══════════════════════════════════════
       RESET
    ══════════════════════════════════════ */
    *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }
    html  { scroll-behavior: smooth; }
    body  { font-family: 'Nunito', sans-serif; background: var(--bg); color: var(--text); line-height: 1.65; overflow-x: hidden; }
    img   { max-width: 100%; height: auto; display: block; }
    a     { text-decoration: none; color: inherit; }
    ul    { list-style: none; }
    button { cursor: pointer; }

    /* ══════════════════════════════════════
       TYPOGRAPHY
    ══════════════════════════════════════ */
    h1 { font-family: 'Fredoka One', cursive; font-size: clamp(2.4rem, 6vw, 4.4rem); line-height: 1.1; }
    h2 { font-family: 'Fredoka One', cursive; font-size: clamp(1.8rem, 4vw, 2.9rem); line-height: 1.15; }
    h3 { font-size: 1.25rem; font-weight: 800; }

    .section-label {
      display: inline-block;
      font-size: .72rem;
      font-weight: 800;
      letter-spacing: .15em;
      text-transform: uppercase;
      color: var(--coral);
      background: var(--coral-light);
      padding: 4px 14px;
      border-radius: 100px;
      margin-bottom: .9rem;
    }
    .section-head { text-align: center; margin-bottom: 3rem; }
    .section-head h2 { margin-bottom: .6rem; }
    .section-sub { color: var(--muted); font-size: 1.05rem; max-width: 540px; margin: 0 auto; }

    /* ══════════════════════════════════════
       LAYOUT
    ══════════════════════════════════════ */
    .container  { width: 100%; max-width: 1160px; margin: 0 auto; padding: 0 1.5rem; }
    .section-pad{ padding: 5rem 0; }

    /* ══════════════════════════════════════
       BUTTONS
    ══════════════════════════════════════ */
    .btn {
      display: inline-flex; align-items: center; gap: 8px;
      padding: .85rem 1.9rem; border-radius: 100px;
      font-family: 'Nunito', sans-serif; font-weight: 800; font-size: .98rem;
      border: none; transition: transform .25s var(--ease), box-shadow .25s var(--ease), background .2s;
      white-space: nowrap;
    }
    .btn-primary {
      background: var(--coral); color: var(--white);
      box-shadow: 0 4px 20px rgba(255,71,133,.38);
    }
    .btn-primary:hover  { background: var(--coral-dark); transform: translateY(-2px); box-shadow: 0 8px 28px rgba(255,71,133,.5); }
    .btn-primary:active { transform: translateY(0); }

    .btn-outline {
      background: transparent; color: var(--white);
      border: 2.5px solid rgba(255,255,255,.55);
    }
    .btn-outline:hover { background: rgba(255,255,255,.12); border-color: var(--white); }

    .btn-dark {
      background: var(--purple-dark); color: var(--white);
      box-shadow: 0 4px 20px rgba(45,27,105,.3);
    }
    .btn-dark:hover { background: #3c258c; transform: translateY(-2px); }

    .btn-wa {
      background: #25D366; color: var(--white);
      box-shadow: 0 4px 20px rgba(37,211,102,.38);
    }
    .btn-wa:hover { background: #1db854; transform: translateY(-2px); box-shadow: 0 8px 28px rgba(37,211,102,.5); }

    /* ══════════════════════════════════════
       NAVIGATION
    ══════════════════════════════════════ */
    .nav {
      position: fixed; top: 0; left: 0; right: 0; z-index: 1000;
      padding: 1.1rem 0;
      transition: background .3s, box-shadow .3s;
    }
    .nav.scrolled {
      background: rgba(255,255,255,.94);
      backdrop-filter: blur(14px);
      box-shadow: 0 2px 20px rgba(107,78,255,.1);
    }
    .nav__inner { display: flex; align-items: center; justify-content: space-between; }

    .nav__logo { font-family: 'Fredoka One', cursive; font-size: 1.55rem; color: var(--white); transition: color .3s; }
    .nav__logo span { color: var(--yellow); }
    .nav.scrolled .nav__logo { color: var(--purple-dark); }
    .nav.scrolled .nav__logo span { color: var(--coral); }

    .nav__links { display: flex; align-items: center; gap: 1.8rem; }
    .nav__links a { font-weight: 700; font-size: .93rem; color: rgba(255,255,255,.8); transition: color .2s; }
    .nav__links a:hover { color: var(--white); }
    .nav.scrolled .nav__links a { color: var(--muted); }
    .nav.scrolled .nav__links a:hover { color: var(--purple-dark); }

    .nav__cta {
      background: var(--yellow); color: var(--purple-dark) !important;
      padding: .5rem 1.3rem; border-radius: 100px; font-weight: 900 !important;
    }
    .nav__cta:hover { box-shadow: 0 4px 16px rgba(255,212,56,.5); transform: translateY(-1px); }

    .nav__burger { display: none; flex-direction: column; gap: 5px; background: none; border: none; padding: 4px; }
    .nav__burger span { display: block; width: 26px; height: 2.5px; background: var(--white); border-radius: 4px; transition: transform .3s, opacity .3s; }
    .nav.scrolled .nav__burger span { background: var(--purple-dark); }
    .nav__burger.open span:nth-child(1) { transform: rotate(45deg) translate(5px,5px); }
    .nav__burger.open span:nth-child(2) { opacity: 0; }
    .nav__burger.open span:nth-child(3) { transform: rotate(-45deg) translate(5px,-5px); }

    .nav__mobile {
      display: none; position: fixed; inset: 0; z-index: 999;
      background: var(--purple-dark);
      flex-direction: column; align-items: center; justify-content: center; gap: 2rem;
    }
    .nav__mobile.open { display: flex; }
    .nav__mobile a { font-family: 'Fredoka One', cursive; font-size: 2.1rem; color: var(--white); }
    .nav__mobile a:hover { color: var(--yellow); }

    /* ══════════════════════════════════════
       HERO
    ══════════════════════════════════════ */
    .hero {
      position: relative; min-height: 100vh;
      display: flex; align-items: center;
      background: linear-gradient(135deg, var(--purple-dark) 0%, #4730B0 55%, #8840C5 100%);
      overflow: hidden; padding-top: 80px;
    }

    /* — Confetti (CSS only, signature element) — */
    .confetti-wrap { position: absolute; inset: 0; pointer-events: none; overflow: hidden; }
    .c { position: absolute; border-radius: 3px; opacity: 0; animation: cFall linear infinite; }
    .c:nth-child(odd)  { border-radius: 50%; }

    .c:nth-child(1)  { left:4%;   width:8px;  height:14px; background:var(--coral);  animation-duration:4.2s; animation-delay:0s; }
    .c:nth-child(2)  { left:10%;  width:10px; height:10px; background:var(--yellow); animation-duration:5.1s; animation-delay:.6s; }
    .c:nth-child(3)  { left:17%;  width:6px;  height:14px; background:var(--sky);    animation-duration:3.7s; animation-delay:1.1s; }
    .c:nth-child(4)  { left:24%;  width:10px; height:10px; background:var(--mint);   animation-duration:5.6s; animation-delay:.2s; }
    .c:nth-child(5)  { left:32%;  width:12px; height:8px;  background:var(--coral);  animation-duration:4.5s; animation-delay:1.6s; }
    .c:nth-child(6)  { left:41%;  width:8px;  height:8px;  background:var(--yellow); animation-duration:3.9s; animation-delay:.9s; }
    .c:nth-child(7)  { left:49%;  width:10px; height:12px; background:var(--sky);    animation-duration:5.3s; animation-delay:.3s; }
    .c:nth-child(8)  { left:57%;  width:14px; height:6px;  background:var(--mint);   animation-duration:4.8s; animation-delay:1.4s; }
    .c:nth-child(9)  { left:64%;  width:9px;  height:9px;  background:var(--coral);  animation-duration:3.4s; animation-delay:.7s; }
    .c:nth-child(10) { left:71%;  width:6px;  height:12px; background:var(--yellow); animation-duration:5.8s; animation-delay:0s; }
    .c:nth-child(11) { left:78%;  width:10px; height:10px; background:var(--sky);    animation-duration:4.1s; animation-delay:2.0s; }
    .c:nth-child(12) { left:85%;  width:8px;  height:8px;  background:var(--mint);   animation-duration:5.0s; animation-delay:.5s; }
    .c:nth-child(13) { left:91%;  width:12px; height:8px;  background:var(--coral);  animation-duration:3.6s; animation-delay:1.3s; }
    .c:nth-child(14) { left:96%;  width:8px;  height:14px; background:var(--yellow); animation-duration:4.9s; animation-delay:1.8s; }
    .c:nth-child(15) { left:7%;   width:9px;  height:9px;  background:var(--mint);   animation-duration:5.5s; animation-delay:2.3s; }
    .c:nth-child(16) { left:36%;  width:7px;  height:11px; background:var(--sky);    animation-duration:4.3s; animation-delay:.4s; }
    .c:nth-child(17) { left:53%;  width:11px; height:7px;  background:var(--coral);  animation-duration:3.8s; animation-delay:1.0s; }
    .c:nth-child(18) { left:68%;  width:8px;  height:13px; background:var(--yellow); animation-duration:5.2s; animation-delay:.8s; }
    .c:nth-child(19) { left:82%;  width:10px; height:10px; background:var(--mint);   animation-duration:4.6s; animation-delay:1.7s; }
    .c:nth-child(20) { left:45%;  width:7px;  height:7px;  background:var(--sky);    animation-duration:3.5s; animation-delay:2.1s; }

    @keyframes cFall {
      0%   { transform: translateY(-30px) rotate(0deg);    opacity: 0;   }
      8%   { opacity: 1; }
      92%  { opacity: .7; }
      100% { transform: translateY(108vh)  rotate(740deg); opacity: 0;   }
    }

    /* — Ambient bubbles — */
    .hero-bg-blob {
      position: absolute; border-radius: 50%; opacity: .07;
      animation: blobFloat ease-in-out infinite alternate;
    }
    .hero-bg-blob:nth-child(1) { width:420px; height:420px; background:var(--sky);   top:-120px; right:-100px; animation-duration:9s; }
    .hero-bg-blob:nth-child(2) { width:260px; height:260px; background:var(--coral); bottom:-60px; left:-80px;  animation-duration:7s; }
    .hero-bg-blob:nth-child(3) { width:190px; height:190px; background:var(--yellow);top:42%; left:32%;         animation-duration:11s; }
    @keyframes blobFloat {
      from { transform: translateY(0) scale(1); }
      to   { transform: translateY(-28px) scale(1.06); }
    }

    .hero__content { position: relative; z-index: 2; max-width: 680px; }

    .hero__eyebrow {
      display: inline-flex; align-items: center; gap: 8px;
      background: rgba(255,255,255,.12); border: 1px solid rgba(255,255,255,.2);
      color: var(--yellow); font-size: .82rem; font-weight: 800;
      letter-spacing: .1em; text-transform: uppercase;
      padding: 6px 16px; border-radius: 100px; margin-bottom: 1.4rem;
    }

    .hero__title { color: var(--white); margin-bottom: 1.1rem; }
    .hero__title .accent {
      background: linear-gradient(125deg, var(--yellow), var(--coral));
      -webkit-background-clip: text; -webkit-text-fill-color: transparent;
      background-clip: text;
    }

    .hero__sub { color: rgba(255,255,255,.72); font-size: 1.12rem; margin-bottom: 2.4rem; max-width: 500px; }

    .hero__ctas { display: flex; flex-wrap: wrap; gap: 1rem; align-items: center; }

    .hero__scroll {
      position: absolute; bottom: 2rem; left: 50%; transform: translateX(-50%);
      color: rgba(255,255,255,.38); font-size: .72rem; font-weight: 700;
      letter-spacing: .1em; text-transform: uppercase;
      display: flex; flex-direction: column; align-items: center; gap: 6px;
      animation: scrollBounce 2s ease-in-out infinite;
    }
    @keyframes scrollBounce {
      0%,100% { transform: translateX(-50%) translateY(0); }
      50%      { transform: translateX(-50%) translateY(7px); }
    }

    /* ══════════════════════════════════════
       WAVE DIVIDERS
    ══════════════════════════════════════ */
    .wave { display: block; width: 100%; overflow: hidden; line-height: 0; margin-top: -1px; }
    .wave svg { display: block; width: 100%; }

    /* ══════════════════════════════════════
       STATS
    ══════════════════════════════════════ */
    .stats { background: var(--white); padding: 3.5rem 0; }
    .stats__grid {
      display: grid; grid-template-columns: repeat(4,1fr); gap: 2rem; text-align: center;
    }
    .stats__num {
      font-family: 'Fredoka One', cursive; font-size: 2.8rem;
      color: var(--purple); line-height: 1; margin-bottom: .2rem;
    }
    .stats__lbl { font-size: .88rem; font-weight: 700; color: var(--muted); }

    /* ══════════════════════════════════════
       SERVICES
    ══════════════════════════════════════ */
    .services { background: var(--lavender); padding: 5rem 0; }
    .services__grid {
      display: grid; grid-template-columns: repeat(auto-fit, minmax(250px,1fr)); gap: 1.4rem;
    }
    .svc-card {
      background: var(--white); border-radius: var(--r-lg); padding: 2rem;
      box-shadow: var(--sh-sm); transition: transform .3s var(--ease), box-shadow .3s var(--ease);
    }
    .svc-card:hover { transform: translateY(-8px); box-shadow: var(--sh-lg); }

    .svc-icon {
      width: 64px; height: 64px; border-radius: 18px;
      display: flex; align-items: center; justify-content: center;
      font-size: 2rem; margin-bottom: 1.1rem;
    }
    .svc-card:nth-child(1) .svc-icon { background: var(--coral-light); }
    .svc-card:nth-child(2) .svc-icon { background: #E7F7FF; }
    .svc-card:nth-child(3) .svc-icon { background: var(--yellow-light); }
    .svc-card:nth-child(4) .svc-icon { background: #E5FDF5; }

    .svc-card h3 { color: var(--purple-dark); margin-bottom: .4rem; }
    .svc-desc    { color: var(--muted); font-size: .92rem; margin-bottom: 1.2rem; }

    .svc-list { display: flex; flex-direction: column; gap: .35rem; }
    .svc-list li {
      display: flex; align-items: flex-start; gap: 8px;
      font-size: .88rem; font-weight: 700; color: var(--text);
    }
    .svc-list li::before { content:'✓'; color: var(--mint); font-weight: 900; flex-shrink: 0; }

    .svc-badge {
      display: inline-block; margin-top: 1.4rem;
      background: var(--lavender); color: var(--purple);
      font-size: .78rem; font-weight: 800; padding: 4px 12px; border-radius: 100px;
    }

    /* ══════════════════════════════════════
       HOW IT WORKS
    ══════════════════════════════════════ */
    .how { background: var(--white); padding: 5rem 0; }
    .how__steps {
      display: grid; grid-template-columns: repeat(3,1fr); gap: 2rem; position: relative;
    }
    .how__steps::before {
      content:''; position: absolute;
      top: 40px; left: 17%; right: 17%;
      height: 2px;
      background: linear-gradient(90deg, var(--coral), var(--purple), var(--sky));
      border-radius: 4px;
    }
    .how__step { text-align: center; padding: .5rem 1rem; }
    .how__num {
      width: 80px; height: 80px; border-radius: 50%;
      background: linear-gradient(135deg, var(--coral), var(--purple));
      color: var(--white); font-family: 'Fredoka One', cursive; font-size: 2rem;
      display: flex; align-items: center; justify-content: center;
      margin: 0 auto 1.4rem; position: relative; z-index: 1;
      box-shadow: 0 6px 22px rgba(107,78,255,.3);
    }
    .how__step:nth-child(2) .how__num { background: linear-gradient(135deg,var(--purple),var(--sky)); }
    .how__step:nth-child(3) .how__num { background: linear-gradient(135deg,var(--sky),var(--mint)); }
    .how__step h3 { color: var(--purple-dark); margin-bottom: .4rem; }
    .how__step p  { color: var(--muted); font-size: .92rem; }

    /* ══════════════════════════════════════
       GALLERY
    ══════════════════════════════════════ */
    .gallery { background: var(--yellow-light); padding: 5rem 0; }
    .gallery__grid {
      display: grid;
      grid-template-columns: repeat(3,1fr);
      gap: 1rem;
    }
    .g-item { border-radius: var(--r-sm); overflow: hidden; aspect-ratio:1; position: relative; }
    .g-item:nth-child(1),
    .g-item:nth-child(4) { grid-column: span 2; aspect-ratio: 2/1; }

    .g-fill {
      width:100%; height:100%; min-height:200px;
      display: flex; flex-direction: column; align-items: center; justify-content: center;
      gap: .4rem; transition: transform .4s ease;
    }
    .g-item:hover .g-fill { transform: scale(1.04); }

    .g-item:nth-child(1) .g-fill { background: linear-gradient(135deg,#FF8CB8,#FF4785); }
    .g-item:nth-child(2) .g-fill { background: linear-gradient(135deg,#B89CFF,#6B4EFF); }
    .g-item:nth-child(3) .g-fill { background: linear-gradient(135deg,#7DDFF7,#38C9F0); }
    .g-item:nth-child(4) .g-fill { background: linear-gradient(135deg,#FFEA80,#FFD438); }
    .g-item:nth-child(5) .g-fill { background: linear-gradient(135deg,#7EE8C2,#3DD9A4); }
    .g-item:nth-child(6) .g-fill { background: linear-gradient(135deg,#FFAB9A,#FF6A50); }

    .g-emoji { font-size: 3rem; }
    .g-lbl   { font-family: 'Fredoka One', cursive; font-size: 1.2rem; color: rgba(255,255,255,.92); }

    .g-overlay {
      position: absolute; inset: 0;
      background: linear-gradient(to top, rgba(45,27,105,.72), transparent);
      opacity: 0; display: flex; align-items: flex-end; padding: 1rem;
      transition: opacity .3s;
    }
    .g-item:hover .g-overlay { opacity: 1; }
    .g-caption { color: var(--white); font-weight: 800; font-size: .88rem; }

    .gallery__cta { text-align: center; margin-top: 2.5rem; }

    /* ══════════════════════════════════════
       TESTIMONIALS
    ══════════════════════════════════════ */
    .testimonials { background: var(--white); padding: 5rem 0; }

    .testi-slider { overflow: hidden; }
    .testi-track  { display: flex; transition: transform .5s var(--ease); }
    .testi-slide  { min-width: 100%; padding: 0 1rem; }
    .testi-inner  {
      background: var(--lavender); border-radius: var(--r-lg);
      padding: 2.5rem; max-width: 680px; margin: 0 auto; text-align: center;
    }
    .testi-stars  { color: var(--yellow-dark); font-size: 1.4rem; letter-spacing: 2px; margin-bottom: .9rem; }
    .testi-text   { font-size: 1.1rem; font-style: italic; color: var(--text); margin-bottom: 1.4rem; line-height: 1.75; }
    .testi-author { display: flex; align-items: center; justify-content: center; gap: 12px; }
    .testi-avatar {
      width: 48px; height: 48px; border-radius: 50%;
      background: linear-gradient(135deg,var(--coral),var(--purple));
      display: flex; align-items: center; justify-content: center; font-size: 1.4rem;
    }
    .testi-name { font-weight: 800; color: var(--purple-dark); }
    .testi-role { font-size: .82rem; color: var(--muted); }

    .testi-dots { display: flex; justify-content: center; gap: 8px; margin-top: 1.8rem; }
    .testi-dot  {
      width: 10px; height: 10px; border-radius: 50%;
      background: rgba(107,78,255,.18); border: none;
      transition: background .3s, transform .3s;
    }
    .testi-dot.active { background: var(--purple); transform: scale(1.35); }

    /* ══════════════════════════════════════
       CTA BANNER
    ══════════════════════════════════════ */
    .cta-strip {
      background: linear-gradient(135deg,var(--coral),#C42868);
      padding: 4.5rem 0; text-align: center;
    }
    .cta-strip h2 { color: var(--white); margin-bottom: .8rem; }
    .cta-strip p  { color: rgba(255,255,255,.78); font-size: 1.08rem; margin-bottom: 2rem; }
    .cta-strip__btns { display: flex; justify-content: center; flex-wrap: wrap; gap: 1rem; }

    /* ══════════════════════════════════════
       CONTACT
    ══════════════════════════════════════ */
    .contact { background: var(--bg); padding: 5rem 0; }
    .contact__grid { display: grid; grid-template-columns: 1fr 1fr; gap: 3rem; align-items: start; }

    .contact__info { display: flex; flex-direction: column; gap: 1.4rem; }
    .c-item { display: flex; align-items: flex-start; gap: 1rem; }
    .c-icon {
      width: 48px; height: 48px; border-radius: 14px;
      background: var(--lavender);
      display: flex; align-items: center; justify-content: center;
      font-size: 1.3rem; flex-shrink: 0;
    }
    .c-item h4 { font-weight: 800; color: var(--purple-dark); margin-bottom: 2px; }
    .c-item p, .c-item a { color: var(--muted); font-size: .92rem; }
    .c-item a:hover { color: var(--coral); }

    .c-map {
      margin-top: 1rem; border-radius: var(--r-sm); overflow: hidden;
      height: 200px; background: var(--lavender);
      display: flex; align-items: center; justify-content: center;
      color: var(--muted); font-size: .9rem; font-weight: 600;
    }
    .c-map iframe { width: 100%; height: 100%; border: 0; }

    /* Form */
    .contact__form {
      background: var(--white); border-radius: var(--r-lg);
      padding: 2.5rem; box-shadow: var(--sh-md);
    }
    .contact__form h3 { font-size: 1.45rem; color: var(--purple-dark); margin-bottom: 1.4rem; }

    .fg { margin-bottom: 1.1rem; }
    .fg label { display: block; font-weight: 800; font-size: .88rem; color: var(--text); margin-bottom: .35rem; }
    .fg input, .fg select, .fg textarea {
      width: 100%; padding: .72rem 1rem;
      border: 2px solid rgba(107,78,255,.15); border-radius: var(--r-sm);
      font-family: 'Nunito', sans-serif; font-size: .97rem; color: var(--text);
      background: var(--bg); appearance: none;
      transition: border-color .2s, box-shadow .2s;
    }
    .fg input:focus, .fg select:focus, .fg textarea:focus {
      outline: none; border-color: var(--purple);
      box-shadow: 0 0 0 3px rgba(107,78,255,.1);
    }
    .fg textarea { resize: vertical; min-height: 96px; }
    .fg .err { font-size: .78rem; color: var(--coral); font-weight: 700; margin-top: 3px; display: none; }
    .fg.invalid input, .fg.invalid select, .fg.invalid textarea { border-color: var(--coral); }
    .fg.invalid .err { display: block; }

    .fg-row { display: grid; grid-template-columns: 1fr 1fr; gap: 1rem; }

    .form-success {
      display: none; text-align: center; padding: 2rem 1rem;
      color: var(--purple-dark);
    }
    .form-success.show { display: block; }
    .form-success .big { font-size: 3.5rem; margin-bottom: .6rem; }

    /* ══════════════════════════════════════
       FOOTER
    ══════════════════════════════════════ */
    .footer { background: var(--purple-dark); padding: 3.5rem 0 2rem; color: rgba(255,255,255,.65); }
    .footer__grid {
      display: grid; grid-template-columns: 2fr 1fr 1fr; gap: 3rem; margin-bottom: 2.5rem;
    }
    .footer__logo { font-family: 'Fredoka One', cursive; font-size: 1.55rem; color: var(--white); display: block; margin-bottom: .9rem; }
    .footer__logo span { color: var(--yellow); }
    .footer__brand p { font-size: .88rem; line-height: 1.75; max-width: 280px; }

    .footer__socials { display: flex; gap: .7rem; margin-top: 1.1rem; }
    .footer__soc {
      width: 40px; height: 40px; border-radius: 10px;
      background: rgba(255,255,255,.1);
      display: flex; align-items: center; justify-content: center; font-size: 1.1rem;
      transition: background .2s, transform .2s;
    }
    .footer__soc:hover { background: var(--coral); transform: translateY(-2px); }

    .footer__col h4 { font-family: 'Fredoka One', cursive; color: var(--white); font-size: 1.08rem; margin-bottom: .9rem; }
    .footer__col ul { display: flex; flex-direction: column; gap: .55rem; }
    .footer__col a  { font-size: .88rem; transition: color .2s; }
    .footer__col a:hover { color: var(--yellow); }

    .footer__bottom {
      border-top: 1px solid rgba(255,255,255,.1); padding-top: 1.4rem;
      display: flex; justify-content: space-between; align-items: center;
      font-size: .82rem; flex-wrap: wrap; gap: .5rem;
    }

    /* ══════════════════════════════════════
       WHATSAPP FLOAT
    ══════════════════════════════════════ */
    .wa-float { position: fixed; bottom: 2rem; right: 2rem; z-index: 2000; display: flex; flex-direction: column; align-items: flex-end; gap: 10px; }

    .wa-bubble {
      background: var(--white); border-radius: 12px;
      padding: 9px 14px; font-size: .82rem; font-weight: 700; color: var(--text);
      box-shadow: var(--sh-md); max-width: 200px; text-align: right;
      opacity: 0; transform: scale(.85) translateY(8px);
      transition: opacity .3s, transform .3s; pointer-events: none;
    }
    .wa-float:hover .wa-bubble { opacity: 1; transform: scale(1) translateY(0); pointer-events: auto; }

    .wa-btn {
      width: 62px; height: 62px; border-radius: 50%; background: #25D366;
      display: flex; align-items: center; justify-content: center;
      box-shadow: 0 4px 22px rgba(37,211,102,.5);
      transition: transform .2s, box-shadow .2s; position: relative;
    }
    .wa-btn:hover { transform: scale(1.1); box-shadow: 0 8px 32px rgba(37,211,102,.65); }
    .wa-btn::before {
      content: ''; position: absolute; inset: 0; border-radius: 50%;
      background: #25D366; animation: waPulse 2.2s ease-out infinite;
    }
    .wa-btn svg { position: relative; z-index: 1; }
    @keyframes waPulse {
      0%   { transform: scale(1);  opacity: .6; }
      100% { transform: scale(1.8);opacity: 0;  }
    }

    /* ══════════════════════════════════════
       SCROLL REVEAL
    ══════════════════════════════════════ */
    .reveal { opacity: 0; transform: translateY(28px); transition: opacity .6s ease, transform .6s ease; }
    .reveal.visible { opacity: 1; transform: none; }
    .reveal.d1 { transition-delay: .1s; }
    .reveal.d2 { transition-delay: .2s; }
    .reveal.d3 { transition-delay: .3s; }

    /* ══════════════════════════════════════
       RESPONSIVE
    ══════════════════════════════════════ */
    @media (max-width: 960px) {
      .nav__links  { display: none; }
      .nav__burger { display: flex; }
      .stats__grid { grid-template-columns: repeat(2,1fr); }
      .how__steps  { grid-template-columns: 1fr; }
      .how__steps::before { display: none; }
      .gallery__grid { grid-template-columns: repeat(2,1fr); }
      .g-item:nth-child(1),
      .g-item:nth-child(4) { grid-column: span 1; aspect-ratio: 1; }
      .contact__grid { grid-template-columns: 1fr; }
      .footer__grid  { grid-template-columns: 1fr 1fr; }
      .footer__brand { grid-column: span 2; }
    }
    @media (max-width: 600px) {
      .section-pad    { padding: 3.5rem 0; }
      .hero__ctas     { flex-direction: column; align-items: flex-start; }
      .services__grid { grid-template-columns: 1fr; }
      .gallery__grid  { grid-template-columns: 1fr; }
      .g-item:nth-child(1),
      .g-item:nth-child(4) { grid-column: span 1; aspect-ratio: 1; }
      .fg-row         { grid-template-columns: 1fr; }
      .footer__grid   { grid-template-columns: 1fr; }
      .footer__brand  { grid-column: span 1; }
      .footer__bottom { flex-direction: column; text-align: center; }
      .cta-strip__btns{ flex-direction: column; align-items: center; }
    }

    /* Reduced motion */
    @media (prefers-reduced-motion: reduce) {
      .c, .hero-bg-blob, .wa-btn::before { animation: none; }
      .reveal { opacity: 1; transform: none; }
    }
  </style>
</head>
<body>

  <!-- ═══════════ NAVIGATION ═══════════ -->
  <nav class="nav" id="nav" aria-label="Navegación principal">
    <div class="container">
      <div class="nav__inner">
        <a href="#inicio" class="nav__logo">Fiesta<span>Mágica</span> 🎉</a>

        <ul class="nav__links" role="list">
          <li><a href="#servicios">Servicios</a></li>
          <li><a href="#galeria">Galería</a></li>
          <li><a href="#testimonios">Testimonios</a></li>
          <li><a href="#contacto">Contacto</a></li>
          <li>
            <a href="https://wa.me/5491100000000?text=Hola!%20Quiero%20consultar%20sobre%20una%20fiesta%20%F0%9F%8E%89"
               target="_blank" rel="noopener noreferrer" class="nav__cta">
              ¡Cotizá ahora!
            </a>
          </li>
        </ul>

        <button class="nav__burger" id="burger" aria-label="Abrir menú" aria-expanded="false">
          <span></span><span></span><span></span>
        </button>
      </div>
    </div>
  </nav>

  <!-- Mobile overlay menu -->
  <nav class="nav__mobile" id="mobileMenu" aria-label="Menú móvil">
    <a href="#servicios"   class="mob-link">Servicios</a>
    <a href="#galeria"     class="mob-link">Galería</a>
    <a href="#testimonios" class="mob-link">Testimonios</a>
    <a href="#contacto"    class="mob-link">Contacto</a>
    <a href="https://wa.me/5491100000000?text=Hola!%20Quiero%20consultar%20sobre%20una%20fiesta%20%F0%9F%8E%89"
       target="_blank" rel="noopener noreferrer"
       class="btn btn-wa" style="margin-top:1rem">
      💬 Escribinos por WhatsApp
    </a>
  </nav>

  <!-- ═══════════ HERO ═══════════ -->
  <section id="inicio" class="hero">
    <!-- Confetti rain — signature element -->
    <div class="confetti-wrap" aria-hidden="true">
      <div class="c"></div><div class="c"></div><div class="c"></div><div class="c"></div>
      <div class="c"></div><div class="c"></div><div class="c"></div><div class="c"></div>
      <div class="c"></div><div class="c"></div><div class="c"></div><div class="c"></div>
      <div class="c"></div><div class="c"></div><div class="c"></div><div class="c"></div>
      <div class="c"></div><div class="c"></div><div class="c"></div><div class="c"></div>
    </div>

    <div class="hero-bg-blob" aria-hidden="true"></div>
    <div class="hero-bg-blob" aria-hidden="true"></div>
    <div class="hero-bg-blob" aria-hidden="true"></div>

    <div class="container">
      <div class="hero__content">
        <div class="hero__eyebrow">🎊 Especialistas en eventos infantiles</div>

        <h1 class="hero__title">
          La fiesta que tu hijo<br>
          siempre <span class="accent">soñó</span>
        </h1>

        <p class="hero__sub">
          Creamos celebraciones únicas y personalizadas: decoración, animación, candy bar y mucho más.
          ¡Hacemos que cada momento sea <strong style="color:rgba(255,255,255,.9)">mágico</strong>!
        </p>

        <div class="hero__ctas">
          <a href="https://wa.me/5491100000000?text=Hola!%20Quiero%20cotizar%20una%20fiesta%20infantil%20%F0%9F%8E%89"
             target="_blank" rel="noopener noreferrer" class="btn btn-primary">
            💬 Cotizá por WhatsApp
          </a>
          <a href="#servicios" class="btn btn-outline">Ver paquetes ↓</a>
        </div>
      </div>
    </div>

    <div class="hero__scroll" aria-hidden="true">
      <span>Explorá</span>
      <svg width="16" height="22" viewBox="0 0 16 22" fill="none" aria-hidden="true">
        <path d="M8 2v13M2 10l6 6 6-6" stroke="white" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
      </svg>
    </div>
  </section>

  <!-- Wave: hero → stats -->
  <div class="wave" style="background:linear-gradient(135deg,#2D1B69,#8840C5)">
    <svg viewBox="0 0 1440 64" preserveAspectRatio="none" xmlns="http://www.w3.org/2000/svg" style="height:64px">
      <path d="M0,32 C480,80 960,0 1440,32 L1440,64 L0,64 Z" fill="#ffffff"/>
    </svg>
  </div>

  <!-- ═══════════ STATS ═══════════ -->
  <section class="stats" aria-label="Nuestros números">
    <div class="container">
      <div class="stats__grid">
        <div class="reveal">
          <div class="stats__num">+500</div>
          <div class="stats__lbl">Eventos realizados</div>
        </div>
        <div class="reveal d1">
          <div class="stats__num">8</div>
          <div class="stats__lbl">Años de experiencia</div>
        </div>
        <div class="reveal d2">
          <div class="stats__num">98%</div>
          <div class="stats__lbl">Clientes satisfechos</div>
        </div>
        <div class="reveal d3">
          <div class="stats__num">+50</div>
          <div class="stats__lbl">Temáticas disponibles</div>
        </div>
      </div>
    </div>
  </section>

  <!-- Wave: stats → services -->
  <div class="wave" style="background:#ffffff">
    <svg viewBox="0 0 1440 64" preserveAspectRatio="none" xmlns="http://www.w3.org/2000/svg" style="height:64px">
      <path d="M0,20 C360,64 1080,0 1440,20 L1440,64 L0,64 Z" fill="#F0EBFF"/>
    </svg>
  </div>

  <!-- ═══════════ SERVICES ═══════════ -->
  <section id="servicios" class="services">
    <div class="container">
      <div class="section-head reveal">
        <span class="section-label">✨ Lo que hacemos</span>
        <h2>Paquetes para cada<br>celebración</h2>
        <p class="section-sub">Desde el cumpleaños más íntimo hasta la fiesta temática más elaborada, tenemos la propuesta perfecta para vos.</p>
      </div>

      <div class="services__grid">
        <!-- Card 1 -->
        <article class="svc-card reveal">
          <div class="svc-icon">🎂</div>
          <h3>Cumpleaños Clásico</h3>
          <p class="svc-desc">La opción perfecta para festejar en familia con todo el amor y sin complicaciones.</p>
          <ul class="svc-list">
            <li>Decoración completa del espacio</li>
            <li>Mesa de dulces y snacks</li>
            <li>Coordinación el día del evento</li>
            <li>Hasta 40 invitados</li>
          </ul>
          <span class="svc-badge">Desde $XX.XXX</span>
        </article>

        <!-- Card 2 -->
        <article class="svc-card reveal d1">
          <div class="svc-icon">🦄</div>
          <h3>Fiesta Temática</h3>
          <p class="svc-desc">¡Dale vida al personaje favorito de tu peque! Más de 50 temáticas disponibles.</p>
          <ul class="svc-list">
            <li>Ambientación 100% personalizada</li>
            <li>Disfraz para el cumpleañero/a</li>
            <li>Piñata y sorpresitas temáticas</li>
            <li>Animador/a incluido/a</li>
          </ul>
          <span class="svc-badge">Desde $XX.XXX</span>
        </article>

        <!-- Card 3 -->
        <article class="svc-card reveal d2">
          <div class="svc-icon">⭐</div>
          <h3>Pack Premium Todo Incluido</h3>
          <p class="svc-desc">La experiencia completa para que no te preocupes por nada el gran día.</p>
          <ul class="svc-list">
            <li>Decoración y ambientación total</li>
            <li>Candy bar profesional</li>
            <li>Fotógrafo/a por 2 horas</li>
            <li>Shows, juegos y animación</li>
            <li>Globología y pintacaritas</li>
          </ul>
          <span class="svc-badge">¡El más elegido! ⭐</span>
        </article>

        <!-- Card 4 -->
        <article class="svc-card reveal d3">
          <div class="svc-icon">🎪</div>
          <h3>Servicios Adicionales</h3>
          <p class="svc-desc">Sumá lo que quieras a tu paquete y hacelo todavía más especial.</p>
          <ul class="svc-list">
            <li>Show de magia y burbujas</li>
            <li>Alquiler de inflables</li>
            <li>DJ y pista de baile</li>
            <li>Catering personalizado</li>
            <li>Cobertura fotográfica extra</li>
          </ul>
          <span class="svc-badge">A consultar</span>
        </article>
      </div>
    </div>
  </section>

  <!-- Wave: services → how -->
  <div class="wave" style="background:#F0EBFF">
    <svg viewBox="0 0 1440 64" preserveAspectRatio="none" xmlns="http://www.w3.org/2000/svg" style="height:64px">
      <path d="M0,40 C360,0 1080,64 1440,24 L1440,64 L0,64 Z" fill="#ffffff"/>
    </svg>
  </div>

  <!-- ═══════════ HOW IT WORKS ═══════════ -->
  <section class="how section-pad">
    <div class="container">
      <div class="section-head reveal">
        <span class="section-label">🚀 Simple y sin estrés</span>
        <h2>¿Cómo funciona?</h2>
        <p class="section-sub">En solo 3 pasos organizamos la fiesta perfecta para tu hijo.</p>
      </div>

      <div class="how__steps">
        <div class="how__step reveal">
          <div class="how__num">1</div>
          <h3>Nos contactás</h3>
          <p>Escribinos por WhatsApp o completá el formulario. Contanos la fecha, el lugar, la cantidad de invitados y la temática que tenés en mente.</p>
        </div>
        <div class="how__step reveal d1">
          <div class="how__num">2</div>
          <h3>Armamos tu propuesta</h3>
          <p>Te asesoramos y diseñamos un paquete personalizado con todo lo que necesitás, ajustado a tu presupuesto y tus ideas.</p>
        </div>
        <div class="how__step reveal d2">
          <div class="how__num">3</div>
          <h3>¡A celebrar!</h3>
          <p>El día de la fiesta, nosotros nos encargamos de todo. Vos solo disfrutás junto a tu familia sin preocuparte por absolutamente nada.</p>
        </div>
      </div>
    </div>
  </section>

  <!-- Wave: how → gallery -->
  <div class="wave" style="background:#ffffff">
    <svg viewBox="0 0 1440 64" preserveAspectRatio="none" xmlns="http://www.w3.org/2000/svg" style="height:64px">
      <path d="M0,24 C720,80 720,0 1440,24 L1440,64 L0,64 Z" fill="#FFFCE8"/>
    </svg>
  </div>

  <!-- ═══════════ GALLERY ═══════════ -->
  <section id="galeria" class="gallery">
    <div class="container">
      <div class="section-head reveal">
        <span class="section-label">📸 Nuestras fiestas</span>
        <h2>Galería de eventos</h2>
        <p class="section-sub">Cada fiesta es única. Mirá algunos de los momentos mágicos que creamos juntos.</p>
      </div>

      <div class="gallery__grid reveal">
        <div class="g-item">
          <div class="g-fill">
            <span class="g-emoji">🦄</span>
            <span class="g-lbl">Unicornio Dreams</span>
          </div>
          <div class="g-overlay"><span class="g-caption">Fiesta Unicornio · 45 invitados</span></div>
        </div>
        <div class="g-item">
          <div class="g-fill">
            <span class="g-emoji">🚀</span>
            <span class="g-lbl">Space Party</span>
          </div>
          <div class="g-overlay"><span class="g-caption">Fiesta Espacial · 30 invitados</span></div>
        </div>
        <div class="g-item">
          <div class="g-fill">
            <span class="g-emoji">🐠</span>
            <span class="g-lbl">Under the Sea</span>
          </div>
          <div class="g-overlay"><span class="g-caption">Fiesta Sirenas · 50 invitados</span></div>
        </div>
        <div class="g-item">
          <div class="g-fill">
            <span class="g-emoji">🎂</span>
            <span class="g-lbl">Primera Añito</span>
          </div>
          <div class="g-overlay"><span class="g-caption">1er Cumpleaños · 60 invitados</span></div>
        </div>
        <div class="g-item">
          <div class="g-fill">
            <span class="g-emoji">🦖</span>
            <span class="g-lbl">Dino Fiesta</span>
          </div>
          <div class="g-overlay"><span class="g-caption">Fiestas Dinosaurios · 35 invitados</span></div>
        </div>
        <div class="g-item">
          <div class="g-fill">
            <span class="g-emoji">🏰</span>
            <span class="g-lbl">Princesas</span>
          </div>
          <div class="g-overlay"><span class="g-caption">Fiesta Principesca · 40 invitados</span></div>
        </div>
      </div>

      <div class="gallery__cta">
        <a href="https://www.instagram.com/" target="_blank" rel="noopener noreferrer" class="btn btn-primary">
          📷 Ver más en Instagram
        </a>
      </div>
    </div>
  </section>

  <!-- Wave: gallery → testimonials -->
  <div class="wave" style="background:#FFFCE8">
    <svg viewBox="0 0 1440 64" preserveAspectRatio="none" xmlns="http://www.w3.org/2000/svg" style="height:64px">
      <path d="M0,40 C480,0 960,64 1440,20 L1440,64 L0,64 Z" fill="#ffffff"/>
    </svg>
  </div>

  <!-- ═══════════ TESTIMONIALS ═══════════ -->
  <section id="testimonios" class="testimonials">
    <div class="container">
      <div class="section-head reveal">
        <span class="section-label">💬 Lo que dicen</span>
        <h2>Papás y mamás felices</h2>
      </div>

      <div class="testi-slider reveal" id="testiSlider">
        <div class="testi-track" id="testiTrack">

          <div class="testi-slide">
            <div class="testi-inner">
              <div class="testi-stars">★★★★★</div>
              <p class="testi-text">"Contratamos el paquete temático de dinosaurios para el cumpleaños de Mateo y fue ¡increíble! Cada detalle fue pensado con mucho cariño. Los chicos estuvieron entretenidos toda la tarde y los adultos también disfrutamos. ¡Ya están reservados para el año que viene!"</p>
              <div class="testi-author">
                <div class="testi-avatar">👩</div>
                <div>
                  <div class="testi-name">Laura G.</div>
                  <div class="testi-role">Mamá de Mateo, 5 años</div>
                </div>
              </div>
            </div>
          </div>

          <div class="testi-slide">
            <div class="testi-inner">
              <div class="testi-stars">★★★★★</div>
              <p class="testi-text">"La primera fiesta de mi hija Sofía fue perfecta. Desde la decoración de unicornio hasta el candy bar, todo fue de ensueño. El equipo es muy profesional y se nota que le ponen mucho corazón a cada evento. 100% recomendable."</p>
              <div class="testi-author">
                <div class="testi-avatar">👨</div>
                <div>
                  <div class="testi-name">Martín R.</div>
                  <div class="testi-role">Papá de Sofía, 1 año</div>
                </div>
              </div>
            </div>
          </div>

          <div class="testi-slide">
            <div class="testi-inner">
              <div class="testi-stars">★★★★★</div>
              <p class="testi-text">"Pedí el pack todo incluido para los 7 años de Valentina y no me arrepiento para nada. Me olvidé del estrés de organizar y pude disfrutar la fiesta con toda mi familia. La decoración era preciosa y la animadora fue un amor con los nenes."</p>
              <div class="testi-author">
                <div class="testi-avatar">👩</div>
                <div>
                  <div class="testi-name">Marcela P.</div>
                  <div class="testi-role">Mamá de Valentina, 7 años</div>
                </div>
              </div>
            </div>
          </div>

        </div>
      </div>

      <div class="testi-dots" role="group" aria-label="Navegación de testimonios">
        <button class="testi-dot active" data-i="0" aria-label="Testimonio 1"></button>
        <button class="testi-dot"        data-i="1" aria-label="Testimonio 2"></button>
        <button class="testi-dot"        data-i="2" aria-label="Testimonio 3"></button>
      </div>
    </div>
  </section>

  <!-- ═══════════ CTA STRIP ═══════════ -->
  <section class="cta-strip">
    <div class="container">
      <h2>¿Listo para crear magia? 🎉</h2>
      <p>Contactanos hoy y empezamos a planear la fiesta perfecta para tu peque.</p>
      <div class="cta-strip__btns">
        <a href="https://wa.me/5491100000000?text=Hola!%20Quiero%20cotizar%20una%20fiesta%20%F0%9F%8E%89"
           target="_blank" rel="noopener noreferrer" class="btn btn-wa">
          💬 Escribir por WhatsApp
        </a>
        <a href="#contacto" class="btn btn-outline">📝 Completar formulario</a>
      </div>
    </div>
  </section>

  <!-- Wave: cta → contact -->
  <div class="wave" style="background:linear-gradient(135deg,var(--coral),#C42868)">
    <svg viewBox="0 0 1440 64" preserveAspectRatio="none" xmlns="http://www.w3.org/2000/svg" style="height:64px">
      <path d="M0,32 C720,80 720,0 1440,32 L1440,64 L0,64 Z" fill="#FDFBFF"/>
    </svg>
  </div>

  <!-- ═══════════ CONTACT ═══════════ -->
  <section id="contacto" class="contact">
    <div class="container">
      <div class="section-head reveal">
        <span class="section-label">📞 Contacto</span>
        <h2>¡Hablemos!</h2>
        <p class="section-sub">Contanos sobre el evento que tenés en mente y te respondemos en menos de 24&nbsp;hs.</p>
      </div>

      <div class="contact__grid">

        <!-- Info column -->
        <div class="contact__info reveal">
          <div class="c-item">
            <div class="c-icon">💬</div>
            <div>
              <h4>WhatsApp</h4>
              <a href="https://wa.me/5491100000000" target="_blank" rel="noopener noreferrer">+54 9 11 0000-0000</a>
            </div>
          </div>
          <div class="c-item">
            <div class="c-icon">📧</div>
            <div>
              <h4>Email</h4>
              <a href="mailto:hola@fiestamagica.com.ar">hola@fiestamagica.com.ar</a>
            </div>
          </div>
          <div class="c-item">
            <div class="c-icon">📍</div>
            <div>
              <h4>Zona de cobertura</h4>
              <p>Buenos Aires y Gran Buenos Aires</p>
            </div>
          </div>
          <div class="c-item">
            <div class="c-icon">🕐</div>
            <div>
              <h4>Horario de atención</h4>
              <p>Lunes a Sábado · 9:00 – 20:00 hs</p>
            </div>
          </div>

          <!-- Map placeholder — reemplazá por iframe de Google Maps real -->
          <div class="c-map">
            <!--
              Para activar el mapa real, reemplazá este div con:
              <iframe
                src="https://www.google.com/maps/embed?pb=TU_EMBED_URL_AQUÍ"
                loading="lazy" allowfullscreen
                referrerpolicy="no-referrer-when-downgrade">
              </iframe>
            -->
            <span>📍 Mapa de ubicación</span>
          </div>
        </div>

        <!-- Form column -->
        <div class="contact__form reveal d1" id="formWrap">
          <h3>Consultá sin compromiso</h3>

          <div class="form-success" id="formSuccess">
            <div class="big">🎉</div>
            <h3>¡Gracias por tu consulta!</h3>
            <p>Te vamos a responder en menos de 24&nbsp;hs. ¡Ya está en camino la fiesta perfecta!</p>
          </div>

          <form id="contactForm" novalidate>
            <div class="fg-row">
              <div class="fg" id="fg-nombre">
                <label for="nombre">Nombre *</label>
                <input type="text" id="nombre" name="nombre" placeholder="Tu nombre" autocomplete="given-name">
                <span class="err">Por favor ingresá tu nombre.</span>
              </div>
              <div class="fg" id="fg-tel">
                <label for="tel">Teléfono *</label>
                <input type="tel" id="tel" name="tel" placeholder="11 1234-5678" autocomplete="tel">
                <span class="err">Por favor ingresá tu teléfono.</span>
              </div>
            </div>

            <div class="fg" id="fg-email">
              <label for="email">Email *</label>
              <input type="email" id="email" name="email" placeholder="tu@email.com" autocomplete="email">
              <span class="err">Por favor ingresá un email válido.</span>
            </div>

            <div class="fg-row">
              <div class="fg">
                <label for="fecha">Fecha del evento</label>
                <input type="date" id="fecha" name="fecha">
              </div>
              <div class="fg">
                <label for="paquete">Paquete de interés</label>
                <select id="paquete" name="paquete">
                  <option value="">Seleccioná...</option>
                  <option value="clasico">Cumpleaños Clásico</option>
                  <option value="tematico">Fiesta Temática</option>
                  <option value="premium">Pack Premium</option>
                  <option value="adicional">Servicios Adicionales</option>
                  <option value="otro">Otro / No sé aún</option>
                </select>
              </div>
            </div>

            <div class="fg">
              <label for="msg">Contanos más (opcional)</label>
              <textarea id="msg" name="msg" placeholder="Edad del niño/a, temática que tiene en mente, cantidad de invitados..."></textarea>
            </div>

            <button type="submit" class="btn btn-primary" style="width:100%; justify-content:center;">
              📩 Enviar consulta
            </button>
          </form>
        </div>

      </div>
    </div>
  </section>

  <!-- Wave: contact → footer -->
  <div class="wave" style="background:#FDFBFF">
    <svg viewBox="0 0 1440 64" preserveAspectRatio="none" xmlns="http://www.w3.org/2000/svg" style="height:64px">
      <path d="M0,20 C480,64 960,0 1440,20 L1440,64 L0,64 Z" fill="#2D1B69"/>
    </svg>
  </div>

  <!-- ═══════════ FOOTER ═══════════ -->
  <footer class="footer">
    <div class="container">
      <div class="footer__grid">

        <div class="footer__brand">
          <a href="#inicio" class="footer__logo">Fiesta<span>Mágica</span> 🎉</a>
          <p>Creamos celebraciones únicas e inolvidables para los más pequeños. Más de 8 años haciendo magia en Buenos Aires y GBA.</p>
          <div class="footer__socials">
            <a href="https://www.instagram.com/" target="_blank" rel="noopener noreferrer" class="footer__soc" aria-label="Instagram">📷</a>
            <a href="https://www.facebook.com/"  target="_blank" rel="noopener noreferrer" class="footer__soc" aria-label="Facebook">👍</a>
            <a href="https://wa.me/5491100000000" target="_blank" rel="noopener noreferrer" class="footer__soc" aria-label="WhatsApp">💬</a>
          </div>
        </div>

        <nav class="footer__col" aria-label="Servicios">
          <h4>Servicios</h4>
          <ul>
            <li><a href="#servicios">Cumpleaños Clásico</a></li>
            <li><a href="#servicios">Fiestas Temáticas</a></li>
            <li><a href="#servicios">Pack Premium</a></li>
            <li><a href="#servicios">Servicios Extra</a></li>
          </ul>
        </nav>

        <nav class="footer__col" aria-label="Páginas">
          <h4>Sitio</h4>
          <ul>
            <li><a href="#inicio">Inicio</a></li>
            <li><a href="#galeria">Galería</a></li>
            <li><a href="#testimonios">Testimonios</a></li>
            <li><a href="#contacto">Contacto</a></li>
          </ul>
        </nav>

      </div>

      <div class="footer__bottom">
        <span>© 2025 FiestaMágica. Todos los derechos reservados.</span>
        <span>Hecho con ❤️ para los más chicos</span>
      </div>
    </div>
  </footer>

  <!-- ═══════════ WHATSAPP FLOATING BUTTON ═══════════ -->
  <div class="wa-float">
    <div class="wa-bubble">¡Hola! Consultanos sobre tu fiesta 🎉</div>
    <a href="https://wa.me/5491100000000?text=Hola!%20Quiero%20consultar%20sobre%20una%20fiesta%20infantil%20%F0%9F%8E%89"
       target="_blank" rel="noopener noreferrer"
       class="wa-btn"
       aria-label="Contactar por WhatsApp">
      <svg width="30" height="30" viewBox="0 0 24 24" fill="white" xmlns="http://www.w3.org/2000/svg" aria-hidden="true">
        <path d="M17.472 14.382c-.297-.149-1.758-.867-2.03-.967-.273-.099-.471-.148-.67.15-.197.297-.767.966-.94 1.164-.173.199-.347.223-.644.075-.297-.15-1.255-.463-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.298-.347.446-.52.149-.174.198-.298.298-.497.099-.198.05-.371-.025-.52-.075-.149-.669-1.612-.916-2.207-.242-.579-.487-.5-.669-.51-.173-.008-.371-.01-.57-.01-.198 0-.52.074-.792.372-.272.297-1.04 1.016-1.04 2.479 0 1.462 1.065 2.875 1.213 3.074.149.198 2.096 3.2 5.077 4.487.709.306 1.262.489 1.694.625.712.227 1.36.195 1.871.118.571-.085 1.758-.719 2.006-1.413.248-.694.248-1.289.173-1.413-.074-.124-.272-.198-.57-.347m-5.421 7.403h-.004a9.87 9.87 0 01-5.031-1.378l-.361-.214-3.741.982.998-3.648-.235-.374a9.86 9.86 0 01-1.51-5.26c.001-5.45 4.436-9.884 9.888-9.884 2.64 0 5.122 1.03 6.988 2.898a9.825 9.825 0 012.893 6.994c-.003 5.45-4.437 9.884-9.885 9.884m8.413-18.297A11.815 11.815 0 0012.05 0C5.495 0 .16 5.335.157 11.892c0 2.096.547 4.142 1.588 5.945L.057 24l6.305-1.654a11.882 11.882 0 005.683 1.448h.005c6.554 0 11.89-5.335 11.893-11.893a11.821 11.821 0 00-3.48-8.413z"/>
      </svg>
    </a>
  </div>

  <!-- ═══════════ JAVASCRIPT ═══════════ -->
  <script>
    /* ── Sticky nav ── */
    const nav = document.getElementById('nav');
    window.addEventListener('scroll', () => {
      nav.classList.toggle('scrolled', window.scrollY > 60);
    }, { passive: true });

    /* ── Mobile menu ── */
    const burger    = document.getElementById('burger');
    const mobileMenu = document.getElementById('mobileMenu');
    const mobLinks  = document.querySelectorAll('.mob-link');

    function toggleMenu(open) {
      burger.classList.toggle('open', open);
      mobileMenu.classList.toggle('open', open);
      burger.setAttribute('aria-expanded', open);
      document.body.style.overflow = open ? 'hidden' : '';
    }

    burger.addEventListener('click', () => toggleMenu(!mobileMenu.classList.contains('open')));
    mobLinks.forEach(l => l.addEventListener('click', () => toggleMenu(false)));

    /* ── Scroll reveal ── */
    const reveals = document.querySelectorAll('.reveal');
    const revealObs = new IntersectionObserver((entries) => {
      entries.forEach(e => {
        if (e.isIntersecting) {
          e.target.classList.add('visible');
          revealObs.unobserve(e.target);
        }
      });
    }, { threshold: 0.1, rootMargin: '0px 0px -40px 0px' });
    reveals.forEach(el => revealObs.observe(el));

    /* ── Testimonial slider ── */
    const track = document.getElementById('testiTrack');
    const dots  = document.querySelectorAll('.testi-dot');
    let cur = 0, autoTimer;

    function goTo(i) {
      cur = i;
      track.style.transform = `translateX(-${i * 100}%)`;
      dots.forEach((d, idx) => d.classList.toggle('active', idx === i));
    }

    dots.forEach(d => d.addEventListener('click', () => {
      clearInterval(autoTimer);
      goTo(parseInt(d.dataset.i));
      startAuto();
    }));

    function startAuto() {
      autoTimer = setInterval(() => goTo((cur + 1) % dots.length), 5000);
    }
    startAuto();

    /* ── Form validation ── */
    const form       = document.getElementById('contactForm');
    const formSuccess = document.getElementById('formSuccess');

    const isEmail = v => /^[^\s@]+@[^\s@]+\.[^\s@]+$/.test(v);

    function setInvalid(id, invalid) {
      document.getElementById(id).classList.toggle('invalid', invalid);
    }

    form.addEventListener('submit', e => {
      e.preventDefault();
      const nombre = document.getElementById('nombre').value.trim();
      const tel    = document.getElementById('tel').value.trim();
      const email  = document.getElementById('email').value.trim();

      setInvalid('fg-nombre', !nombre);
      setInvalid('fg-tel',    !tel);
      setInvalid('fg-email',  !isEmail(email));

      if (nombre && tel && isEmail(email)) {
        form.style.display = 'none';
        formSuccess.classList.add('show');
        /*
         * Para envío real, conectá aquí Formspree, EmailJS o tu backend:
         * fetch('https://formspree.io/f/TU_ID', { method:'POST', body: new FormData(form) })
         *
         * O redirigí a WhatsApp con los datos del formulario:
         * const msg = `Hola! Soy ${nombre}. Tel: ${tel}. Email: ${email}.`;
         * window.open(`https://wa.me/5491100000000?text=${encodeURIComponent(msg)}`, '_blank');
         */
      }
    });

    ['nombre','tel','email'].forEach(id => {
      const el = document.getElementById(id);
      if (el) el.addEventListener('input', () => {
        const fg = document.getElementById('fg-' + id);
        if (fg) fg.classList.remove('invalid');
      });
    });
  </script>

</body>
</html>
