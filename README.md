<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>GIRS Internacional — Experiencias Innovadoras · ONU-Hábitat</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,700;0,900;1,700&family=DM+Sans:wght@300;400;500;600&family=DM+Mono:wght@400;500&display=swap" rel="stylesheet">
<style>
/* ─── Reset & Base ─────────────────────────────────────────────────── */
*, *::before, *::after { margin:0; padding:0; box-sizing:border-box; }
:root {
  --ink:    #0D1117;
  --ink2:   #1E2532;
  --muted:  #6B7280;
  --muted2: #9CA3AF;
  --paper:  #F8F6F1;
  --white:  #FFFFFF;
  --az:     #1A3A5C;
  --az2:    #2E75B6;
  --az3:    #DBEAFE;
  --ve:     #0F5132;
  --ve2:    #DCFCE7;
  --na:     #C55A11;
  --na2:    #FEF3C7;
  --mo:     #5B21B6;
  --mo2:    #EDE9FE;
  --ro:     #991B1B;
  --ro2:    #FEE2E2;
  --am:     #92400E;
  --am2:    #FEF9C3;
  --te:     #065F46;
  --te2:    #D1FAE5;
  --gold:   #D4A017;
  --accent: #E63946;
  --r: .75rem;
  --r2: 1.25rem;
  --shadow: 0 2px 12px rgba(0,0,0,.08);
  --shadow2: 0 8px 40px rgba(0,0,0,.14);
}
html { scroll-behavior: smooth; }
body {
  font-family: 'DM Sans', sans-serif;
  background: var(--paper);
  color: var(--ink);
  line-height: 1.65;
  overflow-x: hidden;
}
/* ─── Scrollbar ─────────────────────────────────────────────────────── */
::-webkit-scrollbar { width:6px; }
::-webkit-scrollbar-track { background: var(--paper); }
::-webkit-scrollbar-thumb { background: var(--az2); border-radius:3px; }

