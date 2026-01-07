# Preparacion de datos
Preprocesamiento de datos (limpieza de datos, manipulación de datos)
- Valor faltante
- Formato de datos 
- Normalización de datos 
- Clasificación de datos
- Variables categóricas 

- **Cleaning → Formatting → Normalization → Encoding**


- Cleaning (Limpieza):	Eliminación de valores nulos, duplicados, errores o datos irrelevantes.
- Formatting (Formateo):	Ajuste del tipo de dato, estructura o formato (por ejemplo, convertir fechas, separar texto, estandarizar unidades).
- Normalization(Normalización):	Escalamiento o ajuste de valores numéricos para mantener proporciones (por ejemplo, convertir valores a rango 0–1 o a media 0 y desviación estándar 1).
- Encoding (Codificación):	Conversión de variables categóricas en valores numéricos (por ejemplo, F→0, M→1 o mediante one-hot encoding).

## LIMPIEZA DE VALORES FALTANTES

Valores faltantes (NaN, en blanco)

¿Cómo tratar los datos faltantes?

Verificar con la fuente de recolección de datos
1.	Evaluar la posibilidad si el recolector puede averiguar o recolectar el valor faltante
2.	Eliminar los valores faltantes
   
•	Eliminar la variable

•	Eliminar la entrada de datos (cuando son pocos)

4.	Reemplazar los valores faltantes
•	Reemplazarlos con un promedio (de puntos de datos similares)
•	Reemplazarlos según la frecuencia (modo más común, cuando no es número)
•	Reemplazarlos con base en otras funciones (Conocimiento del recolector sobre experiencia)

6.	Dejar los valores faltantes 

