# Challenge-Telecom-X
Este repositorio contiene el flujo de trabajo completo para el análisis de la tasa de cancelación (Churn) de la empresa Telecom X. El proyecto abarca desde la extracción de datos crudos en formato JSON hasta la generación de un informe estratégico basado en hallazgos estadísticos y visuales.

# Propósito del Proyecto
El objetivo principal es identificar los factores determinantes que impulsan la pérdida de clientes. Mediante el uso de Python, se busca proporcionar al equipo de Data Science un dataset depurado y una serie de insights accionables para reducir la tasa de evasión, la cual se sitúa inicialmente en un 26.5%.

# Estructura del Proyecto
El proyecto se organiza en las siguientes fases:
* ETL (Extracción, Transformación y Carga): Procesamiento de datos anidados y limpieza de inconsistencias.
* Estandarización: Traducción de variables y normalización de tipos de datos para análisis matemático.
* EDA (Análisis Exploratorio de Datos): Visualización de patrones de comportamiento mediante librerías estadísticas.
* Análisis de Correlación: Identificación de variables con mayor peso predictivo sobre la evasión.

# Tecnologías y Dependencias
Para ejecutar este proyecto, se requiere Python 3.x y las siguientes bibliotecas:
* pandas: Para la manipulación y análisis de estructuras de datos.
* numpy: Para operaciones numéricas y tratamiento de valores nulos.
* matplotlib: Para la creación de gráficos estáticos.
* seaborn: Para visualizaciones estadísticas avanzadas.
* json: Para la lectura de la fuente de datos original.

# Instalación y Uso
Para reproducir el análisis en un entorno local o en Google Colab, se deben seguir estos pasos:
* Clonar el repositorio o descargar los archivos TelecomX_Data.json y TelecomX_diccionario.md.
* Cargar los archivos en el entorno de ejecución.
* Ejecutar el script de limpieza para generar el archivo TelecomX_Estandarizado.csv.
* Abrir el notebook principal para visualizar los gráficos de distribución y correlación.

# Principales Hallazgos (Insights)
* Segmento Crítico: Los clientes con contratos "mes a mes" representan el mayor volumen de fuga (42.7%).
* Impacto Tecnológico: Los usuarios de fibra óptica muestran una mayor propensión a la cancelación en comparación con los de DSL.
* Factor de Retención: La contratación de servicios adicionales de seguridad y soporte técnico reduce drásticamente la probabilidad de churn.

# Posibles Problemas y Soluciones
* Valores Nulos: Se detectaron registros sin etiqueta de Churn. El sistema los elimina automáticamente para no sesgar el análisis.
* Formatos Numéricos: La columna Charges.Total se importa originalmente como texto; el código incluye una función de conversión forzada a float64 para evitar errores en el cálculo de promedios.
