
🧠 Credit-card-frauds-ML
Proyecto integrador: Aprendizaje de Máquina Aplicado
📌 Descripción
Este proyecto aplica técnicas de análisis exploratorio y modelado predictivo para detectar transacciones fraudulentas en un dataset real de tarjetas de crédito. El objetivo es construir modelos robustos que manejen el alto desbalance de clases y optimicen métricas relevantes para la detección de fraude.

📁 Contenido del repositorio

notebook.ipynb: Notebook con carga de datos, limpieza, EDA, ingeniería de características y modelos.
reporte_fraude_credito.pdf: Reporte estilo artículo con resumen del trabajo.
poster_creditcard_fraud.pdf: Póster visual con metodología y resultados clave.
Resumen_Proyecto_Fraude.docx: Documento ejecutivo con conclusiones y recomendaciones.
data/: Dataset original (opcional).
requirements.txt: Dependencias del proyecto.


📊 Dataset
Fuente: https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud
Características:

Tamaño: 284,807 transacciones.
Variables:

Time: segundos desde la primera transacción.
Amount: monto de la transacción.
V1 a V28: componentes PCA para anonimización.
Class: variable objetivo (0 = legítima, 1 = fraude).


Desbalance extremo:

Clase 0: ~99.83%
Clase 1: ~0.17%




🔍 Metodología
Se siguió el proceso CRISP-DM:

Comprensión del negocio: impacto del fraude y objetivos.
Comprensión de datos: análisis exploratorio, correlaciones, distribución.
Preparación: limpieza, eliminación de duplicados, escalado, balanceo.
Modelado:

Baseline: Regresión Logística.
Modelos avanzados: RandomForest y XGBoost.


Evaluación: métricas ROC-AUC, Precision, Recall, F1-score.
Despliegue: recomendaciones y documentación.


✅ Resultados clave




















ModeloROC-AUC ValidaciónROC-AUC TestRandomForest0.850.85XGBoost0.9840.978
Variables más importantes: V17, V12, V14, V10, V11, V16.

📌 Conclusiones

El dataset está limpio pero altamente desbalanceado, lo que afecta métricas tradicionales como Accuracy.
XGBoost ofrece el mejor rendimiento y es recomendado para producción.
Las variables PCA son altamente discriminantes; Time y Amount aportan menos valor.


🔮 Recomendaciones

Aplicar técnicas de balanceo (SMOTE, undersampling).
Monitorear métricas como Precision, Recall y F1-score.
Implementar ingeniería de características temporales (rangos horarios).
Actualizar el modelo periódicamente para adaptarse a nuevos patrones de fraude.
