# 📊 Análisis de Ventas Multicanal LATAM | Python & Pandas

![Python](https://img.shields.io/badge/Python-3.x-blue?style=flat&logo=python)
![Pandas](https://img.shields.io/badge/Library-Pandas-150458?style=flat&logo=pandas)
![Seaborn](https://img.shields.io/badge/Library-Seaborn-388E3C?style=flat)
![Status](https://img.shields.io/badge/Estado-Completado-brightgreen)
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/TU_USUARIO/TU_REPOSITORIO/blob/main/TU_CUADERNO.ipynb)

## 🎯 Descripción del Proyecto
Este repositorio contiene un análisis práctico de datos enfocado en el comportamiento de ventas de una empresa multicanal con presencia en Latinoamérica (**Web, App, Tienda Física y WhatsApp**). 

El objetivo principal es transformar datos crudos en **KPIs financieros** e **insights accionables**, evaluando el rendimiento por país, canal, categoría de producto y nivel de rentabilidad.

---

## 🛠️ Tecnologías y Librerías Utilizadas
* **Lenguaje:** Python 3.x
* **Entorno:** Google Colab / Jupyter Notebook
* **Análisis de Datos:** `pandas`
* **Visualización de Datos:** `matplotlib`, `seaborn`

---

## 📌 Flujo de Trabajo (Pipeline Analítico)
1. **Carga y Exploración Inicial:** Lectura de datos, revisión de dimensiones (`shape`), tipos de datos (`info`) y evaluación de nulos.
2. **Limpieza y Preparación (Data Wrangling):**
   * Normalización de formatos de fecha y texto (`str.strip()`).
   * Imputación de valores faltantes mediante **mediana** para variables numéricas y etiquetas como `"No informado"` para variables categóricas.
   * Preservación del dataset original mediante la creación de un `df_limpio`.
3. **Automatización:** Uso de bucles `for` para el análisis descriptivo rápido de múltiples métricas clave.
4. **Cálculo de KPIs Globales:**
   * **Ingresos Totales:** $235.68M
   * **Costos Totales:** $153.46M
   * **Unidades Vendidas:** 331
   * **Satisfacción Promedio:** 7.43 / 10
5. **Visualización & Storytelling:**
   * Comparativa de ingresos por categoría de producto usando `seaborn.barplot()`.
   * Formateo avanzado de ejes financieros para mejor lectura de negocio.

---

## 📈 Hallazgos y Conclusiones Clave
* **Estructura de Datos Resiliente:** Se logró una limpieza del 100% de los datos faltantes sin perder registros esenciales.
* **Distribución de Ingresos:** Las categorías de producto muestran diferencias claras en volumen de ventas, lo que permite enfocar estrategias de inventario y campañas de marketing específicas.
* **Calidad de Servicio:** La tasa de satisfacción promedio se mantiene en niveles saludables (**7.43/10**), aunque existen áreas de oportunidad en los tiempos de entrega.

---

## 📁 Estructura del Repositorio
```text
├── datasets/
│   └── sprint07_proyecto_ventas_multicanal_latam.csv
├── notebooks/
│   └── proyecto_guiado_sprint7.ipynb
└── README.md

# 📊 Análisis Exploratorio de Datos (EDA) y Segmentación de Clientes - ConnectaTel

##  Objetivo del Proyecto
El objetivo principal de este proyecto es realizar un Análisis Exploratorio de Datos (EDA) sobre la base de usuarios y el consumo de servicios de **ConnectaTel**. A través de este análisis se busca entender el comportamiento de uso (llamadas y mensajes), identificar anomalías o datos sesgados, segmentar a los clientes según su nivel de consumo y edad, y generar **insights estratégicos** que impulsen decisiones comerciales como campañas de *upselling* y diseño de nuevos planes.

---

##  Datasets Utilizados
El análisis combina dos fuentes de datos principales:

1. **`users_latam.csv`**: Contiene la información demográfica y contractual de los clientes:
   * `user_id`: Identificador único del usuario.
   * `first_name`, `last_name`: Nombre y apellido.
   * `age`: Edad del usuario.
   * `city`: Ciudad de residencia.
   * `reg_date`: Fecha de registro en la compañía.
   * `plan`: Tipo de plan contratado (`Basico` o `Premium`).
   * `churn_date`: Fecha de cancelación del servicio (si aplica).

2. **`usage.csv`**: Registra la actividad y consumo histórico de los usuarios:
   * `user_id`: Identificador del usuario.
   * `type`: Tipo de servicio (`call` o `text`).
   * `duration`: Duración de las llamadas en minutos.
   * `length`: Longitud de los mensajes de texto en caracteres.

---

##  Etapas del Análisis
El proyecto se desarrolló en las siguientes etapas consecutivas:

1. **Limpieza y Preparación de Datos:**
   * Tratamiento de valores *sentinels* (ej. `-999` en edad reemplazado por la mediana).
   * Identificación y manejo de datos faltantes (`pd.NA` en ciudades y nulos estructurales en consumos).
   * Corrección de formatos de fecha y filtrado de registros fuera de rango.
2. **Agregación por Usuario (`Summary Statistics`):**
   * Creación de métricas consolidadas: `cant_mensajes`, `cant_llamadas` y `cant_minutos_llamada`.
   * Unificación de tablas (`users` + `usage_agg`) mediante un *LEFT JOIN*.
3. **Análisis Estadístico y Distribuciones:**
   * Cálculo de medidas de tendencia central y dispersión.
   * Visualización mediante histogramas comparativos por tipo de plan (`hue='plan'`).
4. **Identificación de Outliers:**
   * Detección visual con *Boxplots*.
   * Cálculo de límites mediante el método del **Rango Intercuartílico (IQR)** y evaluación de su impacto en el negocio.
5. **Segmentación de Clientes:**
   * Clasificación por nivel de uso: `Bajo uso`, `Uso medio` y `Alto uso`.
   * Clasificación demográfica por edad: `Joven`, `Adulto` y `Adulto Mayor`.
6. **Conclusiones e Insights Ejecutivos:**
   * Traducción de hallazgos estadísticos en recomendaciones accionables para los *stakeholders*.

---

## 🛠️ Cómo Ejecutar el Notebook

# Opción 1: Google Colab (Recomendado)
1. Haz clic en el botón de la parte superior del notebook **"Open in Colab"** o sube el archivo `.ipynb` directamente a [Google Colab](https://colab.research.google.com/).
2. Asegúrate de cargar los archivos de datos `users_latam.csv` y `usage.csv` en el panel lateral de archivos de Colab (`/content/`).
3. Ejecuta las celdas en orden secuencial (`Entorno de ejecución > Ejecutar todas`).

---
