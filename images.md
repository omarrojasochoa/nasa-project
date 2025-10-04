# 🖼️ Checklist de Imágenes y Recursos Gráficos – CuyTECH

---

## 🎨 1. Pantallas principales (fondos estáticos)

| Elemento | Descripción | Tamaño sugerido | Prioridad |
|-----------|--------------|-----------------|------------|
| `bg_inicio.png` | Fondo del menú principal (paisaje estrellado, chacra peruana) | 1920x1080 | 🔥 Alta |
| `bg_select_region.png` | Mapa caricaturesco de Perú (Costa/Sierra/Selva) | 1920x1080 | 🔥 Alta |
| `bg_sierra.png` | Chacra con andenes y nevados | 1920x1080 | 🔥 Alta |
| `bg_costa.png` | Chacra de arroz/maíz con cielo claro | 1920x1080 | 🟡 Media |
| `bg_selva.png` | Cafetales y vegetación densa | 1920x1080 | 🟡 Media |
| `bg_resultado.png` | Fondo neutral para mostrar score y trivia | 1920x1080 | 🟢 Baja |
| `bg_festival.png` | Fondo festivo con banderines, luces, confetti | 1920x1080 | 🔥 Alta |
| `bg_ranking.png` | Fondo simple con podio o marcador Pachamama | 1920x1080 | 🟢 Baja |

---

## 🐹 2. Personaje principal – El Cuy Astronauta

| Archivo | Descripción | Tamaño sugerido | Formato | Prioridad |
|----------|--------------|-----------------|----------|------------|
| `cuy_idle.png` | Cuy quieto, sonriendo | 256x256 | PNG | 🔥 Alta |
| `cuy_run.png` | Animación de caminar/correr (3–5 frames) | 256x256 cada frame | SpriteSheet | 🔥 Alta |
| `cuy_talk.png` | Boca abierta para hablar en diálogos | 256x256 | PNG | 🔥 Alta |
| `cuy_happy.png` | Pose de victoria (brazos arriba o saltando) | 256x256 | PNG | 🔥 Alta |
| `cuy_sad.png` | Cuy cansado/triste (para derrota) | 256x256 | PNG | 🔥 Alta |
| `cuy_dance.png` | Animación corta bailando (para festivales) | 256x256 | SpriteSheet | 🟡 Media |

---

## 📱 3. Satélite Apus (HUD principal)

| Elemento | Descripción | Tamaño sugerido | Notas |
|-----------|--------------|-----------------|-------|
| `hud_apus_frame.png` | Marco general del Apus (tablet decorada con motivos andinos) | 700x400 | Puede incluir espacio para texto/íconos |
| `icon_tanque_agua.png` | Gota sonriente (nivel de humedad) | 64x64 | — |
| `icon_sonrisa_verde.png` | Hoja feliz (NDVI) | 64x64 | — |
| `icon_sol_intenso.png` | Sol rojo expresivo (temperatura alta) | 64x64 | — |
| `icon_lluvia_futurera.png` | Nube simpática con gotas | 64x64 | — |
| `icon_energia_inti.png` | Sol dorado brillante (radiación) | 64x64 | opcional |
| `bar_vigor.png` | Barra horizontal de Sonrisa Verde | 400x20 | — |

---

## 🌾 4. Cultivos y campo

| Elemento | Descripción | Tamaño sugerido | Notas |
|-----------|--------------|-----------------|-------|
| `plantas_papa.png` | Papas en 3 estados: saludable / media / dañada | 128x128 cada frame | 🔥 Alta |
| `plantas_maiz.png` | Para misiones de costa | 128x128 | 🟡 Media |
| `plantas_cafe.png` | Para misiones de selva | 128x128 | 🟡 Media |
| `suelo_tile.png` | Textura base del terreno | 256x256 | Tile repetible |
| `surco_area.png` | Zona interactiva (para cubrir con manta o sembrar) | 256x128 | invisible hitbox |

---

## 🧣 5. Mini-juego “Manta Andina”

