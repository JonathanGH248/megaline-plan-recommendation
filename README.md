# 📱 Megaline Plan Recommendation - Sprint 9

Este proyecto forma parte del Sprint 9 del curso de *Introducción al Machine Learning*. El objetivo es desarrollar un modelo que recomiende el plan más adecuado para cada cliente de Megaline (Smart o Ultra), basado en su comportamiento mensual.

## 📊 Objetivo

Clasificar si un cliente debe tener el plan **Ultra** (`1`) o **Smart** (`0`) con una **exactitud mínima de 0.75**.

## 📁 Dataset

Se utilizó el archivo `users_behavior.csv`, que contiene las siguientes variables mensuales por cliente:

- `calls`: número de llamadas realizadas
- `minutes`: duración total de llamadas en minutos
- `messages`: mensajes de texto enviados
- `mb_used`: tráfico de Internet usado en MB
- `is_ultra`: plan actual del cliente (1 = Ultra, 0 = Smart)

## ⚙️ Proceso

1. Carga y análisis exploratorio de datos
2. División del dataset en conjuntos de entrenamiento, validación y prueba
3. Entrenamiento y ajuste de tres modelos:
   - Árbol de Decisión
   - Bosque Aleatorio (Random Forest)
   - Regresión Logística
4. Comparación de hiperparámetros para mejorar la exactitud
5. Prueba de cordura con un modelo `DummyClassifier` para validar el desempeño real

## 🧠 Resultados

| Modelo              | Mejor configuración     | Exactitud |
|---------------------|--------------------------|-----------|
| Árbol de Decisión   | max_depth = 3            | 0.7854    |
| Bosque Aleatorio    | n_estimators = 40, max_depth = 8 | **0.8087** |
| Regresión Logística | -                        | 0.7092    |
| Dummy Classifier    | -                        | 0.6843    |

✅ El **modelo Random Forest** obtuvo la mayor exactitud, superando el umbral mínimo del 75%.

## 📌 Conclusión

El modelo de Random Forest cumple con los objetivos del negocio, proporcionando una solución confiable y precisa para recomendar planes móviles óptimos a los clientes. Este modelo puede integrarse en procesos automatizados de atención al cliente o marketing digital.

## 🧰 Herramientas utilizadas

- Python 3
- Pandas
- Scikit-learn
- Jupyter Notebook
