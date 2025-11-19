# Modelado-de-datos-temporales-con-redes-neuronales
Esta actividad permitío aplicar técnicas de análisis, visualización y recuperación de datos faltantes en series temporales, comprendiendo su impacto en la calidad del modelado y la interpretación de resultados.

# 📝 **Tarea semana 4 - Opción Low-Code: Imputación de valores faltantes y modelado de series temporales**

## 📌 **Descripción del dataset**

El conjunto de datos corresponde a mediciones de calidad del aire recogidas en una estación en Italia, con registros horarios entre marzo de 2004 y abril de 2005.
Las variables principales son:

| N° | Variable      | Descripción                                                               |
| -- | ------------- | ------------------------------------------------------------------------- |
| 2  | CO(GT)        | Concentración verdadera de CO (mg/m³, referencia)                         |
| 3  | PT08.S1(CO)   | Respuesta del sensor de óxido de estaño (target: CO)                      |
| 4  | NMHC(GT)      | Concentración verdadera de hidrocarburos no metánicos (μg/m³, referencia) |
| 5  | C6H6(GT)      | Concentración verdadera de benceno (μg/m³, referencia)                    |
| 6  | PT08.S2(NMHC) | Respuesta del sensor de titania (target: NMHC)                            |
| 7  | NOx(GT)       | Concentración verdadera de NOx (ppb, referencia)                          |
| 8  | PT08.S3(NOx)  | Respuesta del sensor de óxido de tungsteno (target: NOx)                  |
| 9  | NO2(GT)       | Concentración verdadera de NO2 (μg/m³, referencia)                        |
| 10 | PT08.S4(NO2)  | Respuesta del sensor de óxido de tungsteno (target: NO2)                  |
| 11 | PT08.S5(O3)   | Respuesta del sensor de óxido de indio (target: O3)                       |
| 12 | T             | Temperatura (°C)                                                          |
| 13 | RH            | Humedad relativa (%)                                                      |
| 14 | AH            | Humedad absoluta                                                          |


## 🎯 **Propósito de la tarea**

La tarea tiene dos objetivos principales:

### 1️⃣ **Imputación de valores faltantes**


* Simular valores faltantes en el dataset mediante dos enfoques:

  * **Aleatorio (at random)**: Se eliminan valores de forma dispersa.
  * **En bloques (in blocks)**: Se eliminan valores en secuencias consecutivas para simular fallos de sensores.
* Aplicar un método de imputación (por ejemplo, interpolación, modelo simple, técnica automática de la biblioteca proporcionada) para completar los datos.

### 2️⃣ **Modelado de serie temporal**


* Seleccionar una variable adecuada para modelar con un **LSTM** o un **Transformer**.
* La variable recomendada es:
  **CO(GT)** (Concentración de monóxido de carbono en mg/m³)
  👉 **Justificación:** CO(GT) es una variable con patrones estacionales y tendencias temporales claras, es de interés ambiental y presenta correlación con otras mediciones del dataset.
* Desarrollar un modelo básico (low-code) para predecir el valor futuro de CO(GT), usando las variables disponibles como entradas y evaluando el desempeño del modelo.


## ⚙️ **Instrucciones**

* Esta es una tarea **low-code**: Se proporcionarán plantillas de código o scripts básicos, enfócate en:

  * Comprender el proceso de imputación y modelado.
  * Ejecutar el flujo de trabajo.
  * Interpretar y discutir los resultados: calidad de la imputación y precisión del modelo de predicción.
* Analizar las métricas (MAE, MSE, RMSE, R²) para la imputación y la predicción.


## ✅ **Entregables**

* Un breve informe que incluya:

  * Gráficos de la serie original, con y sin imputación.
  * Métricas de evaluación de la imputación.
  * Gráficos y métricas del modelo LSTM o Transformer (por ejemplo: RMSE en test).
  * Reflexión sobre la calidad de la imputación y el modelo.
