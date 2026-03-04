#📊 Análisis de Evasión de Clientes (Churn) - Telecom X
Este proyecto realiza un análisis integral de los datos de Telecom X para identificar patrones que influyen en la pérdida de clientes (Churn). Utiliza técnicas de ingeniería de datos para procesar información desde una API y análisis estadístico para generar recomendaciones estratégicas.

#🚀 Estructura del Proyecto
El proyecto está desarrollado en un notebook de Google Colab y se divide en cuatro fases principales siguiendo el modelo ETL:

Extracción: Conexión con la API de Telecom X y carga de datos crudos.

Transformación: Normalización de JSON anidado, limpieza de datos y creación de nuevas métricas.

Carga y Análisis: Visualización de datos, matrices de correlación y detección de patrones de fuga.

Informe Final: Resumen de hallazgos y sugerencias de negocio.

#🛠️ Tecnologías Utilizadas
Python 3.x

Pandas: Manipulación y normalización de datos.

Requests: Consumo de la API JSON.

Matplotlib & Seaborn: Visualización de datos y mapas de calor (Heatmaps).

Google Colab: Entorno de desarrollo.

#📋 Requisitos e Instalación
Para ejecutar este proyecto localmente o en Colab, asegúrate de tener instaladas las siguientes librerías:

Bash
pip install pandas requests matplotlib seaborn
⚙️ Pasos Clave del Desarrollo
1. Normalización de Datos
El dataset original presentaba estructuras anidadas (diccionarios dentro de columnas). Se utilizó pd.json_normalize para aplanar los datos y permitir el acceso a variables críticas como el tipo de contrato (contract) y los cargos mensuales (monthly).

2. Ingeniería de Variables
Se creó la columna cuentas_diarias dividiendo el cargo mensual entre 30, lo que permite analizar el impacto del costo diario en la decisión de abandono del cliente.

3. Análisis de Correlación
Se implementó una matriz de correlación para identificar qué factores tienen mayor relación con la evasión. Se descubrió una correlación negativa significativa entre la antigüedad (tenure) y el churn.

#📈 Hallazgos Principales
El factor contrato: Los clientes con contratos mensuales ("Month-to-month") representan el segmento con mayor tasa de fuga.

Fidelización por servicios: Existe una relación inversa entre la cantidad de servicios adicionales contratados (seguridad, soporte, etc.) y la probabilidad de churn.

Sensibilidad al precio: Los clientes con cargos diarios más altos tienden a abandonar el servicio con mayor frecuencia si no tienen un contrato de largo plazo.

#💡 Recomendaciones Propuestas
Migración Contractual: Incentivar el paso de contratos mensuales a anuales mediante descuentos estratégicos.

Estrategia Multi-producto: Fomentar la adopción de servicios adicionales para aumentar el "costo de salida" del cliente.

Monitoreo Temprano: Implementar alertas de retención para clientes con baja antigüedad (menor a 6 meses).

Autor:  Anahi Leticia Lagunas Mercado 
Proyecto: Challenge Data Science - LATAM / Telecom X
