# Ordenamiento_Multivariado

# Modelación estadística y ordenamiento de cultivares según rendimiento y calidad

Este repositorio contiene los scripts desarrollados para el procesamiento de datos fenotípicos y de calidad de trigo pan, en el marco de la Tesis Doctoral.

## 📁 Estructura del Script

### 1. Preprocesamiento y Limpieza (PASO 1-3)
* Limpieza: Filtrado inicial de datos inconsistentes (<= 0) transformándolos en missing values.
* Screening: Uso de PROC UNIVARIATE para detectar outliers y evaluar normalidad.
* Transformación: Aplicación de logaritmos (log_ESTAB) para estabilizar varianzas.

### 2. Modelos Mixtos y LS-Means (PASO 4-5)
* Macro %validar_supuestos: Automatización de PROC MIXED para obtención de medias ajustadas.
* Estimación de LS-Means por Cultivar considerando efectos fijos y aleatorios.
* Modelado de interacción Genotipo x Ambiente (Año, Loc y sus cruces).

### 3. Construcción del Índice de Mérito (PASO 6)
* Normalización (0-1): Reescalado de variables para comparabilidad multivariada.
* Cenizas: Normalización inversa (menor valor = mayor puntuación).
* Indice_Merito: Ponderación final balanceada (50% Rendimiento / 50% Calidad).

### 4. Visualización y Selección Élite (PASO 7-8)
* Matriz de Selección: Gráfico SGPLOT para identificar el "Top 20" frente a la población.
* Análisis de Correlaciones: Evaluación de Pearson sobre el grupo élite para validar antagonismos.

---

## 🛠️ Requisitos
* Software: SAS (9.4 o SAS OnDemand for Academics).
* Datos de entrada: El script requiere un dataset en WORK.IMPORT con variables de rinde y calidad.

## 📝 Referencia de la Tesis
* **Autor:** Mójica, Claudia Julieta.
* **Título:** Desarrollo e implementación de protocolos para el análisis del rendimiento y calidad en redes de evaluación de cultivares de trigo.
* **Capítulo Relacionado:** Capítulo 6: Modelación estadística y ordenamiento de cultivares según rendimiento y calidad.
* **Grado:** Tesis para optar al título de Doctora en Ciencias Agropecuarias.
* **Estado:** En preparación / Finalización de manuscrito (2026).
