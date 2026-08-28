<!doctype html>
<html lang="en">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>Insurance Hub · Monarch Agency Solutions</title>
<meta name="description" content="Find the coverage you need — health, life, property and casualty, and business owner options.">
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800;900&display=swap">
<style>
:root{
  /* Monarch Insurance Hub palette. Sits alongside the wordmark without copying it:
     the blues run deeper and more saturated than the butterfly's silvery tint, and
     --monarch is the orange the logo abstracted away, used sparingly as a signal. */
  --ink:#12212E;        /* structure, headings, category blocks */
  --tide:#2C5A78;       /* primary action, illustrations */
  --haze:#E3ECF2;       /* tinted surfaces, route line */
  --paper:#FBFCFD;      /* page ground */
  --slate:#55697A;      /* secondary text - 5.54:1 on paper */
  --monarch:#E0712A;    /* accent. Non-text and large only - 3.11:1 on paper */
  --white:#fff;

  --radius-lg:22px;
  --radius-md:14px;
  --shadow-soft:0 10px 28px rgba(18,33,46,.08);
  --shadow:0 22px 54px rgba(18,33,46,.16);

  --display:'Bricolage Grotesque',Segoe UI,Arial,Helvetica,sans-serif;
  --body:'Source Sans 3',Segoe UI,Arial,Helvetica,sans-serif;
  --ease:cubic-bezier(.23,1,.32,1);
  --slide:300ms;
  --fade:200ms;
  --nav-h:76px;
}
*,*::before,*::after{box-sizing:border-box}
html{-webkit-text-size-adjust:100%}
body{margin:0;background:var(--paper);color:var(--ink);font-family:var(--body);
     font-size:17px;line-height:1.55;-webkit-font-smoothing:antialiased;
     overflow-x:hidden}
h1,h2,h3{font-family:var(--display);font-weight:800;letter-spacing:-.02em;line-height:1.12;margin:0}
p{margin:0}
button{font:inherit;color:inherit}
a{color:var(--tide)}
.sr-only{position:absolute;width:1px;height:1px;padding:0;margin:-1px;overflow:hidden;
         clip:rect(0 0 0 0);white-space:nowrap;border:0}
.skip{position:absolute;left:12px;top:-60px;z-index:60;background:var(--ink);color:var(--white);
      padding:12px 20px;border-radius:0 0 12px 12px;text-decoration:none;transition:top 160ms var(--ease)}
.skip:focus{top:0}
:focus-visible{outline:3px solid var(--monarch);outline-offset:3px;border-radius:8px}

/* ---------- nav ---------- */
.nav{position:sticky;top:0;z-index:30;min-height:var(--nav-h);display:flex;align-items:center;
     justify-content:space-between;gap:16px;padding:12px clamp(16px,4vw,44px);
     background:var(--white);border-bottom:1px solid var(--haze)}
.nav__brand{display:inline-flex;align-items:center;flex:0 1 auto;min-width:0}
.nav__logo{display:block;height:clamp(34px,5.2vw,50px);width:auto;max-width:100%}
.nav__hub{flex:0 0 auto;display:inline-flex;align-items:center;justify-content:center;gap:7px;
          min-height:44px;padding:11px 26px;border-radius:999px;background:var(--ink);
          color:var(--white);font-family:var(--display);font-weight:700;font-size:15px;
          text-decoration:none;transition:background var(--fade) var(--ease)}
.nav__hub:hover{background:var(--tide)}
.nav__hub[aria-current="page"]{background:transparent;color:var(--slate);
                               box-shadow:inset 0 0 0 1.5px var(--haze)}

/* ---------- landing ---------- */
.land{max-width:1120px;margin:0 auto;padding:clamp(34px,6.5vw,80px) clamp(16px,4vw,44px) 72px}
.land__eyebrow{font-family:var(--display);font-weight:600;font-size:13px;letter-spacing:.16em;
               text-transform:uppercase;color:var(--slate);margin-bottom:14px}
.land__title{font-size:clamp(34px,6vw,60px)}
.land__sub{font-size:clamp(17px,2.1vw,20px);color:var(--slate);margin:14px 0 clamp(30px,5vw,50px);
           max-width:46ch}
.cats{display:grid;grid-template-columns:repeat(3,1fr);gap:clamp(14px,1.9vw,20px)}
.cat--wide{grid-column:1 / -1}
.catbtn{position:relative;display:flex;flex-direction:column;align-items:flex-start;gap:12px;
        width:100%;height:100%;text-align:left;text-decoration:none;color:var(--white);
        background:var(--ink);border:0;border-radius:var(--radius-lg);
        padding:clamp(24px,3vw,32px);overflow:hidden;cursor:pointer;
        transition:transform var(--fade) var(--ease),box-shadow var(--fade) var(--ease)}
.catbtn::after{content:"";position:absolute;left:0;right:0;bottom:0;height:3px;
               background:var(--monarch);transform:scaleX(0);transform-origin:left;
               transition:transform var(--slide) var(--ease)}
