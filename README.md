# Sweet-Lift-Taxi
La compañía Sweet Lift Taxi ha recopilado datos históricos sobre pedidos de taxis en los aeropuertos. El objetivo es predecir la cantidad de pedidos de taxis para la próxima hora, con el fin de atraer a más conductores durante las horas pico y mejorar la disponibilidad del servicio. 

# 🚖 Sweet Lift Taxi - Predicción de Pedidos

## 📌 Descripción del proyecto
La compañía **Sweet Lift Taxi** ha recopilado datos históricos sobre pedidos de taxis en los aeropuertos.  
El objetivo es **predecir la cantidad de pedidos de taxis para la próxima hora**, con el fin de atraer a más conductores durante las horas pico y mejorar la disponibilidad del servicio.

La métrica de evaluación es **RMSE (Root Mean Squared Error)**, y el valor en el conjunto de prueba no debe superar **48**.

---

## 📂 Dataset
- Archivo: `taxi.csv`  
- Columna objetivo: `num_orders` (número de pedidos de taxi)  
- Intervalo temporal: cada **10 minutos**, remuestreado a **1 hora** para el modelado.  

---

## ⚙️ Flujo de trabajo
1. **Carga y exploración de datos**
   - Lectura del dataset.
   - Conversión de la columna de fechas a índice temporal.
   - Remuestreo de los datos a intervalos de una hora.
   - Análisis exploratorio de series de tiempo.

2. **Preparación de datos**
   - Generación de características basadas en la fecha y en retardos (lags).
   - División del dataset en entrenamiento y prueba (10% de los datos iniciales para prueba).

3. **Entrenamiento de modelos**
   - **Regresión Lineal**
   - **Random Forest Regressor** (con ajuste de hiperparámetros usando GridSearchCV)
   - **LightGBM** (modelo de gradient boosting optimizado para velocidad y eficiencia)

4. **Evaluación**
   - Comparación de modelos utilizando **RMSE**.
   - Selección del mejor modelo en función de precisión y generalización.

5. **Conclusiones**
   - Se logró construir un modelo que cumple con la métrica requerida (**RMSE < 48 en el conjunto de prueba**).
   - LightGBM mostró mejor balance entre rendimiento y tiempo de entrenamiento, siendo el modelo recomendado para la predicción.

---

## 📊 Tecnologías utilizadas
- **Python 3**
- **Pandas** (manipulación y análisis de datos)
- **NumPy** (operaciones numéricas)
- **Matplotlib** (visualización)
- **Scikit-learn** (modelado y evaluación)
- **LightGBM** (modelos de boosting)

---

## 🚀 Clona este repositorio:
   ```bash
   git clone https://github.com/tuusuario/Sweet-Lift-Taxi.git
   cd Sweet-Lift-Taxi
