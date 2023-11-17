# individual_02
Data Analisis
## Proyecto de Mejora de Acceso a Internet en Hogares por Provincia
Descripción
Este proyecto tiene como objetivo aumentar en un 2% el acceso al servicio de internet en los hogares de cada provincia durante el próximo trimestre. La iniciativa busca mejorar la conectividad y facilitar el acceso a la información y recursos en línea para un mayor número de hogares.

Objetivo
Incrementar el acceso a internet en cada provincia en un 2%, considerando 100 hogares como base de referencia.

Metodología
Para calcular el nuevo porcentaje de acceso a internet por provincia, se utilizará la siguiente fórmula:

Nuevo Porcentaje de Acceso
=
Porcentaje Actual
+
2
Nuevo Porcentaje de Acceso=Porcentaje Actual+2

Donde el "Porcentaje Actual" es el porcentaje de acceso a internet actual en cada provincia.

## Pasos.
Conjunto de Datos
El conjunto de datos utilizado en este análisis se encuentra en el archivo Internet_Penetracion.csv en el directorio dataset. Este archivo contiene información relevante sobre la penetración de Internet en varias ubicaciones.

Información del Conjunto de Datos
El conjunto de datos tiene las siguientes columnas:

Año: Año en el que se recopilaron los datos (tipo de dato: int64).
Trimestre: Trimestre en el que se recopilaron los datos (tipo de dato: int64).
Provincia: Nombre de la provincia (tipo de dato: object).
Accesos por cada 100 hogares: Número de accesos a Internet por cada 100 hogares (tipo de dato: object).
Unnamed: 4, Unnamed: 5, Unnamed: 6: Columnas sin nombre que parecen no contener datos (tipo de dato: float64).
El conjunto de datos tiene un total de 864 entradas, con algunas columnas que contienen valores nulos.

Conjunto de Datos
El conjunto de datos utilizado en este análisis se encuentra en el archivo Internet_Penetracion.csv en el directorio dataset. Este archivo contiene información relevante sobre la penetración de Internet en varias ubicaciones.

Información del Conjunto de Datos
El conjunto de datos tiene las siguientes columnas:

Año: Año en el que se recopilaron los datos (tipo de dato: int64).
Trimestre: Trimestre en el que se recopilaron los datos (tipo de dato: int64).
Provincia: Nombre de la provincia (tipo de dato: object).
Banda ancha fija: Número de conexiones de banda ancha fija (tipo de dato: int64).
Dial up: Número de conexiones Dial-up (tipo de dato: float64) con 862 valores no nulos.
Total: Número total de conexiones (tipo de dato: int64).
El conjunto de datos tiene un total de 864 entradas.

### En el primer conjunto de datos elimino las columnas con datos nulos y transformo el tipo de datos del campo Accesos por cada 100 hogares



