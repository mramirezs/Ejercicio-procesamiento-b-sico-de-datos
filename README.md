# Ejercicio: procesamiento básico de datos

## Obtención de datos biológicos

Archivo de anotación genética:

https://ftp.ebi.ac.uk/pub/databases/gencode/Gencode_human/release_46/gencode.v46.annotation.gff3.gz

Vamos a nuestro terminal.

### Comandos básicos

- Crear el directorio de trabajo genecode_annotation_v46
- Descargar el archivo de anotación gencode.v46.annotation.gff3.gz
- Verificar el tamaño de archivo gencode.v46.annotation.gff3.gz
- Visualizar las primeras líneas del archivo de anotación sin descomprimir (zcat)
- Usar la opción `-l` con zcat y verficar los datos.
- Descomprimir el archivo de anotación (gunzip).
- Visualizar el contenido total del archivo descomprimido.

### comandos intermedios

- Omitir las `#` al inicio de las líneas del archivo descomprimido (`^`).
- Obtener la tercera columna del archivo y observar las 10 primeras líneas
- Ordenarlos y contar las categorias únicos que se encuentran en la columna.
- ¿Cuál es el número de `transcript` que se obtienen?
- Convertir el archvivo gff a bed.
- Ordenar por cromosomas y por la posición inicial (`-V`)
- Convertir al formato punto y coma (`tr`)

