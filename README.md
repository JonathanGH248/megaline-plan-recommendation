# 📱 Megaline Plan Recommendation - Sprint 9

Este proyecto forma parte del Sprint 9 del curso de Introducción al Machine Learning. Se desarrolla un modelo para ayudar a Megaline a recomendar el plan más adecuado (Smart o Ultra) para cada cliente, en función de su comportamiento mensual.

## 📊 Objetivo

Clasificar si un cliente debe tener el plan **Ultra** (`1`) o **Smart** (`0`) con una **exactitud mínima de 0.75**.

## 📁 Dataset

Se utilizó el archivo `users_behavior.csv`, que contiene:

- `calls`: número de llamadas
- `minutes`: minutos usados en llamadas
- `messages`: mensajes de texto enviados
- `mb_used`: tráfico de Internet en MB
- `is_ultra`: tipo de plan actual (1=Ultra, 0=Smart)

## ⚙️ Proceso

1. Carga y análisis exploratorio de datos.
2. División en entrenamiento, validación y prueba.
3. Evaluación de tres modelos:
   - Árbol de Decisión
   - Bosque Aleatorio
   - Regresión Logística
4. Comparación de hiperparámetros.
5. Prueba de cordura con modelo `Dummy`.

## 🧠 Resultados

| Modelo              | Mejor resultado | Exactitud |
|---------------------|------------------|-----------|
| Árbol de Decisión   | depth=3          | 0.7854    |
| Bosque Aleatorio    | estimators=40, depth=8 | **0.8087** |
| Regresión Logística | -                | 0.7092    |
| Dummy Classifier    | -                | 0.6843    |

✅ El **modelo Random Forest** es el ganador y supera ampliamente el umbral de 0.75.

## 📌 Conclusión

El modelo Random Forest cumple con los objetivos de exactitud del negocio. Puede ser integrado como sistema de recomendación para asignar el plan óptimo a los clientes de Megaline según su uso real de llamadas, mensajes y datos móviles.

## 🧰 Herramientas utilizadas

- Python
- Pandas
- Scikit-learn
- Jupyter Notebook
