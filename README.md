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

## Conversión de un archivo fastq a fasta

Archivo de datos crudos:

ftp://ftp.sra.ebi.ac.uk/vol1/fastq/ERR000/ERR000001/ERR000001_1.fastq.gz

Vamos a nuestro terminal, nuevamente.

### Comandos básicos

- Crear el directorio de trabajo Project_genome_001.
- Dentro del directorio de trabajo crear el directorio raw_data.
- Descargar el archivo de lecturas crudas ERR000001_1.fastq.gz.
- Desccomprimir el archivo ERR000001_1.fastq.gz.
- Convertir el archivo fastq a un archivo tabular ERR000001_1.tab.txt
- Visualizar las 10 primeras líneas del archivo tabular ERR000001_1.tab.txt.
- Buscar el patrón CCCCCTTAAAA en el archivo tabular ERR000001_1.tab.txt.

### Comandos avanzados

```
awk '/patrón de búsqueda/ {Acción}' Archivo
```

- Buscar el patrón CCCCCTTAAAA en el archivo tabular ERR000001_1.tab.txt e imprimir las líneas.
- Buscar el patrón CCCCCTTAAAA en el archivo tabular ERR000001_1.tab.txt e imprimir la columna 1 y 3.
- Buscar la base N en la tercera columna del archivo tabular ERR000001_1.tab.txt
- Ordenar el archivo tabular ERR000001_1.tab.txt en base a la 3 columna y guardarlo como  ERR000001_1_tab.srt.
- Ordenar el archivo tabular EERR000001_1_tab.srt en base a la 3 columna y eliminar los duplicados guardándolo como  ERR000001_1_tab.srt.unq.
- ¿Cuántas líneas tiene el archivo ERR000001_1_tab.srt.unq?.

```
sed 's/patrón/reemplazo/' archivo.txt
```

- Imprimir las columnnas 1 y 3 del archivo ERR000001_1_tab.srt.unq y almacenarlos como ERR000001_1.allseqs.txt.
- Agregar el simbolo `>` al archivo  ERR000001_1.allseqs.txt
- Obtener el archivo ERR000001_1.allseqs.fasta en el formato oficial. 