/* ─── HERO ──────────────────────────────────────────────────────────── */
.hero {
  min-height: 100vh;
  background: var(--ink);
  position: relative;
  display: flex;
  flex-direction: column;
  justify-content: center;
  padding: 6rem 4vw 4rem;
  overflow: hidden;
}
.hero-grid {
  position: absolute; inset: 0;
  background-image:
    linear-gradient(rgba(46,117,182,.06) 1px, transparent 1px),
    linear-gradient(90deg, rgba(46,117,182,.06) 1px, transparent 1px);
  background-size: 60px 60px;
}
.hero-accent {
  position: absolute; top: -120px; right: -120px;
  width: 600px; height: 600px; border-radius: 50%;
  background: radial-gradient(circle, rgba(46,117,182,.18) 0%, transparent 70%);
  pointer-events: none;
}
.hero-accent2 {
  position: absolute; bottom: -80px; left: -80px;
  width: 400px; height: 400px; border-radius: 50%;
  background: radial-gradient(circle, rgba(212,160,23,.1) 0%, transparent 70%);
  pointer-events: none;
}
.hero-badge {
  display: inline-flex; align-items: center; gap: .5rem;
  background: rgba(46,117,182,.2); border: 1px solid rgba(46,117,182,.4);
  color: #93C5FD; font-size: .75rem; font-weight: 600; letter-spacing: .1em;
  padding: .35rem .9rem; border-radius: 100px; margin-bottom: 2rem;
  text-transform: uppercase; width: fit-content;
}
.hero h1 {
  font-family: 'Playfair Display', serif;
  font-size: clamp(2.8rem, 6vw, 5.5rem);
  font-weight: 900; color: var(--white);
  line-height: 1.05; max-width: 900px; margin-bottom: 1.5rem;
}
.hero h1 em { color: var(--gold); font-style: italic; }
.hero-sub {
  color: #9CA3AF; font-size: 1.1rem; max-width: 560px;
  margin-bottom: 2.5rem; line-height: 1.7;
}
.hero-stats {
  display: flex; gap: 2.5rem; flex-wrap: wrap; margin-bottom: 3rem;
}
.hero-stat-item { color: var(--white); }
.hero-stat-num {
  font-family: 'Playfair Display', serif;
  font-size: 2.8rem; font-weight: 700; color: var(--gold);
  display: block; line-height: 1;
}
.hero-stat-label { font-size: .8rem; color: #6B7280; margin-top: .25rem; letter-spacing: .06em; }
.hero-ctas { display: flex; gap: 1rem; flex-wrap: wrap; }
.btn {
  display: inline-flex; align-items: center; gap: .5rem;
  padding: .8rem 1.8rem; border-radius: 100px;
  font-size: .9rem; font-weight: 600; cursor: pointer;
  text-decoration: none; transition: all .2s; border: none;
}
.btn-primary { background: var(--az2); color: var(--white); }
.btn-primary:hover { background: #1E5FA0; transform: translateY(-1px); box-shadow: 0 6px 20px rgba(46,117,182,.4); }
.btn-ghost { background: transparent; color: #9CA3AF; border: 1px solid #374151; }
.btn-ghost:hover { border-color: var(--az2); color: var(--az2); }

/* ─── NAV ───────────────────────────────────────────────────────────── */
nav {
  position: sticky; top: 0; z-index: 200;
  background: rgba(13,17,23,.95); backdrop-filter: blur(12px);
  border-bottom: 1px solid #1F2937;
  display: flex; align-items: center; justify-content: space-between;
  padding: .9rem 4vw; gap: 1rem;
}
.nav-logo {
  font-family: 'Playfair Display', serif;
  font-size: 1.1rem; color: var(--white); font-weight: 700;
}
.nav-logo span { color: var(--gold); }
.nav-links { display: flex; gap: .25rem; }
.nav-link {
  color: #6B7280; font-size: .82rem; font-weight: 500;
  padding: .4rem .85rem; border-radius: 100px; cursor: pointer;
  transition: all .2s; text-decoration: none; white-space: nowrap;
}
.nav-link:hover, .nav-link.active { background: rgba(46,117,182,.2); color: #93C5FD; }

/* ─── SECTIONS ──────────────────────────────────────────────────────── */
section { padding: 5rem 4vw; }
.section-header { margin-bottom: 3rem; }
.section-eyebrow {
  font-size: .72rem; font-weight: 700; letter-spacing: .15em;
  text-transform: uppercase; color: var(--az2); margin-bottom: .6rem;
}
.section-title {
  font-family: 'Playfair Display', serif;
  font-size: clamp(1.8rem, 3.5vw, 2.8rem); font-weight: 700;
  color: var(--ink); line-height: 1.15;
}
.section-title em { color: var(--az2); font-style: italic; }
.section-desc { color: var(--muted); max-width: 560px; margin-top: .75rem; font-size: .95rem; }

/* ─── MAP SECTION ───────────────────────────────────────────────────── */
#map-section { background: var(--ink); padding: 5rem 0 0; }
#map-section .section-eyebrow { color: #93C5FD; }
#map-section .section-title { color: var(--white); }
#map-section .section-desc { color: #9CA3AF; }
.map-header { padding: 0 4vw 2rem; }
.map-container {
  width: 100%; height: 520px; position: relative;
  background: #0D1117;
}
/* SVG World Map */
.world-map-svg {
  width: 100%; height: 100%;
  display: block;
}
.map-pin {
  cursor: pointer; transition: transform .2s;
  transform-origin: center;
}
.map-pin:hover { transform: scale(1.3); }
.map-pin circle.outer {
  fill: rgba(46,117,182,.25); animation: pulse-pin 2.5s ease-in-out infinite;
}
.map-pin.tema-b circle.outer {
  fill: rgba(15,81,50,.3); animation: pulse-pin-green 2.5s ease-in-out infinite;
}
@keyframes pulse-pin {
  0%,100% { r:18; opacity:.6; }
  50%       { r:26; opacity:.2; }
}
@keyframes pulse-pin-green {
  0%,100% { r:18; opacity:.6; }
  50%       { r:26; opacity:.2; }
}
.map-tooltip {
  position: absolute; background: var(--white); border-radius: var(--r2);
  padding: 1rem 1.25rem; box-shadow: var(--shadow2);
  min-width: 200px; pointer-events: none; opacity: 0;
  transition: opacity .2s; z-index: 50;
}
.map-tooltip.visible { opacity: 1; }
.mt-num { font-family: 'DM Mono', monospace; font-size: .7rem; color: var(--az2); font-weight: 500; }
.mt-name { font-weight: 700; font-size: .9rem; color: var(--ink); margin: .15rem 0; }
.mt-country { font-size: .78rem; color: var(--muted); }
.mt-score {
  margin-top: .6rem; padding: .35rem .75rem; border-radius: 100px;
  font-size: .78rem; font-weight: 700; display: inline-block;
}
.map-legend {
  display: flex; gap: 1.5rem; padding: 1.25rem 4vw;
  background: #111827; border-top: 1px solid #1F2937;
  flex-wrap: wrap;
}
.ml-item { display: flex; align-items: center; gap: .5rem; }
.ml-dot { width:10px; height:10px; border-radius:50%; }
.ml-label { font-size: .78rem; color: #9CA3AF; }

/* ─── INDEX TABLE ───────────────────────────────────────────────────── */
#index-section { background: var(--white); }
.index-controls {
  display: flex; gap: .75rem; margin-bottom: 2rem; flex-wrap: wrap;
}
.filter-btn {
  padding: .45rem 1.1rem; border-radius: 100px; border: 1.5px solid #E5E7EB;
  background: var(--white); color: var(--muted); font-size: .82rem;
  font-weight: 600; cursor: pointer; transition: all .18s;
}
.filter-btn:hover { border-color: var(--az2); color: var(--az2); }
.filter-btn.active { background: var(--az2); border-color: var(--az2); color: var(--white); }
.index-table-wrap { overflow-x: auto; border-radius: var(--r2); box-shadow: var(--shadow); }
table { width: 100%; border-collapse: collapse; }
thead tr { background: var(--ink); }
thead th {
  padding: .9rem 1rem; text-align: left;
  font-size: .72rem; font-weight: 700; letter-spacing: .08em;
  color: #9CA3AF; text-transform: uppercase; white-space: nowrap;
}
thead th:first-child { border-radius: var(--r2) 0 0 0; }
thead th:last-child  { border-radius: 0 var(--r2) 0 0; }
tbody tr { border-bottom: 1px solid #F3F4F6; transition: background .15s; cursor: pointer; }
tbody tr:hover { background: var(--az3); }
tbody tr:last-child { border-bottom: none; }
td { padding: .8rem 1rem; font-size: .88rem; vertical-align: middle; }
.td-num { font-family: 'DM Mono', monospace; font-size: .72rem; color: var(--az2); font-weight: 600; }
.td-name { font-weight: 700; color: var(--ink); }
.td-country { color: var(--muted); font-size: .8rem; }
.dim-score {
  display: inline-flex; align-items: center; justify-content: center;
  width: 28px; height: 28px; border-radius: 6px;
  font-family: 'DM Mono', monospace; font-size: .82rem; font-weight: 700;
}
.ds-high { background: var(--ve2); color: var(--ve); }
.ds-mid  { background: var(--am2); color: var(--am); }
.ds-low  { background: var(--ro2); color: var(--ro); }
.total-badge {
  font-family: 'Playfair Display', serif;
  font-size: 1.2rem; font-weight: 900;
}
.nivel-badge {
  padding: .3rem .8rem; border-radius: 100px;
  font-size: .72rem; font-weight: 700; letter-spacing: .06em;
  text-transform: uppercase; white-space: nowrap;
}
.nivel-alta { background: var(--ve2); color: var(--ve); }
.nivel-media { background: var(--na2); color: var(--na); }

/* ─── DIM LEGEND ────────────────────────────────────────────────────── */
.dim-legend {
  display: flex; gap: .75rem; margin-bottom: 1.5rem; flex-wrap: wrap;
}
.dim-chip {
  padding: .3rem .75rem; border-radius: 100px;
  font-size: .72rem; font-weight: 600; letter-spacing: .04em;
}

/* ─── FICHAS GRID ───────────────────────────────────────────────────── */
#fichas-section { background: var(--paper); }
.fichas-filters {
  display: flex; gap: .5rem; margin-bottom: 2.5rem; flex-wrap: wrap;
}
.fichas-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(340px, 1fr));
  gap: 1.75rem;
}
.ficha-card {
  background: var(--white); border-radius: var(--r2);
  box-shadow: var(--shadow); overflow: hidden;
  cursor: pointer; transition: all .25s;
  display: flex; flex-direction: column;
}
.ficha-card:hover {
  transform: translateY(-4px);
  box-shadow: var(--shadow2);
}
.ficha-card.hidden { display: none; }
.fc-stripe {
  height: 6px; width: 100%;
}
.fc-header {
  padding: 1.25rem 1.5rem .75rem;
  display: flex; align-items: flex-start; justify-content: space-between; gap: 1rem;
}
.fc-num-wrap { display: flex; align-items: center; gap: .75rem; }
.fc-num {
  font-family: 'DM Mono', monospace; font-size: .65rem; font-weight: 700;
  color: var(--muted); letter-spacing: .1em;
}
.fc-tema {
  font-size: .68rem; font-weight: 700; letter-spacing: .08em;
  text-transform: uppercase; padding: .22rem .65rem;
  border-radius: 100px; white-space: nowrap;
}
.tema-a { background: var(--az3); color: var(--az); }
.tema-b { background: var(--ve2); color: var(--ve); }
.fc-title {
  font-family: 'Playfair Display', serif;
  font-size: 1.15rem; font-weight: 700; color: var(--ink);
  padding: 0 1.5rem; line-height: 1.25; margin-bottom: .3rem;
}
.fc-location {
  padding: 0 1.5rem; font-size: .8rem; color: var(--muted);
  margin-bottom: .9rem; display: flex; align-items: center; gap: .35rem;
}
.fc-desc {
  padding: 0 1.5rem; font-size: .85rem; color: #4B5563;
  line-height: 1.6; flex: 1; margin-bottom: 1rem;
}
.fc-scores {
  padding: .9rem 1.5rem; background: var(--paper);
  border-top: 1px solid #F3F4F6;
}
.fc-score-row {
  display: flex; align-items: center; justify-content: space-between;
  margin-bottom: .45rem;
}
.fc-score-label { font-size: .72rem; color: var(--muted); font-weight: 500; }
.fc-score-bar-wrap {
  flex: 1; height: 6px; background: #E5E7EB; border-radius: 3px;
  margin: 0 .75rem; overflow: hidden;
}
.fc-score-bar { height: 100%; border-radius: 3px; transition: width .6s ease; }
.fc-score-val { font-family: 'DM Mono', monospace; font-size: .72rem; font-weight: 700; }
.fc-footer {
  padding: 1rem 1.5rem;
  display: flex; align-items: center; justify-content: space-between;
  border-top: 1px solid #F3F4F6;
}
.fc-total {
  font-family: 'Playfair Display', serif; font-size: 1.5rem; font-weight: 900;
}
.fc-nivel { }
.fc-btn {
  background: none; border: none; color: var(--az2);
  font-size: .82rem; font-weight: 600; cursor: pointer;
  display: flex; align-items: center; gap: .3rem;
}

/* ─── MODAL ─────────────────────────────────────────────────────────── */
.modal-overlay {
  position: fixed; inset: 0; z-index: 1000;
  background: rgba(0,0,0,.7); backdrop-filter: blur(4px);
  display: flex; align-items: center; justify-content: center;
  padding: 1.5rem; opacity: 0; pointer-events: none; transition: opacity .25s;
}
.modal-overlay.open { opacity: 1; pointer-events: all; }
.modal {
  background: var(--white); border-radius: var(--r2);
  width: 100%; max-width: 800px; max-height: 90vh;
  overflow-y: auto; position: relative;
  transform: translateY(20px); transition: transform .3s;
  box-shadow: 0 24px 80px rgba(0,0,0,.3);
}
.modal-overlay.open .modal { transform: translateY(0); }
.modal-stripe { height: 8px; width: 100%; border-radius: var(--r2) var(--r2) 0 0; }
.modal-header { padding: 2rem 2rem 1rem; }
.modal-close {
  position: absolute; top: 1.25rem; right: 1.25rem;
  width: 36px; height: 36px; border-radius: 50%;
  background: #F3F4F6; border: none; cursor: pointer;
  display: flex; align-items: center; justify-content: center;
  font-size: 1rem; color: var(--muted); transition: all .15s;
}
.modal-close:hover { background: var(--accent); color: var(--white); }
.modal-num { font-family: 'DM Mono', monospace; font-size: .7rem; color: var(--az2); font-weight: 600; }
.modal-title {
  font-family: 'Playfair Display', serif;
  font-size: 1.7rem; font-weight: 700; color: var(--ink);
  line-height: 1.2; margin: .4rem 0 .5rem;
}
.modal-meta { display: flex; gap: .75rem; flex-wrap: wrap; align-items: center; }
.modal-country {
  display: flex; align-items: center; gap: .4rem;
  font-size: .83rem; color: var(--muted); font-weight: 500;
}
.modal-body { padding: 0 2rem 2rem; }
.modal-section-title {
  font-size: .7rem; font-weight: 800; letter-spacing: .14em;
  text-transform: uppercase; color: var(--az2);
  margin: 1.5rem 0 .6rem; display: flex; align-items: center; gap: .5rem;
}
.modal-section-title::after {
  content:''; flex:1; height:1px; background: var(--az3);
}
.modal-text { font-size: .9rem; color: #374151; line-height: 1.7; }
.modal-tags { display: flex; gap: .5rem; flex-wrap: wrap; margin-top: .75rem; }
.modal-tag {
  padding: .25rem .65rem; border-radius: 100px;
  font-size: .72rem; font-weight: 600;
}
/* Score grid inside modal */
.modal-scores-grid {
  display: grid; grid-template-columns: 1fr 1fr;
  gap: .75rem; margin-top: .75rem;
}
.modal-score-item {
  background: var(--paper); border-radius: var(--r); padding: .75rem;
}
.msi-label { font-size: .72rem; color: var(--muted); margin-bottom: .35rem; font-weight: 500; }
.msi-bar-wrap { height: 8px; background: #E5E7EB; border-radius: 4px; overflow:hidden; margin-bottom: .3rem; }
.msi-bar { height: 100%; border-radius: 4px; }
.msi-val { font-family: 'DM Mono', monospace; font-size: .85rem; font-weight: 700; }
.modal-total-row {
  display: flex; align-items: center; justify-content: space-between;
  background: var(--ink); border-radius: var(--r2);
  padding: 1.25rem 1.5rem; margin-top: 1rem;
}
.mtr-label { font-size: .75rem; color: #9CA3AF; font-weight: 600; letter-spacing: .06em; text-transform: uppercase; }
.mtr-total { font-family: 'Playfair Display', serif; font-size: 2.4rem; font-weight: 900; }
.mtr-nivel { }
/* ODS tags */
.ods-tag {
  padding: .28rem .65rem; border-radius: 6px;
  font-size: .7rem; font-weight: 700; color: var(--white);
}
/* Lección negativa badge */
.leccion-neg {
  background: var(--ro2); border: 1px solid #FCA5A5;
  border-radius: var(--r); padding: .75rem 1rem; margin: .75rem 0;
  font-size: .85rem; color: var(--ro); display: flex; gap: .5rem;
}

/* ─── RADAR CHART ───────────────────────────────────────────────────── */
.radar-wrap {
  display: flex; justify-content: center; margin: 2rem 0;
}
.radar-svg { max-width: 340px; width: 100%; }

/* ─── METHODOLOGY ───────────────────────────────────────────────────── */
#method-section { background: var(--ink); color: var(--white); }
#method-section .section-eyebrow { color: #93C5FD; }
#method-section .section-title { color: var(--white); }
.method-grid { display: grid; grid-template-columns: repeat(auto-fill, minmax(260px, 1fr)); gap: 1.25rem; margin-top: 2.5rem; }
.method-card {
  background: #111827; border: 1px solid #1F2937;
  border-radius: var(--r2); padding: 1.5rem;
}
.mc-num {
  font-family: 'DM Mono', monospace; font-size: .7rem; color: var(--az2);
  font-weight: 700; letter-spacing: .1em; margin-bottom: .75rem;
}
.mc-title { font-weight: 700; font-size: 1rem; color: var(--white); margin-bottom: .5rem; }
.mc-desc { font-size: .85rem; color: #9CA3AF; line-height: 1.6; }
.mc-new { border-color: rgba(91,33,182,.4); background: rgba(91,33,182,.08); }
.mc-new .mc-num { color: #A78BFA; }

/* ─── FOOTER ─────────────────────────────────────────────────────────── */
footer {
  background: #060A10; padding: 3rem 4vw;
  display: flex; align-items: center; justify-content: space-between;
  gap: 2rem; flex-wrap: wrap; border-top: 1px solid #111827;
}
.footer-logo {
  font-family: 'Playfair Display', serif;
  color: var(--white); font-size: 1.1rem; font-weight: 700;
}
.footer-logo span { color: var(--gold); }
.footer-text { font-size: .8rem; color: #4B5563; }

/* ─── Animations ─────────────────────────────────────────────────────── */
.fade-in { opacity: 0; transform: translateY(24px); transition: opacity .6s ease, transform .6s ease; }
.fade-in.visible { opacity: 1; transform: translateY(0); }
</style>
</head>
<body>

<!-- ═══ HERO ═══════════════════════════════════════════════════════════ -->
<div class="hero" id="top">
  <div class="hero-grid"></div>
  <div class="hero-accent"></div>
  <div class="hero-accent2"></div>
  <div class="hero-badge">
    <svg width="10" height="10" viewBox="0 0 10 10"><circle cx="5" cy="5" r="5" fill="#93C5FD"/></svg>
    ONU-Hábitat · Consultoría GIRS Bolivia y Bogotá Circular · 2026
  </div>
  <h1>Experiencias <em>internacionales</em> innovadoras en Gestión de Residuos</h1>
  <p class="hero-sub">8 casos analizados en 4 continentes — con índice ampliado de transferibilidad de 8 dimensiones para contextos andinos.</p>
  <div class="hero-stats">
    <div class="hero-stat-item"><span class="hero-stat-num">8</span><span class="hero-stat-label">Experiencias</span></div>
    <div class="hero-stat-item"><span class="hero-stat-num">8</span><span class="hero-stat-label">Dimensiones de análisis</span></div>
    <div class="hero-stat-item"><span class="hero-stat-num">80</span><span class="hero-stat-label">Puntaje máximo</span></div>
    <div class="hero-stat-item"><span class="hero-stat-num">5</span><span class="hero-stat-label">Casos ALTA transferibilidad</span></div>
  </div>
  <div class="hero-ctas">
    <a href="#fichas-section" class="btn btn-primary">Ver las 8 fichas ↓</a>
    <a href="#index-section" class="btn btn-ghost">Índice de transferibilidad</a>
  </div>
</div>

<!-- ═══ NAV ════════════════════════════════════════════════════════════ -->
<nav>
  <div class="nav-logo">GIRS <span>Internacional</span></div>
  <div class="nav-links">
    <a class="nav-link" href="#map-section">Mapa</a>
    <a class="nav-link" href="#index-section">Índice</a>
    <a class="nav-link" href="#fichas-section">Fichas</a>
    <a class="nav-link" href="#method-section">Metodología</a>
  </div>
</nav>

<!-- ═══ MAP ════════════════════════════════════════════════════════════ -->
<section id="map-section">
  <div class="map-header fade-in">
    <div class="section-eyebrow">Distribución global</div>
    <h2 class="section-title">8 ciudades. 4 continentes. <em>Un marco común.</em></h2>
    <p class="section-desc">Haz clic en cada pin para explorar la experiencia.</p>
  </div>
  <div class="map-container">
    <svg class="world-map-svg" viewBox="0 0 1000 500" xmlns="http://www.w3.org/2000/svg" id="world-svg">
      <!-- Ocean background -->
      <rect width="1000" height="500" fill="#0D1117"/>
      <!-- Grid lines -->
      <g stroke="#1F2937" stroke-width="0.5" opacity="0.5">
        <line x1="0" y1="125" x2="1000" y2="125"/>
        <line x1="0" y1="250" x2="1000" y2="250"/>
        <line x1="0" y1="375" x2="1000" y2="375"/>
        <line x1="250" y1="0" x2="250" y2="500"/>
        <line x1="500" y1="0" x2="500" y2="500"/>
        <line x1="750" y1="0" x2="750" y2="500"/>
      </g>
      <!-- Simplified continent shapes -->
      <!-- North America -->
      <path d="M 60 60 L 185 55 L 205 90 L 220 130 L 210 170 L 190 185 L 185 215 L 165 230 L 150 210 L 140 180 L 120 175 L 110 155 L 100 140 L 75 130 L 60 100 Z" fill="#1A2535" stroke="#2E3A50" stroke-width="0.8"/>
      <!-- Greenland -->
      <path d="M 185 30 L 230 25 L 245 50 L 225 65 L 195 60 Z" fill="#1A2535" stroke="#2E3A50" stroke-width="0.8"/>
      <!-- Central America + Caribbean -->
      <path d="M 165 230 L 185 245 L 195 268 L 185 278 L 170 270 L 165 255 Z" fill="#1A2535" stroke="#2E3A50" stroke-width="0.8"/>
      <!-- South America -->
      <path d="M 190 265 L 240 260 L 270 285 L 280 320 L 275 360 L 265 395 L 245 420 L 225 430 L 205 415 L 190 380 L 180 340 L 175 300 L 180 275 Z" fill="#1A2535" stroke="#2E3A50" stroke-width="0.8"/>
      <!-- Europe -->
      <path d="M 430 60 L 490 55 L 510 70 L 505 95 L 490 110 L 470 115 L 455 105 L 440 95 L 435 75 Z" fill="#1A2535" stroke="#2E3A50" stroke-width="0.8"/>
      <!-- Africa -->
      <path d="M 450 130 L 510 125 L 535 145 L 545 180 L 550 220 L 545 265 L 530 300 L 510 330 L 490 340 L 470 330 L 450 300 L 440 260 L 435 215 L 435 170 L 440 145 Z" fill="#1A2535" stroke="#2E3A50" stroke-width="0.8"/>
      <!-- Middle East -->
      <path d="M 535 120 L 580 115 L 595 140 L 585 165 L 555 170 L 535 155 Z" fill="#1A2535" stroke="#2E3A50" stroke-width="0.8"/>
      <!-- Russia/Kazakhstan -->
      <path d="M 490 40 L 700 35 L 730 65 L 720 100 L 680 110 L 620 115 L 590 105 L 550 100 L 520 85 L 495 70 Z" fill="#1A2535" stroke="#2E3A50" stroke-width="0.8"/>
      <!-- South/Southeast Asia -->
      <path d="M 600 110 L 700 105 L 750 125 L 770 160 L 760 195 L 735 210 L 700 205 L 665 190 L 640 165 L 615 145 L 600 130 Z" fill="#1A2535" stroke="#2E3A50" stroke-width="0.8"/>
      <!-- India -->
      <path d="M 635 155 L 680 150 L 700 175 L 705 210 L 690 240 L 668 250 L 645 240 L 630 210 L 628 180 Z" fill="#1A2535" stroke="#2E3A50" stroke-width="0.8"/>
      <!-- Southeast Asia islands (Indonesia region) -->
      <path d="M 740 225 L 790 220 L 820 240 L 825 265 L 800 275 L 765 270 L 745 255 Z" fill="#1A2535" stroke="#2E3A50" stroke-width="0.8"/>
      <path d="M 800 230 L 855 225 L 875 250 L 870 275 L 840 280 L 810 270 Z" fill="#1A2535" stroke="#2E3A50" stroke-width="0.8"/>
      <path d="M 855 240 L 900 238 L 915 260 L 905 278 L 875 280 Z" fill="#1A2535" stroke="#2E3A50" stroke-width="0.8"/>
      <!-- Japan -->
      <path d="M 860 90 L 880 82 L 895 100 L 890 120 L 870 118 Z" fill="#1A2535" stroke="#2E3A50" stroke-width="0.8"/>
      <!-- China -->
      <path d="M 700 80 L 810 72 L 850 95 L 845 130 L 820 145 L 780 150 L 750 140 L 720 125 L 700 105 Z" fill="#1A2535" stroke="#2E3A50" stroke-width="0.8"/>
      <!-- Australia -->
      <path d="M 790 310 L 875 300 L 920 325 L 935 370 L 920 410 L 875 425 L 830 415 L 795 385 L 780 345 Z" fill="#1A2535" stroke="#2E3A50" stroke-width="0.8"/>

      <!-- Equator label -->
      <text x="12" y="253" fill="#374151" font-size="9" font-family="DM Mono, monospace">0°</text>
      <text x="12" y="130" fill="#374151" font-size="9" font-family="DM Mono, monospace">45°N</text>

      <!-- PINS — each positioned by geo coordinates mapped to SVG viewBox 0-1000,0-500 -->
      <!-- lon: (lon+180)/360*1000  lat: (90-lat)/180*500 -->
      <!-- 01 Milan (lon=9.19, lat=45.46) → x=525, y=247 → wait: (9.19+180)/360*1000=525 (90-45.46)/180*500=124 -->
      <g class="map-pin" data-case="0" onclick="openModal(0)">
        <circle class="outer" cx="525" cy="124" r="18" fill="rgba(46,117,182,.25)"/>
        <circle cx="525" cy="124" r="9" fill="#2E75B6"/>
        <circle cx="525" cy="124" r="5" fill="white"/>
        <text x="525" y="128" text-anchor="middle" fill="#1A3A5C" font-size="7" font-weight="700" font-family="DM Mono, monospace">01</text>
      </g>
      <!-- 02 Hermosillo (-110.97, 29.07) → x=(69.03/360)*1000=192, y=(60.93/180)*500=169 -->
      <g class="map-pin" data-case="1" onclick="openModal(1)">
        <circle class="outer" cx="192" cy="169" r="18" fill="rgba(46,117,182,.25)"/>
        <circle cx="192" cy="169" r="9" fill="#2E75B6"/>
        <circle cx="192" cy="169" r="5" fill="white"/>
        <text x="192" y="173" text-anchor="middle" fill="#1A3A5C" font-size="7" font-weight="700" font-family="DM Mono, monospace">02</text>
      </g>
      <!-- 03 Iqaluit (-68.52, 63.75) → x=(111.48/360)*1000=309, y=(26.25/180)*500=73 -->
      <g class="map-pin" data-case="2" onclick="openModal(2)">
        <circle class="outer" cx="309" cy="73" r="18" fill="rgba(46,117,182,.25)"/>
        <circle cx="309" cy="73" r="9" fill="#2E75B6"/>
        <circle cx="309" cy="73" r="5" fill="white"/>
        <text x="309" y="77" text-anchor="middle" fill="#1A3A5C" font-size="7" font-weight="700" font-family="DM Mono, monospace">03</text>
      </g>
      <!-- 04 Nakuru (36.07, -0.28) → x=(216.07/360)*1000=600, y=(90.28/180)*500=251 -->
      <g class="map-pin tema-b" data-case="3" onclick="openModal(3)">
        <circle class="outer" cx="600" cy="251" r="18" fill="rgba(15,81,50,.3)"/>
        <circle cx="600" cy="251" r="9" fill="#0F5132"/>
        <circle cx="600" cy="251" r="5" fill="white"/>
        <text x="600" y="255" text-anchor="middle" fill="#DCFCE7" font-size="7" font-weight="700" font-family="DM Mono, monospace">04</text>
      </g>
      <!-- 05 Granollers (2.29, 41.61) → x=(182.29/360)*1000=506, y=(48.39/180)*500=134 -->
      <g class="map-pin tema-b" data-case="4" onclick="openModal(4)">
        <circle class="outer" cx="506" cy="134" r="18" fill="rgba(15,81,50,.3)"/>
        <circle cx="506" cy="134" r="9" fill="#0F5132"/>
        <circle cx="506" cy="134" r="5" fill="white"/>
        <text x="506" y="138" text-anchor="middle" fill="#DCFCE7" font-size="7" font-weight="700" font-family="DM Mono, monospace">05</text>
      </g>
      <!-- 06 Bandung (107.61, -6.92) → x=(287.61/360)*1000=799, y=(96.92/180)*500=269 -->
      <g class="map-pin" data-case="5" onclick="openModal(5)">
        <circle class="outer" cx="799" cy="269" r="18" fill="rgba(46,117,182,.25)"/>
        <circle cx="799" cy="269" r="9" fill="#2E75B6"/>
        <circle cx="799" cy="269" r="5" fill="white"/>
        <text x="799" y="273" text-anchor="middle" fill="#1A3A5C" font-size="7" font-weight="700" font-family="DM Mono, monospace">06</text>
      </g>
      <!-- 07 Pune (73.86, 18.52) → x=(253.86/360)*1000=705, y=(71.48/180)*500=198 -->
      <g class="map-pin tema-b" data-case="6" onclick="openModal(6)">
        <circle class="outer" cx="705" cy="198" r="18" fill="rgba(15,81,50,.3)"/>
        <circle cx="705" cy="198" r="9" fill="#0F5132"/>
        <circle cx="705" cy="198" r="5" fill="white"/>
        <text x="705" y="202" text-anchor="middle" fill="#DCFCE7" font-size="7" font-weight="700" font-family="DM Mono, monospace">07</text>
      </g>
      <!-- 08 Comas, Lima (-77.05, -11.93) → x=(102.95/360)*1000=286, y=(101.93/180)*500=283 -->
      <g class="map-pin tema-b" data-case="7" onclick="openModal(7)">
        <circle class="outer" cx="286" cy="283" r="18" fill="rgba(15,81,50,.3)"/>
        <circle cx="286" cy="283" r="9" fill="#0F5132"/>
        <circle cx="286" cy="283" r="5" fill="white"/>
        <text x="286" y="287" text-anchor="middle" fill="#DCFCE7" font-size="7" font-weight="700" font-family="DM Mono, monospace">08</text>
      </g>
    </svg>
    <div class="map-tooltip" id="map-tooltip"></div>
  </div>
  <div class="map-legend">
    <div class="ml-item"><div class="ml-dot" style="background:#2E75B6"></div><span class="ml-label">Tema A: Economía Circular</span></div>
    <div class="ml-item"><div class="ml-dot" style="background:#0F5132"></div><span class="ml-label">Tema B: DDHH e Inclusión</span></div>
    <div class="ml-item" style="margin-left:auto"><span class="ml-label">Haz clic en un pin para ver la ficha</span></div>
  </div>
</section>

<!-- ═══ INDEX TABLE ════════════════════════════════════════════════════ -->
<section id="index-section">
  <div class="section-header fade-in">
    <div class="section-eyebrow">Índice comparativo</div>
    <h2 class="section-title">Transferibilidad ampliada — <em>8 dimensiones</em></h2>
    <p class="section-desc">Máximo 80 puntos. Las dimensiones 7 y 8 son contribución analítica del equipo consultor.</p>
  </div>
  <div class="dim-legend fade-in">
    <span class="dim-chip" style="background:#DBEAFE;color:#1A3A5C">Pertinencia</span>
    <span class="dim-chip" style="background:#DBEAFE;color:#1A3A5C">Contexto inst.</span>
    <span class="dim-chip" style="background:#DBEAFE;color:#1A3A5C">Normativa</span>
    <span class="dim-chip" style="background:#DBEAFE;color:#1A3A5C">Financiero</span>
    <span class="dim-chip" style="background:#DBEAFE;color:#1A3A5C">Social</span>
    <span class="dim-chip" style="background:#DBEAFE;color:#1A3A5C">Tecnológico</span>
    <span class="dim-chip" style="background:#DCFCE7;color:#0F5132">Inclusión / Género ★</span>
    <span class="dim-chip" style="background:#EDE9FE;color:#5B21B6">Emancipatorio ★</span>
    <span style="font-size:.72rem;color:var(--muted);align-self:center">★ Nuevas dimensiones</span>
  </div>
  <div class="index-controls fade-in">
    <button class="filter-btn active" onclick="filterIndex('all',this)">Todas</button>
    <button class="filter-btn" onclick="filterIndex('alta',this)">ALTA transferibilidad</button>
    <button class="filter-btn" onclick="filterIndex('media',this)">MEDIA transferibilidad</button>
  </div>
  <div class="index-table-wrap fade-in">
    <table id="index-table">
      <thead>
        <tr>
          <th>#</th><th>Experiencia</th><th>País</th>
          <th title="Pertinencia contextual">Pert.</th>
          <th title="Contexto institucional">Inst.</th>
          <th title="Habilitadores normativos">Norm.</th>
          <th title="Viabilidad financiera">Fin.</th>
          <th title="Aceptación social">Soc.</th>
          <th title="Viabilidad tecnológica">Tec.</th>
          <th title="Inclusión / Género" style="color:#86EFAC">Inc./Gén.</th>
          <th title="Modelo emancipatorio" style="color:#C4B5FD">Eman.</th>
          <th>Total</th><th>Nivel</th>
        </tr>
      </thead>
      <tbody id="index-tbody"></tbody>
    </table>
  </div>
</section>

<!-- ═══ FICHAS ═════════════════════════════════════════════════════════ -->
<section id="fichas-section">
  <div class="section-header fade-in">
    <div class="section-eyebrow">Fichas descriptivas</div>
    <h2 class="section-title">Las <em>8 experiencias</em> en detalle</h2>
    <p class="section-desc">Haz clic en una tarjeta para ver la ficha completa con contexto, modelo operativo, resultados y recomendaciones.</p>
  </div>
  <div class="fichas-filters fade-in">
    <button class="filter-btn active" onclick="filterFichas('all',this)">Todas</button>
    <button class="filter-btn" onclick="filterFichas('a',this)">Tema A: Economía Circular</button>
    <button class="filter-btn" onclick="filterFichas('b',this)">Tema B: DDHH e Inclusión</button>
    <button class="filter-btn" onclick="filterFichas('alta',this)">ALTA transferibilidad</button>
  </div>
  <div class="fichas-grid" id="fichas-grid"></div>
</section>

<!-- ═══ METHODOLOGY ════════════════════════════════════════════════════ -->
<section id="method-section">
  <div class="section-header fade-in">
    <div class="section-eyebrow">Metodología</div>
    <h2 class="section-title">Cómo se construyó el <em>índice</em></h2>
    <p class="section-desc" style="color:#9CA3AF">El índice es el resultado del juicio analítico informado del equipo consultor, no de una fórmula automática.</p>
  </div>
  <div class="method-grid fade-in">
    <div class="method-card">
      <div class="mc-num">DIM 01</div>
      <div class="mc-title">Pertinencia contextual</div>
      <div class="mc-desc">¿Las condiciones del municipio receptor son similares al caso? (tamaño, fracción orgánica, informalidad, base fiscal)</div>
    </div>
    <div class="method-card">
      <div class="mc-num">DIM 02</div>
      <div class="mc-title">Contexto institucional</div>
      <div class="mc-desc">¿Existe capacidad institucional suficiente a nivel municipal, departamental y nacional para implementar el modelo?</div>
    </div>
    <div class="method-card">
      <div class="mc-num">DIM 03</div>
      <div class="mc-title">Habilitadores normativos</div>
      <div class="mc-desc">¿Existen marcos legales o regulatorios comparables que permitan implementar el modelo sin cambios normativos mayores?</div>
    </div>
    <div class="method-card">
      <div class="mc-num">DIM 04</div>
      <div class="mc-title">Viabilidad financiera</div>
      <div class="mc-desc">¿El modelo puede financiarse de forma sostenida con recursos públicos, tarifas o ingresos propios, sin cooperación externa permanente?</div>
    </div>
    <div class="method-card">
      <div class="mc-num">DIM 05</div>
      <div class="mc-title">Aceptación social</div>
      <div class="mc-desc">¿Existe o puede construirse una base social dispuesta a participar y sostener el modelo en el largo plazo?</div>
    </div>
    <div class="method-card">
      <div class="mc-num">DIM 06</div>
      <div class="mc-title">Viabilidad tecnológica</div>
      <div class="mc-desc">¿La tecnología requerida es accesible, manejable localmente y adaptable a las condiciones del territorio receptor?</div>
    </div>
    <div class="method-card mc-new">
      <div class="mc-num">DIM 07 — NUEVA</div>
      <div class="mc-title">Inclusión y perspectiva de género</div>
      <div class="mc-desc">¿El modelo incorpora activamente a recicladores de base y mujeres, con mecanismos de educación ciudadana y participación comunitaria? Escala 9-10: inclusión estructural con paridad de género.</div>
    </div>
    <div class="method-card mc-new">
      <div class="mc-num">DIM 08 — NUEVA</div>
      <div class="mc-title">Modelo emancipatorio</div>
      <div class="mc-desc">¿El modelo reconoce a los recicladores como agentes de cambio con control sobre activos, gobernanza democrática e ingresos dignos propios? 10/10: propiedad + gobernanza + ingresos dignos.</div>
    </div>
  </div>
  <div style="margin-top:2.5rem;background:#111827;border:1px solid #1F2937;border-radius:var(--r2);padding:1.5rem 2rem;" class="fade-in">
    <div style="display:flex;gap:3rem;flex-wrap:wrap">
      <div><div style="font-size:.72rem;color:#9CA3AF;letter-spacing:.08em;text-transform:uppercase;margin-bottom:.5rem">Umbral ALTA</div><div style="font-family:'Playfair Display',serif;font-size:2rem;font-weight:900;color:#86EFAC">≥ 53 / 80</div></div>
      <div><div style="font-size:.72rem;color:#9CA3AF;letter-spacing:.08em;text-transform:uppercase;margin-bottom:.5rem">Umbral MEDIA</div><div style="font-family:'Playfair Display',serif;font-size:2rem;font-weight:900;color:#FCD34D">37–52 / 80</div></div>
      <div><div style="font-size:.72rem;color:#9CA3AF;letter-spacing:.08em;text-transform:uppercase;margin-bottom:.5rem">Umbral BAJA</div><div style="font-family:'Playfair Display',serif;font-size:2rem;font-weight:900;color:#FCA5A5">&lt; 37 / 80</div></div>
      <div style="flex:1;min-width:200px;align-self:center"><div style="font-size:.85rem;color:#9CA3AF;line-height:1.6">El índice evalúa la viabilidad de <strong style="color:#E5E7EB">adaptar</strong> el modelo al contexto andino, no la calidad de la experiencia en su lugar de origen. Un puntaje MEDIA no implica que la experiencia sea menos valiosa.</div></div>
    </div>
  </div>
</section>

<!-- ═══ FOOTER ══════════════════════════════════════════════════════════ -->
<footer>
  <div>
    <div class="footer-logo">GIRS <span>Internacional</span></div>
    <div class="footer-text" style="margin-top:.4rem">Consultoría ONU-Hábitat · Bolivia y Bogotá Circular · 2026</div>
  </div>
  <div class="footer-text">Manuela Benavides · Maria José Angarita · Sofía Ramos Castellanos<br>Universidad del Rosario</div>
</footer>

<!-- ═══ MODAL ═══════════════════════════════════════════════════════════ -->
<div class="modal-overlay" id="modal-overlay" onclick="closeModalOutside(event)">
  <div class="modal" id="modal-content"></div>
</div>

<!-- ═══════════════════════════════════════════════════════════════════ -->
<!-- DATA + LOGIC                                                       -->
<!-- ═══════════════════════════════════════════════════════════════════ -->
<script>
const CASES = [
  {
    num:'01', tema:'a', color:'#2E75B6',
    name:'Food Waste Hubs', city:'Milán', country:'Italia', flag:'🇮🇹',
    entidad:'Ayuntamiento de Milán / AMSA / Asociación Recup',
    pop:'1,4 M (3,2 M metrop.)', anio:'2019',
    scores: { pertinencia:7, contexto:5, normativa:6, financiero:5, social:7, tecnologico:6, inclusion:4, emancipatorio:2 },
    total:42, nivel:'MEDIA',
    tagline:'Recuperación comunitaria de desperdicio alimentario a escala urbana.',
    contexto:'Milán genera ~1,4 M toneladas/año de RSU, con 30-35% de orgánicos. Antes de 2019, el 45% de ciudadanos participaba en recolección selectiva y el material llegaba con 25-30% de contaminación cruzada. El 15-20% de alimentos aptos para consumo terminaban desechados.',
    modelo:'Red de 26 hubs anti-desperdicio distribuidos en los 9 distritos municipales. Cada hub capta excedentes de supermercados (AMSA los recolecta refrigerados) y redistribuye a 27.000 personas vulnerables. Dos modalidades: familias registradas (3x/semana, hasta 15 kg) y comedores sociales.',
    normativa:'Legge Gadda (Ley 166/2016): eliminó barreras fiscales a la donación corporativa, permitió deducción fiscal del 15% de ingresos brutos. Plan Comunal 2018: meta -20% desperdicio per cápita para 2025.',
    resultados:'26 hubs operativos · 180-220 t/mes de alimentos recuperados · 27.000 personas beneficiarias · Inversión €450.000-650.000 (60% municipal + 30% ERDF-UE + 10% corporativo).',
    leccion:'Los hubs representan solo el 2% del desperdicio total: son complemento, no sustituto de transformaciones sistémicas. El modelo no integra recicladores informales (limitación crítica para transferencia a contextos andinos).',
    asimetria:'El elemento más transferible para Bolivia y Bogotá es la lógica de redistribución desde mercados hacia comedores comunitarios (ollas populares). La segmentación de audiencias en la estrategia educativa es directamente replicable.',
    ods:['ODS 2','ODS 10','ODS 11','ODS 12','ODS 13','ODS 17'],
    odsColors:['#DDA63A','#DD1367','#FD9D24','#BF8B2E','#3F7E44','#19486A'],
  },
  {
    num:'02', tema:'a', color:'#2E75B6',
    name:'Proyecto Biciclando', city:'Hermosillo', country:'México', flag:'🇲🇽',
    entidad:'IMPLAN Hermosillo / UNDP',
    pop:'958.000 hab.', anio:'2023',
    scores: { pertinencia:8, contexto:7, normativa:7, financiero:6, social:9, tecnologico:7, inclusion:8, emancipatorio:5 },
    total:57, nivel:'ALTA',
    tagline:'Economía circular, movilidad sostenible y empoderamiento femenino en un solo modelo.',
    contexto:'Hermosillo enfrenta tres problemas simultáneos: tasa de reciclaje <2%, transporte motorizado genera 35% de GEI, y barreras de género para empleo formal en sector ambiental. El 50,1% de habitantes son mujeres.',
    modelo:'Centros de Economía Circular (CEC) con liderazgo femenino + recolección puerta a puerta con bicicletas eléctricas cargo + sistema GIS para rutas + Zona Salva (espacio seguro de capacitación para mujeres). Más de 30 bicicladoras formalizadas.',
    normativa:'Reglamento de Ecología de Hermosillo 2024 (art.5 XXI) · Ley de Movilidad y Seguridad Vial de Sonora · Ley Federal del Trabajo · Reconocimiento UNDP como buena práctica ODS.',
    resultados:'>30 mujeres formalizadas con empleo digno · >26.800 kg desviados del relleno sanitario · >4 km de infraestructura ciclista promovida · 1 CEC con liderazgo femenino creado.',
    leccion:'El diseño desde el género genera valor sistémico, no solo equitativo. La sostenibilidad económica post-UNDP es el reto no resuelto: los ingresos por venta de materiales deben demostrar autofinanciación a escala.',
    asimetria:'Altamente transferible a ciudades intermedias de Bolivia y localidades bogotanas con recicladoras de oficio. La Zona Salva es el componente más directamente replicable en centros de acopio de ORs.',
    ods:['ODS 5','ODS 8','ODS 10','ODS 11','ODS 12','ODS 13'],
    odsColors:['#FF3A21','#A21942','#DD1367','#FD9D24','#BF8B2E','#3F7E44'],
  },
  {
    num:'03', tema:'a', color:'#2E75B6',
    name:'Waste Management Initiative', city:'Iqaluit', country:'Canadá', flag:'🇨🇦',
    entidad:'Gobierno Municipal / Gobierno de Nunavut / WWF Arctic',
    pop:'7.740 hab.', anio:'2014+',
    scores: { pertinencia:8, contexto:6, normativa:7, financiero:5, social:7, tecnologico:6, inclusion:3, emancipatorio:2 },
    total:44, nivel:'MEDIA',
    tagline:'Gestión de residuos en el Ártico: diseño situado en condiciones extremas.',
    contexto:'Iqaluit es la capital de Nunavut, Ártico canadiense. Sin ningún camino a otras comunidades, la mayor parte de residuos debe enviarse al sur por barco en el corto período estival. El incidente Dumpcano (2014) —incendio de 4 meses, 2.000°C— evidenció los riesgos del sistema. Crecimiento del 38% desde 2001.',
    modelo:'Vertedero mejorado con controles reforzados + Centro de reuso comunitario + Gestión diferenciada de materiales peligrosos + Compostaje adaptado al permafrost (técnica propia de bajo ciclo térmico) + Exportación estival de reciclables al sur.',
    normativa:'Ley de Residuos Sólidos Enmienda #651 de Iqaluit: tarifas diferenciadas por tipo de residuo, permite reutilización o venta de subproductos. Marcos territoriales de Nunavut para subsidios estructurales.',
    resultados:'Tasa de desvío proyectada: 25-50% · Reducción de incendios espontáneos en el vertedero · Centro de reuso activo · Mayor conciencia ciudadana sobre fragilidad del ecosistema ártico.',
    leccion:'El valor de Iqaluit es METODOLÓGICO, no operativo: las políticas de GIRS deben construirse desde las condiciones del territorio, no desde estándares diseñados para contextos radicalmente distintos. La gobernanza multinivel es necesidad operativa, no ideal normativo.',
    asimetria:'El principio de diseño situado es directamente aplicable a municipios amazónicos y étnicos de Bolivia (Guayaramerín, Cobija, San Matías, San Ignacio de Moxos). El centro de reuso es el componente operativo más transferible, de bajo costo.',
    ods:['ODS 3','ODS 11','ODS 12','ODS 13','ODS 15','ODS 16'],
    odsColors:['#4C9F38','#FD9D24','#BF8B2E','#3F7E44','#56C02B','#00689D'],
  },
  {
    num:'04', tema:'b', color:'#0F5132',
    name:'NAWACOM', city:'Nakuru', country:'Kenia', flag:'🇰🇪',
    entidad:'NAWACOM / Practical Action Kenya',
    pop:'570.000 hab.', anio:'2002',
    scores: { pertinencia:9, contexto:8, normativa:7, financiero:7, social:10, tecnologico:7, inclusion:8, emancipatorio:9 },
    total:65, nivel:'ALTA',
    tagline:'Cooperativa de recicladores que produce compost de marca propia y gestiona su sistema democráticamente.',
    contexto:'Nakuru: 4a ciudad más poblada de Kenia. El 60-65% de la población en asentamientos informales. El sistema municipal cubría solo el 30% de la ciudad. 513 t/día de residuos (80% orgánicos) se gestionaban via deposición en cunetas, márgenes del lago Nakuru y quema abierta. Desde los años 1990, mujeres desempleadas iniciaron grupos comunitarios de reciclaje.',
    modelo:'12 CBOs fundadoras (2002) → NAWACOM: cooperativa de 336 miembros en 25 grupos comunitarios, gobernanza "one member, one vote". Recolección vecinal descentralizada (carritos y triciclos) + almacén go-down 400m² + compostaje 90 días con control de calidad (pH, microscopio) + marca Mazingira Organic Fertilizer para agricultores ecológicos.',
    normativa:'Cooperative Societies Act (Kenia) como habilitador legal → préstamo Kenya Women Finance Trust (2006, US$26.000 para go-down) → Reconocimiento Nakuru County Government post-descentralización 2010: permiso dumpsite, cesión terreno 20 años, compra preferencial compost.',
    resultados:'336 miembros activos · 2.500-3.000 t orgánicos/año a US$20-27/t (vs. US$40-80/t municipal) · Incremento de ingresos del 275% · 68% de miembros son mujeres · 5/9 directivos son mujeres · Permanencia promedio: de 1,5 a 4,8 años.',
    leccion:'La integración emancipatoria genera eficiencia superior al compostaje municipal formal. La cooperativa (personería jurídica) fue el habilitador estructural para el préstamo, el terreno y las cuentas bancarias. Identificar el mercado destino ANTES de escalar la producción.',
    asimetria:'Referente más directamente transferible para Bolivia: la tradición cooperativista boliviana, OECOMAs y perfil de recicladores son análogos. Proceso: diagnóstico → cooperativa (cuota 40% mujeres) → identificar mercado compost → microfinanzas → convenio municipal.',
    ods:['ODS 1','ODS 2','ODS 5','ODS 8','ODS 11','ODS 12'],
    odsColors:['#E5243B','#DDA63A','#FF3A21','#A21942','#FD9D24','#BF8B2E'],
    esLeccionNeg: false,
  },
  {
    num:'05', tema:'b', color:'#991B1B',
    name:'Granollers — Reciclaje informal', city:'Granollers', country:'España', flag:'🇪🇸',
    entidad:'Ayuntamiento de Granollers / AMSA / UAB',
    pop:'61.129 hab.', anio:'2013-2023',
    scores: { pertinencia:8, contexto:7, normativa:6, financiero:5, social:6, tecnologico:7, inclusion:3, emancipatorio:2 },
    total:44, nivel:'MEDIA',
    tagline:'Lección negativa: cómo la eficiencia técnica puede coexistir con exclusión social severa.',
    contexto:'Sistema de GIRS técnicamente eficiente: 82% participación, 43,2% tasa de reciclaje (2022). Sin embargo, entre 2013-2023 emerge proliferación de chatarreros/cartoneros informales —migrantes en situación irregular— que recuperan el 44% del cartón comercial antes de la recolección oficial (estudio UAB 2018-2019, 37 trabajadores).',
    modelo:'Sistema formal: 234 rutas mecanizadas, eficiente. Sistema informal: recorridos nocturnos 22:00-6:00, carritos improvisados, 80-150 kg/ruta, €8-15/ruta, €150-300/mes. Mesa de Diálogo Reciclaje Inclusivo (2021-2022): 6 reuniones, propuesta piloto pendiente de aprobación presupuestaria.',
    normativa:'Ley 7/2022 RSU España: residuos en vía pública son propiedad municipal desde deposición → limbo legal. Contratación pública requiere situación legal (78% de recicladores carece de ella). Las mesas de diálogo no tienen poder ejecutivo ni presupuesto asignado.',
    resultados:'Sistema formal: técnicamente satisfactorio. Sistema informal: 37 trabajadores en extrema precariedad, sin protección social, sin reconocimiento. Parálisis decisoria >10 años. Represión (2015-2018) discontinuada. Tolerancia pasiva desde 2019.',
    leccion:'1) El orden importa: no se puede tecnificar sin haber integrado primero. 2) La eficiencia técnica puede coexistir con exclusión social severa. 3) Sin mecanismos de reconocimiento al margen del estatus migratorio, la integración formal es imposible. 4) Las mesas de diálogo sin mandato político y presupuesto no producen cambios.',
    asimetria:'ADVERTENCIA explícita para Bolivia y Bogotá: no avanzar en tecnificación del sistema (contenedores inteligentes, trazabilidad digital, nuevas rutas) sin diseñar simultáneamente el mecanismo de integración del reciclador informal. Toda modernización en Bogotá debe ir precedida de análisis de impacto en ORs.',
    ods:['ODS 1','ODS 8','ODS 10','ODS 11','ODS 12','ODS 16'],
    odsColors:['#E5243B','#A21942','#DD1367','#FD9D24','#BF8B2E','#00689D'],
    esLeccionNeg: true,
  },
  {
    num:'06', tema:'a', color:'#2E75B6',
    name:'Zero Waste Cities / YPBB', city:'Bandung', country:'Indonesia', flag:'🇮🇩',
    entidad:'YPBB / Municipio de Bandung / GAIA',
    pop:'2,5 M hab.', anio:'2005+',
    scores: { pertinencia:9, contexto:8, normativa:7, financiero:8, social:9, tecnologico:8, inclusion:6, emancipatorio:5 },
    total:60, nivel:'ALTA',
    tagline:'Transformación comunitaria de la gestión de residuos — 86% de desvío potencial con compostaje descentralizado.',
    contexto:'Bandung genera 1.500-1.600 t/día de RSU (63% orgánicos). El colapso del vertedero Leuwigajah (2005, +140 muertes) creó el momentum político para transformar el sistema. El desastre impulsó la Ley de Gestión de Residuos 18/2008.',
    modelo:'Modelo descentralizado de 4 componentes: (1) Segregación en fuente domiciliar (múltiples contenedores) · (2) Recolección separada por operadores locales · (3) Compostaje doméstico y comunitario de orgánicos · (4) Waste banks para inorgánicos reciclables con créditos individuales por hogares. Kelurahan (barrios) como unidades de implementación.',
    normativa:'Ley 18/2008 post-desastre Leuwigajah: enfoque integral reducción-reciclaje-tratamiento. Políticas municipales de Bandung fortaleciendo separación en fuente y expansión de waste banks.',
    resultados:'>40% participación en barrios piloto · Reducciones significativas en residuos al sistema municipal · Proyección: 86% de reducción con separación y compostaje a escala ciudad · Expansión de red de waste banks.',
    leccion:'La participación comunitaria transforma los sistemas de GIRS incluso en alta densidad, sin infraestructura centralizada costosa. Los waste banks son infraestructura SOCIAL (incentivo económico + separación domiciliar). El desafío es la escalabilidad fuera de los kelurahan piloto.',
    asimetria:'La composición de residuos bolivianos (60-70% orgánicos) es análoga a la de Bandung (63%), haciendo el modelo de compostaje descentralizado altamente pertinente para municipios bolivianos de cualquier escala. Los waste banks son directamente replicables en zonas periurbanas con mercados agrícolas locales.',
    ods:['ODS 3','ODS 4','ODS 11','ODS 12','ODS 13','ODS 15'],
    odsColors:['#4C9F38','#C5192D','#FD9D24','#BF8B2E','#3F7E44','#56C02B'],
  },
  {
    num:'07', tema:'b', color:'#0F5132',
    name:'SWaCH', city:'Pune', country:'India', flag:'🇮🇳',
    entidad:'SWaCH Cooperative / PMC / KKPKP',
    pop:'6 M hab.', anio:'2007',
    scores: { pertinencia:9, contexto:8, normativa:7, financiero:8, social:10, tecnologico:7, inclusion:9, emancipatorio:10 },
    total:68, nivel:'ALTA',
    tagline:'El caso más robusto de integración emancipatoria a gran escala: 3.761 recicladores, US$4,8 M en ahorros para la municipalidad.',
    contexto:'Pune, Maharashtra, India. La red informal de kabadiwallas (recicladores) recolectaba ~144 t/día, generando ahorros de US$220.000/año para el PMC. El sindicato KKPKP cuantificó ese valor y lo usó como argumento económico —no solo social— para construir voluntad política municipal.',
    modelo:'Cooperativa SWaCH + PMC: modelo de doble ingreso (tarifa mensual de usuarios + derecho a venta de materiales recuperados). Arquitectura híbrida: recolección descentralizada por 3.761 recicladores organizados geográficamente + clasificación centralizada en 12 plantas MRF (provistas por PMC, operadas por SWaCH). Cobertura: >800.000 hogares.',
    normativa:'Reglas de Gestión de RSU 2016 de India: reconocimiento formal de recicladores de base. Convenio contractual PMC-SWaCH. El riesgo es la dependencia de la voluntad política municipal ante cambios de gobierno.',
    resultados:'>800.000 hogares atendidos · 277 t/día desviadas del vertedero · Ahorros para PMC: US$4,2-4,8 M/año · Incremento de ingresos de recicladores: 500-800% · Acceso a protección social previamente vedada · Mayoría de trabajadores son mujeres.',
    leccion:'El argumento económico (US$220.000 ahorros) fue más efectivo que el argumento de justicia social para construir voluntad política. La integración emancipatoria supera en eficiencia a contratistas privados. El doble ingreso elimina la dependencia del subsidio. Riesgo: dependencia de voluntad política ante cambios de gobierno.',
    asimetria:'Referente más directo para Bogotá Circular. Recomendaciones: contratos mínimo 5 años con ORs + doble ingreso explícito en convenios UAESP + fondo de capitalización para que ORs sean propietarias de activos + 50% representación femenina como requisito de elegibilidad.',
    ods:['ODS 3','ODS 5','ODS 8','ODS 10','ODS 11','ODS 12'],
    odsColors:['#4C9F38','#FF3A21','#A21942','#DD1367','#FD9D24','#BF8B2E'],
  },
  {
    num:'08', tema:'b', color:'#0F5132',
    name:'Formalización de Recicladores', city:'Comas, Lima', country:'Perú', flag:'🇵🇪',
    entidad:'Municipalidad Distrital de Comas / OPMI',
    pop:'Distrito Lima Metropolitana', anio:'2023',
    scores: { pertinencia:10, contexto:9, normativa:8, financiero:7, social:9, tecnologico:7, inclusion:7, emancipatorio:7 },
    total:64, nivel:'ALTA',
    tagline:'El referente latinoamericano más cercano para Bolivia: formalización via ordenanza municipal.',
    contexto:'Comas, norte de Lima Metropolitana. Crecimiento acelerado y expansión urbana desorganizada: incremento de 640 t en generación de RSU (OPMI 2023). La informalidad de recicladores generaba botaderos clandestinos y ausencia de derechos laborales. El municipio reconoció a los recicladores como actores clave, no como problema a eliminar.',
    modelo:'Formalización de 4 asociaciones de recicladores (ACOSUR, Prince de Paz, ARULN, Luz Divina) mediante convenios municipales y permisos administrativos. 17 recicladores formalizados. Áreas de acondicionamiento para clasificación y almacenamiento temporal. Recolección diferenciada en origen. Campañas de sensibilización con recicladores formalizados como agentes de confianza.',
    normativa:'Ley de Residuos Sólidos del Perú y reglamento · Ley General del Ambiente · Ordenanza Municipal de Comas 2023: instrumento local que otorga permisos y reconoce las cuatro asociaciones como actores formales del sistema.',
    resultados:'17 recicladores formalizados con personería jurídica · Aumento de residuos diferenciados en hogares, comercios e instituciones · Mejoramiento de condiciones laborales (seguridad social) · Reducción de botaderos clandestinos · Mejor coordinación público-privada en rutas.',
    leccion:'La formalización con reconocimiento de derechos transforma al reciclador: de trabajador invisible a actor reconocido del sistema. La cobertura limitada (17 recicladores) es el principal desafío. Escalar e incorporar el doble ingreso de SWaCH son condiciones para la sostenibilidad económica.',
    asimetria:'Mayor pertinencia contextual para Bolivia: crecimiento urbano desorganizado, alta informalidad, marco legal nacional habilitador comparable, asociaciones preexistentes y capacidad municipal limitada. Replicable en Cochabamba, Oruro, Santa Cruz, El Alto, Tarija. Para Bogotá: el Decreto 596/2016 ya existe, pero requiere contratos más largos y el doble ingreso.',
    ods:['ODS 1','ODS 3','ODS 8','ODS 10','ODS 11','ODS 12'],
    odsColors:['#E5243B','#4C9F38','#A21942','#DD1367','#FD9D24','#BF8B2E'],
  },
];

const DIM_KEYS   = ['pertinencia','contexto','normativa','financiero','social','tecnologico','inclusion','emancipatorio'];
const DIM_LABELS = ['Pertinencia','Inst.','Norm.','Fin.','Social','Tec.','Inc./Gén.','Eman.'];

function scoreClass(v) {
  if (v >= 8) return 'ds-high';
  if (v >= 5) return 'ds-mid';
  return 'ds-low';
}

function nivelBadge(nivel) {
  const cls = nivel === 'ALTA' ? 'nivel-alta' : 'nivel-media';
  return `<span class="nivel-badge ${cls}">${nivel}</span>`;
}

function barColor(v) {
  if (v >= 8) return '#22C55E';
  if (v >= 5) return '#F59E0B';
  return '#EF4444';
}

// ── Build INDEX TABLE ──────────────────────────────────────────────────
function buildIndex(filter='all') {
  const tbody = document.getElementById('index-tbody');
  tbody.innerHTML = '';
  CASES.forEach((c,i) => {
    if (filter === 'alta' && c.nivel !== 'ALTA') return;
    if (filter === 'media' && c.nivel !== 'MEDIA') return;
    const tr = document.createElement('tr');
    tr.dataset.case = i;
    tr.onclick = () => openModal(i);
    const dimCells = DIM_KEYS.map(k => {
      const v = c.scores[k];
      const cls = scoreClass(v);
      const extra = (k==='inclusion'||k==='emancipatorio') ? 'border-left:2px solid #4B5563;' : '';
      return `<td style="${extra}"><span class="dim-score ${cls}">${v}</span></td>`;
    }).join('');
    const tc = c.nivel==='ALTA' ? '#22C55E' : '#F59E0B';
    tr.innerHTML = `
      <td><span class="td-num">${c.num}</span></td>
      <td><div class="td-name">${c.name}</div><div class="td-country">${c.flag} ${c.city}</div></td>
      <td><span class="td-country">${c.country}</span></td>
      ${dimCells}
      <td><span class="total-badge" style="color:${tc}">${c.total}</span></td>
      <td>${nivelBadge(c.nivel)}</td>
    `;
    tbody.appendChild(tr);
  });
}
buildIndex();

function filterIndex(f, btn) {
  document.querySelectorAll('.index-controls .filter-btn').forEach(b=>b.classList.remove('active'));
  btn.classList.add('active');
  buildIndex(f);
}

// ── Build FICHAS GRID ──────────────────────────────────────────────────
function buildFichas(filter='all') {
  const grid = document.getElementById('fichas-grid');
  grid.innerHTML = '';
  CASES.forEach((c,i) => {
    let show = true;
    if (filter==='a' && c.tema!=='a') show=false;
    if (filter==='b' && c.tema!=='b') show=false;
    if (filter==='alta' && c.nivel!=='ALTA') show=false;
    const card = document.createElement('div');
    card.className = 'ficha-card' + (show?'':' hidden');
    card.onclick = () => openModal(i);
    const temaLabel = c.tema==='a' ? 'Tema A' : 'Tema B';
    const temaClass = c.tema==='a' ? 'tema-a' : 'tema-b';
    const tc = c.nivel==='ALTA' ? '#0F5132' : '#C55A11';
    const nb = c.nivel==='ALTA' ? '#DCFCE7' : '#FEF3C7';
    // Score bars for top 4 dims
    const barRows = ['pertinencia','social','inclusion','emancipatorio'].map((k,idx) => {
      const labels = ['Pertinencia','Social','Inclusión/Gén.','Emancipatorio'];
      const v = c.scores[k];
      const bc = barColor(v);
      return `
        <div class="fc-score-row">
          <span class="fc-score-label">${labels[idx]}</span>
          <div class="fc-score-bar-wrap"><div class="fc-score-bar" style="width:${v*10}%;background:${bc}"></div></div>
          <span class="fc-score-val" style="color:${bc}">${v}</span>
        </div>`;
    }).join('');
    const negBadge = c.esLeccionNeg ? `<div style="display:inline-flex;align-items:center;gap:.3rem;background:#FEE2E2;color:#991B1B;font-size:.68rem;font-weight:700;padding:.2rem .6rem;border-radius:100px;margin-left:.5rem">⚠ Lección negativa</div>` : '';
    card.innerHTML = `
      <div class="fc-stripe" style="background:${c.color}"></div>
      <div class="fc-header">
        <div class="fc-num-wrap">
          <span class="fc-num">FICHA ${c.num}</span>
          ${negBadge}
        </div>
        <span class="fc-tema ${temaClass}">${temaLabel}</span>
      </div>
      <div class="fc-title">${c.name}</div>
      <div class="fc-location">📍 ${c.flag} ${c.city}, ${c.country}</div>
      <div class="fc-desc">${c.tagline}</div>
      <div class="fc-scores">${barRows}</div>
      <div class="fc-footer">
        <div><span class="fc-total" style="color:${tc}">${c.total}/80</span></div>
        ${nivelBadge(c.nivel)}
        <button class="fc-btn">Ver ficha completa →</button>
      </div>`;
    grid.appendChild(card);
  });
}
buildFichas();

function filterFichas(f, btn) {
  document.querySelectorAll('.fichas-filters .filter-btn').forEach(b=>b.classList.remove('active'));
  btn.classList.add('active');
  buildFichas(f);
}

// ── MODAL ──────────────────────────────────────────────────────────────
function openModal(i) {
  const c = CASES[i];
  const overlay = document.getElementById('modal-overlay');
  const content = document.getElementById('modal-content');
  const tc = c.nivel==='ALTA' ? '#0F5132' : '#C55A11';
  const nb = c.nivel==='ALTA' ? '#DCFCE7' : '#FEF3C7';

  const scoreCells = DIM_KEYS.map((k,idx) => {
    const v = c.scores[k];
    const bc = barColor(v);
    const isNew = k==='inclusion'||k==='emancipatorio';
    return `
      <div class="modal-score-item" ${isNew?'style="border:1.5px solid #DDD6FE"':''}>
        <div class="msi-label" ${isNew?'style="color:#7C3AED"':''}>${DIM_LABELS[idx]}${isNew?' ★':''}</div>
        <div class="msi-bar-wrap"><div class="msi-bar" style="width:${v*10}%;background:${bc}"></div></div>
        <span class="msi-val" style="color:${bc}">${v}/10</span>
      </div>`;
  }).join('');

  const odsBadges = c.ods.map((o,idx)=>
    `<span class="ods-tag" style="background:${c.odsColors[idx]}">${o}</span>`
  ).join('');

  const negBlock = c.esLeccionNeg ? `
    <div class="leccion-neg">
      <span>⚠</span>
      <span><strong>Lección negativa:</strong> Este caso no documenta un modelo a replicar sino una advertencia: ilustra los riesgos de tecnificar sin integrar previamente al reciclador informal.</span>
    </div>` : '';

  // Mini radar SVG
  const radarSVG = buildRadar(c.scores, c.color);

  content.innerHTML = `
    <div class="modal-stripe" style="background:${c.color}"></div>
    <button class="modal-close" onclick="closeModal()">✕</button>
    <div class="modal-header">
      <div class="modal-num">FICHA ${c.num} · ${c.tema==='a'?'TEMA A: ECONOMÍA CIRCULAR':'TEMA B: DDHH E INCLUSIÓN'}</div>
      <div class="modal-title">${c.name}</div>
      <div class="modal-meta">
        <span class="modal-country">📍 ${c.flag} ${c.city}, ${c.country}</span>
        <span style="color:var(--muted);font-size:.8rem">·</span>
        <span style="font-size:.8rem;color:var(--muted)">${c.entidad}</span>
        <span style="color:var(--muted);font-size:.8rem">·</span>
        <span style="font-size:.8rem;color:var(--muted)">Población: ${c.pop}</span>
      </div>
    </div>
    <div class="modal-body">
      ${negBlock}
      <div class="modal-section-title">Contexto</div>
      <p class="modal-text">${c.contexto}</p>

      <div class="modal-section-title">Modelo operativo e innovación</div>
      <p class="modal-text">${c.modelo}</p>

      <div class="modal-section-title">Marco normativo</div>
      <p class="modal-text">${c.normativa}</p>

      <div class="modal-section-title">Resultados alcanzados</div>
      <p class="modal-text">${c.resultados}</p>

      <div class="modal-section-title">Lección aprendida / Lectura crítica</div>
      <p class="modal-text">${c.leccion}</p>

      <div class="modal-section-title">Asimetría territorial — Bolivia y Bogotá</div>
      <p class="modal-text">${c.asimetria}</p>

      <div class="modal-section-title">Vinculación con los ODS</div>
      <div class="modal-tags">${odsBadges}</div>

      <div class="modal-section-title">Índice de transferibilidad</div>
      <div class="radar-wrap">${radarSVG}</div>
      <div class="modal-scores-grid">${scoreCells}</div>
      <div class="modal-total-row">
        <div>
          <div class="mtr-label">Puntuación total</div>
          <div class="mtr-total" style="color:${tc}">${c.total}/80</div>
        </div>
        <div style="text-align:center">
          <div class="mtr-label" style="margin-bottom:.4rem">Dims 1-6 (base)</div>
          <div style="font-family:'Playfair Display',serif;font-size:1.6rem;font-weight:900;color:#93C5FD">${DIM_KEYS.slice(0,6).reduce((s,k)=>s+c.scores[k],0)}/60</div>
        </div>
        <div style="text-align:center">
          <div class="mtr-label" style="margin-bottom:.4rem">Dims 7-8 (ampliadas)</div>
          <div style="font-family:'Playfair Display',serif;font-size:1.6rem;font-weight:900;color:#C4B5FD">${c.scores.inclusion+c.scores.emancipatorio}/20</div>
        </div>
        <div>${nivelBadge(c.nivel)}</div>
      </div>
    </div>`;

  overlay.classList.add('open');
  document.body.style.overflow = 'hidden';
}

function buildRadar(scores, color) {
  const vals = DIM_KEYS.map(k => scores[k]);
  const N = vals.length;
  const cx=140, cy=130, r=90;
  const angles = vals.map((_,i) => -Math.PI/2 + (i/N)*2*Math.PI);
  const point = (v, i) => {
    const a = angles[i];
    const d = (v/10)*r;
    return [cx + d*Math.cos(a), cy + d*Math.sin(a)];
  };
  // grid circles
  const circles = [2,4,6,8,10].map(v => {
    const pts = vals.map((_,i)=>point(v,i));
    return `<polygon points="${pts.map(p=>p.join(',')).join(' ')}" fill="none" stroke="#E5E7EB" stroke-width="0.7"/>`;
  }).join('');
  // spokes
  const spokes = vals.map((_,i) => {
    const [px,py] = point(10,i);
    return `<line x1="${cx}" y1="${cy}" x2="${px}" y2="${py}" stroke="#E5E7EB" stroke-width="0.7"/>`;
  }).join('');
  // data polygon
  const dataPts = vals.map((_,i)=>point(vals[i],i));
  const polygon = `<polygon points="${dataPts.map(p=>p.join(',')).join(' ')}" fill="${color}" fill-opacity="0.18" stroke="${color}" stroke-width="1.8"/>`;
  // dots
  const dots = dataPts.map(([px,py],i) => {
    const isNew = i>=6;
    return `<circle cx="${px}" cy="${py}" r="${isNew?4:3}" fill="${isNew?'#7C3AED':color}" stroke="white" stroke-width="1.2"/>`;
  }).join('');
  // labels
  const labels = DIM_LABELS.map((l,i) => {
    const [px,py] = point(11.5,i);
    const isNew = i>=6;
    return `<text x="${px}" y="${py}" text-anchor="middle" dominant-baseline="middle" font-size="8.5" fill="${isNew?'#7C3AED':'#6B7280'}" font-family="DM Sans, sans-serif" font-weight="${isNew?'700':'400'}">${l}</text>`;
  }).join('');

  return `<svg class="radar-svg" viewBox="0 0 280 260" xmlns="http://www.w3.org/2000/svg">
    ${circles}${spokes}${polygon}${dots}${labels}
  </svg>`;
}

function closeModal() {
  document.getElementById('modal-overlay').classList.remove('open');
  document.body.style.overflow = '';
}
function closeModalOutside(e) {
  if (e.target === document.getElementById('modal-overlay')) closeModal();
}
document.addEventListener('keydown', e => { if (e.key === 'Escape') closeModal(); });

// ── MAP TOOLTIP ─────────────────────────────────────────────────────
document.querySelectorAll('.map-pin').forEach(pin => {
  pin.addEventListener('mouseenter', e => {
    const idx = parseInt(pin.dataset.case);
    const c = CASES[idx];
    const tt = document.getElementById('map-tooltip');
    const tc = c.nivel==='ALTA' ? '#0F5132' : '#C55A11';
    const nb = c.nivel==='ALTA' ? '#DCFCE7' : '#FEF3C7';
    tt.innerHTML = `
      <div class="mt-num">FICHA ${c.num}</div>
      <div class="mt-name">${c.name}</div>
      <div class="mt-country">${c.flag} ${c.city}, ${c.country}</div>
      <div class="mt-score nivel-badge" style="background:${nb};color:${tc};margin-top:.5rem">${c.total}/80 · ${c.nivel}</div>`;
    const rect = pin.closest('svg').getBoundingClientRect();
    const svgEl = pin.closest('svg');
    const pt = svgEl.createSVGPoint();
    const circles = pin.querySelectorAll('circle');
    const mainCircle = circles[1];
    pt.x = parseFloat(mainCircle.getAttribute('cx'));
    pt.y = parseFloat(mainCircle.getAttribute('cy'));
    const svgPt = pt.matrixTransform(svgEl.getScreenCTM());
    const container = document.querySelector('.map-container');
    const cRect = container.getBoundingClientRect();
    let left = svgPt.x - cRect.left + 15;
    let top  = svgPt.y - cRect.top  - 70;
    if (left + 210 > cRect.width) left = svgPt.x - cRect.left - 215;
    if (top < 0) top = svgPt.y - cRect.top + 20;
    tt.style.left = left + 'px';
    tt.style.top  = top  + 'px';
    tt.classList.add('visible');
  });
  pin.addEventListener('mouseleave', () => {
    document.getElementById('map-tooltip').classList.remove('visible');
  });
});

// ── NAV active on scroll ─────────────────────────────────────────────
const navLinks = document.querySelectorAll('.nav-link');
const sections = ['map-section','index-section','fichas-section','method-section'];
window.addEventListener('scroll', () => {
  let current = '';
  sections.forEach(id => {
    const el = document.getElementById(id);
    if (el && el.getBoundingClientRect().top < 120) current = id;
  });
  navLinks.forEach(l => {
    l.classList.toggle('active', l.getAttribute('href') === '#'+current);
  });
});

// ── Intersection Observer for fade-in ───────────────────────────────
const io = new IntersectionObserver(entries => {
  entries.forEach(e => { if (e.isIntersecting) { e.target.classList.add('visible'); io.unobserve(e.target); }});
}, { threshold: 0.08 });
document.querySelectorAll('.fade-in').forEach(el => io.observe(el));
</script>
</body>
</html>
