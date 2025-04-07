# 🚗 Predicción del Precio de Vehículos Usados con Modelos de Machine Learning

## 📌 Descripción del Proyecto

Este proyecto tiene como finalidad desarrollar, comparar y optimizar modelos de regresión para predecir el precio de vehículos usados en el mercado del Reino Unido. A través del uso de técnicas de machine learning como **Random Forest** y **XGBoost**, se buscó minimizar el **Error Absoluto Medio (MAE)** como métrica de evaluación principal.

El proceso abarcó desde la limpieza y preprocesamiento de datos hasta la implementación de estrategias avanzadas de optimización, incluyendo búsqueda de hiperparámetros y selección de características.

---

## 🧠 Modelos Utilizados

- Regresión Lineal *(descartada por bajo rendimiento)*
- Random Forest Regressor
- XGBoost Regressor

---

## ⚙️ Metodología

### 🔍 Preprocesamiento de Datos

- Imputación de valores nulos por media agrupada (`make`)
- Eliminación de duplicados y outliers (`year = 2060`)
- Codificación categórica con **One-Hot Encoding**
- Normalización con **Min-Max Scaling**
- División del dataset: **70% entrenamiento / 30% prueba**

---

### 📊 Evaluación Inicial

| Modelo            | MAE (Baseline) |
|-------------------|----------------|
| Regresión Lineal  | 2962.55        |
| Random Forest     | 1440.67        |
| XGBoost           | 1496.08        |

---

## 🛠️ Optimización de Modelos

Se utilizaron tres estrategias principales para mejorar el rendimiento:

- Ajuste manual de hiperparámetros
- Grid Search
- Selección de mejores features

---

### 🔧 Resultados de Optimización (MAE)

| Estrategia                  | Random Forest | XGBoost    |
|----------------------------|----------------|------------|
| Baseline                   | 1440.67        | 1496.03    |
| Mejores Hiperparámetros    | 1410.67        | 1386.53    |
| Grid Search                | 1496.78        | **1358.74**|
| Selección de Features      | 1553.23        | 1562.91    |

---

## 🏁 Resultados Finales

- ✅ **XGBoost + GridSearch** fue el modelo más preciso con un MAE de **1358.74**.
- 🟡 **Random Forest** tuvo buen rendimiento pero fue superado tanto en precisión como en eficiencia.

---

## 🧾 Conclusiones

- 🔥 **XGBoost se posiciona como el mejor modelo**, combinando velocidad y precisión gracias a su capacidad de boosting secuencial y ajuste fino de hiperparámetros.
- ⚖️ **Random Forest**, aunque más interpretable y robusto, presentó un MAE ligeramente mayor y mayor tiempo de entrenamiento.
- 🚫 La **reducción de features no mejoró el rendimiento**, evidenciando la importancia de mantener la riqueza del dataset completo.
- 🧪 **Grid Search fue clave** para mejorar el rendimiento de XGBoost, mostrando la importancia de la búsqueda sistemática de combinaciones.

---

**Autor:** Mayco Castellanos  
**Curso:** *Machine Learning Models*  