.catbtn:hover{transform:translateY(-5px);box-shadow:var(--shadow)}
.catbtn:hover::after{transform:scaleX(1)}
.catbtn__icon{width:60px;height:45px;color:#8FBBD6}
.catbtn__label{font-family:var(--display);font-weight:800;font-size:clamp(20px,2.5vw,25px);
               line-height:1.15;letter-spacing:-.02em}
.catbtn__label small{display:block;font-weight:600;font-size:.66em;opacity:.72;letter-spacing:0;
                     margin-top:4px}
.catbtn__blurb{font-size:15px;color:rgba(255,255,255,.7);line-height:1.45}
.catbtn__go{margin-top:auto;padding-top:10px;font-family:var(--display);font-weight:700;
            font-size:14px;color:#8FBBD6}

.land__extra{margin-top:clamp(22px,3vw,32px);display:flex;justify-content:center}
.extralink{display:inline-flex;align-items:center;gap:9px;min-height:44px;padding:11px 24px;
           font-weight:600;color:var(--tide);text-decoration:none;border-radius:999px;
           background:var(--white);box-shadow:inset 0 0 0 1.5px var(--haze);
           transition:box-shadow var(--fade) var(--ease),background var(--fade) var(--ease)}
.extralink:hover{background:var(--haze);box-shadow:inset 0 0 0 1.5px var(--tide)}
.extralink[aria-disabled="true"]{color:var(--slate);pointer-events:none}

/* ---------- category view ---------- */
.cv{max-width:1120px;margin:0 auto;padding:clamp(20px,3.5vw,40px) clamp(16px,4vw,44px) 72px}
.back{display:inline-flex;align-items:center;gap:7px;min-height:44px;color:var(--tide);
      font-weight:600;text-decoration:none}
.back:hover{text-decoration:underline}
.cv__title{font-size:clamp(30px,5vw,50px);margin-top:10px;text-align:center}
.cv__sub{color:var(--slate);margin:12px auto clamp(6px,2vw,16px);font-size:clamp(16px,2vw,19px);
         max-width:52ch;text-align:center}

.carousel{display:grid;grid-template-columns:48px minmax(0,1fr) 48px;align-items:center;gap:6px}
.arrow{width:48px;height:48px;border-radius:999px;border:1.5px solid var(--haze);
       background:var(--white);color:var(--ink);cursor:pointer;display:grid;place-items:center;
       font-size:22px;line-height:1;padding:0;
       transition:border-color var(--fade) var(--ease),background var(--fade) var(--ease)}
.arrow:hover:not(:disabled){border-color:var(--tide);background:var(--haze)}
.arrow:disabled{opacity:.32;cursor:default}
.stage{overflow:hidden;padding:30px 0 34px}
.track{display:flex;align-items:stretch;will-change:transform;
       transition:transform var(--slide) var(--ease)}

.card{position:relative;flex:0 0 var(--cw,330px);margin:0 11px;background:var(--white);
      border-radius:var(--radius-lg);box-shadow:var(--shadow-soft);padding:28px 26px 30px;
      overflow:hidden;
      display:flex;flex-direction:column;align-items:flex-start;gap:13px;text-align:left;
      border:0;cursor:pointer;opacity:.42;transform:scale(.85);transform-origin:center;
      transition:opacity var(--fade) var(--ease),transform var(--fade) var(--ease),
                 box-shadow var(--fade) var(--ease)}
.card::before{content:"";position:absolute;left:0;right:0;top:0;height:4px;
              background:var(--tide);opacity:0;
              transition:opacity var(--fade) var(--ease)}
.card.is-active{opacity:1;transform:scale(1);box-shadow:var(--shadow)}
.card.is-active::before{opacity:1}
.card__icon{width:64px;height:48px;color:var(--tide);flex:none}
.card__title{font-size:22px}
.card__blurb{font-size:15.5px;line-height:1.5;color:var(--slate)}
.card__soon{font-family:var(--display);font-size:11px;font-weight:700;letter-spacing:.1em;
            text-transform:uppercase;background:var(--monarch);color:var(--ink);
            padding:5px 12px;border-radius:999px}
.card.is-soon{filter:saturate(.3)}
.card.is-soon .card__icon{color:var(--slate)}
.card.is-soon.is-active{filter:saturate(.55)}

/* ---------- the route line ---------- */
.route{position:relative;margin:0 auto clamp(26px,4vw,36px);max-width:640px;padding:0 8px}
.route__rail{position:absolute;left:8px;right:8px;top:21px;height:2px;background:var(--haze);
             border-radius:2px}
.route__done{position:absolute;left:8px;top:21px;height:2px;background:var(--tide);
             border-radius:2px;width:0;
             transition:width var(--slide) var(--ease)}
.route__stops{position:relative;display:flex;justify-content:space-between;align-items:flex-start}
.stop{position:relative;width:44px;height:44px;border:0;background:none;padding:0;cursor:pointer;
      display:grid;place-items:center}
.stop::before{content:"";width:10px;height:10px;border-radius:999px;background:var(--white);
              box-shadow:inset 0 0 0 2px var(--haze);
              transition:background var(--fade) var(--ease),box-shadow var(--fade) var(--ease),
                         transform var(--fade) var(--ease)}
.stop.is-done::before{background:var(--tide);box-shadow:none}
.stop[aria-current="true"]::before{background:var(--monarch);box-shadow:0 0 0 4px rgba(224,113,42,.2);
                                   transform:scale(1.5)}
.route__pos{text-align:center;margin-top:2px;font-family:var(--display);font-weight:600;
            font-size:12.5px;letter-spacing:.1em;text-transform:uppercase;color:var(--slate)}

/* ---------- call to action ---------- */
.cta{display:flex;align-items:center;justify-content:center;gap:10px;width:100%;max-width:470px;
     margin:0 auto;text-align:center;font-family:var(--display);font-weight:800;font-size:17.5px;
     padding:19px 30px;border-radius:999px;border:0;background:var(--ink);color:var(--white);
     text-decoration:none;cursor:pointer;box-shadow:var(--shadow-soft);
     transition:background var(--fade) var(--ease),transform var(--fade) var(--ease)}
.cta:hover{background:var(--tide);transform:translateY(-2px)}
.cta__arrow{transition:transform var(--fade) var(--ease)}
.cta:hover .cta__arrow{transform:translateX(4px)}
.cta.is-disabled{background:var(--haze);color:var(--slate);pointer-events:none;box-shadow:none}
.cta-note{text-align:center;color:var(--slate);font-size:15px;margin:14px auto 0;max-width:44ch}
.cta-note a{font-weight:700}

/* ---------- footer ---------- */
.foot{background:var(--ink);color:rgba(255,255,255,.72);padding:38px clamp(16px,4vw,44px);
      text-align:center;font-size:14.5px}
.foot a{color:#8FBBD6;font-weight:600}
.foot__contact{font-size:17px;margin-bottom:12px}
.foot__legal{max-width:620px;margin:0 auto;font-size:13px;opacity:.6;line-height:1.55}

/* ---------- responsive ---------- */
@media (max-width:900px){
  .cats{grid-template-columns:1fr}
  .cat--wide{grid-column:1 / -1}
}
@media (max-width:700px){
  body{font-size:16px}
  /* The arrows stop taking grid columns and float over the stage instead.
     Keeping them in the grid left the active card wider than its own stage,
     which clipped the card's rounded corners and hid the peek entirely. */
  .carousel{grid-template-columns:minmax(0,1fr);position:relative}
  .arrow{position:absolute;top:50%;z-index:2;width:42px;height:42px;font-size:20px;
         transform:translateY(-50%);background:rgba(255,255,255,.94);
         box-shadow:0 3px 12px rgba(18,33,46,.16)}
  .arrow--prev{left:0}
  .arrow--next{right:0}
  .card{--cw:min(74vw,300px);margin:0 7px}
  .card:not(.is-active){transform:scale(.9)}
  .route{max-width:100%}
  .stop{width:34px}
}
@media (max-width:420px){
  .stop{width:26px}
  .route__pos{font-size:11.5px}
}


/* ════════ Noir · Sky ════════
   Folded in 2026-08-28 from themes/_motion.css + _noir.css + n1-sky.css,
   which is why this reads as three stacked layers: motion and interaction
   first, then the dark shell, then the highlight colour. Overrides what is
   above it deliberately — the original tokens are left in place so the
   diff against insurance-hub.ORIGINAL-2026-08-28.html stays readable. */

/* Shared by every direction: entrance motion, press feedback, and the STRUCTURE
   of the hover states. Each theme file supplies the colors these flood with, via
   --accent / --on-accent / --flood / --on-flood / --shadow-hover.

   Nothing here is decorative-only. Every animation marks a cause: you arrived,
   you pointed at something, you pressed it, you moved to the next option.

   Hover effects live inside @media (hover:hover). A phone has no hover, and a
   :hover rule on a touchscreen sticks after the tap — the flood would stay on
   the tile you last touched. Touch gets the :active press instead, which is
   outside the query and works everywhere. */

:root{
  --ease:cubic-bezier(.22,1,.36,1);      /* settle */
  --spring:cubic-bezier(.34,1.42,.5,1);  /* slight overshoot — the "confident" feel */
  --slide:440ms;                          /* carousel travel, was 300ms */
  --fade:240ms;
  --quick:150ms;
}

/* ────────── entrance ──────────
   The views re-render on every route change, so these replay each time you move
   between the landing view and a category. fill-mode is `backwards`, not `both`,
   on purpose: `both` pins the final transform and silently kills every hover
   transform below it. */
@keyframes riseIn{from{opacity:0;transform:translateY(24px)}to{opacity:1;transform:none}}
@keyframes popIn{from{opacity:0;transform:scale(.94) translateY(18px)}to{opacity:1;transform:none}}
@keyframes fadeIn{from{opacity:0}to{opacity:1}}
@keyframes railGrow{from{transform:scaleX(0)}to{transform:scaleX(1)}}
@keyframes nudge{0%,100%{transform:translateX(0)}50%{transform:translateX(4px)}}
@keyframes beacon{0%,100%{transform:scale(1.5);box-shadow:0 0 0 4px var(--beacon,rgba(224,113,42,.25))}
                  50%{transform:scale(1.64);box-shadow:0 0 0 10px rgba(0,0,0,0)}}
@keyframes sheen{from{transform:translateX(-140%) skewX(-18deg)}to{transform:translateX(320%) skewX(-18deg)}}

.land__eyebrow{animation:riseIn 520ms var(--ease) backwards}
.land__title  {animation:riseIn 620ms var(--spring) 70ms backwards}
.land__sub    {animation:riseIn 620ms var(--spring) 140ms backwards}
.land__extra  {animation:riseIn 520ms var(--ease) 560ms backwards}
.cat:nth-child(1) .catbtn{animation:popIn 560ms var(--spring) 220ms backwards}
.cat:nth-child(2) .catbtn{animation:popIn 560ms var(--spring) 300ms backwards}
.cat:nth-child(3) .catbtn{animation:popIn 560ms var(--spring) 380ms backwards}
.cat:nth-child(4) .catbtn{animation:popIn 560ms var(--spring) 460ms backwards}

.back      {animation:fadeIn 400ms var(--ease) backwards}
.cv__title {animation:riseIn 560ms var(--spring) 60ms backwards}
.cv__sub   {animation:riseIn 560ms var(--spring) 120ms backwards}
.route     {animation:riseIn 520ms var(--ease) 200ms backwards}
.route__rail{transform-origin:left;animation:railGrow 620ms var(--ease) 260ms backwards}
.stage     {animation:popIn 620ms var(--spring) 260ms backwards}
.cta       {animation:riseIn 520ms var(--spring) 400ms backwards}
.cta-note  {animation:fadeIn 420ms var(--ease) 520ms backwards}

/* ────────── transitions and press feedback (all devices) ────────── */
.catbtn{isolation:isolate;transition:transform 320ms var(--spring),box-shadow 320ms var(--ease)}
.catbtn::before{content:"";position:absolute;inset:0;z-index:0;background:var(--flood);
                transform:translateY(101%);transition:transform 400ms var(--ease)}
.catbtn>*{position:relative;z-index:1}
.catbtn::after{height:4px;z-index:2}
.catbtn:active{transform:translateY(-3px) scale(.995);transition-duration:90ms}
.catbtn:active::before{transform:translateY(0)}
.catbtn__icon,.catbtn__label,.catbtn__blurb,.catbtn__go{
  transition:color 300ms var(--ease),transform 360ms var(--spring)}

.track{transition:transform var(--slide) var(--spring)}
.card{transition:opacity var(--fade) var(--ease),transform 380ms var(--spring),
                 box-shadow var(--fade) var(--ease),filter var(--fade) var(--ease)}
.card:active{transform:scale(.97);transition-duration:90ms}
.card::before{height:5px}
.card__icon{transition:transform 360ms var(--spring),color var(--fade) var(--ease)}

.arrow{transition:background var(--quick) var(--ease),border-color var(--quick) var(--ease),
                  color var(--quick) var(--ease),transform 260ms var(--spring)}
.arrow:active:not(:disabled){transform:scale(.92);background:var(--accent);
                             border-color:var(--accent);color:var(--on-accent);
                             transition-duration:80ms}

.stop::before{transition:background var(--fade) var(--ease),box-shadow var(--fade) var(--ease),
                         transform 320ms var(--spring)}
.stop[aria-current="true"]::before{animation:beacon 2.6s ease-in-out infinite}
.route__done{transition:width var(--slide) var(--spring)}

.cta{position:relative;overflow:hidden;
     transition:background 280ms var(--ease),color 280ms var(--ease),
                transform 300ms var(--spring),box-shadow 300ms var(--ease)}
.cta::after{content:"";position:absolute;top:0;bottom:0;left:0;width:38%;pointer-events:none;
            background:linear-gradient(90deg,transparent,var(--sheen,rgba(255,255,255,.28)),transparent);
            transform:translateX(-140%) skewX(-18deg)}
.cta:active:not(.is-disabled){transform:translateY(-1px) scale(.99);background:var(--accent);
                              color:var(--on-accent);transition-duration:90ms}
.cta__arrow{animation:nudge 2.2s ease-in-out infinite}

.nav__hub{transition:background var(--fade) var(--ease),color var(--fade) var(--ease),
                     transform 260ms var(--spring),box-shadow var(--fade) var(--ease)}
.nav__hub:active{transform:scale(.97);background:var(--accent);color:var(--on-accent);
                 transition-duration:80ms}
.back{transition:transform 260ms var(--spring),color var(--fade) var(--ease)}
.extralink{transition:background var(--fade) var(--ease),color var(--fade) var(--ease),
                      box-shadow var(--fade) var(--ease),transform 260ms var(--spring)}

/* ────────── keyboard gets the same treatment as the mouse ────────── */
.catbtn:focus-visible{transform:translateY(-9px) scale(1.012);box-shadow:var(--shadow-hover)}
.catbtn:focus-visible::before{transform:translateY(0)}
.catbtn:focus-visible::after{transform:scaleX(1)}
.catbtn:focus-visible .catbtn__icon{color:var(--on-flood);transform:scale(1.09) rotate(-3deg)}
.catbtn:focus-visible .catbtn__label,.catbtn:focus-visible .catbtn__go{color:var(--on-flood)}
.catbtn:focus-visible .catbtn__blurb{color:var(--on-flood-soft)}
.arrow:focus-visible:not(:disabled){background:var(--accent);border-color:var(--accent);
                                    color:var(--on-accent)}

/* ────────── hover — pointing devices only ────────── */
@media (hover:hover){
  .catbtn:hover{transform:translateY(-9px) scale(1.012);box-shadow:var(--shadow-hover)}
  .catbtn:hover::before{transform:translateY(0)}
  .catbtn:hover::after{transform:scaleX(1)}
  .catbtn:hover .catbtn__icon{color:var(--on-flood);transform:scale(1.09) rotate(-3deg)}
  .catbtn:hover .catbtn__label{color:var(--on-flood)}
  .catbtn:hover .catbtn__blurb{color:var(--on-flood-soft)}
  .catbtn:hover .catbtn__go{color:var(--on-flood);transform:translateX(6px)}

  .card:not(.is-active):hover{opacity:.9;transform:scale(.93);box-shadow:var(--shadow)}
  .card.is-active:hover{transform:scale(1.025);box-shadow:var(--shadow-hover)}
  .card:hover .card__icon{transform:scale(1.08) translateY(-2px)}

  .arrow:hover:not(:disabled){background:var(--accent);border-color:var(--accent);
                              color:var(--on-accent);transform:scale(1.14)}

  .stop:hover::before{transform:scale(1.5);box-shadow:inset 0 0 0 2.5px var(--accent)}

  .cta:hover:not(.is-disabled){background:var(--accent);color:var(--on-accent);
                               transform:translateY(-4px) scale(1.02);box-shadow:var(--shadow-hover)}
  .cta:hover:not(.is-disabled)::after{animation:sheen 720ms var(--ease)}
  .cta:hover .cta__arrow{animation:none;transform:translateX(8px)}

  .nav__hub:hover{background:var(--accent);color:var(--on-accent);transform:translateY(-2px)}
  .nav__hub[aria-current="page"]:hover{background:var(--accent);color:var(--on-accent)}

  .back:hover{transform:translateX(-5px);color:var(--accent)}

  .extralink:not([aria-disabled="true"]):hover{background:var(--accent);color:var(--on-accent);
                                               box-shadow:0 8px 22px rgba(0,0,0,.14);
                                               transform:translateY(-3px)}
}

/* On mobile the inactive cards sit closer, so keep the original resting scale
   rather than the desktop one this file's transitions inherit. */
@media (max-width:700px){
  .card:not(.is-active){transform:scale(.9)}
}

/* @base Noir — the dark shell. Not built on its own; the n*.css files extend it
   and supply the highlight colour. Everything here is hue-neutral so that
   swapping one token set changes the accent and nothing else.

   The Monarch mark is a black wordmark, so it would disappear on this ground.
   Rather than recolour it, it sits on a white plate in the nav — a deliberate
   dark-UI convention that leaves the artwork untouched. */

:root{
  /* Highlight tokens (--tide, --monarch, --accent, --on-accent, --flood,
     --on-flood, --on-flood-soft, --beacon) come from the extending theme. */
  --ink:#EAF2F8;       /* body text, not a surface — see the overrides below */
  --haze:#26313D;
  --paper:#0A0F15;
  --slate:#9FB3C4;     /* 8.1:1 on paper */
  --white:#141C25;     /* "surface", not white — cards, arrows, nav all use it */

  --sheen:rgba(255,255,255,.18);

  --radius-lg:18px;
  --radius-md:16px;
  --shadow-soft:0 2px 14px rgba(0,0,0,.5);
  --shadow:0 18px 44px rgba(0,0,0,.62);
  --shadow-hover:0 22px 60px var(--glow);   /* --glow is the highlight, from the theme */

  --display:'Inter',Segoe UI,Arial,Helvetica,sans-serif;
  --body:'Inter',Segoe UI,Arial,Helvetica,sans-serif;
}

h1,h2,h3{font-weight:800;letter-spacing:-.035em}
.land__title{font-size:clamp(40px,7vw,72px);line-height:1}
.land__eyebrow{color:var(--monarch);font-weight:600;letter-spacing:.22em;font-size:12px}
.land__sub{color:var(--slate)}

/* nav — the logo keeps its own light ground */
.nav{background:rgba(10,15,21,.82);backdrop-filter:blur(12px);border-bottom:1px solid var(--haze)}
.nav__brand{background:#FFFFFF;padding:5px 13px;border-radius:12px}
.nav__hub{background:var(--haze);color:var(--ink);font-weight:600}
.nav__hub[aria-current="page"]{background:transparent;color:var(--slate);
                               box-shadow:inset 0 0 0 1.5px var(--haze)}

/* panels */
.catbtn{background:#141C25;color:var(--ink);box-shadow:var(--shadow-soft);
        outline:1px solid var(--haze);outline-offset:-1px}
.catbtn::after{background:var(--monarch)}
.catbtn__icon{color:var(--tide)}
.catbtn__label{font-weight:800;letter-spacing:-.03em}
.catbtn__blurb{color:var(--slate)}
.catbtn__go{color:var(--monarch);font-weight:600}

.card{background:#141C25;outline:1px solid var(--haze);outline-offset:-1px;
      box-shadow:var(--shadow-soft)}
.card::before{background:var(--monarch)}
.card.is-active{box-shadow:var(--shadow)}
.card__title{font-weight:700;letter-spacing:-.025em}
.card__blurb{color:var(--slate)}
.card__icon{color:var(--tide)}
.card__soon{background:var(--monarch);color:var(--on-flood);font-weight:700}
.card.is-soon{filter:saturate(.35) brightness(.9)}
.card.is-soon.is-active{filter:saturate(.6) brightness(.95)}

.arrow{background:#141C25;border-color:var(--haze);color:var(--ink)}
.extralink{background:#141C25;color:var(--tide);box-shadow:inset 0 0 0 1.5px var(--haze)}
.extralink[aria-disabled="true"]{color:var(--slate);background:transparent}
.back{color:var(--tide)}

.route__rail{background:var(--haze)}
.route__done{background:var(--monarch)}
.stop::before{background:var(--paper);box-shadow:inset 0 0 0 2px var(--haze)}
.stop.is-done::before{background:var(--monarch);box-shadow:none}
.route__pos{color:var(--slate)}

.cta{background:var(--haze);color:var(--ink);box-shadow:var(--shadow-soft)}
.cta.is-disabled{background:#131A22;color:#6D808F;box-shadow:none}
.cta-note{color:var(--slate)}

.foot{background:#0D141B;color:var(--slate);border-top:1px solid var(--haze)}
.foot a{color:var(--monarch)}

@media (max-width:700px){
  .arrow{background:rgba(20,28,37,.94);box-shadow:0 3px 14px rgba(0,0,0,.6)}
}

/* The brightest of the three: a saturated cyan-leaning sky blue. Reads as
   energy and daylight against the near-black ground — the most "tech" of the
   set, and the furthest from the muted blue in the mark. */

:root{
  --tide:#7DD3FC;      /* links, card icons, back arrow */
  --monarch:#7DD3FC;   /* the accent rules the base page inherited */
  --accent:#7DD3FC;
  --on-accent:#04141F;
  --flood:linear-gradient(135deg,#9BE0FD 0%,#5CC3F5 100%);
  --on-flood:#04141F;
  --on-flood-soft:rgba(4,20,31,.86);
  --beacon:rgba(125,211,252,.34);
  --glow:rgba(125,211,252,.26);
}

/* ── phone ──
   Measured at 390px on 2026-08-28. The arrows were 42x42, under the 44x44 touch
   minimum, on the one device class where touch is the only input. They float
   over the stage rather than taking grid columns, so 44 costs no layout.

   The route stops stay 26px wide and that is deliberate: nine of them at 44px
   need 396px of rail inside a 374px content box. The geometry does not allow it.
   They are a convenience — the arrows, the card taps and the keyboard arrows all
   do the same job at full size — so the dots keep their 44px HEIGHT and lose
   width, rather than the rail overflowing or the count being hidden. */
@media (max-width:700px){
  .arrow{width:44px;height:44px}
}
</style>
</head>
<body>
<a class="skip" href="#view">Skip to content</a>

<header class="nav">
  <a class="nav__brand" href="#hub" aria-label="Monarch Agency Solutions — Insurance Hub home">
    <img class="nav__logo" src="data:image/png;base64,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" alt="Monarch Agency Solutions">
  </a>
  <a class="nav__hub" id="navHub" href="#hub">Hub</a>
</header>

<main id="view" tabindex="-1"></main>

<footer class="foot">
  <p class="foot__contact" id="footContact"></p>
  <p class="foot__legal">Monarch Agency Solutions. This page provides information and referrals only.
     It is not a quote, an offer of insurance, or a guarantee of coverage. Eligibility and final
     terms are determined by the carrier during underwriting.</p>
</footer>

<svg id="sprite" aria-hidden="true" style="display:none" xmlns="http://www.w3.org/2000/svg">
<symbol id="art-cat-health" viewBox="0 0 64 48" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M32 41s-14-8.6-14-17.8A7.9 7.9 0 0 1 32 17.4 7.9 7.9 0 0 1 46 23.2C46 32.4 32 41 32 41Z" fill="currentColor" fill-opacity=".15" stroke="none"/><path d="M32 41s-14-8.6-14-17.8A7.9 7.9 0 0 1 32 17.4 7.9 7.9 0 0 1 46 23.2C46 32.4 32 41 32 41Z"/><path d="M19.5 26h5.7l2.6-4.6 3.9 9.2 2.6-4.6h9.7"/></symbol>
<symbol id="art-cat-life" viewBox="0 0 64 48" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M32 7 47 12.5v11.7c0 8.6-6.3 14.6-15 17.2-8.7-2.6-15-8.6-15-17.2V12.5L32 7Z"/><path d="M32 34s-7.6-4.7-7.6-9.8A4.3 4.3 0 0 1 32 21.5a4.3 4.3 0 0 1 7.6 2.7c0 5.1-7.6 9.8-7.6 9.8Z" fill="currentColor" fill-opacity=".16" stroke="none"/><path d="M32 34s-7.6-4.7-7.6-9.8A4.3 4.3 0 0 1 32 21.5a4.3 4.3 0 0 1 7.6 2.7c0 5.1-7.6 9.8-7.6 9.8Z"/></symbol>
<symbol id="art-cat-pc" viewBox="0 0 64 48" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M11 25 32 8l21 17"/><path d="M16.5 22.5V41h31V22.5"/><rect x="26.5" y="29" width="11" height="12" rx="1.5" fill="currentColor" fill-opacity=".16" stroke="none"/><path d="M26.5 41V29h11v12"/></symbol>
<symbol id="art-cat-business" viewBox="0 0 64 48" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M14 41V9h20v32"/><path d="M19 15h4M29 15h1M19 22h4M29 22h1M19 29h4M29 29h1"/><path d="M34 41V22h14v19" fill="currentColor" fill-opacity=".16"/><path d="M34 41V22h14v19"/><path d="M39 28h4M39 34h4"/><path d="M10 41h44"/></symbol>

<symbol id="art-aca" viewBox="0 0 64 48" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M13 21 32 10l19 11Z" fill="currentColor" fill-opacity=".16" stroke="none"/><path d="M13 21 32 10l19 11"/><path d="M18 24v12M26 24v12M32 24v12M38 24v12M46 24v12"/><path d="M15 36h34M12 40h40"/></symbol>
<symbol id="art-private" viewBox="0 0 64 48" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M32 7 47 12.5v11.7c0 8.6-6.3 14.6-15 17.2-8.7-2.6-15-8.6-15-17.2V12.5L32 7Z" fill="currentColor" fill-opacity=".1"/><circle cx="32" cy="21" r="4"/><path d="M24 33.5c1.6-4.2 4.5-6.3 8-6.3s6.4 2.1 8 6.3"/></symbol>
<symbol id="art-senior" viewBox="0 0 64 48" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><circle cx="28" cy="12" r="4.2" fill="currentColor" fill-opacity=".16"/><path d="M28 16.5V29"/><path d="M28 29l-4.5 12M28 29l4.5 12"/><path d="M22.5 22.5 28 20l5.5 3"/><path d="M42 19v22"/><path d="M42 19c0-2.4 3.4-2.4 3.4 0"/><path d="M38.5 41h7"/></symbol>
<symbol id="art-dental" viewBox="0 0 64 48" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M21 16.5c0-4.6 3.7-7.5 7.3-7.5 2.2 0 3.3.9 3.7.9s1.5-.9 3.7-.9c3.6 0 7.3 2.9 7.3 7.5 0 5.6-1.8 8.3-2.9 14-.9 4.5-1.3 10.1-3.8 10.1-2.2 0-2.7-4.9-4.3-4.9s-2.1 4.9-4.3 4.9c-2.5 0-2.9-5.6-3.8-10.1-1.1-5.7-2.9-8.4-2.9-14Z" fill="currentColor" fill-opacity=".1"/><path d="M27 16.5c1.6-1 3.4-1 5 0"/></symbol>

<symbol id="art-whole" viewBox="0 0 64 48" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M32 7 47 12.5v11.7c0 8.6-6.3 14.6-15 17.2-8.7-2.6-15-8.6-15-17.2V12.5L32 7Z"/><path d="M25.5 24.5c0-2.2 1.6-3.8 3.6-3.8 2.9 0 3.8 3.4 5.1 3.4s2.2-1.8 3.8-1.8c2 0 3.6 1.6 3.6 3.8s-1.6 3.8-3.6 3.8c-2.9 0-3.8-3.4-5.1-3.4s-2.2 1.8-3.8 1.8c-2 0-3.6-1.6-3.6-3.8Z" fill="currentColor" fill-opacity=".16"/></symbol>
<symbol id="art-iul" viewBox="0 0 64 48" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M15 33.5l8.5-6.5 6 4.5L38 20l9 6.5V39H15V33.5Z" fill="currentColor" fill-opacity=".16" stroke="none"/><path d="M15 33.5l8.5-6.5 6 4.5L38 20l9 6.5"/><path d="M13 39h38"/><path d="M13 35.5h38" stroke-dasharray="3 3.5" stroke-width="1.6"/><path d="M42 20h5v5"/></symbol>
<symbol id="art-term" viewBox="0 0 64 48" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><rect x="14" y="11" width="36" height="30" rx="3"/><path d="M14 20h36" /><path d="M14 11h36v9H14z" fill="currentColor" fill-opacity=".16" stroke="none"/><path d="M23 7.5v6M41 7.5v6"/><path d="M22 32h20"/><path d="M22 28.5v7M42 28.5v7"/></symbol>
<symbol id="art-final" viewBox="0 0 64 48" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M32 24s-7-4.4-7-9A3.9 3.9 0 0 1 32 12.5a3.9 3.9 0 0 1 7 2.5c0 4.6-7 9-7 9Z" fill="currentColor" fill-opacity=".16"/><path d="M19 29v6.5A6.5 6.5 0 0 0 25.5 42h13a6.5 6.5 0 0 0 6.5-6.5V29"/><path d="M19 29a3 3 0 0 1 6 0M39 29a3 3 0 0 1 6 0"/></symbol>
<symbol id="art-mortgage" viewBox="0 0 64 48" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M10 26 26 13l11 8.9"/><path d="M14.5 24v17h17V24"/><path d="M20 41V32h6v9"/><path d="M45 22.5l8 2.8v5.9c0 4-3.4 6.6-8 7.8-4.6-1.2-8-3.8-8-7.8v-5.9l8-2.8Z" fill="currentColor" fill-opacity=".16"/></symbol>

<symbol id="art-auto" viewBox="0 0 64 48" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M18.5 25.5l2.8-6.3A3 3 0 0 1 24 17.5h16a3 3 0 0 1 2.7 1.7l2.8 6.3Z" fill="currentColor" fill-opacity=".16"/><path d="M14 33v-6l4.5-8.6A4 4 0 0 1 22 16h20a4 4 0 0 1 3.5 2.4L50 27v6"/><path d="M14 26.5h36"/><circle cx="21.5" cy="33" r="3.4"/><circle cx="42.5" cy="33" r="3.4"/><path d="M14 33h4.1M45.9 33H50"/></symbol>
<symbol id="art-home" viewBox="0 0 64 48" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M11 25 32 8l21 17"/><path d="M16.5 22.5V41h31V22.5"/><rect x="26.5" y="29" width="11" height="12" rx="1.5" fill="currentColor" fill-opacity=".16" stroke="none"/><path d="M26.5 41V29h11v12"/><path d="M41 13.5V9h4v7.7"/></symbol>
<symbol id="art-renters" viewBox="0 0 64 48" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><rect x="14" y="9" width="21" height="32" rx="2.5"/><path d="M14 9h21v8H14z" fill="currentColor" fill-opacity=".16" stroke="none"/><path d="M20 22h9M20 29h9M20 36h9"/><circle cx="45" cy="20" r="4.5"/><path d="M45 24.5V38"/><path d="M45 29h4.5M45 33.5h3.5"/></symbol>
<symbol id="art-commercial" viewBox="0 0 64 48" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M11 34V16h20v18"/><path d="M16 21h4M16 27h4"/><path d="M31 23h8.5l6.5 6.5V34H31Z" fill="currentColor" fill-opacity=".16"/><path d="M31 23h8.5l6.5 6.5V34"/><path d="M9 34h37"/><circle cx="19" cy="35" r="3.2"/><circle cx="40" cy="35" r="3.2"/></symbol>
<symbol id="art-liability" viewBox="0 0 64 48" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M32 14.5V40"/><path d="M24 40h16"/><path d="M17 19h30"/><circle cx="32" cy="11.5" r="2.8"/><path d="M17 19l-5.5 10a6 6 0 0 0 11 0L17 19Z" fill="currentColor" fill-opacity=".16"/><path d="M47 19l-5.5 10a6 6 0 0 0 11 0L47 19Z"/></symbol>
<symbol id="art-eo" viewBox="0 0 64 48" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M17 8h15l10 10v14"/><path d="M42 32v6a2 2 0 0 1-2 2H19a2 2 0 0 1-2-2V10a2 2 0 0 1 2-2Z" stroke="none" fill="none"/><path d="M17 10a2 2 0 0 1 2-2v32a2 2 0 0 1-2-2Z" stroke="none" fill="none"/><path d="M17 8v32a2 2 0 0 0 2 2h11"/><path d="M32 8v10h10" fill="currentColor" fill-opacity=".16"/><path d="M23 23h9M23 29h6"/><circle cx="41" cy="33" r="6.5"/><path d="M45.8 37.8 51 43"/></symbol>
<symbol id="art-liquor" viewBox="0 0 64 48" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M17 10h13l-1.1 10.5a5.4 5.4 0 0 1-10.8 0L17 10Z"/><path d="M23.5 26v11"/><path d="M18.5 38h10"/><path d="M39 9h6v6.5l3 6V39a2 2 0 0 1-2 2h-8a2 2 0 0 1-2-2V21.5l3-6.5V9Z"/><path d="M36 26h12v13a2 2 0 0 1-2 2h-8a2 2 0 0 1-2-2V26Z" fill="currentColor" fill-opacity=".16" stroke="none"/></symbol>
<symbol id="art-workcomp" viewBox="0 0 64 48" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M12 34a20 20 0 0 1 40 0Z" fill="currentColor" fill-opacity=".12"/><path d="M10 34h44"/><path d="M26 15.5v-1.5a2.5 2.5 0 0 1 2.5-2.5h7a2.5 2.5 0 0 1 2.5 2.5v1.5"/><path d="M26 15.5c-3.4 2.4-4.5 6.6-4.5 10.5M38 15.5c3.4 2.4 4.5 6.6 4.5 10.5"/><path d="M26 15.5h12"/></symbol>
<symbol id="art-cyber" viewBox="0 0 64 48" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M32 7 47 12.5v11.7c0 8.6-6.3 14.6-15 17.2-8.7-2.6-15-8.6-15-17.2V12.5L32 7Z"/><rect x="26" y="23" width="12" height="10" rx="2" fill="currentColor" fill-opacity=".16"/><path d="M29 23v-3.5a3 3 0 0 1 6 0V23"/><path d="M32 27v2.5"/></symbol>

<symbol id="art-group" viewBox="0 0 64 48" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><circle cx="32" cy="14" r="4.6" fill="currentColor" fill-opacity=".16"/><circle cx="19" cy="18.5" r="3.6"/><circle cx="45" cy="18.5" r="3.6"/><path d="M23 34.5c0-5 4-8.7 9-8.7s9 3.7 9 8.7"/><path d="M11.5 34.5c0-3.9 3-6.9 7-6.9M52.5 34.5c0-3.9-3-6.9-7-6.9"/><path d="M10 40h44"/></symbol>
<symbol id="art-benefits" viewBox="0 0 64 48" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><rect x="13" y="17" width="38" height="23" rx="3"/><path d="M13 17h38v8H13z" fill="currentColor" fill-opacity=".16" stroke="none"/><path d="M25 17v-3a2.5 2.5 0 0 1 2.5-2.5h9A2.5 2.5 0 0 1 39 14v3"/><path d="M32 27v8M28 31h8"/></symbol>
<symbol id="art-keyperson" viewBox="0 0 64 48" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><circle cx="25" cy="15" r="5"/><path d="M14 38c0-6.1 4.9-10.6 11-10.6S36 31.9 36 38"/><circle cx="45" cy="18" r="4.6" fill="currentColor" fill-opacity=".16"/><path d="M45 22.6V36"/><path d="M45 27h4.5M45 31.5h3.5"/></symbol>
<symbol id="art-owner" viewBox="0 0 64 48" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><circle cx="30" cy="18" r="5.4"/><path d="M18 40c0-6.6 5.4-11.5 12-11.5S42 33.4 42 40"/><path d="M46 7l1.7 3.5 3.8.6-2.8 2.7.7 3.8-3.4-1.8-3.4 1.8.7-3.8-2.8-2.7 3.8-.6L46 7Z" fill="currentColor" fill-opacity=".2"/></symbol>
</svg>

<script>
/* ─────────────────────────────────────────────────────────────────────
   EDIT BELOW — this is the only part of the file you need to touch.

   Paste your real link between the quote marks after  url:
   Leave a url as ""  and that card shows "Coming soon" instead of
   linking anywhere. Nothing you type here can break the page.

   Links must start with  https://
   After editing, run:   node ../tools/check-hub-config.mjs
   ───────────────────────────────────────────────────────────────────── */
const HUB = {
  contact: { phone: "561-709-3617", email: "abinsurance561@gmail.com" },
  supplementalUrl: "",                 // <- the "Supplemental Coverage Not Listed" link
  categories: [
    {
      id: "health", label: "Health Insurance", art: "cat-health",
      blurb: "Medical coverage for you and your family.",
      cards: [
        { id: "aca", title: "ACA / Marketplace", art: "aca", url: "",
          blurb: "Marketplace plans with income-based subsidies. Enroll during open enrollment or after a qualifying life event." },
        { id: "private", title: "Private Health", art: "private", url: "",
          blurb: "Medically underwritten coverage priced on your age, sex, and tobacco use. Available year-round." },
        { id: "senior", title: "65+ Options", art: "senior", url: "",
          blurb: "Coverage built for age 65 and older, including supplement and advantage-style plans." },
        { id: "dental", title: "Dental + Vision", art: "dental", url: "",
          blurb: "Standalone cleanings, fillings, exams, frames, and lenses — usually not part of a medical plan." },
      ],
    },
    {
      id: "life", label: "Life Insurance", art: "cat-life",
      blurb: "Protection for the people who depend on you.",
      cards: [
        { id: "whole", title: "Whole Life", art: "whole", url: "",
          blurb: "Permanent coverage with a fixed premium that builds cash value you can borrow against." },
        { id: "iul", title: "Indexed Universal Life", art: "iul", url: "",
          blurb: "Permanent coverage whose cash value tracks a market index, with a floor that limits downside." },
        { id: "term", title: "Term Life", art: "term", url: "",
          blurb: "The most affordable way to cover a set number of years — typically 10, 20, or 30." },
        { id: "final", title: "Final Expense", art: "final", url: "",
          blurb: "A smaller whole-life policy sized to cover funeral, burial, and last medical bills." },
        { id: "mortgage", title: "Mortgage Protection", art: "mortgage", url: "",
          blurb: "Designed to cover the mortgage so your family can keep the house." },
      ],
    },
    {
      id: "pc", label: "Property & Casualty", art: "cat-pc",
      blurb: "Cover what you own, and what you could be held responsible for.",
      cards: [
        { id: "auto", title: "Auto", art: "auto", url: "",
          blurb: "Liability, collision, and comprehensive coverage for your personal vehicles." },
        { id: "home", title: "Home", art: "home", url: "",
          blurb: "Covers the structure, your belongings, and your liability if someone is hurt on the property." },
        { id: "renters", title: "Renters", art: "renters", url: "",
          blurb: "Covers your belongings and your liability in a place you don't own." },
        { id: "commercial", title: "Commercial Auto & Property", art: "commercial", url: "",
          blurb: "Vehicles, buildings, and equipment your business owns or leases." },
        { id: "liability", title: "General & Professional Liability", art: "liability", url: "",
          blurb: "Claims of bodily injury, property damage, or professional negligence against your business." },
        { id: "eo", title: "Errors & Omissions", art: "eo", url: "",
          blurb: "Protection when a client claims your professional advice or service caused them a loss." },
        { id: "liquor", title: "Liquor Liability", art: "liquor", url: "",
          blurb: "For businesses that serve or sell alcohol — often required by a lease or a license." },
        { id: "workcomp", title: "Workers' Compensation", art: "workcomp", url: "",
          blurb: "Medical bills and lost wages when an employee is injured on the job." },
        { id: "cyber", title: "Cyber Liability", art: "cyber", url: "",
          blurb: "Breach response, customer notification, and recovery costs after a data breach or ransomware." },
      ],
    },
    {
      id: "business", label: "Business Owner Options", art: "cat-business",
      blurb: "Coverage for you and the people who work for you.",
      cards: [
        { id: "group", title: "Group Health", art: "group", url: "",
          blurb: "Medical coverage offered to your employees, with the business sharing the premium." },
        { id: "benefits", title: "Employee Benefits", art: "benefits", url: "",
          blurb: "Dental, vision, disability, and life benefits that round out a package." },
        { id: "keyperson", title: "Key Person", art: "keyperson", url: "",
          blurb: "Pays the business if an owner or an essential employee dies or becomes disabled." },
        { id: "owner", title: "Owner Benefits", art: "owner", url: "",
          blurb: "Coverage structured for the owner personally, often more tax-efficient through the business." },
      ],
    },
  ],
};
/* ───────────────────────── STOP EDITING HERE ───────────────────────── */

const view = document.getElementById("view");
const navHub = document.getElementById("navHub");
const esc = (s) => String(s).replace(/[&<>"']/g, (c) =>
  ({ "&": "&amp;", "<": "&lt;", ">": "&gt;", '"': "&quot;", "'": "&#39;" }[c]));
const telHref = (p) => "tel:" + p.replace(/[^0-9+]/g, "");
const catById = (id) => HUB.categories.find((c) => c.id === id) || null;

function renderFooter() {
  const bits = [];
  if (HUB.contact.phone) bits.push(`<a href="${esc(telHref(HUB.contact.phone))}">${esc(HUB.contact.phone)}</a>`);
  if (HUB.contact.email) bits.push(`<a href="mailto:${esc(HUB.contact.email)}">${esc(HUB.contact.email)}</a>`);
  const el = document.getElementById("footContact");
  el.innerHTML = bits.join(" &middot; ");
  el.hidden = bits.length === 0;
}

function renderLanding() {
  const blocks = HUB.categories.map((c) => `
    <div class="cat${c.id === "business" ? " cat--wide" : ""}">
      <a class="catbtn" href="#${esc(c.id)}">
        <svg class="catbtn__icon" aria-hidden="true"><use href="#art-${esc(c.art)}"></use></svg>
        <span class="catbtn__label">${esc(c.label)}${
          c.id === "business" ? "<small>for Self &amp; Employees</small>" : ""}</span>
        <span class="catbtn__blurb">${esc(c.blurb)}</span>
        <span class="catbtn__go">See options <span aria-hidden="true">&rarr;</span></span>
      </a>
    </div>`).join("");

  const supp = HUB.supplementalUrl
    ? `<a class="extralink" href="${esc(HUB.supplementalUrl)}" target="_blank" rel="noopener noreferrer">
         Supplemental Coverage Not Listed <span aria-hidden="true">&rsaquo;</span>
         <span class="sr-only">(opens in a new tab)</span></a>`
    : `<span class="extralink" aria-disabled="true">Supplemental Coverage Not Listed &mdash; coming soon</span>`;

  view.innerHTML = `
    <section class="land">
      <p class="land__eyebrow">Monarch Agency Solutions</p>
      <h1 class="land__title">Find your coverage.</h1>
      <p class="land__sub">Pick a category and we'll take you straight to the right place.
         Not sure which one? Call us &mdash; that's what we're here for.</p>
      <div class="cats">${blocks}</div>
      <div class="land__extra">${supp}</div>
    </section>`;
  document.title = "Insurance Hub · Monarch Agency Solutions";
  navHub.setAttribute("aria-current", "page");
}

function renderCategory(category, cardId) {
  const cards = category.cards;
  const found = cards.findIndex((c) => c.id === cardId);
  let idx = found >= 0 ? found : 0;

  view.innerHTML = `
    <section class="cv">
      <a class="back" href="#hub"><span aria-hidden="true">&lsaquo;</span> All categories</a>
      <h1 class="cv__title">${esc(category.label)}</h1>
      <p class="cv__sub">${esc(category.blurb)}</p>

      <div class="carousel" role="group" aria-roledescription="carousel"
           aria-label="${esc(category.label)} options">
        <button class="arrow arrow--prev" id="prev" type="button" aria-label="Previous option">&lsaquo;</button>
        <div class="stage" id="stage">
          <div class="track" id="track">
            ${cards.map((c, i) => `
              <button class="card${c.url ? "" : " is-soon"}" type="button" data-i="${i}"
                      tabindex="${i === idx ? 0 : -1}"${c.url ? "" : ' aria-disabled="true"'}>
                <svg class="card__icon" aria-hidden="true"><use href="#art-${esc(c.art)}"></use></svg>
                ${c.url ? "" : '<span class="card__soon">Coming soon</span>'}
                <h2 class="card__title">${esc(c.title)}</h2>
                <p class="card__blurb">${esc(c.blurb)}</p>
              </button>`).join("")}
          </div>
        </div>
        <button class="arrow arrow--next" id="next" type="button" aria-label="Next option">&rsaquo;</button>
      </div>

      <div class="route">
        <div class="route__rail"></div>
        <div class="route__done" id="routeDone"></div>
        <div class="route__stops" id="stops">
          ${cards.map((c, i) => `<button class="stop" type="button" data-i="${i}"
              aria-label="Show ${esc(c.title)}"${i === idx ? ' aria-current="true"' : ""}></button>`).join("")}
        </div>
        <p class="route__pos" id="routePos"></p>
      </div>

      <a class="cta" id="cta"></a>
      <p class="cta-note" id="ctaNote" hidden></p>
      <p class="sr-only" aria-live="polite" id="live"></p>
    </section>`;

  const track = document.getElementById("track");
  const stage = document.getElementById("stage");
  const cta = document.getElementById("cta");
  const ctaNote = document.getElementById("ctaNote");
  const live = document.getElementById("live");
  const routeDone = document.getElementById("routeDone");
  const routePos = document.getElementById("routePos");
  const els = [...track.querySelectorAll(".card")];
  const stops = [...document.querySelectorAll(".stop")];
  const prev = document.getElementById("prev");
  const next = document.getElementById("next");

  function select(i, announce) {
    idx = Math.min(Math.max(i, 0), cards.length - 1);
    const card = cards[idx];

    els.forEach((el, n) => {
      el.classList.toggle("is-active", n === idx);
      el.tabIndex = n === idx ? 0 : -1;
    });
    stops.forEach((s, n) => {
      s.classList.toggle("is-done", n < idx);
      if (n === idx) s.setAttribute("aria-current", "true");
      else s.removeAttribute("aria-current");
    });

    const active = els[idx];
    const offset = active.offsetLeft + active.offsetWidth / 2 - stage.clientWidth / 2;
    track.style.transform = `translateX(${-offset}px)`;

    if (stops.length > 1) {
      const first = stops[0], cur = stops[idx];
      const span = stops[stops.length - 1].offsetLeft - first.offsetLeft;
      routeDone.style.width = span > 0 ? `${cur.offsetLeft - first.offsetLeft}px` : "0";
    }
    routePos.textContent = `${idx + 1} of ${cards.length}`;

    prev.disabled = idx === 0;
    next.disabled = idx === cards.length - 1;

    if (card.url) {
      cta.innerHTML = `Receive ${esc(card.title)} Options <span class="cta__arrow" aria-hidden="true">&rarr;</span>
                       <span class="sr-only">(opens in a new tab)</span>`;
      cta.href = card.url;
      cta.target = "_blank";
      cta.rel = "noopener noreferrer";
      cta.classList.remove("is-disabled");
      cta.removeAttribute("aria-disabled");
      ctaNote.hidden = true;
    } else {
      cta.textContent = `${card.title} — coming soon`;
      cta.removeAttribute("href");
      cta.removeAttribute("target");
      cta.classList.add("is-disabled");
      cta.setAttribute("aria-disabled", "true");
      ctaNote.hidden = false;
      ctaNote.innerHTML = HUB.contact.phone
        ? `Call <a href="${esc(telHref(HUB.contact.phone))}">${esc(HUB.contact.phone)}</a> and we'll walk you through this one.`
        : "Give us a call and we'll walk you through this one.";
    }

    const hash = `#${category.id}/${card.id}`;
    if (location.hash !== hash) history.replaceState(null, "", hash);
    if (announce) live.textContent = `${card.title}, ${idx + 1} of ${cards.length}`;
  }

  els.forEach((el, n) => el.addEventListener("click", () => {
    if (n !== idx) { select(n, true); els[n].focus(); return; }
    if (cards[n].url) window.open(cards[n].url, "_blank", "noopener,noreferrer");
  }));
  stops.forEach((s, n) => s.addEventListener("click", () => select(n, true)));
  prev.addEventListener("click", () => select(idx - 1, true));
  next.addEventListener("click", () => select(idx + 1, true));

  track.addEventListener("keydown", (e) => {
    const jump = { ArrowRight: idx + 1, ArrowLeft: idx - 1, Home: 0, End: cards.length - 1 };
    if (!(e.key in jump)) return;
    e.preventDefault();
    select(jump[e.key], true);
    els[idx].focus();
  });

  let x0 = null;
  stage.addEventListener("pointerdown", (e) => { x0 = e.clientX; });
  stage.addEventListener("pointerup", (e) => {
    if (x0 === null) return;
    const dx = e.clientX - x0;
    x0 = null;
    if (Math.abs(dx) > 40) select(idx + (dx < 0 ? 1 : -1), true);
  });
  stage.addEventListener("pointercancel", () => { x0 = null; });

  window.addEventListener("resize", onResize, { passive: true });
  function onResize() {
    if (!document.body.contains(track)) {
      window.removeEventListener("resize", onResize);
      return;
    }
    select(idx, false);
  }

  document.title = `${category.label} · Monarch Insurance Hub`;
  select(idx, false);
}

function parseHash() {
  const raw = location.hash.replace(/^#/, "");
  if (!raw || raw === "hub") return { cat: null, card: null };
  const [cat, card] = raw.split("/");
  return { cat: cat || null, card: card || null };
}

function route() {
  const { cat, card } = parseHash();
  const category = cat ? catById(cat) : null;
  if (cat && !category) {
    history.replaceState(null, "", location.pathname + location.search);
    renderLanding();
    return;
  }
  if (!category) { renderLanding(); return; }
  navHub.removeAttribute("aria-current");
  renderCategory(category, card);
}

let lastHash = location.hash;
window.addEventListener("hashchange", () => {
  const now = location.hash;
  const sameCategory = parseHash().cat && lastHash.split("/")[0] === now.split("/")[0];
  lastHash = now;
  if (sameCategory) return;   // card-level replaceState, already rendered
  route();
  view.focus();
});

renderFooter();
route();
</script>
</body>
</html>
