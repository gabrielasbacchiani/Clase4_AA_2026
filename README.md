# Clase 4 – Aprendizaje Automático: Aprendizaje Supervisado

Repositorio con las actividades de la Clase 4: regresión lineal y regresión logística.

## Contenido del repositorio

- `Clase4_AA_2026.ipynb` — Actividad 1: regresión lineal
- `Regresion_logistica.ipynb` — Actividad 2: regresión logística
- `academic_survival_longitudinal.csv` — dataset usado en la Actividad 1
- `usuarios_win_mac_lin.csv` — dataset usado en la Actividad 2

## Actividad 1: Regresión lineal

**Objetivo:** predecir el promedio del semestre (`Sem_GPA`) de un estudiante a partir de variables académicas y socioeconómicas.

**Dataset:** [Student Retention and Academic Performance Data](https://www.kaggle.com/datasets/razanihababdellatif/student-retention-and-academic-performance-data) (Kaggle). Contiene 79.239 registros longitudinales de 20.000 estudiantes (una fila por estudiante y semestre), con variables como asistencia, horas de trabajo, ingreso familiar, estrés financiero, materias desaprobadas, visitas de tutoría, entre otras.

**Proceso:**
1. Carga y primera exploración de los datos
2. Análisis exploratorio (AED): distribución de la variable objetivo, detección de valores atípicos y correlaciones con las posibles predictoras
3. Limpieza: corrección de valores de asistencia fuera de rango (0–100%) e imputación de valores faltantes con la mediana
4. Selección de variables predictoras según su correlación con el promedio
5. División en conjuntos de entrenamiento (80%) y prueba (20%)
6. Entrenamiento de un modelo de regresión lineal (`scikit-learn`)
7. Evaluación con error absoluto medio, error cuadrático medio, error absoluto mediano, varianza explicada y R²

**Resultado:** R² ≈ 0,36 y error absoluto medio ≈ 0,26 puntos de promedio (escala 0–4). El modelo captura una tendencia real pero moderada; el detalle de la interpretación está en la conclusión del notebook.

## Actividad 2: Regresión logística

**Objetivo:** predecir qué sistema operativo (Windows, Macintosh o Linux) usa un usuario que visita un sitio web, a partir de datos de comportamiento tomados de Google Analytics (duración de la visita, páginas vistas, cantidad de acciones y valor de las acciones).

**Dataset:** `usuarios_win_mac_lin.csv`, provisto por la cátedra.

**Proceso:** carga de datos, entrenamiento de un clasificador de regresión logística (`scikit-learn`) y evaluación de las predicciones.

## Cómo ejecutar los notebooks

Los notebooks están pensados para correr en [Google Colab](https://colab.research.google.com/):

1. Abrir el archivo `.ipynb` en Colab (subiéndolo o desde GitHub con *Open in Colab*).
2. Ejecutar las celdas en orden (*Entorno de ejecución → Ejecutar todas*).
3. El CSV de la Actividad 1 se lee directamente desde este repositorio, así que no hace falta subir ningún archivo a mano.

## Herramientas utilizadas

- Python
- pandas / numpy
- matplotlib
- scikit-learn

## Autora

Gabriela Bacchiani