| Elemento | Descripción | Tamaño sugerido | Formato |
|-----------|--------------|-----------------|----------|
| `manta_andina.png` | Manta colorida con patrón textil | 512x128 | PNG |
| `manta_shadow.png` | Sombra proyectada (para efecto 2D) | 512x128 | PNG |
| `fx_calor.png` | Pequeño brillo cálido al cubrir plantas | 128x128 | PNG |
| `timer_bar.png` | Barra de cuenta regresiva (opcional) | 300x20 | PNG |

---

## 🌧️ 6. Efectos sorpresa

| Elemento | Descripción | Tamaño sugerido | Formato |
|-----------|--------------|-----------------|----------|
| `llama.png` | Llama caricaturesca con animación | 256x256 (3 frames) | SpriteSheet |
| `tucan.png` | Tucán colorido volando | 256x256 (2–3 frames) | SpriteSheet |
| `neblina.png` | Capa blanca translúcida (overlay 60–80% opacity) | 1920x1080 | PNG |
| `confetti.png` | Confetti animado para festivales | 1920x1080 | PNG o animación en Construct |

---

## 🧩 7. Interfaz de usuario (UI)

| Elemento | Descripción | Tamaño sugerido |
|-----------|--------------|-----------------|
| `btn_jugar.png` | Botón principal del menú | 300x100 |
| `btn_regar.png` | Botón de riego | 200x80 |
| `btn_manta.png` | Botón para manta | 200x80 |
| `btn_esperar.png` | Botón para esperar | 200x80 |
| `btn_ok.png` | Confirmar (trivia, resultado) | 150x60 |
| `btn_reintentar.png` | Volver a intentar misión | 150x60 |
| `panel_trivia.png` | Pizarra o cartel para preguntas | 700x400 |
| `icon_correcto.png` | Check verde | 64x64 |
| `icon_incorrecto.png` | X roja | 64x64 |
| `panel_score.png` | Caja donde aparece puntaje | 600x200 |

---

## 🎉 8. Festivales / Medallas

| Elemento | Descripción | Tamaño sugerido | Notas |
|-----------|--------------|-----------------|-------|
| `medalla_papa.png` | Medalla dorada con papas y hojas | 256x256 | Sierra |
| `medalla_agua.png` | Medalla azul con gotas | 256x256 | Costa |
| `medalla_cafe.png` | Medalla marrón con grano de café | 256x256 | Selva |
| `banderines.png` | Guirnaldas coloridas de fondo | 1920x200 | parte superior |
| `fireworks.png` | Efecto pirotecnia simple | 1920x1080 | PNG o animación |

---

## 🏆 9. Ranking Pachamama

| Elemento | Descripción | Tamaño sugerido | Notas |
|-----------|--------------|-----------------|-------|
| `panel_ranking.png` | Fondo tipo piedra o pergamino | 800x600 | — |
| `icon_novato.png` | Rama verde | 128x128 | Nivel 1 |
| `icon_guardian.png` | Sol y montaña | 128x128 | Nivel 2 |
| `icon_heroe.png` | Tierra con halo dorado | 128x128 | Nivel 3 |
| `podio.png` | Base de 3 niveles | 600x300 | — |

---

## 🔊 10. Efectos de sonido y música

| Recurso | Tipo | Descripción |
|----------|------|-------------|
| `sfx_click.wav` | Efecto | Botones y selección |
| `sfx_regar.wav` | Efecto | Sonido de riego |
| `sfx_manta.wav` | Efecto | Sonido de cubrir con manta |
| `sfx_ok.wav` | Efecto | Trivia correcta |
| `sfx_fail.wav` | Efecto | Trivia incorrecta |
| `sfx_festival.wav` | Efecto | Música alegre (charango, cajón, quena) |
| `music_bg.mp3` | BGM | Fondo del juego (melodía andina ligera) |

---

## 🧠 11. Opcional (para futuras expansiones)

| Elemento | Descripción | Tamaño sugerido |
|-----------|--------------|-----------------|
| `bg_amazonas.png` | Escenario adicional para expansión | 1920x1080 |
| `npc_agricultor.png` | Personaje secundario o tutorial | 256x256 |
| `hud_notificacion.png` | Ventana tipo mensaje del cuy | 600x200 |
| `icon_biodiversidad.png` | Mariposa o flor para nuevos indicadores | 64x64 |

---
