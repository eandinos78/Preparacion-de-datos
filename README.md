📊 Preparación y Preprocesamiento de Datos

El preprocesamiento de datos es una etapa fundamental en cualquier proyecto de análisis o ciencia de datos. Su objetivo es mejorar la calidad de los datos antes de aplicar técnicas estadísticas o modelos de aprendizaje automático.

🔹 Etapas del Preprocesamiento
El flujo general aplicado en este proyecto sigue la siguiente secuencia:

Cleaning → Formatting → Normalization → Encoding

1. Cleaning (Limpieza de datos)
Consiste en identificar y corregir problemas en los datos originales, tales como:

Eliminación de valores nulos o vacíos.

Eliminación de registros duplicados.

Corrección de errores o inconsistencias.

Eliminación de datos irrelevantes para el análisis.

2. Formatting (Formateo de datos)
Se enfoca en estandarizar la estructura y el tipo de los datos:

Conversión de tipos de datos (fechas, números, texto).

Estandarización de formatos (fechas, unidades de medida).

Separación o combinación de campos de texto cuando es necesario.

3. Normalization (Normalización de datos)
Proceso de escalamiento de variables numéricas para mantener proporciones adecuadas entre los valores:

Normalización en rango [0,1].

Estandarización con media 0 y desviación estándar 1.

Este paso es clave para algoritmos sensibles a la magnitud de los datos.

4. Encoding (Codificación de variables categóricas)
Transformación de variables categóricas en valores numéricos:

Codificación binaria (ejemplo: F → 0, M → 1).

One-Hot Encoding para variables con múltiples categorías.


🧹 Limpieza de Valores Faltantes

🔸 Identificación de valores faltantes
Los valores faltantes pueden presentarse como:

NaN

Campos en blanco

Valores nulos

🔸 Estrategias para tratar valores faltantes
Antes de tomar una decisión, se recomienda:

Verificar la fuente de recolección de datos.

Evaluar si es posible recuperar el valor faltante con el recolector de datos.

Las estrategias aplicables incluyen:

✔️ Eliminación de valores faltantes

Eliminar la variable: cuando el porcentaje de valores faltantes es muy alto.

Eliminar registros: cuando el número de filas afectadas es reducido.

✔️ Reemplazo de valores faltantes

Reemplazo por el promedio (para variables numéricas).

Reemplazo por la moda o valor más frecuente (para variables categóricas).

Reemplazo basado en criterios del dominio, apoyado en la experiencia del recolector o experto.

✔️ Conservación de valores faltantes

En algunos casos, los valores faltantes se conservan si aportan información relevante o si el modelo puede manejarlos directamente.


# Informacion general de los datos 

-Nombre de las columnas 

df.columnas

- Tamaño del conjunto de datos

df.shape

-Tipos de los datos de cada variable 

df.dtypes

-Estadística básica 

df. describe() #Solo numérico 

df.describe(include="all") #Incluye todos 


- Resumen técnico del df

df.info()


-Deterninar los valores faltantes

print(df.isnull().sum())


# Limpieza 

-Limpieza de valores faltantes

import numpy as np

df = df.replace("?", np.nan)


# Visualizacion de Datos 

- Jornada

conteo_jornada = df["Jornada_ Estudio"].value_counts()
conteo_jornada

for col in df.columns:
    if df[col].isnull().sum() > 0:
        print(f"\nColumna: {col}")
        print(df[col].value_counts())


