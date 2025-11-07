
##  Contenido
- **dataset.xlsx** → Base de datos de clientes con variables demográficas, de contrato y facturación. Exportado del Repositorio Analisis Preliminar TelecomX.
- **notebook.ipynb** → Código en Python (Google Colab) para:
  - Carga y exploración de datos
  - Preprocesamiento (codificación de variables categóricas, normalización)
  - Balanceo con SMOTE
  - Entrenamiento de modelos
  - Evaluación de métricas
  - Análisis de importancia de variables
- **informe.md** → Informe detallado con conclusiones y estrategias de retención.

---

##  Tecnologías utilizadas
- **Python 3**
- **Bibliotecas**:
  - `pandas`, `numpy` → Manipulación y análisis de datos
  - `matplotlib`, `seaborn` → Visualización
  - `scikit-learn` → Modelos de Machine Learning y métricas
  - `imblearn` → SMOTE para balanceo de clases

---

##  Flujo del proyecto
1. **Carga de datos** desde Excel (xls)
2. **Limpieza y preprocesamiento**:
   - Eliminación de filas sin la variable objetivo (`Churn`).
   - Codificación de variables categóricas con OneHotEncoder.
   - Estandarización de variables numéricas para modelos sensibles a escala.
3. **Balanceo de clases** con SMOTE para mejorar la detección de cancelaciones.
4. **Entrenamiento de modelos**:
   - **Regresión Logística** (con normalización)
   - **Random Forest** (sin normalización)
5. **Evaluación** con:
   - Exactitud (Accuracy)
   - Precisión
   - Recall
   - F1-score
   - Matriz de confusión
6. **Análisis de importancia de variables** y propuestas de estrategias de retención.

---

##  Principales hallazgos
- Variables más influyentes: `tenure`, `Contract_Month-to-month`, `InternetService_Fiber optic`, `PaymentMethod_Electronic check`, `Charges.Total`.
- **Regresión Logística** tuvo mejor recall, siendo útil para identificar clientes que podrían cancelar.
- **Random Forest** mostró mejor accuracy y precisión, pero con posible overfitting.

---

##  Estrategias de retención propuestas
1. Incentivar cambio de contratos mensuales a anuales.
2. Mejorar experiencia de clientes nuevos durante los primeros meses.
3. Revisar calidad y soporte del servicio de fibra óptica.
4. Fomentar métodos de pago automáticos.
5. Ofrecer paquetes con valor agregado para clientes con bajo gasto total.

---
