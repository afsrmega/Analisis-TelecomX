
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
<img width="1318" height="1091" alt="Corelation" src="https://github.com/user-attachments/assets/0cd91858-d714-4f37-a114-da72da095893" />
<img width="541" height="402" alt="Boxplot Contrato" src="https://github.com/user-attachments/assets/90865894-da76-4742-a75c-74135ebbc001" />
<img width="560" height="402" alt="Gasto Cancelacion" src="https://github.com/user-attachments/assets/236a4615-abbb-4e90-a19f-ec675edbe247" />
<img width="583" height="402" alt="Dispersion" src="https://github.com/user-attachments/assets/ab854c12-5ad9-47a1-9b26-1fc7a621eb28" />


- Variables más influyentes: `tenure`, `Contract_Month-to-month`, `InternetService_Fiber optic`, `PaymentMethod_Electronic check`, `Charges.Total`.
- **Regresión Logística** tuvo mejor recall, siendo útil para identificar clientes que podrían cancelar.
  <img width="483" height="402" alt="Matriz Confusion" src="https://github.com/user-attachments/assets/d218af0b-c913-4206-ba94-c7d59351afca" />

- **Random Forest** mostró mejor accuracy y precisión, pero con posible overfitting.
<img width="472" height="402" alt="download" src="https://github.com/user-attachments/assets/2c12c793-3d91-4867-94a3-aa8284597bd1" />

---

##  Estrategias de retención propuestas
1. Incentivar cambio de contratos mensuales a anuales.
2. Mejorar experiencia de clientes nuevos durante los primeros meses.
3. Revisar calidad y soporte del servicio de fibra óptica.
4. Fomentar métodos de pago automáticos.
5. Ofrecer paquetes con valor agregado para clientes con bajo gasto total.

---
