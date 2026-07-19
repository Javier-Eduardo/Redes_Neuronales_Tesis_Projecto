# Modelo de Predicción del Consumo de Combustible con Redes Neuronales

## Descripción
Este proyecto desarrolla un modelo de predicción del consumo de combustible basado en arquitecturas de redes neuronales recurrentes para la Estación de Servicio Divino Niño (comercializadora Petroecuador) ubicada en Latacunga, Ecuador. El objetivo es optimizar la gestión del inventario de gasolina Extra, Súper y Diésel, reemplazando las estimaciones empíricas por modelos predictivos impulsados por Inteligencia Artificial.

## Metodología y Datos
* **Conjunto de Datos:** Se analizaron 466.137 registros transaccionales históricos del período de febrero 2022 a noviembre 2025, consolidados en 1.368 observaciones diarias.
* **Enfoque Mixto:** La fase cuantitativa se complementó con una fase cualitativa mediante entrevistas técnicas al personal de la estación, permitiendo incorporar eventos exógenos y definir el horizonte operativo ideal de 7 días.

## Tecnologías Utilizadas
* **Lenguaje Principal:** Python 3.11
* **Procesamiento de Datos:** Pandas, NumPy
* **Aprendizaje Profundo:** TensorFlow / Keras
* **Estadística y Baseline:** Scikit-learn (GradientBoosting Regressor)
* **Visualización:** Matplotlib, Seaborn

## Resultados Principales
* Se evaluaron y compararon cuatro arquitecturas: LSTM univariante, BiLSTM, CNN-LSTM y LSTM Multivariante.
* La arquitectura **BiLSTM** resultó ser la ganadora, logrando el mayor coeficiente de determinación promedio ($R^2=0.1606$) y el menor error porcentual promedio ($sMAPE=22.69\%$).
* Para el Diésel, el modelo BiLSTM superó al modelo estadístico de referencia, reduciendo el MAE de 383,12 a 311,01 galones y elevando el $R^2$ de 0,179 a 0,434.
* Para la gasolina Extra, el error relativo del modelo (13,28%) se sitúa dentro del umbral de tolerancia operativa del negocio.

## Autor
**Eduardo Javier Oña Chiriboga** - Ingeniero en Sistemas de la Información
Pontificia Universidad Católica del Ecuador, Sede Ambato (PUCESA)