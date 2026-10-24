<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover">
<meta name="theme-color" content="#0d3a45">
<title>Mi agua</title>
<style>
  :root {
    --bg: #e6f0ee;
    --ink: #0d3a45;
    --ink-soft: #4b6b72;
    --card: #f7fbfa;
    --water: #1f8fa6;
    --water-deep: #0d3a45;
    --low: #d99a2b;
    --ok: #1f8fa6;
    --high: #b4483a;
    --line: #c9dcd9; --on-ok: #fff; --on-high: #fff;
  }
  @media (prefers-color-scheme: dark) {
    :root {
      --bg: #0a2a32; --ink: #e3f1ef; --ink-soft: #8fb0b3; --card: #10394300;
      --card: #0f3842; --line: #1d4f5a; --water: #4fc3d9; --water-deep: #4fc3d9;
      --low: #e3ae4a; --ok: #4fc3d9; --high: #e8806f; --on-ok: #06242b; --on-high: #2a0d08;
    }
  }
  * { box-sizing: border-box; margin: 0; }
  html, body { background: var(--bg); color: var(--ink); }
  body {
    font-family: ui-rounded, "SF Pro Rounded", "Segoe UI", system-ui, sans-serif;
    padding: max(16px, env(safe-area-inset-top)) 16px max(32px, env(safe-area-inset-bottom));
    max-width: 520px; margin: 0 auto; line-height: 1.4;
  }
  h1 { font-size: 1.1rem; font-weight: 600; color: var(--ink-soft); margin-bottom: 12px; }
  h2 { font-size: 1rem; font-weight: 600; margin-bottom: 10px; }
  .card { background: var(--card); border: 1px solid var(--line); border-radius: 18px; padding: 16px; margin-bottom: 14px; }

  /* Botella: lo memorable de la app */
  .hero { display: grid; grid-template-columns: 110px 1fr; gap: 18px; align-items: center; }
  .bottle { width: 110px; height: auto; display: block; }
  .bottle .glass { fill: none; stroke: var(--ink); stroke-width: 3; }
  .bottle .water { fill: var(--water); transition: y .6s ease, height .6s ease; }
  .bottle .cap { fill: var(--ink); }
  .bottle .tick { stroke: var(--ink); stroke-width: 1.5; opacity: .35; }
  .total { font-size: 2.6rem; font-weight: 700; line-height: 1; }
  .total small { font-size: 1rem; font-weight: 500; color: var(--ink-soft); }
  .of { color: var(--ink-soft); font-size: .9rem; margin-top: 4px; }
  .badge { display: inline-block; margin-top: 10px; padding: 5px 12px; border-radius: 999px; font-weight: 600; font-size: .9rem; color: var(--on-ok); background: var(--ok); }
  .badge.low { background: var(--low); color: #2a1d00; }
  .badge.high { background: var(--high); color: var(--on-high); }
  .badge.sm { font-size: .75rem; padding: 3px 10px; margin: 6px 0 0; }
  .pace { color: var(--ink-soft); font-size: .9rem; margin-top: 12px; }

  .btns { display: grid; grid-template-columns: 1fr 1fr; gap: 10px; margin-top: 4px; }
  button { font: inherit; cursor: pointer; border: 0; border-radius: 14px; padding: 14px 10px; font-weight: 600; color: var(--ink); background: var(--line); }
  button.main { grid-column: 1 / -1; background: var(--water-deep); color: var(--bg); font-size: 1.05rem; padding: 18px; }
  button:active { transform: scale(.98); }
  button:focus-visible, input:focus-visible, summary:focus-visible { outline: 3px solid var(--water); outline-offset: 2px; }
  .custom { display: flex; gap: 10px; grid-column: 1 / -1; }
  input { font: inherit; padding: 12px; border-radius: 12px; border: 1px solid var(--line); background: var(--bg); color: var(--ink); width: 100%; min-width: 0; }
  .link { background: none; padding: 6px 0; color: var(--ink-soft); font-weight: 500; text-decoration: underline; }

  .tabs { display: flex; gap: 6px; margin: 6px 0 4px; }
  .tabs button { flex: 1; padding: 10px 6px; font-size: .85rem; }
  .tabs button.on { background: var(--water-deep); color: var(--bg); }
  .chart { display: flex; gap: 4px; height: 170px; position: relative; margin-top: 8px; }
  .col { flex: 1; min-width: 0; display: flex; flex-direction: column; cursor: pointer; }
  .barwrap { flex: 1; display: flex; align-items: flex-end; }
  .bar { width: 100%; border-radius: 6px 6px 2px 2px; background: var(--ok); min-height: 3px; }
  .bar.low { background: var(--low); } .bar.high { background: var(--high); } .bar.none { background: var(--line); }
  .col.sel .bar { box-shadow: 0 0 0 2px var(--ink); }
  .lbl { height: 20px; line-height: 20px; text-align: center; font-size: .7rem; color: var(--ink-soft); overflow: visible; white-space: nowrap; }
  .col.today .lbl { color: var(--ink); font-weight: 700; }
  .goalline { position: absolute; left: 0; right: 0; border-top: 2px dashed var(--ink-soft); opacity: .5; pointer-events: none; }
  .yearnav { display: flex; justify-content: space-between; align-items: center; }
  .yearnav h2 { margin: 0; font-size: 1.2rem; }
  .yearnav button { width: 48px; padding: 8px; font-size: 1.3rem; }
  button:disabled { opacity: .35; cursor: default; }
  .legend { display: flex; flex-wrap: wrap; gap: 4px 12px; font-size: .75rem; color: var(--ink-soft); margin: 8px 0; }
  .legend i { display: inline-block; width: 10px; height: 10px; border-radius: 3px; margin-right: 4px; vertical-align: -1px; }
  .daypanel { position: sticky; top: calc(env(safe-area-inset-top, 0px) + 8px); z-index: 5; background: var(--card); border: 1px solid var(--line); border-radius: 14px; padding: 10px 12px; box-shadow: 0 4px 14px rgba(0,0,0,.14); max-height: 48vh; overflow: auto; font-size: .9rem; }
  .dp-head { display: flex; justify-content: space-between; gap: 8px; }
  .dp-head strong { text-transform: capitalize; }
  .dp-add { display: flex; gap: 6px; margin-top: 8px; }
  .dp-add button { padding: 10px 8px; font-size: .85rem; white-space: nowrap; }
  .dp-add input { padding: 10px; }
  .x { background: none; color: var(--high); font-size: 1.2rem; padding: 0 8px; margin-left: 4px; }
  .months { display: grid; grid-template-columns: 1fr 1fr; gap: 16px 12px; margin-top: 12px; }
  .months.big { grid-template-columns: 1fr; }
  .mhead { display: flex; justify-content: space-between; align-items: baseline; font-size: .85rem; font-weight: 600; margin-bottom: 4px; text-transform: capitalize; }
  .mhead span { font-weight: 500; color: var(--ink-soft); font-size: .7rem; text-transform: none; }
  .mgrid { display: grid; grid-template-columns: repeat(7, 1fr); gap: 2px; }
  .dow { font-size: .6rem; color: var(--ink-soft); text-align: center; }
  .cell { aspect-ratio: 1; min-width: 0; padding: 0; border-radius: 5px; font-size: .65rem; font-weight: 500; background: var(--line); color: var(--ink-soft); display: flex; align-items: center; justify-content: center; }
  .months.big .cell { font-size: .9rem; border-radius: 8px; }
  .cell.low { background: var(--low); color: #2a1d00; }
  .cell.ok { background: var(--ok); color: var(--on-ok); }
  .cell.high { background: var(--high); color: var(--on-high); }
  .cell.blank { background: transparent; pointer-events: none; }
  .cell.future { background: transparent; opacity: .45; border: 1px dashed var(--line); }
  .cell.today { outline: 2px solid var(--ink); outline-offset: 1px; }
  .cell.sel { box-shadow: 0 0 0 2px var(--card), 0 0 0 4px var(--ink); position: relative; z-index: 1; }
  .stats { display: grid; grid-template-columns: repeat(3, 1fr); gap: 10px; margin-top: 18px; }
  .stat b { display: block; font-size: 1.35rem; }
  .stat span { font-size: .8rem; color: var(--ink-soft); }

  details summary { cursor: pointer; font-weight: 600; }
  .field { display: grid; gap: 4px; margin-top: 12px; font-size: .9rem; color: var(--ink-soft); }
  .row2 { display: grid; grid-template-columns: 1fr 1fr; gap: 10px; }
  .note { font-size: .8rem; color: var(--ink-soft); margin-top: 12px; }
  .list { list-style: none; padding: 0; font-size: .9rem; }
  .list li { display: flex; justify-content: space-between; padding: 6px 0; border-bottom: 1px solid var(--line); }

  #toast { position: fixed; left: 16px; right: 16px; bottom: max(16px, env(safe-area-inset-bottom)); max-width: 488px; margin: 0 auto;
    background: var(--water-deep); color: var(--bg); border-radius: 14px; padding: 14px 16px; display: flex; justify-content: space-between; align-items: center; gap: 12px;
    transform: translateY(150%); transition: transform .3s ease; }
  #toast.show { transform: none; }
  #toast button { background: transparent; color: var(--bg); text-decoration: underline; padding: 4px 8px; }
  @media (prefers-reduced-motion: reduce) { * { transition: none !important; } }
</style>
</head>
<body>

<h1 id="fecha"></h1>

<section class="card hero" aria-live="polite">
  <svg class="bottle" viewBox="0 0 120 270" role="img" aria-label="Botella con el progreso del día">
    <defs><clipPath id="clip"><path d="M30 66 Q30 52 44 52 H76 Q90 52 90 66 V240 Q90 256 74 256 H46 Q30 256 30 240 Z"/></clipPath></defs>
    <rect class="cap" x="44" y="8" width="32" height="16" rx="5"/>
    <rect x="48" y="24" width="24" height="28" fill="none" stroke="var(--ink)" stroke-width="3"/>
    <rect id="water" class="water" x="20" y="256" width="80" height="0" clip-path="url(#clip)"/>
    <path class="glass" d="M30 66 Q30 52 44 52 H76 Q90 52 90 66 V240 Q90 256 74 256 H46 Q30 256 30 240 Z"/>
    <g class="tick"><line x1="30" x2="44" y1="100" y2="100"/><line x1="30" x2="44" y1="152" y2="152"/><line x1="30" x2="44" y1="204" y2="204"/></g>
  </svg>
  <div>
    <div class="total"><span id="total">0</span> <small>ml</small></div>
    <div class="of" id="of"></div>
    <span class="badge" id="badge"></span>
    <p class="pace" id="pace"></p>
  </div>
</section>

<section class="card">
  <div class="btns">
    <button class="main" id="addBottle"></button>
    <button id="addHalf"></button>
    <button id="addGlass">Vaso 250 ml</button>
    <div class="custom">
      <input id="customMl" type="number" inputmode="numeric" min="10" max="2000" placeholder="Otra cantidad (ml)" aria-label="Otra cantidad en ml">
      <button id="addCustom">Añadir</button>
    </div>
  </div>
  <button class="link" id="undo">Deshacer el último registro</button>
  <ul class="list" id="todayList"></ul>
</section>

<section class="card">
  <h2>Gráfica</h2>
  <div class="tabs" id="tabs">
    <button data-r="7" class="on">7 días</button>
    <button data-r="30">30 días</button>
    <button data-r="year">Año</button>
  </div>
  <div class="chart" id="chart"></div>
  <p class="note" id="chartNote"></p>
  <div class="stats">
    <div class="stat"><b id="sAvg">–</b><span>media diaria (ml)</span></div>
    <div class="stat"><b id="sStreak">0</b><span>días seguidos en rango</span></div>
    <div class="stat"><b id="sDays">0</b><span>días que has bebido</span></div>
  </div>
</section>

<section class="card">
  <div class="yearnav">
    <button id="yPrev" aria-label="Año anterior">‹</button>
    <h2 id="yLabel"></h2>
    <button id="yNext" aria-label="Año siguiente">›</button>
  </div>
  <div class="legend">
    <span><i style="background:var(--line)"></i>Sin registro</span>
    <span><i style="background:var(--low)"></i>Poco</span>
    <span><i style="background:var(--ok)"></i>En rango</span>
    <span><i style="background:var(--high)"></i>Demasiado</span>
  </div>
  <div class="daypanel" id="dayPanel"></div>
  <div class="months" id="months"></div>
  <button class="link" id="zoomBtn">Ver meses más grandes</button>
</section>

<section class="card">
  <details>
    <summary>Ajustes y recordatorios</summary>
    <div class="row2">
      <label class="field">Capacidad botella (ml)<input id="cfgBottle" type="number" inputmode="numeric"></label>
      <label class="field">Objetivo diario (ml)<input id="cfgGoal" type="number" inputmode="numeric"></label>
      <label class="field">Mínimo del rango (ml)<input id="cfgMin" type="number" inputmode="numeric"></label>
      <label class="field">Máximo del rango (ml)<input id="cfgMax" type="number" inputmode="numeric"></label>
      <label class="field">Empiezo el día a las (h)<input id="cfgStart" type="number" inputmode="numeric" min="0" max="23"></label>
      <label class="field">Termino el día a las (h)<input id="cfgEnd" type="number" inputmode="numeric" min="1" max="24"></label>
    </div>
    <label class="field">Horas de recordatorio (separadas por comas)
      <input id="cfgTimes" type="text" placeholder="10:00, 13:00, 17:00, 20:00"></label>
    <div class="btns" style="margin-top:12px">
      <button id="remindBtn" class="main" style="font-size:1rem;padding:14px"></button>
    </div>
    <p class="note">Los recordatorios del navegador solo suenan con la app abierta o en segundo plano reciente. Para avisos 100 % fiables, crea alarmas repetidas en el móvil con el mismo texto.</p>
    <p class="note">Rango de referencia: los adultos suelen necesitar entre 1,5 y 2,5 L de bebida al día (el resto llega por la comida). Cambia los valores si tu médico te indica otros. Esto no es consejo médico.</p>
    <button class="link" id="exportBtn">Copiar copia de seguridad</button><br>
    <button class="link" id="resetBtn">Borrar todos los datos</button>
  </details>
</section>

<div id="toast" role="status"><span id="toastMsg"></span><button id="toastUndo">Deshacer</button></div>

<script>
(function () {
  const KEY = 'agua_v1';
  const DEF = { bottle: 800, goal: 2000, min: 1500, max: 3000, start: 8, end: 22, times: '10:00, 13:00, 17:00, 20:00', remind: false };
  let S = load();

  function load() {
    try {
      const raw = JSON.parse(localStorage.getItem(KEY));
      if (raw && raw.days) return { cfg: Object.assign({}, DEF, raw.cfg), days: raw.days, notified: raw.notified || {} };
    } catch (e) {}
    return { cfg: Object.assign({}, DEF), days: {}, notified: {} };
  }
  function save() { try { localStorage.setItem(KEY, JSON.stringify(S)); } catch (e) {} }

  const $ = id => document.getElementById(id);
  const pad = n => String(n).padStart(2, '0');
  const keyOf = d => d.getFullYear() + '-' + pad(d.getMonth() + 1) + '-' + pad(d.getDate());
  const todayKey = () => keyOf(new Date());
  const total = k => (S.days[k] || []).reduce((a, e) => a + e.ml, 0);
  const fmt = n => Math.round(n).toLocaleString('es-ES');

  function status(ml) { return ml < S.cfg.min ? 'low' : ml > S.cfg.max ? 'high' : 'ok'; }

  let chartRange = '7', calYear = new Date().getFullYear(), selKey = todayKey(), lastKey = todayKey();
  const thisYear = new Date().getFullYear();
  const keyParts = k => k.split('-').map(Number);
  const stamp = k => { if (k === todayKey()) return Date.now(); const p = keyParts(k); return new Date(p[0], p[1] - 1, p[2], 12).getTime(); };

  function add(ml, key) {
    key = key || todayKey();
    ml = Math.round(ml);
    if (!(ml > 0) || ml > 3000 || key > todayKey()) return;
    (S.days[key] = S.days[key] || []).push({ t: stamp(key), ml: ml });
    lastKey = key; save(); render();
    toast('+' + fmt(ml) + ' ml registrados' + (key === todayKey() ? '' : ' el ' + key.split('-').reverse().join('/')));
  }
  function undo(key) {
    key = key || todayKey();
    const list = S.days[key];
    if (!list || !list.length) return;
    list.pop();
    if (!list.length) delete S.days[key];
    save(); render();
  }
  function removeEntry(key, i) {
    const list = S.days[key];
    if (!list) return;
    list.splice(i, 1);
    if (!list.length) delete S.days[key];
    save(); render();
  }

  let toastTimer;
  function toast(msg) {
    $('toastMsg').textContent = msg;
    $('toast').classList.add('show');
    clearTimeout(toastTimer);
    toastTimer = setTimeout(() => $('toast').classList.remove('show'), 5000);
  }

  function render() {
    const c = S.cfg, k = todayKey(), t = total(k), st = status(t);
    const now = new Date();
    $('fecha').textContent = now.toLocaleDateString('es-ES', { weekday: 'long', day: 'numeric', month: 'long' });
    $('total').textContent = fmt(t);
    $('of').textContent = 'de ' + fmt(c.goal) + ' ml · ' + (t / c.bottle).toFixed(1).replace('.', ',') + ' botellas';

    // Botella: se llena según el objetivo diario
    const pct = Math.min(1, t / c.goal), top = 52, bottom = 256;
    const h = (bottom - top) * pct;
    $('water').setAttribute('y', bottom - h);
    $('water').setAttribute('height', h);

    const badge = $('badge');
    badge.className = 'badge ' + st;
    badge.textContent = st === 'low' ? 'Poco: bajo el rango' : st === 'high' ? 'Demasiado: sobre el rango' : 'En el rango normal';

    // Ritmo según la hora del día
    const hr = now.getHours() + now.getMinutes() / 60;
    const frac = Math.min(1, Math.max(0, (hr - c.start) / Math.max(1, c.end - c.start)));
    const expected = c.goal * frac;
    let pace = '';
    if (st === 'high') pace = 'Ya pasas el máximo de ' + fmt(c.max) + ' ml. Mejor parar por hoy.';
    else if (t >= c.goal) pace = 'Objetivo cumplido. Buen trabajo.';
    else if (frac >= 1) pace = 'El día termina y te faltaron ' + fmt(c.goal - t) + ' ml.';
    else if (frac > 0 && t < expected * 0.85) pace = 'Vas por detrás: a esta hora tocarían unos ' + fmt(expected) + ' ml (te faltan ' + fmt(expected - t) + ').';
    else if (frac > 0) pace = 'Vas bien de ritmo para esta hora.';
    else pace = 'Aún no ha empezado tu día de agua.';
    $('pace').textContent = pace;

    $('addBottle').textContent = '+ Botella entera (' + fmt(c.bottle) + ' ml)';
    $('addHalf').textContent = 'Media botella ' + fmt(c.bottle / 2) + ' ml';

    // Registros de hoy
    const list = (S.days[k] || []).slice().reverse();
    $('todayList').innerHTML = '';
    list.forEach(e => {
      const li = document.createElement('li');
      const a = document.createElement('span'), b = document.createElement('span');
      a.textContent = new Date(e.t).toLocaleTimeString('es-ES', { hour: '2-digit', minute: '2-digit' });
      b.textContent = '+' + fmt(e.ml) + ' ml';
      li.append(a, b); $('todayList').appendChild(li);
    });

    renderChart();
    renderCalendar();
    renderSettings();
  }

  function renderChart() {
    const c = S.cfg, chart = $('chart'), now = new Date();
    chart.innerHTML = '';
    document.querySelectorAll('#tabs button').forEach(bt => bt.classList.toggle('on', bt.dataset.r === chartRange));
    const items = [];
    let sum = 0, cnt = 0;
    if (chartRange === 'year') {
      for (let m = 0; m < 12; m++) {
        const n = new Date(calYear, m + 1, 0).getDate();
        let ms = 0, mc = 0;
        for (let d = 1; d <= n; d++) { const t = total(calYear + '-' + pad(m + 1) + '-' + pad(d)); if (t > 0) { ms += t; mc++; } }
        sum += ms; cnt += mc;
        const dt = new Date(calYear, m, 1);
        items.push({ v: mc ? ms / mc : 0, lbl: dt.toLocaleDateString('es-ES', { month: 'narrow' }).toUpperCase(),
          tip: dt.toLocaleDateString('es-ES', { month: 'long', year: 'numeric' }) + (mc ? ' (' + mc + ' días con registro)' : ''),
          today: calYear === now.getFullYear() && m === now.getMonth(), avg: true });
      }
    } else {
      const n = chartRange === '30' ? 30 : 7;
      for (let i = n - 1; i >= 0; i--) {
        const d = new Date(); d.setDate(d.getDate() - i);
        const v = total(keyOf(d));
        if (v > 0) { sum += v; cnt++; }
        items.push({ v: v, today: i === 0,
          lbl: n === 7 ? d.toLocaleDateString('es-ES', { weekday: 'narrow' }).toUpperCase() : (((n - 1 - i) % 5 === 0 || i === 0) ? String(d.getDate()) : ''),
          tip: d.toLocaleDateString('es-ES', { weekday: 'long', day: 'numeric', month: 'long' }) });
      }
    }
    const scale = Math.max(c.goal * 1.25, ...items.map(x => x.v));
    const defNote = (chartRange === 'year' ? 'Media diaria por mes en ' + calYear + '. ' : '') + 'Toca una barra para ver el valor.';
    $('chartNote').textContent = defNote;
    items.forEach(it => {
      const col = document.createElement('div');
      col.className = 'col' + (it.today ? ' today' : '');
      col.setAttribute('role', 'button'); col.tabIndex = 0;
      const wrap = document.createElement('div'); wrap.className = 'barwrap';
      const bar = document.createElement('div');
      bar.className = 'bar ' + (it.v === 0 ? 'none' : status(it.v));
      bar.style.height = (it.v / scale * 100) + '%';
      wrap.appendChild(bar);
      const lbl = document.createElement('div'); lbl.className = 'lbl'; lbl.textContent = it.lbl;
      col.append(wrap, lbl);
      const show = () => {
        chart.querySelectorAll('.col').forEach(x => x.classList.remove('sel')); col.classList.add('sel');
        $('chartNote').textContent = it.tip + ': ' + (it.v ? fmt(it.v) + ' ml' + (it.avg ? ' de media al día' : '') : 'sin registros');
      };
      col.onclick = show;
      col.onkeydown = e => { if (e.key === 'Enter' || e.key === ' ') { e.preventDefault(); show(); } };
      chart.appendChild(col);
    });
    const gl = document.createElement('div'); gl.className = 'goalline';
    gl.style.bottom = 'calc((100% - 20px) * ' + (c.goal / scale) + ' + 20px)';
    chart.appendChild(gl);

    $('sAvg').textContent = cnt ? fmt(sum / cnt) : '–';
    // Racha de días seguidos en rango (si hoy aún no llegas, cuenta desde ayer)
    let streak = 0, d = new Date();
    if (status(total(keyOf(d))) !== 'ok') d.setDate(d.getDate() - 1);
    while (total(keyOf(d)) > 0 && status(total(keyOf(d))) === 'ok') { streak++; d.setDate(d.getDate() - 1); }
    $('sStreak').textContent = streak;
    $('sDays').textContent = Object.keys(S.days).filter(k => total(k) > 0).length;
  }

  // ---- Calendario anual ----
  function renderCalendar() {
    $('yLabel').textContent = calYear;
    $('yNext').disabled = calYear >= thisYear;
    const box = $('months'), tk = todayKey();
    box.innerHTML = '';
    for (let m = 0; m < 12; m++) {
      const first = new Date(calYear, m, 1), n = new Date(calYear, m + 1, 0).getDate();
      const wrap = document.createElement('div');
      let ms = 0, mc = 0;
      const grid = document.createElement('div'); grid.className = 'mgrid';
      'LMXJVSD'.split('').forEach(ch => { const h = document.createElement('div'); h.className = 'dow'; h.textContent = ch; grid.appendChild(h); });
      for (let i = 0; i < (first.getDay() + 6) % 7; i++) { const b = document.createElement('div'); b.className = 'cell blank'; grid.appendChild(b); }
      for (let d = 1; d <= n; d++) {
        const key = calYear + '-' + pad(m + 1) + '-' + pad(d), t = total(key);
        if (t > 0) { ms += t; mc++; }
        const cell = document.createElement('button');
        cell.className = 'cell' + (key > tk ? ' future' : t > 0 ? ' ' + status(t) : '') + (key === tk ? ' today' : '') + (key === selKey ? ' sel' : '');
        cell.textContent = d;
        cell.setAttribute('aria-label', d + ' de ' + first.toLocaleDateString('es-ES', { month: 'long' }) + ': ' + (t ? fmt(t) + ' ml' : 'sin registro'));
        cell.onclick = () => { selKey = key; renderCalendar(); };
        grid.appendChild(cell);
      }
      const head = document.createElement('div'); head.className = 'mhead';
      const nm = document.createElement('div'); nm.textContent = first.toLocaleDateString('es-ES', { month: 'long' });
      const av = document.createElement('span'); av.textContent = mc ? fmt(ms / mc) + ' ml/día · ' + mc + ' d' : '';
      head.append(nm, av);
      wrap.append(head, grid); box.appendChild(wrap);
    }
    renderDayPanel();
  }

  function renderDayPanel() {
    const key = selKey, p = keyParts(key), d = new Date(p[0], p[1] - 1, p[2]);
    const t = total(key), st = status(t), list = S.days[key] || [], future = key > todayKey(), isToday = key === todayKey();
    let h = '<div class="dp-head"><strong>' + d.toLocaleDateString('es-ES', { weekday: 'long', day: 'numeric', month: 'long', year: 'numeric' }) +
      '</strong><span>' + (t ? fmt(t) + ' ml' : (future ? '' : 'Sin registro')) + '</span></div>';
    if (t) h += '<span class="badge sm ' + st + '">' + (st === 'low' ? 'Poco' : st === 'high' ? 'Demasiado' : 'En rango') + '</span>';
    if (list.length) {
      h += '<ul class="list">' + list.map((e, i) => '<li><span>' +
        (isToday ? new Date(e.t).toLocaleTimeString('es-ES', { hour: '2-digit', minute: '2-digit' }) : 'Registro ' + (i + 1)) +
        '</span><span>' + fmt(e.ml) + ' ml<button class="x" data-i="' + i + '" aria-label="Borrar registro">×</button></span></li>').join('') + '</ul>';
    }
    if (!future) {
      h += '<div class="dp-add"><button data-a="b">+ Botella</button><button data-a="g">+ Vaso</button>' +
        '<input id="dpMl" type="number" inputmode="numeric" min="10" max="2000" placeholder="ml" aria-label="Cantidad en ml"><button data-a="c">Añadir</button></div>';
    } else h += '<p class="note">Este día aún no ha llegado.</p>';
    const box = $('dayPanel'); box.innerHTML = h;
    box.querySelectorAll('.x').forEach(bt => bt.onclick = () => removeEntry(key, +bt.dataset.i));
    box.querySelectorAll('[data-a]').forEach(bt => bt.onclick = () => {
      const a = bt.dataset.a;
      if (a === 'b') add(S.cfg.bottle, key);
      else if (a === 'g') add(250, key);
      else add(parseInt($('dpMl').value, 10), key);
    });
  }

  function renderSettings() {
    const c = S.cfg;
    if (document.activeElement && document.activeElement.closest('details')) return;
    $('cfgBottle').value = c.bottle; $('cfgGoal').value = c.goal; $('cfgMin').value = c.min; $('cfgMax').value = c.max;
    $('cfgStart').value = c.start; $('cfgEnd').value = c.end; $('cfgTimes').value = c.times;
    $('remindBtn').textContent = c.remind ? 'Recordatorios activados (tocar para desactivar)' : 'Activar recordatorios';
  }

  function readSettings() {
    const n = (id, d) => { const v = parseInt($(id).value, 10); return v > 0 ? v : d; };
    const c = S.cfg;
    c.bottle = n('cfgBottle', c.bottle); c.goal = n('cfgGoal', c.goal);
    c.min = n('cfgMin', c.min); c.max = n('cfgMax', c.max);
    c.start = Math.min(23, n('cfgStart', c.start)); c.end = Math.max(c.start + 1, Math.min(24, n('cfgEnd', c.end)));
    c.times = $('cfgTimes').value.trim();
    save(); render();
  }

  // ---- Recordatorios ----
  function notify(msg) {
    try {
      if ('Notification' in window && Notification.permission === 'granted') {
        new Notification('Hora de beber agua', { body: msg });
      }
    } catch (e) {}
    toast(msg);
  }
  function checkReminders() {
    if (!S.cfg.remind) return;
    const now = new Date(), hhmm = pad(now.getHours()) + ':' + pad(now.getMinutes()), k = todayKey();
    const times = S.cfg.times.split(',').map(s => s.trim()).filter(Boolean).map(s => { const [h, m] = s.split(':'); return pad(+h) + ':' + pad(+m || 0); });
    if (!times.includes(hhmm)) return;
    const id = k + ' ' + hhmm;
    if (S.notified[id]) return;
    S.notified = { [id]: 1 }; save();
    const t = total(k);
    if (t >= S.cfg.goal) return;
    notify('Llevas ' + fmt(t) + ' ml de ' + fmt(S.cfg.goal) + '. ¿Un poco de agua?');
  }
  async function toggleReminders() {
    if (!S.cfg.remind) {
      if ('Notification' in window && Notification.permission === 'default') await Notification.requestPermission();
      S.cfg.remind = true;
    } else S.cfg.remind = false;
    save(); render();
  }

  // ---- Eventos ----
  $('addBottle').onclick = () => add(S.cfg.bottle);
  $('addHalf').onclick = () => add(S.cfg.bottle / 2);
  $('addGlass').onclick = () => add(250);
  $('addCustom').onclick = () => { add(parseInt($('customMl').value, 10)); $('customMl').value = ''; };
  $('undo').onclick = () => undo();
  $('toastUndo').onclick = () => { undo(lastKey); $('toast').classList.remove('show'); };
  document.querySelectorAll('#tabs button').forEach(bt => bt.onclick = () => { chartRange = bt.dataset.r; renderChart(); });
  function goYear(delta) {
    calYear = Math.min(thisYear, calYear + delta);
    selKey = calYear === thisYear ? todayKey() : calYear + '-01-01';
    render();
  }
  $('yPrev').onclick = () => goYear(-1);
  $('yNext').onclick = () => goYear(1);
  $('zoomBtn').onclick = () => {
    const big = $('months').classList.toggle('big');
    $('zoomBtn').textContent = big ? 'Ver meses más pequeños' : 'Ver meses más grandes';
  };
  ['cfgBottle', 'cfgGoal', 'cfgMin', 'cfgMax', 'cfgStart', 'cfgEnd', 'cfgTimes'].forEach(id => $(id).addEventListener('change', readSettings));
  $('remindBtn').onclick = toggleReminders;
  $('exportBtn').onclick = () => {
    const txt = JSON.stringify(S);
    (navigator.clipboard ? navigator.clipboard.writeText(txt) : Promise.reject()).then(() => toast('Copia guardada en el portapapeles'), () => prompt('Copia estos datos:', txt));
  };
  $('resetBtn').onclick = () => { if (confirm('¿Borrar todos los registros y ajustes?')) { S = { cfg: Object.assign({}, DEF), days: {}, notified: {} }; save(); render(); } };

  // ---- NFC: la pegatina abre la app con ?add=1 y suma una botella ----
  const params = new URLSearchParams(location.search);
  const nfcAdd = params.has('add');
  if (nfcAdd) {
    history.replaceState(null, '', location.pathname); // evita duplicados al recargar
    const last = Number(sessionStorage.getItem('lastNfc') || 0);
    if (Date.now() - last > 15000) { // protección contra doble lectura
      sessionStorage.setItem('lastNfc', String(Date.now()));
      add(S.cfg.bottle);
    }
  }

  render();
  setInterval(checkReminders, 20000);
  setInterval(render, 5 * 60 * 1000);
  document.addEventListener('visibilitychange', () => { if (!document.hidden) { render(); checkReminders(); } });
})();
</script>
</body>
</html>
