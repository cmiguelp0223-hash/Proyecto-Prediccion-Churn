# Proyecto: Predicción de Fuga de Clientes para TeleConnect

Un modelo de machine learning para identificar proactivamente a los clientes con alta probabilidad de cancelar su servicio, permitiendo a la empresa aplicar estrategias de retención efectivas.

---

## 🎯 Objetivo de Negocio

El objetivo de este proyecto es reducir la pérdida de ingresos causada por la fuga de clientes. Al predecir qué clientes están en riesgo, la empresa "TeleConnect" puede ofrecerles incentivos personalizados para mejorar su satisfacción y permanencia.

---

## 🛠️ Proceso y Herramientas

El proyecto siguió un ciclo de vida de ciencia de datos estructurado:

1.  **Análisis Exploratorio de Datos (EDA) con SQL:**
    * Se utilizó una base de datos **SQLite** para simular un entorno de producción.
    * El análisis reveló un hallazgo clave: los clientes con **Fibra Óptica** y contratos de **Mes a Mes** tenían una tasa de fuga superior al 57%.

2.  **Preparación de Datos y Modelado:**
    * Se usó **Python** y librerías como **Pandas** y **Scikit-learn**.
    * Se transformaron las variables categóricas con la técnica de **One-Hot Encoding**.
    * Se entrenó un modelo **Random Forest Classifier** por su alto rendimiento y capacidad para manejar relaciones complejas en los datos.

3.  **Evaluación y Optimización:**
    * El modelo inicial alcanzó un `recall` del 50% para los clientes en riesgo.
    * Se **ajustó el umbral de predicción** a 0.30 para aumentar la sensibilidad del modelo, priorizando la reducción de Falsos Negativos, que son el error más costoso para el negocio.

---

## 📊 Resultados

El modelo final optimizado alcanzó un **recall del 72%** en el conjunto de prueba.

* **Esto significa que el modelo es capaz de identificar correctamente al 72% de todos los clientes que estaban en riesgo real de abandonar la empresa.**

| Métrica   | Valor |
| :-------- | :---- |
| Precisión | 0.55  |
| **Recall** | **0.72** |
| F1-Score  | 0.62  |

---

## 🚀 Puesta en Práctica

Este modelo está listo para ser desplegado como una **API en tiempo real**. Podría integrarse con el sistema de CRM de la empresa para que, cuando un cliente en riesgo contacte al soporte técnico, el agente reciba una alerta en su pantalla y pueda ofrecerle una solución o descuento proactivo.

---

## 📁 Cómo Usar este Repositorio

1.  Abre y ejecuta el notebook `notebooks/1_Analisis_Exploratorio_con_SQL.ipynb` para ver el análisis inicial y la creación de la base de datos.
2.  Abre y ejecuta el notebook `notebooks/2_Entrenamiento_y_Evaluacion_Modelo.ipynb` para replicar el proceso de entrenamiento, evaluación y optimización del modelo.
