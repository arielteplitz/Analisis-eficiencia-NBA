# 📘 Proyecto NBA — Análisis y Simulación de Eficiencia de Tiro
Proyecto personal de análisis NBA. Trabajo con datos reales y simulados por cuarto para estudiar eficiencia de tiro, comparaciones entre etapas y futuras simulaciones de rendimiento con Python.

## 1. 🎯 Objetivo
Analizar y predecir si el **tiro de media distancia** mantiene o mejora su eficiencia respecto a los **triples y bandejas** durante los **últimos cuartos** de partidos de NBA, especialmente en **playoffs**.  
El propósito es comprobar si esta hipótesis tiene sustento estadístico o no.

---

## 2. 📊 Fuentes de datos
- Estadísticas oficiales de la NBA → [nba.com/stats](https://www.nba.com/stats)  
- Kaggle Datasets:  
  - *NBA Player Stats (2022–2024)*  
  - *NBA Play-by-Play Data (regular & playoffs)*  
- Datos complementarios simulados de forma proporcional (por cuarto y tipo de tiro) basados en tendencias reales.  
- API: *nba_api.stats.endpoints* (para ampliar datos futuros).  

> 🔹 En esta versión inicial se usaron datos reales agregados + simulación detallada para segmentar por cuarto.

---

## 3. 🧩 Estructura del dataset
- **850 filas** (jugadores y partidos combinados)  
- **Columnas principales:**
  - Jugador  
  - Equipo  
  - Temporada  
  - Etapa (Regular / Playoffs)  
  - Tiros_triples_tomados / metidos (por cuarto)  
  - Tiros_media_tomados / metidos (por cuarto)  
  - Bandejas_tomadas / metidas (por cuarto)  
  - Minutos_por_partido  
  - Promedio_puntos  
  - %Eficiencia_Total  

> Se mantienen los mismos jugadores a lo largo de los cuartos para reflejar consistencia de rendimiento.

---

## 4. ⚙️ Preparación de datos
1. **Limpieza inicial:** eliminación de filas vacías o duplicadas.  
2. **Estandarización:** normalización de porcentajes y nombres de equipos/jugadores.  
3. **Creación de columnas derivadas:**  
   - % de acierto por tipo de tiro  
   - eficiencia ponderada por minutos  
   - segmentación por etapa (regular vs playoffs)  
4. **Validación:** comparación de promedios con estadísticas oficiales para asegurar coherencia.  

---

## 5. 🔍 Análisis planeado
- **Exploratorio:** distribución de aciertos por tipo de tiro y etapa.  
- **Comparativo:** diferencia de medias y dispersión entre regular y playoffs.  
- **Predictivo (futuro):** regresión logística en toma de decisiones y su efectividad para ver qué variables predicen la victoria o la ventaja en el 4º cuarto.  

---

## 6. ⚠️ Limitaciones
- Parte de los datos son simulaciones basadas en tendencias, no play-by-play reales.  
- No se incluye aún la variable “situación del partido” (diferencia de puntos).  
- Dataset reducido (850 filas).  

---

## 7. 💡 Próximos pasos
1. Ampliar con datos reales por posesión (NBA API).  
2. Incorporar contexto de juego (ventaja/desventaja, rival, fatiga).  
3. Visualizar eficiencia en los últimos 3 minutos de partidos cerrados.  
4. Entrenar un modelo predictivo y validar su precisión.  

---

## 📂 Archivos del repositorio
- `base_nba.xlsx` → Dataset principal.  
- `base_nba.csv` → Versión en formato CSV.  
- `notebook_nba.ipynb` → Análisis y visualizaciones en Python.  
- `README.md` → Descripción y documentación del proyecto.  

---


