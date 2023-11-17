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

### En el primer conjunto de datos elimino las columnas con datos nulos y transformo el tipo de datos del campo Accesos por cada 100 hogares.
<img width="398" alt="Captura de pantalla 2023-11-17 a la(s) 3 12 44 p m" src="https://github.com/teamlider/individual_02/assets/54252072/0657b28d-8256-413b-ae82-b5b41cfda750">

<img width="983" alt="Captura de pantalla 2023-11-17 a la(s) 3 12 54 p m" src="https://github.com/teamlider/individual_02/assets/54252072/e0bffdc0-de07-421c-823b-9cf2bf04fd6e">

### Despues de realizar el proceso de limpieza de los dos archivos. 
### Inicio con el analisis de los campos.
reviso la distribucion de los diferentes campos para tener una idea clara de la información 


### Distribución del campo años y del campo provicias.

<img width="848" alt="Captura de pantalla 2023-11-17 a la(s) 3 21 00 p m" src="https://github.com/teamlider/individual_02/assets/54252072/9b9d17d8-ea4a-43d7-9a81-f9277d431ccf">

<img width="1006" alt="Captura de pantalla 2023-11-17 a la(s) 3 21 11 p m" src="https://github.com/teamlider/individual_02/assets/54252072/a82e388f-a66d-4991-9d50-8cb1ca1e5f2e">

### Fusióno los DataFrames:

realizo un merge de los dos DataFrames (df_p y penetracion_dos) utilizando las columnas 'Año', 'Trimestre' y 'Provincia' como claves de fusión. El resultado se almacena en merged_df.
cálculo de Nuevo Acceso:
calculo un nuevo acceso utilizando la fórmula proporcionada: Nuevo Acceso = (Accesos por cada 100 hogares * 100) * (1 + 0.02). Se multiplica por 100 para convertir el resultado a enteros y se almacena en la columna 'Nuevo Acceso' del DataFrame.
Cálculo el KPI (Indicador Clave de Rendimiento):
calculo el KPI utilizando la fórmula proporcionada: KPI = ((Nuevo Acceso - Accesos por cada 100 hogares * 100) / (Accesos por cada 100 hogares * 100)) * 100. Este valor se expresa como un porcentaje y se almacena en la columna 'KPI' del DataFrame.
Muestro el DataFrame resultante:
Se seleccionan las columnas relevantes ('Año', 'Trimestre', 'Provincia', 'Accesos por cada 100 hogares', 'Nuevo Acceso', 'KPI') y se muestra el DataFrame resultante.
<img width="675" alt="Captura de pantalla 2023-11-17 a la(s) 3 27 05 p m" src="https://github.com/teamlider/individual_02/assets/54252072/42b2957e-8bbc-461d-8510-4691ad026178">

## Análisis de Datos - Gráficos de Nuevos Accesos en las Provincias (Últimos 2 Trimestres del 2022)
### Realizo una grafica por provincia.

El objetivo es visualizar datos específicos de un DataFrame fusionado (merged_df). filtrando y representando gráficamente los nuevos accesos en las provincias durante los dos últimos trimestres del año 2022.

<img width="717" alt="Captura de pantalla 2023-11-17 a la(s) 3 32 32 p m" src="https://github.com/teamlider/individual_02/assets/54252072/fb9a9709-e5bb-47fa-b78e-050adc3defac">

<img width="704" alt="Captura de pantalla 2023-11-17 a la(s) 3 32 50 p m" src="https://github.com/teamlider/individual_02/assets/54252072/11401fd9-39cc-402d-a931-6673dc3ce6ee">
