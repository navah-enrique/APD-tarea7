# APD-tarea7
Repo sobre la tarea7 de Arquitectura de Producto de Datos (MGE)

# Preguntas
Toma el archivo review.json JSON y cuantífica cuánto pesa el archivo en disco.

R: 5.21 GBs

Carga el JSON en Spark y cuantífica cuánto pesa el DataFramen en memoria RAM.

R: 

Guarda el DataFrame como parquet en disco y muestra cuánto pesa el archivo. Cómo se compara con el JSON crudo.

Utiliza el DataFrame, optimiza el tipo de dato que hay en cada columna (i.e. Int32, Int64, Float32, Float64, String, Categorical) y guarda el nuevo DataFrame como parquet. Cuántifica cuánto pesa el DataFrame en memoria RAM y cuánto pesa en disco. Cómo se compara con el parquet crudo.

Utiliza el DataFrame optimizado, guarda en parquet una nueva versión del DataFrame y particionalo por fecha (date). Otra versión por ciudad. Otra por ciudad y fecha.

Nota: Para particionar por ciudad (city) será necesario que hagas un join con la tabla business.json.
Nota: Para particionar por fecha hazlo por año y mes. Para hacer esto necesitas extraer el año y mes como columnas.
Ejecuta un query utilizando sobre la tabla filtrando por una de las ciudades y un años en particular. Registra el tiempo de ejecución. Aplica el query sobre

la versión en JSON
la versión particionada por fecha y luego
sobre la versión particionada por fecha y lugar
De todos los queries que ejecutaste cuáles fueron más rápidos.
