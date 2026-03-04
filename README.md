#📊 Telecom X: Análisis de Evasión de Clientes (Churn)

Este proyecto tiene como objetivo analizar el comportamiento de los clientes de la empresa Telecom X para identificar los factores que influyen en la cancelación de servicios (Churn). A través de un proceso de ETL (Extracción, Transformación y Carga), se procesaron datos de una API para generar visualizaciones estratégicas y recomendaciones de negocio.

##🎯 Propósito del Análisis

El análisis busca reducir la tasa de abandono de clientes mediante la identificación de perfiles de riesgo. Se centra en responder preguntas clave como:

¿Qué tipos de contrato presentan mayor inestabilidad?

¿Cómo influye la antigüedad del cliente en su lealtad?

¿Existe una relación entre el número de servicios contratados y la permanencia?

📂 Estructura del Proyecto
El proyecto está organizado en un único notebook de Google Colab, dividido visualmente en las siguientes secciones según la metodología de ingeniería de datos:

📌 Extracción: Conexión a la API y carga de datos JSON.

🛠️ Transformación: Normalización de datos anidados (aplanamiento de diccionarios), limpieza de inconsistencias y creación de la métrica cuentas_diarias.

📊 Carga y Análisis: Análisis descriptivo, visualización de variables categóricas y cálculo de matrices de correlación.

📄 Informe Final: Resumen ejecutivo con conclusiones y estrategias sugeridas.

📈 Insights y Gráficos Obtenidos
1. El Factor del Contrato
Se identificó que el tipo de contrato es el predictor más fuerte de fuga. Los clientes con contratos "Month-to-month" (mes a mes) tienen una probabilidad de cancelación significativamente superior a quienes tienen contratos anuales.

2. Análisis de Correlación
Tras normalizar las columnas del dataset (identificando variables como monthly y tenure), la matriz de correlación reveló que:

Antigüedad (Tenure): Tiene una correlación negativa con la evasión; a mayor tiempo en la empresa, menor es el riesgo de churn.

Servicios Adicionales: Cuantos más servicios (seguridad, soporte, etc.) tiene un cliente, más "anclado" está a la empresa.

🚀 Instrucciones de Ejecución
Para ejecutar este proyecto en tu entorno local o en la nube:

Entorno: Se recomienda utilizar Google Colab para una configuración inmediata.

Dependencias: Asegúrate de tener instaladas las librerías necesarias:

Python
pip install pandas requests seaborn matplotlib
Orden de ejecución:

Ejecuta primero la celda de Extracción para obtener los datos de la API.

Importante: El código incluye una etapa de pd.json_normalize para manejar las columnas anidadas como customer, phone y account que de otro modo causarían errores en el análisis.

Sigue el orden secuencial de las celdas para asegurar que las variables calculadas (como churn_binary) estén disponibles para los gráficos.

Desarrollado como parte del Challenge Data Science - LATAM.
Autor: Anahi L. Lagunas M.
