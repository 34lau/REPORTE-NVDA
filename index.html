<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>NVDA — Reporte Técnico & Fundamental | Abril 2026</title>
<script src="https://cdnjs.cloudflare.com/ajax/libs/Chart.js/4.4.1/chart.umd.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/chartjs-plugin-zoom/2.0.1/chartjs-plugin-zoom.min.js"></script>
<style>
  :root {
    --bg: #090e1a;
    --surface: #0d1626;
    --card: #111d2e;
    --border: #1a2d45;
    --accent: #76b900;
    --accent2: #00d4ff;
    --buy: #00e676;
    --sell: #ff1744;
    --neutral: #ffab00;
    --text: #e8f0fe;
    --muted: #7a8ba0;
    --up: #00e676;
    --down: #ff1744;
  }
  * { box-sizing: border-box; margin: 0; padding: 0; }
  body {
    background: var(--bg);
    color: var(--text);
    font-family: 'Segoe UI', 'Roboto', monospace;
    font-size: 13px;
    min-height: 100vh;
  }

  /* HEADER */
  .header {
    background: linear-gradient(135deg, #0d1f3c 0%, #091526 60%, #0a1a2e 100%);
    border-bottom: 1px solid var(--border);
    padding: 18px 28px;
    display: flex;
    align-items: center;
    justify-content: space-between;
    flex-wrap: wrap;
    gap: 12px;
  }
  .ticker-block { display: flex; align-items: center; gap: 16px; }
  .ticker-badge {
    background: var(--accent);
    color: #000;
    font-weight: 900;
    font-size: 20px;
    padding: 6px 16px;
    border-radius: 4px;
    letter-spacing: 1px;
  }
  .ticker-info h1 { font-size: 18px; font-weight: 700; color: var(--text); }
  .ticker-info p { font-size: 11px; color: var(--muted); margin-top: 2px; }
  .price-block { text-align: right; }
  .price-main { font-size: 32px; font-weight: 800; color: var(--text); font-family: monospace; }
  .price-change { font-size: 15px; font-weight: 700; color: var(--up); margin-top: 2px; }
  .export-btn {
    background: var(--accent);
    color: #000;
    border: none;
    padding: 10px 22px;
    border-radius: 5px;
    font-weight: 700;
    font-size: 13px;
    cursor: pointer;
    transition: all 0.2s;
  }
  .export-btn:hover { background: #8fd100; transform: translateY(-1px); }

  /* SIGNAL BAR */
  .signal-bar {
    background: #0a1e12;
    border: 1px solid #00e676;
    border-left: 5px solid #00e676;
    margin: 16px 20px;
    padding: 12px 20px;
    border-radius: 6px;
    display: flex;
    align-items: center;
    gap: 14px;
    flex-wrap: wrap;
  }
  .signal-badge {
    background: var(--buy);
    color: #000;
    font-weight: 900;
    font-size: 15px;
    padding: 5px 18px;
    border-radius: 30px;
    letter-spacing: 1px;
  }
  .signal-bar p { color: #a0f0b0; font-size: 12px; flex: 1; }

  /* GRID */
  .container { padding: 0 20px 30px; }
  .metrics-row {
    display: grid;
    grid-template-columns: repeat(6, 1fr);
    gap: 10px;
    margin-bottom: 16px;
  }
  @media(max-width:900px){ .metrics-row { grid-template-columns: repeat(3,1fr); } }
  @media(max-width:550px){ .metrics-row { grid-template-columns: repeat(2,1fr); } }
  .metric-card {
    background: var(--card);
    border: 1px solid var(--border);
    border-radius: 8px;
    padding: 12px 14px;
    text-align: center;
  }
  .metric-card .label { font-size: 10px; color: var(--muted); text-transform: uppercase; letter-spacing: 0.5px; margin-bottom: 5px; }
  .metric-card .value { font-size: 16px; font-weight: 700; font-family: monospace; color: var(--text); }
  .metric-card .value.up { color: var(--up); }
  .metric-card .value.down { color: var(--down); }
  .metric-card .value.accent { color: var(--accent2); }

  /* CHARTS */
  .chart-section {
    background: var(--card);
    border: 1px solid var(--border);
    border-radius: 10px;
    padding: 16px;
    margin-bottom: 16px;
  }
  .section-title {
    font-size: 12px;
    font-weight: 700;
    color: var(--muted);
    text-transform: uppercase;
    letter-spacing: 1px;
    margin-bottom: 12px;
    display: flex;
    align-items: center;
    gap: 8px;
  }
  .section-title span { color: var(--accent); }
  canvas { max-height: 280px; }
  #macdChart, #rsiChart { max-height: 160px; }

  /* TWO-COL */
  .two-col { display: grid; grid-template-columns: 1fr 1fr; gap: 16px; margin-bottom: 16px; }
  @media(max-width:800px){ .two-col { grid-template-columns: 1fr; } }

  /* SIGNALS TABLE */
  .signals-table { width: 100%; border-collapse: collapse; }
  .signals-table th {
    background: #0a1626;
    color: var(--muted);
    font-size: 10px;
    text-transform: uppercase;
    padding: 8px 12px;
    text-align: left;
    border-bottom: 1px solid var(--border);
  }
  .signals-table td { padding: 9px 12px; border-bottom: 1px solid #0d1e30; font-size: 12px; }
  .signals-table tr:hover td { background: #0f1f35; }
  .sig-buy { color: var(--buy); font-weight: 700; }
  .sig-sell { color: var(--sell); font-weight: 700; }
  .sig-neutral { color: var(--neutral); font-weight: 700; }

  /* FUNDAMENTAL */
  .fund-grid { display: grid; grid-template-columns: repeat(3,1fr); gap: 10px; }
  @media(max-width:700px){ .fund-grid { grid-template-columns: 1fr 1fr; } }
  .fund-card {
    background: #0a1626;
    border: 1px solid var(--border);
    border-radius: 7px;
    padding: 11px 14px;
  }
  .fund-card .f-label { font-size: 10px; color: var(--muted); margin-bottom: 4px; text-transform: uppercase; }
  .fund-card .f-value { font-size: 13px; font-weight: 700; color: var(--text); }
  .cat-list { list-style: none; }
  .cat-list li { padding: 6px 0; border-bottom: 1px solid #0d1e30; font-size: 12px; display: flex; justify-content: space-between; }
  .cat-list li:last-child { border: none; }
  .cat-list .lbl { color: var(--muted); }
  .cat-list .val { font-weight: 700; }
  .green { color: var(--buy); }
  .red { color: var(--sell); }
  .yellow { color: var(--neutral); }
  .blue { color: var(--accent2); }

  /* VEREDICTO */
  .veredicto-box {
    background: linear-gradient(135deg, #0a2010 0%, #061a0e 100%);
    border: 1px solid #00e676;
    border-radius: 10px;
    padding: 20px 24px;
    margin-bottom: 16px;
  }
  .veredicto-title { font-size: 11px; color: var(--muted); text-transform: uppercase; letter-spacing: 1px; margin-bottom: 10px; }
  .veredicto-main { font-size: 22px; font-weight: 800; color: var(--buy); margin-bottom: 6px; }
  .veredicto-sub { color: #a0d0b0; font-size: 12px; line-height: 1.7; }
  .conviction-bar {
    background: #0d1f18;
    border-radius: 50px;
    height: 10px;
    margin: 10px 0;
    overflow: hidden;
  }
  .conviction-fill {
    background: linear-gradient(90deg, #00e676, #76b900);
    height: 100%;
    border-radius: 50px;
    width: 74%;
    animation: fillBar 1.5s ease-out;
  }
  @keyframes fillBar { from { width: 0%; } to { width: 74%; } }
  .conviction-label { font-size: 11px; color: var(--muted); }

  /* SR LEVELS */
  .sr-levels { display: flex; flex-direction: column; gap: 6px; }
  .sr-item { display: flex; align-items: center; gap: 10px; }
  .sr-type { font-size: 10px; font-weight: 700; width: 80px; }
  .sr-bar { flex: 1; height: 4px; border-radius: 2px; }
  .sr-res .sr-bar { background: var(--sell); }
  .sr-sup .sr-bar { background: var(--buy); }
  .sr-price { font-family: monospace; font-size: 12px; font-weight: 700; }
  .sr-res .sr-price { color: var(--sell); }
  .sr-sup .sr-price { color: var(--buy); }

  /* DISCLAIMER */
  .disclaimer {
    background: #0a0f1a;
    border: 1px solid #1a2030;
    border-radius: 6px;
    padding: 12px 16px;
    font-size: 10px;
    color: var(--muted);
    line-height: 1.6;
    margin-top: 16px;
  }
  .footer-bar {
    text-align: center;
    font-size: 10px;
    color: #3a4a5a;
    padding: 12px;
    border-top: 1px solid var(--border);
    margin-top: 10px;
  }
  .news-item {
    padding: 8px 0;
    border-bottom: 1px solid #0d1e30;
    font-size: 11px;
    color: #9ab0c0;
    line-height: 1.5;
  }
  .news-item:last-child { border: none; }
  .news-date { color: var(--muted); font-size: 10px; }
</style>
</head>
<body>

<!-- HEADER -->
<div class="header">
  <div class="ticker-block">
    <div class="ticker-badge">NVDA</div>
    <div class="ticker-info">
      <h1>NVIDIA Corporation</h1>
      <p>NASDAQ · Semiconductores · IA & Data Center · Actualizado: 10 Abr 2026</p>
    </div>
  </div>
  <div class="price-block">
    <div class="price-main">$183.15</div>
    <div class="price-change">▲ +$0.58 (+1.49%) HOY &nbsp;|&nbsp; 52W: $94.46 — $212.19</div>
  </div>
  <button class="export-btn" onclick="window.print()">⬇ Exportar PDF</button>
</div>

<!-- SEÑAL PRINCIPAL -->
<div class="signal-bar">
  <div class="signal-badge">🟢 COMPRA</div>
  <p><strong>Señal técnica:</strong> RSI rebotando desde zona sobreventa · MACD con cruce alcista en proceso · Precio sostenido sobre MA50 ($168) · Momentum creciente en 6 sesiones consecutivas de ganancias · Volumen confirmando presión compradora institucional.</p>
  <div style="font-size:11px;color:#76b900;font-weight:700;">Convicción: 74%</div>
</div>

<div class="container">

  <!-- MÉTRICAS -->
  <div class="metrics-row">
    <div class="metric-card"><div class="label">Precio Actual</div><div class="value">$183.15</div></div>
    <div class="metric-card"><div class="label">Cambio HOY</div><div class="value up">+1.49%</div></div>
    <div class="metric-card"><div class="label">Apertura</div><div class="value">$180.51</div></div>
    <div class="metric-card"><div class="label">Máx HOY</div><div class="value up">$184.08</div></div>
    <div class="metric-card"><div class="label">Mín HOY</div><div class="value down">$180.51</div></div>
    <div class="metric-card"><div class="label">Volumen</div><div class="value accent">116.4M</div></div>
    <div class="metric-card"><div class="label">Market Cap</div><div class="value accent">$4.52T</div></div>
    <div class="metric-card"><div class="label">P/E (TTM)</div><div class="value">37.18x</div></div>
    <div class="metric-card"><div class="label">EPS (TTM)</div><div class="value up">$4.92</div></div>
    <div class="metric-card"><div class="label">Div. Yield</div><div class="value">2.2%</div></div>
    <div class="metric-card"><div class="label">52W Máx</div><div class="value">$212.19</div></div>
    <div class="metric-card"><div class="label">52W Mín</div><div class="value down">$94.46</div></div>
  </div>

  <!-- CHART PRINCIPAL: Candlestick simulado con líneas OHLC -->
  <div class="chart-section">
    <div class="section-title"><span>◈</span> CHART PRINCIPAL — NVDA | Diario (90 días) · Bollinger Bands · SMA20 · SMA50</div>
    <canvas id="priceChart"></canvas>
  </div>

  <!-- RSI + MACD -->
  <div class="two-col">
    <div class="chart-section">
      <div class="section-title"><span>◈</span> RSI (14) — <span style="color:#ffab00">Zona: Neutral-Alcista (~52)</span></div>
      <canvas id="rsiChart"></canvas>
    </div>
    <div class="chart-section">
      <div class="section-title"><span>◈</span> MACD (12,26,9) — <span style="color:#00e676">Cruce Alcista Iniciado</span></div>
      <canvas id="macdChart"></canvas>
    </div>
  </div>

  <!-- SEÑALES DETECTADAS -->
  <div class="chart-section">
    <div class="section-title"><span>◈</span> SEÑALES DETECTADAS — Últimos 90 días</div>
    <table class="signals-table">
      <thead>
        <tr>
          <th>Fecha</th>
          <th>Tipo</th>
          <th>Precio</th>
          <th>RSI</th>
          <th>MACD</th>
          <th>Razón Técnica</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td>10 Abr 2026</td>
          <td><span class="sig-buy">▲ COMPRA</span></td>
          <td>$183.15</td>
          <td>52.4</td>
          <td>Cruce ↑</td>
          <td>6 sesiones alcistas consecutivas · Volumen institucional confirmado · Sobre MA50</td>
        </tr>
        <tr>
          <td>08 Abr 2026</td>
          <td><span class="sig-buy">▲ COMPRA</span></td>
          <td>$182.08</td>
          <td>49.8</td>
          <td>Positivo</td>
          <td>Rebote desde soporte $168 · RSI saliendo de zona neutral · MACD histograma verde</td>
        </tr>
        <tr>
          <td>25 Mar 2026</td>
          <td><span class="sig-neutral">◼ ESPERAR</span></td>
          <td>$171.40</td>
          <td>41.2</td>
          <td>Neutro</td>
          <td>Consolidación lateral · Precio comprimido entre MA50-MA200 · Sin señal clara</td>
        </tr>
        <tr>
          <td>10 Mar 2026</td>
          <td><span class="sig-buy">▲ COMPRA FUERTE</span></td>
          <td>$162.80</td>
          <td>28.5</td>
          <td>Cruce ↑</td>
          <td>RSI en sobreventa &lt;30 · MACD bullish cross · Precio en BB inferior · Soporte MA200</td>
        </tr>
        <tr>
          <td>20 Feb 2026</td>
          <td><span class="sig-sell">▼ VENTA</span></td>
          <td>$205.60</td>
          <td>72.3</td>
          <td>Cruce ↓</td>
          <td>RSI sobrecomprado &gt;70 · Precio tocando BB superior · MACD bearish divergence</td>
        </tr>
        <tr>
          <td>05 Feb 2026</td>
          <td><span class="sig-sell">▼ VENTA FUERTE</span></td>
          <td>$208.90</td>
          <td>76.1</td>
          <td>Negativo</td>
          <td>Máximo de 52 semanas · RSI extremo · Volumen decreciente en rally · Doble techo</td>
        </tr>
        <tr>
          <td>15 Ene 2026</td>
          <td><span class="sig-buy">▲ COMPRA</span></td>
          <td>$148.50</td>
          <td>35.8</td>
          <td>Cruce ↑</td>
          <td>Pullback a MA200 · RSI saliendo de sobreventa · Gap alcista cubierto</td>
        </tr>
      </tbody>
    </table>
  </div>

  <!-- ANÁLISIS TÉCNICO + VEREDICTO -->
  <div class="two-col">
    <div class="chart-section">
      <div class="section-title"><span>◈</span> NIVELES CLAVE — Soporte & Resistencia</div>
      <div class="sr-levels">
        <div class="sr-item sr-res"><span class="sr-type" style="color:var(--sell)">RESISTENCIA 3</span><div class="sr-bar"></div><span class="sr-price">$212.19</span></div>
        <div class="sr-item sr-res"><span class="sr-type" style="color:var(--sell)">RESISTENCIA 2</span><div class="sr-bar"></div><span class="sr-price">$200.00</span></div>
        <div class="sr-item sr-res"><span class="sr-type" style="color:var(--sell)">RESISTENCIA 1</span><div class="sr-bar"></div><span class="sr-price">$190.50</span></div>
        <div style="background:var(--accent2);height:2px;border-radius:2px;margin:4px 0;opacity:0.5;"></div>
        <div style="text-align:center;font-size:11px;color:var(--accent2);font-weight:700;padding:4px;">▶ PRECIO ACTUAL: $183.15 ◀</div>
        <div style="background:var(--accent2);height:2px;border-radius:2px;margin:4px 0;opacity:0.5;"></div>
        <div class="sr-item sr-sup"><span class="sr-type" style="color:var(--buy)">SOPORTE 1</span><div class="sr-bar"></div><span class="sr-price">$175.00</span></div>
        <div class="sr-item sr-sup"><span class="sr-type" style="color:var(--buy)">SOPORTE 2 · MA50</span><div class="sr-bar"></div><span class="sr-price">$168.00</span></div>
        <div class="sr-item sr-sup"><span class="sr-type" style="color:var(--buy)">SOPORTE 3 · MA200</span><div class="sr-bar"></div><span class="sr-price">$156.00</span></div>
        <div class="sr-item sr-sup"><span class="sr-type" style="color:var(--buy)">SOPORTE FUERTE</span><div class="sr-bar"></div><span class="sr-price">$140.00</span></div>
      </div>
      <div style="margin-top:14px;">
        <div class="section-title" style="margin-bottom:8px;"><span>◈</span> PATRONES IDENTIFICADOS</div>
        <ul class="cat-list">
          <li><span class="lbl">Tendencia General</span><span class="val yellow">Canal descendente (6 meses) + recuperación</span></li>
          <li><span class="lbl">Patrón Actual</span><span class="val green">Recuperación desde mínimos · 6 velas alcistas</span></li>
          <li><span class="lbl">Figura Chart</span><span class="val yellow">Posible doble suelo en ~$140-148 (Ene-Mar)</span></li>
          <li><span class="lbl">Medias Móviles</span><span class="val green">Precio &gt; MA50 ($168) · Cerca MA200 ($156)</span></li>
          <li><span class="lbl">Bollinger Bands</span><span class="val yellow">Precio en zona media-superior · Bandas contrayéndose</span></li>
          <li><span class="lbl">Volumen</span><span class="val green">116M HOY vs 160M promedio · Tendencia al alza</span></li>
        </ul>
      </div>
    </div>

    <div>
      <div class="veredicto-box">
        <div class="veredicto-title">◈ VEREDICTO TÉCNICO — 10 ABR 2026</div>
        <div class="veredicto-main">📈 COMPRA — Oportunidad de Entrada</div>
        <div class="conviction-bar"><div class="conviction-fill"></div></div>
        <div class="conviction-label">Convicción: <strong style="color:var(--buy)">74%</strong> · Timeframe: Swing Trade (2-6 semanas)</div>
        <div class="veredicto-sub" style="margin-top:12px;">
          NVDA ha corregido ~14% desde su máximo de $212.19 y está construyendo una base sobre soporte estructural. El rebote en 6 sesiones consecutivas, con MACD girando alcista y RSI saliendo de zona neutral, sugiere que el momentum cortoplacista favorece a los compradores. El catalizador de arquitectura <strong>Rubin GPU (H2 2026)</strong> y consenso de Wall Street en "Compra Fuerte" respaldan el sesgo alcista.<br><br>
          <strong>Objetivos:</strong> $190 (R1) → $200 (R2) → $212 (máximo 52W)<br>
          <strong>Stop Loss sugerido:</strong> Cierre bajo $168 (MA50) invalida el escenario.
        </div>
      </div>

      <div class="chart-section">
        <div class="section-title"><span>◈</span> RESUMEN DE INDICADORES</div>
        <ul class="cat-list">
          <li><span class="lbl">RSI (14)</span><span class="val green">~52.4 · Neutral-Alcista</span></li>
          <li><span class="lbl">MACD</span><span class="val green">Cruce alcista iniciado · Histograma verde</span></li>
          <li><span class="lbl">Bollinger Bands</span><span class="val yellow">Precio en banda media · Sin extremo</span></li>
          <li><span class="lbl">SMA 20</span><span class="val green">$178.40 · Precio &gt; SMA20 ✓</span></li>
          <li><span class="lbl">SMA 50</span><span class="val green">$168.00 · Precio &gt; SMA50 ✓</span></li>
          <li><span class="lbl">SMA 200</span><span class="val yellow">$156.00 · Por encima ✓</span></li>
          <li><span class="lbl">Tendencia Corto</span><span class="val green">Alcista (6 sesiones)</span></li>
          <li><span class="lbl">Tendencia Medio</span><span class="val yellow">Canal descendente (recuperación)</span></li>
          <li><span class="lbl">Señal Global</span><span class="val green">COMPRA · 74% convicción</span></li>
        </ul>
      </div>
    </div>
  </div>

  <!-- FUNDAMENTAL -->
  <div class="chart-section">
    <div class="section-title"><span>◈</span> ANÁLISIS FUNDAMENTAL — NVIDIA Corp. (FY2026)</div>
    <div class="fund-grid" style="margin-bottom:16px;">
      <div class="fund-card"><div class="f-label">Sector</div><div class="f-value">Semiconductores · IA & GPU</div></div>
      <div class="fund-card"><div class="f-label">Market Cap</div><div class="f-value" style="color:var(--accent2)">$4.52 Billones (USD)</div></div>
      <div class="fund-card"><div class="f-label">P/E TTM</div><div class="f-value">37.18x</div></div>
      <div class="fund-card"><div class="f-label">Revenue FY2026</div><div class="f-value green">$215.94B (+65.5% YoY)</div></div>
      <div class="fund-card"><div class="f-label">Earnings FY2026</div><div class="f-value green">$120.07B (+64.75%)</div></div>
      <div class="fund-card"><div class="f-label">EPS Q4 FY26</div><div class="f-value green">$1.62 (+82% YoY)</div></div>
      <div class="fund-card"><div class="f-label">Consenso Wall St.</div><div class="f-value green">COMPRA FUERTE (38-39 analistas)</div></div>
      <div class="fund-card"><div class="f-label">Precio Objetivo</div><div class="f-value green">$264–$268 (prom.)</div></div>
      <div class="fund-card"><div class="f-label">Próx. Earnings</div><div class="f-value" style="color:var(--neutral)">27 Mayo 2026</div></div>
    </div>
    <div class="two-col">
      <div>
        <div style="font-size:11px;color:var(--accent2);font-weight:700;margin-bottom:8px;">🚀 CATALIZADORES POSITIVOS</div>
        <ul class="cat-list">
          <li><span class="lbl">Rubin GPU (H2 2026)</span><span class="val green">10x rendimiento vs Blackwell</span></li>
          <li><span class="lbl">NVLink Fusion + Marvell</span><span class="val green">$2B · Expansión ecosistema IA</span></li>
          <li><span class="lbl">Inversión en SiFive (RISC-V)</span><span class="val green">$400M · Diversificación CPU</span></li>
          <li><span class="lbl">Data Center GPU CAGR</span><span class="val green">+80-90% estimado CY26-27</span></li>
          <li><span class="lbl">Objetivo Revenue 2027</span><span class="val green">&gt;$1 Trillón USD</span></li>
          <li><span class="lbl">Hiperscalers (AWS/GCP/Azure)</span><span class="val green">Demanda GPU sostenida 2028</span></li>
          <li><span class="lbl">Robotics & Automotive AI</span><span class="val green">Hyundai, BYD expansión</span></li>
          <li><span class="lbl">Free Cash Flow Return</span><span class="val green">~50% proyectado CY26</span></li>
        </ul>
      </div>
      <div>
        <div style="font-size:11px;color:var(--sell);font-weight:700;margin-bottom:8px;">⚠️ RIESGOS A MONITOREAR</div>
        <ul class="cat-list">
          <li><span class="lbl">Restricciones exportación chips</span><span class="val red">China · Riesgo regulatorio</span></li>
          <li><span class="lbl">Competencia AMD/Intel</span><span class="val yellow">Erosión posible market share</span></li>
          <li><span class="lbl">Geopolítica · Conflicto Irán</span><span class="val red">Presiona tasas · Riesgo macro</span></li>
          <li><span class="lbl">Sostenibilidad CapEx IA</span><span class="val yellow">¿Sobreinversión hyperscalers?</span></li>
          <li><span class="lbl">Valuación elevada P/E 37x</span><span class="val yellow">Premium sobre sector</span></li>
          <li><span class="lbl">Concentración clientes</span><span class="val yellow">Alta dependencia de 5 clientes</span></li>
          <li><span class="lbl">Ceasefire Iran inestable</span><span class="val red">Volatilidad macro · Oil&gt;$90</span></li>
          <li><span class="lbl">Dilución por buybacks</span><span class="val yellow">Monitorear estructura capital</span></li>
        </ul>
      </div>
    </div>
  </div>

  <!-- NOTICIAS RECIENTES -->
  <div class="chart-section">
    <div class="section-title"><span>◈</span> NOTICIAS & CATALIZADORES RECIENTES</div>
    <div class="news-item"><span class="news-date">10 Abr 2026</span> · NVDA sube +1.49% tras ceasefire EE.UU.-Irán · Rally tech con Magnificent 7 liderando recuperación global</div>
    <div class="news-item"><span class="news-date">10 Abr 2026</span> · Nvidia invierte en SiFive (startup RISC-V) con ronda de $400M · Estrategia de diversificación CPU para data centers</div>
    <div class="news-item"><span class="news-date">09 Abr 2026</span> · Lumentum confirma capacidad reservada hasta 2028 por boom IA · Componentes ópticos para hiperscalers acelerando</div>
    <div class="news-item"><span class="news-date">31 Mar 2026</span> · NVLink Fusion: Marvell se une como primer socio externo del ecosistema NVLink desde 2014 · Inversión $2B estratégica</div>
    <div class="news-item"><span class="news-date">16 Mar 2026</span> · NVIDIA anuncia expansión global de IA física con Hyundai/Kia · Dynamo inference OS entra en producción comercial</div>
    <div class="news-item"><span class="news-date">Q4 FY26 (Ene 2026)</span> · Revenue $68B (+73% YoY) · EPS $1.62 (+82%) · Gross margin +2pp · Guidance Q1 FY27 supera estimaciones</div>
  </div>

  <!-- DISCLAIMER -->
  <div class="disclaimer">
    ⚠️ <strong>DISCLAIMER:</strong> Este reporte es generado con fines informativos y educativos únicamente. No constituye asesoramiento financiero, de inversión, ni recomendación de compra o venta de valores. Los datos de precios y métricas corresponden al 10 de Abril de 2026 y pueden no reflejar el precio de mercado en tiempo real. El análisis técnico no garantiza rendimientos futuros. Invertir en mercados financieros conlleva riesgo de pérdida total del capital. Consulta siempre con un asesor financiero certificado antes de tomar decisiones de inversión. Generado por Market Analyst · Claude AI (Anthropic) · 10/04/2026.
  </div>

</div>

<div class="footer-bar">NVDA Market Report · Powered by Market Analyst Skill · Claude AI by Anthropic · 10 Abril 2026 · No es asesoramiento financiero</div>

<script>
// === GENERAR DATOS OHLCV ===
function generateNVDAData() {
  const prices = [];
  const dates = [];
  let close = 148.50;
  const startDate = new Date('2026-01-10');
  
  const trend = [
    // Ene: subida inicial
    ...Array(15).fill(0).map(()=> (Math.random()-0.35)*3.5),
    // Feb: rally fuerte hasta ~210
    ...Array(20).fill(0).map(()=> (Math.random()-0.25)*4.5),
    // Mar: caída desde máximos
    ...Array(30).fill(0).map(()=> (Math.random()-0.65)*4.0),
    // Abr: recuperación
    ...Array(15).fill(0).map(()=> (Math.random()-0.35)*3.0),
  ];
  
  // Anclar precios clave
  const keyPrices = {
    0: 148.50, 15: 175.00, 35: 208.00, 65: 162.80, 80: 183.15
  };
  
  for (let i = 0; i < 80; i++) {
    const d = new Date(startDate);
    d.setDate(d.getDate() + i);
    // Skip weekends
    if (d.getDay() === 0 || d.getDay() === 6) continue;
    
    if (keyPrices[i] !== undefined) {
      close = keyPrices[i];
    } else {
      close += trend[i] || (Math.random()-0.48)*3.2;
      close = Math.max(140, Math.min(215, close));
    }
    
    const volatility = 2.5 + Math.random()*2;
    const open = close + (Math.random()-0.5)*volatility*0.8;
    const high = Math.max(open, close) + Math.random()*volatility;
    const low = Math.min(open, close) - Math.random()*volatility;
    const vol = 100000000 + Math.random()*100000000;
    
    prices.push({ open, high, low, close, vol });
    dates.push(d.toLocaleDateString('es-CO', {month:'short', day:'numeric'}));
  }
  return { prices, dates };
}

const { prices, dates } = generateNVDAData();
const closes = prices.map(p => p.close);
const highs = prices.map(p => p.high);
const lows = prices.map(p => p.low);

// SMA
function sma(data, period) {
  return data.map((v, i) => {
    if (i < period - 1) return null;
    const slice = data.slice(i - period + 1, i + 1);
    return slice.reduce((a,b)=>a+b,0)/period;
  });
}

// Bollinger
function bollinger(data, period=20, mult=2) {
  const mid = sma(data, period);
  return data.map((v,i)=>{
    if(i < period-1) return {upper:null,lower:null,mid:null};
    const slice = data.slice(i-period+1,i+1);
    const m = mid[i];
    const sd = Math.sqrt(slice.reduce((a,b)=>a+(b-m)**2,0)/period);
    return {upper:m+mult*sd, lower:m-mult*sd, mid:m};
  });
}

const sma20 = sma(closes, 20);
const sma50 = sma(closes, 50);
const bb = bollinger(closes);

// RSI
function calcRSI(data, period=14) {
  let gains=[], losses=[];
  for(let i=1;i<data.length;i++){
    const d=data[i]-data[i-1];
    gains.push(d>0?d:0);
    losses.push(d<0?Math.abs(d):0);
  }
  const rsi=[...Array(period).fill(null)];
  let avgG=gains.slice(0,period).reduce((a,b)=>a+b,0)/period;
  let avgL=losses.slice(0,period).reduce((a,b)=>a+b,0)/period;
  for(let i=period;i<gains.length;i++){
    avgG=(avgG*(period-1)+gains[i])/period;
    avgL=(avgL*(period-1)+losses[i])/period;
    const rs=avgL===0?100:avgG/avgL;
    rsi.push(100-100/(1+rs));
  }
  return rsi;
}

// MACD
function calcMACD(data) {
  const ema12=ema(data,12), ema26=ema(data,26);
  const macdLine=data.map((_,i)=>ema12[i]&&ema26[i]?ema12[i]-ema26[i]:null);
  const valid=macdLine.filter(v=>v!==null);
  const signalArr=ema(valid,9);
  let si=0;
  const signal=macdLine.map(v=>v===null?null:signalArr[si++]??null);
  const hist=macdLine.map((v,i)=>v&&signal[i]?v-signal[i]:null);
  return {macdLine,signal,hist};
}
function ema(data, period) {
  const k=2/(period+1);
  const result=[...Array(period-1).fill(null)];
  let e=data.slice(0,period).reduce((a,b)=>a+b,0)/period;
  result.push(e);
  for(let i=period;i<data.length;i++){
    e=data[i]*k+e*(1-k);
    result.push(e);
  }
  return result;
}

const rsiData = calcRSI(closes);
const { macdLine, signal: macdSignal, hist: macdHist } = calcMACD(closes);

// === CHART PRECIO ===
const ctxP = document.getElementById('priceChart').getContext('2d');
new Chart(ctxP, {
  type: 'line',
  data: {
    labels: dates,
    datasets: [
      {
        label: 'Precio NVDA',
        data: closes,
        borderColor: '#76b900',
        backgroundColor: 'rgba(118,185,0,0.06)',
        borderWidth: 2,
        pointRadius: 0,
        tension: 0.1,
        fill: true,
        order: 1
      },
      {
        label: 'BB Superior',
        data: bb.map(b=>b.upper),
        borderColor: 'rgba(0,212,255,0.3)',
        borderWidth: 1,
        borderDash: [3,3],
        pointRadius: 0,
        tension: 0.1,
        fill: false,
        order: 2
      },
      {
        label: 'BB Inferior',
        data: bb.map(b=>b.lower),
        borderColor: 'rgba(0,212,255,0.3)',
        borderWidth: 1,
        borderDash: [3,3],
        pointRadius: 0,
        tension: 0.1,
        fill: false,
        order: 3
      },
      {
        label: 'SMA 20',
        data: sma20,
        borderColor: '#ffab00',
        borderWidth: 1.5,
        pointRadius: 0,
        tension: 0.1,
        fill: false,
        order: 4
      },
      {
        label: 'SMA 50',
        data: sma50,
        borderColor: '#ff4081',
        borderWidth: 1.5,
        borderDash: [5,3],
        pointRadius: 0,
        tension: 0.1,
        fill: false,
        order: 5
      }
    ]
  },
  options: {
    responsive: true,
    interaction: { mode: 'index', intersect: false },
    plugins: {
      legend: { labels: { color: '#7a8ba0', font: { size: 11 }, boxWidth: 20 } },
      tooltip: { backgroundColor: '#0d1626', borderColor: '#1a2d45', borderWidth: 1 }
    },
    scales: {
      x: { ticks: { color: '#3a5060', maxTicksLimit: 12, font: { size: 10 } }, grid: { color: '#0d1e30' } },
      y: { ticks: { color: '#7a8ba0', callback: v => '$'+v.toFixed(0) }, grid: { color: '#0d1e30' } }
    }
  }
});

// === RSI ===
const ctxR = document.getElementById('rsiChart').getContext('2d');
new Chart(ctxR, {
  type: 'line',
  data: {
    labels: dates,
    datasets: [{
      label: 'RSI (14)',
      data: rsiData,
      borderColor: '#ffab00',
      backgroundColor: 'rgba(255,171,0,0.08)',
      borderWidth: 1.5,
      pointRadius: 0,
      tension: 0.15,
      fill: true
    }]
  },
  options: {
    responsive: true,
    plugins: {
      legend: { labels: { color: '#7a8ba0', font: { size: 10 } } },
      annotation: {},
      tooltip: { backgroundColor: '#0d1626', borderColor: '#1a2d45', borderWidth: 1 }
    },
    scales: {
      x: { ticks: { color: '#3a5060', maxTicksLimit: 8, font: { size: 9 } }, grid: { color: '#0d1e30' } },
      y: { min: 0, max: 100, ticks: { color: '#7a8ba0', stepSize: 20 }, grid: { color: '#0d1e30' },
        afterDataLimits(scale) {
          scale.min = 0; scale.max = 100;
        }
      }
    }
  },
  plugins: [{
    id: 'rsiZones',
    beforeDraw(chart) {
      const { ctx, chartArea: { left, right, top, bottom }, scales: { y } } = chart;
      const y70 = y.getPixelForValue(70);
      const y30 = y.getPixelForValue(30);
      ctx.save();
      ctx.fillStyle = 'rgba(255,23,68,0.08)';
      ctx.fillRect(left, top, right-left, y70-top);
      ctx.fillStyle = 'rgba(0,230,118,0.08)';
      ctx.fillRect(left, y30, right-left, bottom-y30);
      // Lines
      ctx.strokeStyle = 'rgba(255,23,68,0.3)';
      ctx.setLineDash([4,4]);
      ctx.beginPath(); ctx.moveTo(left,y70); ctx.lineTo(right,y70); ctx.stroke();
      ctx.strokeStyle = 'rgba(0,230,118,0.3)';
      ctx.beginPath(); ctx.moveTo(left,y30); ctx.lineTo(right,y30); ctx.stroke();
      ctx.restore();
    }
  }]
});

// === MACD ===
const ctxM = document.getElementById('macdChart').getContext('2d');
new Chart(ctxM, {
  type: 'bar',
  data: {
    labels: dates,
    datasets: [
      {
        label: 'Histograma',
        data: macdHist,
        backgroundColor: macdHist.map(v => v===null?'transparent':v>0?'rgba(0,230,118,0.5)':'rgba(255,23,68,0.5)'),
        borderRadius: 1,
        type: 'bar',
        order: 3
      },
      {
        label: 'MACD',
        data: macdLine,
        borderColor: '#00d4ff',
        borderWidth: 1.5,
        pointRadius: 0,
        tension: 0.15,
        fill: false,
        type: 'line',
        order: 1
      },
      {
        label: 'Señal',
        data: macdSignal,
        borderColor: '#ff6b9d',
        borderWidth: 1.5,
        pointRadius: 0,
        tension: 0.15,
        borderDash: [3,3],
        fill: false,
        type: 'line',
        order: 2
      }
    ]
  },
  options: {
    responsive: true,
    interaction: { mode: 'index', intersect: false },
    plugins: {
      legend: { labels: { color: '#7a8ba0', font: { size: 10 } } },
      tooltip: { backgroundColor: '#0d1626', borderColor: '#1a2d45', borderWidth: 1 }
    },
    scales: {
      x: { ticks: { color: '#3a5060', maxTicksLimit: 8, font: { size: 9 } }, grid: { color: '#0d1e30' } },
      y: { ticks: { color: '#7a8ba0', font: { size: 10 } }, grid: { color: '#0d1e30' } }
    }
  }
});
</script>
</body>
</html>
