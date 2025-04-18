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
| Regresión Lineal  | 2297.88        |
| Random Forest     | 1230.85        |
| XGBoost           | 1375.80        |

---

## 🛠️ Optimización de Modelos

Se utilizaron dos estrategias principales para mejorar el rendimiento:

- Ajuste de hiperparámetros (Grid Search) 
- Selección de mejores features

---

### 🔧 Resultados de Optimización (MAE)

| Estrategia                  | Random Forest | XGBoost    |
|----------------------------|----------------|------------|
| Baseline                   | 1230.85        | 1375.80    |
| Grid Search                | 1264.13        | **1181.38**|
| Selección de Features      | 1553.23        | 1654.71    |

---

## 🏁 Resultados Finales

- ✅ **XGBoost + GridSearch** fue el modelo más preciso con un MAE de **1181.38**.
- 🟡 **Random Forest** tuvo buen rendimiento pero fue superado tanto en precisión como en eficiencia.

---

## 🧾 Conclusiones

- 🔥 **XGBoost se posiciona como el mejor modelo**, combinando velocidad y precisión gracias a su capacidad de boosting secuencial y ajuste fino de hiperparámetros.
- ⚖️ **Random Forest**, aunque más interpretable y robusto, presentó un MAE ligeramente mayor y mayor tiempo de entrenamiento. Sin embargo, en la etapa de optimización no vio mejores resultados.
- 🚫 La **selección de features no mejoró el rendimiento**, evidenciando la importancia de mantener la riqueza del dataset completo. Ver en que casos es util hacer seleccion de mejores features.
- 🧪 **Grid Search fue clave** para mejorar el rendimiento de XGBoost, mostrando la importancia de la búsqueda sistemática de combinaciones.
  

---

**Autor:** Mayco Castellanos  
**Curso:** *Machine Learning Models*  
