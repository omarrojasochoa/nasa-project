# 🎮 CuyTECH: Diseño de Misiones y Desarrollo del Juego

---

## 🌱 1. Estructura de cada misión

1. **Briefing (30–45s)**  
   - Región, cultivo y objetivo.  
   - El cuy abre el **Satélite Apus** y muestra indicadores (Tanque de Agua, Sonrisa Verde, Lluvia Futurera, Sol Intenso).

2. **Plan & Acción (60–120s)**  
   - El jugador toma decisiones (Regar / Manta Andina / Sembrar / Ajustar sombra / Esperar).  
   - Se activan **eventos sorpresa** (llama, tucán, neblina).  
   - Mini-juego (Sembrar o cubrir con Manta Andina).

3. **Cierre**  
   - **Resultado** (victoria o derrota) + **score** + barra de sostenibilidad.  
   - **Trivia educativa** (siempre).  
   - **Medalla/Festival** (si gana).  
   - (Opcional) **Ranking Pachamama**.

> 💡 Los indicadores del Satélite Apus son el puente entre los datos NASA y las decisiones del jugador.

---

## 🔢 2. Componentes de una misión

### A. Variables base
- `region` → costa | sierra | selva  
- `cultivo` → maíz, arroz, papa, quinua, café, cacao  
- `agua` → 0–100 (Tanque de Agua)  
- `sonrisaVerde` → 0–100 (vigor de cultivo)  
- `temperatura` → °C (Sol Intenso / helada)  
- `lluviaProxima` → true / false  
- `duracion` → segundos totales del nivel  

---

### B. Acciones principales del jugador
| Acción | Efecto positivo | Riesgo o penalización |
|--------|-----------------|------------------------|
| **Regar** | +agua, +vigor si no hay lluvia próxima | -puntos si se riega antes de lluvia |
| **Manta Andina** | Protege del frío, mini-juego de cubrir surcos | -pérdida de vigor si no se usa |
| **Sembrar (Tetris)** | Mejora germinación | Menos vigor si fallas el alineado |
| **Ajustar sombra** | Evita estrés térmico en cafetales | Exceso → humedad = hongos |
| **Esperar** | Ahorra agua si se prevé lluvia | Riesgo si la lluvia no llega |

---

### C. Eventos sorpresa
- **Llama traviesa:** pisa surcos → −vigor si no se espanta.  
- **Tucán curioso:** roba semillas → mini-reto para recuperarlas.  
- **Neblina:** oculta valores numéricos por unos segundos → enseña límites de los datos.

---

### D. Condiciones de éxito / fracaso
- **Éxito:**  
  - `sonrisaVerde ≥ umbral` o meta cumplida (ej. “no regar antes de lluvia”).  
- **Fracaso:**  
  - `sonrisaVerde ≤ 0` o decisión crítica mal tomada (ej. regar + lluvia + helada sin manta).

---

### E. Scoring
| Acción | Puntaje |
|---------|----------|
| Decisión correcta | +50 |
| Mini-juego superado | +100 |
| Ahorro de agua | +30 |
| Error leve | −50 |
| Error crítico | −80 |
| Trivia correcta | +50 |

> 🧮 Ranking Pachamama = (Agua Ahorrada 40%) + (Vigor Final 40%) + (Eventos Evitados 20%)

---

## 🌍 3. Plantillas de misiones

### **Misiones de Costa**
**C-1 Riego Inteligente (maíz/arroz)**  
- Estado: `agua=25`, `lluviaProxima=true`, `temperatura=28`  
- Objetivo: No regar antes de la lluvia, mantener `sonrisaVerde ≥ 60`.  
- Penaliza regar con lluvia en camino.  

**C-2 Distribución pareja (arroz)**  
- Estado: `agua=40`, `lluviaProxima=false`  
- Mini-juego: **Sembrar Tetris** (llenar surcos parejos = +vigor).  
- Objetivo: `sonrisaVerde ≥ 70` en 90s.

---

### **Misiones de Sierra**
**S-1 Helada en camino (papa)**  
- Estado: `temperatura=-2`, `lluviaProxima=false`  
- Evento: *Timer Helada* a los 20s.  
- Mini-juego: **Manta Andina** (cubrir ≥2/3 surcos).  
- Objetivo: evitar que `sonrisaVerde < 50`.  

**S-2 Siembra oportuna (quinua)**  
- Estado: `lluviaProxima=true`, `agua=20`  
- Mini-juego: **Sembrar Tetris** → mejor germinación.  
- Objetivo: sembrar antes de la lluvia y lograr `sonrisaVerde ≥ 65`.

---

### **Misiones de Selva**
**J-1 Sombra del cafetal (café)**  
- Estado: `temperatura=32`, `humedad alta`, `lluviaProxima=false`  
- Acción: **Ajustar sombra**.  
- Objetivo: mantener `sonrisaVerde ≥ 70` sin generar hongos.

**J-2 Humedad controlada (cacao)**  
- Estado: `humedad alta`, `lluviaProxima=true`  
- Acción: evitar riego excesivo.  
- Evento: **Neblina** frecuente.  
- Objetivo: evitar hongos, mantener equilibrio hídrico.

---

## 📈 4. Progresión y dificultad

| Nivel | Características | Dificultad |
|-------|------------------|-------------|
| 1 | Tutorial: 1 acción correcta para ganar | 🟢 Fácil |
| 2 | Introduce un mini-juego | 🟢 Medio |
| 3 | Combina dos indicadores (lluvia + temperatura) | 🟡 Medio |
| 4+ | Añade eventos sorpresa + menos tiempo | 🔴 Avanzado |

---

## 🔬 5. Conexión con datos NASA

| Dato NASA | Interpretación en juego |
|------------|-------------------------|
| **Humedad del suelo** | “Tanque de Agua” – determina cuándo regar |
| **Precipitación** | “Lluvia Futurera” – anticipa lluvias |
| **Temperatura superficial** | “Sol Intenso” o “Helada” |
| **NDVI** | “Sonrisa Verde” – vigor de plantas |
| **Radiación solar** | “Energía del Inti” – afecta crecimiento |

**Ejemplo de misión (JSON):**
```json
{
  "id": "S-1",
  "region": "sierra",
  "cultivo": "papa",
  "duracion": 90,
  "estadoInicial": { "agua": 30, "sonrisaVerde": 45, "temperatura": -2, "lluviaProxima": false },
  "reglas": {
    "regar": { "siLluvia": -50, "sinLluvia": +50, "maxAgua": 70 },
    "manta": { "ventanaSeg": 8, "exito": +100, "fallo": -80 }
  },
  "eventos": { "llama": 0.25, "neblina": 0.2 },
  "objetivo": { "metrica": "sonrisaVerde", "umbral": 60 }
}
