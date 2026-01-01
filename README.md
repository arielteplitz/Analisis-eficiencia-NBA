# NBA Shooting Efficiency Analysis

## Objetivo del proyecto
Analizar la eficiencia de tiro en la NBA en función del **contexto del partido**, evaluando si existen diferencias significativas según:
- Tipo de tiro (2PT / 3PT)
- Contexto clutch vs no clutch
- Período del partido
- Tipo de temporada (Regular Season vs Playoffs)

El foco principal del análisis es entender **cómo cambia la eficiencia** cuando varía el contexto competitivo.

---

## Dataset
- Dataset estructurado de tiros en la NBA
- 850 observaciones y 24 variables
- No presenta valores nulos relevantes ni duplicados
- Las variables del 4° cuarto contienen nulos esperados por definición del dataset

El dataset se encuentra limpio y en condiciones para análisis estadístico y modelado.

---

## Metodología

### 1. Análisis Exploratorio de Datos (EDA)
- Revisión de estructura y calidad del dataset
- Análisis descriptivo de eficiencia de tiro por contexto
- Visualizaciones comparativas entre:
  - Regular Season vs Playoffs
  - Clutch vs resto del partido
  - Diferencias por período

### 2. Feature Engineering
- Selección de variables directamente relacionadas con la hipótesis
- Codificación de variables categóricas mediante **One-Hot Encoding**
- Escalado de variables numéricas cuando fue necesario

### 3. Modelado
Se aplicaron modelos supervisados con el objetivo de evaluar si los patrones observados en el EDA se sostienen de forma consistente:
- Regresión Logística
- Modelos de clasificación adicionales para comparación

La evaluación se realizó utilizando:
- Accuracy
- Matriz de confusión
- Análisis de errores

---

## Métrica clave
Se trabaja conceptualmente con la idea de **Δ Eficiencia**, definida como la diferencia de eficiencia de tiro entre dos contextos:

Δ Eficiencia = Eficiencia (Contexto A) − Eficiencia (Contexto B)

Ejemplo:
- T2% (Playoffs Clutch) − T2% (Regular Season No Clutch)

Esta métrica permite evaluar la hipótesis de forma directa e interpretable.

---

## Resultados
- Se observan diferencias claras de eficiencia según el contexto del partido
- El contexto competitivo influye en la probabilidad de conversión
- Los modelos confirman parcialmente los patrones detectados en el EDA
- Se priorizó interpretabilidad por sobre complejidad del modelo

---

## Limitaciones
- El dataset no incluye play-by-play detallado
- No se modelan secuencias de jugadas ni fatiga acumulada
- El análisis se limita a variables contextuales agregadas

---

## Posibles mejoras futuras
- Incorporar métricas avanzadas de eficiencia contextual
- Test de hipótesis formal sobre Δ Eficiencia
- Inclusión de términos de interacción bien justificados
- Uso de datos play-by-play para análisis más fino del contexto

---

## Herramientas utilizadas
- Python
- Pandas
- NumPy
- Matplotlib / Seaborn
- Scikit-learn
- Google Colab

---

## Autor
Proyecto desarrollado por **Ariel Teplitz** como parte de un trabajo académico en Ciencia de Datos de la UTN, con foco en análisis estadístico e interpretabilidad de resultados.
