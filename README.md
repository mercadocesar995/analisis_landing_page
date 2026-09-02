# analisis_landing_page

## Experimento A/B en Landing Page — Análisis de Conversión y Valor Económico
🎯 Objetivo del proyecto

Este proyecto analiza un experimento A/B realizado sobre una página de inicio (landing page), comparando las versiones A y B con el objetivo de identificar cuál presenta un mejor desempeño en términos de tasa de conversión y gasto promedio de los usuarios que convirtieron.

El análisis busca apoyar una decisión de negocio basada en datos y evaluar, además, si variables como la fuente de tráfico y el tipo de usuario presentan una asociación con la conversión.

## Datasets utilizados

### El proyecto utiliza el archivo:

**landing_experiment.csv**

El dataset contiene las siguientes variables:

- **user_id**: Identificador único del usuario.

- **date**: Fecha en la que el usuario fue expuesto a la página.

- **landing**: Versión de la página mostrada al usuario: A o B.

- **region**: Región geográfica del usuario.

- **dispositivo**: Tipo de dispositivo utilizado.

- **traffic_source**: Canal por el que llegó el usuario.

-**user_type**: Tipo de usuario: Nuevo o Recurrente.

- **converted**: Indica si el usuario realizó una conversión: 0 = no, 1 = sí.

- **gasto**: Monto gastado por el usuario; es 0 cuando no existe conversión.


## Herramientas utilizadas

- Python

- Pandas

- NumPy

- Matplotlib

- Seaborn

- SciPy

- Statsmodels

- Google Colab

- GitHub


## Etapas del análisis

El proyecto se desarrolló en las siguientes etapas:


**1. Exploración inicial y validacion de datos**

-Revisión de la estructura y dimensiones del dataset.

-Identificación de tipos de datos.

-Revisión de valores nulos.

-Verificación de usuarios únicos.

-Revisión del rango temporal del experimento.

-Validación de categorías de las variables.

-Revisión de valores negativos y consistencia de gasto.

No se encontraron valores nulos, categorías inesperadas ni valores negativos en gasto. Los valores 0 de gasto corresponden a usuarios que no realizaron una conversión.



**2. Limpieza y transformación**

Se realizaron ajustes en los tipos de datos para facilitar el análisis:

-Conversión de date a formato datetime.

-Conversión de las variables categóricas a tipo category.

-Conservación de converted como variable numérica binaria 0/1.

-Conservación de user_id como identificador.

-Conservación de gasto como variable numérica decimal.



**3. Comparación del gasto promedio — Landing A vs B**

-Se comparó el gasto promedio de los usuarios que realizaron una conversión entre ambas versiones de la landing page.

-Se aplicó una prueba t de Welch para determinar si la diferencia observada era estadísticamente significativa.



**4. Comparación de la tasa de conversión — Landing A vs B**

Se comparó la tasa de conversión entre las dos versiones mediante una prueba z de proporciones.



**5. Relación entre fuente de tráfico y conversión**

Se analizó si existe una asociación entre traffic_source y converted mediante una prueba Chi-cuadrado.



**6. Relación entre tipo de usuario y conversión**

Se analizó la relación entre user_type y converted mediante una prueba Chi-cuadrado.



**7. Visualización de resultados**

Se utilizaron gráficos para complementar los resultados estadísticos y analizar:

-Conversión por versión de landing.

-Relación entre fuente de tráfico y conversión.

-Relación entre tipo de usuario y conversión.

-Volumen de usuarios y conversiones.

-Tasas de conversión.

-Valor generado por fuente de tráfico.



## Principales hallazgos

1. La página B presenta mejores resultados observados

2. La fuente de tráfico presenta diferencias en conversión

3. El tipo de usuario no presenta diferencias relevantes


## Recomendaciones de negocio

1. Priorizar la página B en futuras pruebas

2. Optimizar las fuentes de tráfico según su desempeño

3. No diferenciar la estrategia únicamente por tipo de usuario


## Cómo ejecutar el proyecto


Google Colab: https://colab.research.google.com/drive/1xTa3bs8yPw9fV9skVf1BN8c_NPC_ZBNa?usp=sharing

Ingresa a Google Colab.

Selecciona Archivo → Abrir notebook → Subir.

Carga el archivo .ipynb.

Ejecuta las celdas en orden desde el inicio hasta el final.

