# 📊 Análisis de Evasión de Clientes (Churn) - TelecomX LATAM

Este proyecto realiza un análisis integral de ciencia de datos para identificar los factores que impulsan la pérdida de clientes (**Churn**) en la empresa **TelecomX**. A través de un proceso de Extracción, Transformación y Carga (ETL), seguido de un Análisis Exploratorio de Datos (EDA) y la implementación de un modelo de **Machine Learning**, buscamos proporcionar estrategias accionables para mejorar la retención de usuarios.

## 📁 Estructura del Proyecto

*   `TelecomX_LATAM.ipynb`: Notebook principal con todo el flujo de trabajo (Limpieza, Análisis, Modelado).
*   `TelecomX_Data.json`: Dataset original con información detallada de los clientes.
*   `TelecomX_diccionario.md`: Diccionario de datos que describe cada variable del esquema.
*   `README.md`: Documentación técnica del proyecto.

## 🛠️ Tecnologías Utilizadas

El análisis fue desarrollado en un entorno Jupyter Notebook utilizando las siguientes librerías de Python:

- **Procesamiento de Datos:** `Pandas`, `Numpy`, `JSON`.
- **Visualización:** `Matplotlib`, `Seaborn`.
- **Machine Learning:** `Scikit-Learn` (Random Forest, StandardScaler, train_test_split).

## 🚀 Fases del Proyecto

### 1. Extracción y Normalización
Se transformaron los datos crudos en formato JSON a una estructura tabular. Se realizaron verificaciones iniciales de tipos de datos y estructuras anidadas.

### 2. Transformación y Limpieza (Data Cleaning)
*   **Corrección de Nulos:** Se identificaron valores vacíos en la columna `Cargo_Total` para clientes con 0 meses de antigüedad, corrigiéndolos a valor numérico 0.
*   **Estandarización:** Traducción de columnas y categorías al español (ej: "Fiber optic" -> "Fibra óptica").
*   **Binarización:** Conversión de variables categóricas de tipo Si/No a formato numérico 1/0 para compatibilidad con algoritmos.
*   **Feature Engineering:** 
    *   `Cuentas_Diarias`: Cálculo del costo diario estimado.
    *   `Total_Servicios`: Cuantificación del ecosistema de servicios de cada cliente.

### 3. Análisis Exploratorio (EDA)
Se utilizaron gráficos avanzados como:
*   **Heatmaps de Correlación:** Para ver qué variables influyen más en el abandono.
*   **Gráficos de Violín y Punto:** Para analizar la densidad de gastos y la probabilidad de churn según el volumen de servicios.
*   **Boxplots:** Para comparar la permanencia entre clientes que se quedan y los que se van.

### 4. Modelado Predictivo
Se implementó un modelo de clasificación basado en **Random Forest** para predecir el riesgo de abandono. El modelo analiza patrones históricos y genera una métrica de **Importancia de Características (Feature Importance)**, revelando los principales detonantes del Churn.

## 💡 Principales Hallazgos (Insights)

1.  **Tipo de Contrato:** Los clientes con contrato de **Mes a Mes** tienen una tasa de abandono significativamente mayor que aquellos con compromisos anuales.
2.  **Efecto Ancla:** Existe una correlación inversa entre la cantidad de servicios contratados y el abandono; los clientes "multi-servicio" son más leales.
3.  **Ventana Crítica:** Los primeros **6 meses** de vida del cliente son los más riesgosos; si superan este periodo, la lealtad aumenta drásticamente.
4.  **Soporte Técnico:** La presencia de soporte técnico y seguridad en línea actúa como un fuerte retenedor de usuarios.

## 📋 Conclusiones y Recomendaciones

*   **Migración de Planes:** Incentivar activamente el paso de contratos mensuales a anuales.
*   **Onboarding Proactivo:** Reforzar la atención al cliente durante el primer trimestre de servicio.
*   **Estrategia Multi-producto:** Ofrecer servicios de valor añadido (seguridad, respaldo) para aumentar el costo de cambio del usuario.

---
**Autor:** [Yerson Elias Incahuaman Juro]  
**Fecha:** Diciembre 2025
