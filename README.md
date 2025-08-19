# AluraStore
Alura Store

Análisis integral de desempeño de cuatro tiendas usando Python, pandas y matplotlib, con el objetivo de identificar qué tienda presenta el menor desempeño y recomendar cuál conviene vender según resultados de ingresos, mix de productos/categorías, calificaciones y costos de envío.

🎯 Objetivo del proyecto

Ayudar al Sr. Juan a decidir qué tienda vender con base en evidencia cuantitativa y visual. Para ello, se:

Calculan ingresos totales y volumen de ventas por tienda.

Identifican categorías y productos más y menos vendidos.

Estiman calificaciones promedio de clientes por tienda.

Analizan costos de envío (promedio, dispersión y distribución).

Construye un puntaje de desempeño (0–1) con pesos ajustables para priorizar criterios de negocio.

Se genera un informe final con hallazgos y recomendación.

📦 Datos

Se utilizaron 4 archivos CSV (datasets públicos de Alura):

tienda_1.csv

tienda_2.csv

tienda_3.csv

tienda_4.csv

En el notebook se leen vía pd.read_csv() desde las URLs públicas.

📊 Indicadores y visualizaciones clave

Ingresos totales por tienda (barras, extremos resaltados).

Calificación promedio por tienda (barras con línea de referencia).

Costo de envío: dispersión (scatter por tienda) y boxplot comparativo.

Ventas por categoría (barras).

Top de productos por tienda con barras coloreadas verde (más vendido) y rojo (menos vendido).

Evolución temporal (opcional) por Año-Mes si el dataset incluye fechas limpias.

Puntaje de desempeño (0–1) min–max con pesos configurables.

🧮 Metodología (resumen)

Carga y limpieza de datos (normalización de columnas, conversión de numéricos/fechas).

Cálculo de KPIs: ingresos, volumen, calificaciones, costos de envío.

Análisis por categorías y productos (conteos y rankings).

Visualizaciones para contrastar tiendas y detectar outliers.

Modelo de puntuación con pesos (por defecto):

Ingresos: 0.40 (más es mejor)

Calificación: 0.30 (más es mejor)

Costo de envío: 0.20 (menos es mejor)

Volumen: 0.10 (más es mejor)

Informe final con conclusiones y recomendación de la tienda a vender.

⚙️ Requisitos

Python 3.9+

pandas, numpy, matplotlib, ipython

Instalación rápida en entorno local:

pip install pandas numpy matplotlib ipython

▶️ Cómo ejecutar
Opción A: Google Colab (recomendada)

Abre el notebook store.ipynb en Colab.

Ejecuta las celdas en orden. El notebook descargará los CSV y generará tablas y gráficos.

Se crea automáticamente el archivo informe_tiendas.md con la síntesis final.

Opción B: Entorno local

Clona/descarga el proyecto.

Activa un entorno virtual (opcional) e instala requisitos.

Ejecuta el notebook con Jupyter o VS Code.

Asegúrate de tener acceso a internet para leer los CSV por URL.

📁 Estructura sugerida del proyecto
alura-store/
├─ store.ipynb                # Notebook principal (análisis y gráficos)
├─ informe_tiendas.md         # Informe final (se genera al correr el notebook)
├─ figures/                   # (opcional) Gráficos guardados si decides exportarlos
└─ README.md                  # Este archivo

🧩 Personalización de pesos

En el notebook hay una sección de CONFIG con el diccionario PESOS:

PESOS = {
    "ingresos": 0.40,
    "calificacion": 0.30,
    "costo_envio": 0.20,
    "volumen": 0.10
}


Ajusta los valores según tus prioridades (por ejemplo, subir calificacion si la experiencia del cliente es el foco).

📝 Salidas/Entregables

Tablas y gráficos de todos los KPIs por tienda.

Ranking de productos por tienda con extremos resaltados.

Informe final en Markdown: informe_tiendas.md con:

Introducción y metodología

Resultados por tienda (datos + gráficos)

Comparativa y puntaje de desempeño

Conclusión y recomendación de la tienda a vender

✅ Conclusión (resumen)

El proyecto Alura Store entrega una visión integral y visual del desempeño de cada tienda para sustentar la decisión de venta. La combinación de KPIs, gráficos y un puntaje ponderado permite argumentar de forma clara y objetiva qué tienda presenta menor desempeño y por qué.
