# Telecom-X-Alura-2
Desafío del curso ALURA programa ONE

# Proyecto: Predicción de Cancelación de Clientes en Telecomunicaciones

## Descripción  
Este proyecto analiza un conjunto de datos de clientes de una empresa de telecomunicaciones con el objetivo de predecir la cancelación de clientes (Churn).  

Se aplicaron técnicas de análisis exploratorio de datos (EDA), balanceo de clases, normalización y modelado predictivo usando diferentes algoritmos de Machine Learning.  

## Flujo de trabajo  

1. **Carga y exploración de datos**  
   - Identificación de variables relevantes.  
   - Limpieza de datos y tratamiento de valores nulos.  

2. **Análisis exploratorio (EDA)**  
   - Visualización de la relación entre variables como contrato, método de pago, antigüedad y tipo de servicio con la cancelación.  
   - Identificación de correlaciones más fuertes con churn.  

3. **Preparación de los datos**  
   - Creación de dos datasets:  
     - `df_lineal`: normalizado (para modelos sensibles a la escala).  
     - `df_arbol`: sin normalizar (para árboles de decisión y Random Forest).  
   - Balanceo de clases con SMOTE.  

4. **Modelado**  
   - **Modelo 1: Regresión Logística (df_lineal normalizado)**  
     - Accuracy: ~0.74  
     - Buen recall en clientes que cancelan, aunque menor precisión.  
   - **Modelo 2: Random Forest (df_arbol sin normalizar)**  
     - Accuracy: ~0.78  
     - Resultados más balanceados entre precisión y recall.  

5. **Evaluación de modelos**  
   - Se compararon métricas de Exactitud, Precisión, Recall, F1-score y Matriz de Confusión.  
   - Se identificó que Random Forest tuvo mejor desempeño general.  

## Principales hallazgos  

- Los factores más relevantes para la cancelación de clientes fueron:  
  - Tipo de contrato (mayor cancelación en contratos mensuales).  
  - Método de pago (Electronic Check asociado a mayor churn).  
  - Servicio de internet (Fiber Optic asociado a más cancelaciones).  
  - Antigüedad del cliente (clientes nuevos tienen mayor probabilidad de cancelar).  

## Estrategias de retención propuestas  

1. Incentivar contratos de mayor duración (ofrecer descuentos por contratos anuales o bianuales).  
2. Optimizar la experiencia de clientes con fibra óptica (mejor soporte técnico y estabilidad).  
3. Revisar políticas de pago electrónico (mayor seguridad, facilidad y transparencia en facturación).  
4. Programas de fidelización para clientes nuevos durante los primeros meses de contrato.  

## Archivos incluidos  

- `Telecom_X_2.ipynb` → Notebook con todo el análisis.  
- `datos-telecom-x.csv` → Datos originales sin manipulación.  
- `README.md` → Este documento.  

## Autores
Víctor Fabián Farías Sarango
Proyecto desarrollado como parte de análisis de Machine Learning aplicado a la retención de clientes.  
