# 📊 Análisis de Ventas Multicanal LATAM | Python & Pandas

![Python](https://img.shields.io/badge/Python-3.x-blue?style=flat&logo=python)
![Pandas](https://img.shields.io/badge/Library-Pandas-150458?style=flat&logo=pandas)
![Seaborn](https://img.shields.io/badge/Library-Seaborn-388E3C?style=flat)
![Status](https://img.shields.io/badge/Estado-Completado-brightgreen)

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
