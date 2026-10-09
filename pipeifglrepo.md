<img width="1200" height="480" alt="INGENIERO DE SISTEMAS" src="https://github.com/user-attachments/assets/1c433295-9d17-45d5-af8b-be1a38dec068" />
<div align="center">
</div>
<h3 align="center">Hola 👋, soy Iván Felipe González Lozano</h3>
<p align="center">
  Ingeniero de Sistemas y diseñador UX/UI junior con experiencia en tecnología y diseño digital.
  Cuenta con experiencia en infraestructura tecnológica, administración y mantenimiento de redes,
  soporte técnico, optimización de equipos y desarrollo de soluciones digitales. También ha participado
  en proyectos de UX/UI, diseño web, identidad visual y creación de piezas gráficas. 
<h2 align="center">Ubicación</h2> 

<p align="center">
  <a href="https://www.google.com/maps/search/?api=1&query=Bogotá,+Colombia">
    <img src="https://img.shields.io/badge/UBICACIÓN-Bogotá,%20Colombia-30363D?style=for-the-badge&logo=googlemaps&logoColor=white&labelColor=0D1117" alt="Ubicación: Bogotá, Colombia"> 
  <!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>Mi música</title>
<style>
  * { box-sizing: border-box; }
  body {
    margin: 0; min-height: 100vh; display: grid; place-items: center;
    background: #0d1117; color: #e6edf3;
    font-family: system-ui, -apple-system, "Segoe UI", sans-serif;
  }
  .card {
    width: min(92vw, 520px); background: #161b22; border: 1px solid #30363d;
    border-radius: 18px; padding: 20px; box-shadow: 0 12px 40px rgba(0,0,0,.55);
  }
  .tag { font-size: 12px; letter-spacing: .14em; color: #8b949e; margin-bottom: 12px; }
  .video { position: relative; aspect-ratio: 16 / 9; border-radius: 12px; overflow: hidden; background: #000; }
  .video iframe { position: absolute; inset: 0; width: 100%; height: 100%; border: 0; }
  .info { margin: 16px 2px 12px; }
  .title { font-weight: 700; font-size: 17px; }
  .artist { color: #8b949e; font-size: 14px; margin-top: 2px; }
  .controls { display: flex; align-items: center; gap: 12px; }
  #btn {
    width: 48px; height: 48px; border-radius: 50%; border: 0; cursor: pointer;
    background: #ff0033; color: #fff; font-size: 18px; flex: none;
  }
  #btn:hover { background: #ff3358; }
  .bar { flex: 1; display: flex; flex-direction: column; gap: 4px; }
  input[type=range] { width: 100%; accent-color: #ff0033; cursor: pointer; }
  .time { display: flex; justify-content: space-between; font-size: 12px; color: #8b949e; }
  .vol { display: flex; align-items: center; gap: 8px; margin-top: 12px; color: #8b949e; font-size: 14px; }
  .vol input { max-width: 140px; }
  .back { display: block; text-align: center; margin-top: 16px; font-size: 13px; color: #58a6ff; text-decoration: none; }
</style>
</head>
<body>
  <div class="card">
    <div class="tag">🎧 MI MÚSICA</div>

    <div class="video"><div id="player"></div></div>

    <div class="info">
      <div class="title">No Good [Live from ÆDEN Mexico City]</div>
      <div class="artist">Anyma, Stylo</div>
    </div>

    <div class="controls">
      <button id="btn" aria-label="Reproducir / Pausar">▶</button>
      <div class="bar">
        <input id="seek" type="range" min="0" max="100" value="0" step="0.1" aria-label="Progreso">
        <div class="time"><span id="cur">0:00</span><span id="dur">0:00</span></div>
      </div>
    </div>

    <div class="vol">
      🔊 <input id="vol" type="range" min="0" max="100" value="80" aria-label="Volumen">
    </div>

    <a class="back" href="javascript:history.back()">← Volver al repositorio</a>
  </div>

<script>
  var VIDEO_ID = '9br_LNtG-lg';
  var player, timer;
  var btn = document.getElementById('btn');
  var seek = document.getElementById('seek');
  var vol = document.getElementById('vol');
  var cur = document.getElementById('cur');
  var dur = document.getElementById('dur');

  var tag = document.createElement('script');
  tag.src = 'https://www.youtube.com/iframe_api';
  document.head.appendChild(tag);

  function fmt(s) {
    s = Math.floor(s || 0);
    return Math.floor(s / 60) + ':' + String(s % 60).padStart(2, '0');
  }

  function onYouTubeIframeAPIReady() {
    player = new YT.Player('player', {
      videoId: VIDEO_ID,
      playerVars: { controls: 0, rel: 0, playsinline: 1, modestbranding: 1 },
      events: {
        onReady: function () { player.setVolume(+vol.value); dur.textContent = fmt(player.getDuration()); },
        onStateChange: onState
      }
    });
  }

  function onState(e) {
    var playing = e.data === YT.PlayerState.PLAYING;
    btn.textContent = playing ? '❚❚' : '▶';
    dur.textContent = fmt(player.getDuration());
    clearInterval(timer);
    if (playing) {
      timer = setInterval(function () {
        var d = player.getDuration() || 1;
        seek.value = (player.getCurrentTime() / d) * 100;
        cur.textContent = fmt(player.getCurrentTime());
      }, 500);
    }
  }

  btn.onclick = function () {
    if (!player) return;
    player.getPlayerState() === YT.PlayerState.PLAYING ? player.pauseVideo() : player.playVideo();
  };
  seek.oninput = function () {
    if (!player) return;
    player.seekTo((seek.value / 100) * player.getDuration(), true);
  };
  vol.oninput = function () { if (player) player.setVolume(+vol.value); };
</script>
</body>
</html>
<h2 align="center">Habilidades</h2>
<p align="center">
  <img src="https://img.shields.io/badge/Figma-F24E1E?style=for-the-badge" alt="Figma">
  <img src="https://img.shields.io/badge/Adobe%20XD-FF61F6?style=for-the-badge" alt="Adobe XD">
  <img src="https://img.shields.io/badge/Adobe%20Express-5258E4?style=for-the-badge" alt="Adobe Express">
  <img src="https://img.shields.io/badge/Adobe%20Firefly-EB1000?style=for-the-badge" alt="Adobe Firefly">
  <img src="https://img.shields.io/badge/Canva-00C4CC?style=for-the-badge" alt="Canva">
  <img src="https://img.shields.io/badge/Balsamiq%20Mockups-CC0000?style=for-the-badge" alt="Balsamiq Mockups">
  <img src="https://img.shields.io/badge/Pencil%20Project-4CAF50?style=for-the-badge" alt="Pencil Project">
  <img src="https://img.shields.io/badge/Notion-000000?style=for-the-badge" alt="Notion">
  <img src="https://img.shields.io/badge/Office%20365-D83B01?style=for-the-badge" alt="Office 365">
  <img src="https://img.shields.io/badge/Soporte%20TI-0078D4?style=for-the-badge" alt="Soporte TI">
  <img src="https://img.shields.io/badge/Mantenimiento%20de%20Equipos-6C757D?style=for-the-badge" alt="Mantenimiento de Equipos">
</p>
<h2 align="center">Experiencia laboral</h2>

<!-- EXPERIENCIA 1 -->
<table align="center" width="100%">
  <tr>
    <td width="70%"><h3>🏢 Inflaparque Acuático Ikarus Ecoparque</h3><b>Productor digital</b></td>
    <td width="30%" align="center"><h3>📅 2025 - 2026</h3></td>
  </tr>
  <tr>
    <td colspan="2">
      Desarrolló publicaciones para redes sociales, apoyó iniciativas y proyectos, colaboró en tareas de soporte de TI y marketing digital, atendió consultas de servicio al cliente a través de la página web y gestionó el registro y seguimiento de tickets.
    </td>
  </tr>
</table>

<!-- EXPERIENCIA 2 -->
<table align="center" width="100%">
  <tr>
    <td width="70%"><h3>🏢 Dinamo Marketing</h3><b>Productor digital</b></td>
    <td width="30%" align="center"><h3>📅 2024</h3></td>
  </tr>
  <tr>
    <td colspan="2">
      Planificó y apoyó la producción de contenidos y piezas digitales, coordinó ideas, diseño y publicación según las necesidades de cada proyecto, y colaboró en la creación de materiales para plataformas digitales. Cuidó la calidad visual y la claridad de los mensajes, contribuyendo a mejorar la presentación de los proyectos y a entregar contenidos atractivos para sus usuarios.
    </td>
  </tr>
</table>

<!-- EXPERIENCIA 3 -->
<table align="center" width="100%">
  <tr>
    <td width="70%"><h3>🏢 Nombre de la empresa 3</h3><b>Cargo</b></td>
    <td width="30%" align="center"><h3>📅 2023 - 2024</h3></td>
  </tr>
  <tr>
    <td colspan="2">
      Escribe aquí tu experiencia en esta empresa (mínimo 500 caracteres). Describe las funciones que desempeñaste, las herramientas y tecnologías que utilizaste, los proyectos en los que participaste y los logros o resultados que obtuviste. Por ejemplo: administración y mantenimiento de redes, soporte técnico a usuarios, optimización de equipos, diseño de interfaces en Figma, creación de piezas gráficas y documentación de procesos. Explica también cómo contribuiste al equipo y qué aprendiste durante esta etapa.
    </td>
  </tr>
</table>

<!-- EXPERIENCIA 4 -->
<table align="center" width="100%">
  <tr>
    <td width="70%"><h3>🏢 Nombre de la empresa 4</h3><b>Cargo</b></td>
    <td width="30%" align="center"><h3>📅 2022 - 2023</h3></td>
  </tr>
  <tr>
    <td colspan="2">
      Escribe aquí tu experiencia en esta empresa (mínimo 500 caracteres). Describe las funciones que desempeñaste, las herramientas y tecnologías que utilizaste, los proyectos en los que participaste y los logros o resultados que obtuviste. Por ejemplo: administración y mantenimiento de redes, soporte técnico a usuarios, optimización de equipos, diseño de interfaces en Figma, creación de piezas gráficas y documentación de procesos. Explica también cómo contribuiste al equipo y qué aprendiste durante esta etapa.
    </td>
  </tr>
</table>

<!-- EXPERIENCIA 5 -->
<table align="center" width="100%">
  <tr>
    <td width="70%"><h3>🏢 Nombre de la empresa 5</h3><b>Cargo</b></td>
    <td width="30%" align="center"><h3>📅 2021 - 2022</h3></td>
  </tr>
  <tr>
    <td colspan="2">
      Escribe aquí tu experiencia en esta empresa (mínimo 500 caracteres). Describe las funciones que desempeñaste, las herramientas y tecnologías que utilizaste, los proyectos en los que participaste y los logros o resultados que obtuviste. Por ejemplo: administración y mantenimiento de redes, soporte técnico a usuarios, optimización de equipos, diseño de interfaces en Figma, creación de piezas gráficas y documentación de procesos. Explica también cómo contribuiste al equipo y qué aprendiste durante esta etapa.
    </td>
  </tr>
</table>

<h2 align="left">Conocimientos</h2>

<table>
  <tr>
    <th align="left" width="420">🎨 Diseño UX/UI</th>
  </tr>
  <tr>
    <td>
      ✅ Wireframes<br>
      ✅ Prototipado<br>
      ✅ Diseño responsivo<br>
      ✅ Atomic Design<br>
      ✅ Pixel Perfect<br>
      ✅ Generación de contenido con IA<br>
      ✅ Actualizaciones de software en diseño
    </td>
  </tr>
</table>
