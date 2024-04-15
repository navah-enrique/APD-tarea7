# APD-tarea7
Repo sobre la tarea7 de Arquitectura de Producto de Datos (MGE)

# Preguntas
1. Toma el archivo review.json JSON y cuantífica cuánto pesa el archivo en disco.

R: 4.97 GBs

2. Carga el JSON en Spark y cuantífica cuánto pesa el DataFramen en memoria RAM.

R: 146.66 MBs

3. Guarda el DataFrame como parquet en disco y muestra cuánto pesa el archivo. Cómo se compara con el JSON crudo.

R: 2.80 GBs (-177% vs JSON crudo)

4. Utiliza el DataFrame, optimiza el tipo de dato que hay en cada columna (i.e. Int32, Int64, Float32, Float64, String, Categorical) y guarda el nuevo DataFrame como parquet. Cuántifica cuánto pesa el DataFrame en memoria RAM y cuánto pesa en disco. Cómo se compara con el parquet crudo.

R: RAM: R: 146.66 MBs
Disco: 2.80 GBs (PESA IGUAL que parquet crudo).

5. Utiliza el DataFrame optimizado, guarda en parquet una nueva versión del DataFrame y particionalo por fecha (date). Otra versión por ciudad. Otra por ciudad y fecha.
- Nota: Para particionar por ciudad (city) será necesario que hagas un join con la tabla business.json. (2.78GBs en disco)
- Nota: Para particionar por fecha hazlo por año y mes. Para hacer esto necesitas extraer el año y mes como columnas. (2.95GBs en disco)
- (Ambos: 3.75GBs en disco)

6. Ejecuta un query utilizando sobre la tabla filtrando por una de las ciudades y un años en particular. Registra el tiempo de ejecución. Aplica el query sobre
- la versión en JSON (más bien es la versión post-join con business para sacar el state): CPU times: user 2.48 ms, sys: 1.58 ms, total: 4.06 ms
Wall time: 1.11 s
- la versión particionada por fecha y luego: CPU times: user 3.96 ms, sys: 69 µs, total: 4.03 ms
Wall time: 445 ms
- sobre la versión particionada por fecha y lugar: CPU times: user 10.7 ms, sys: 0 ns, total: 10.7 ms
Wall time: 304 ms
  
De todos los queries que ejecutaste cuáles fueron más rápidos.
