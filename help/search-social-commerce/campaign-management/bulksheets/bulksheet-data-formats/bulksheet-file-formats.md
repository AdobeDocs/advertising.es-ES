---
title: Formatos de archivo de hojas de edición masiva admitidos
description: Consulte los requisitos generales de archivo para hojas de edición masiva.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Formatos de archivo de hojas de edición masiva admitidos

## Formatos de archivo

Puede descargar, cargar y publicar archivos de hojas de edición masiva para redes de publicidad admitidas en cualquiera de los siguientes formatos:

* CSV (valores separados por comas)
* TSV (valores separados por tabulaciones)
* TXT (texto Unicode), delimitado por comas o tabulaciones
* ZIP (comprimido) que contiene un archivo en formato CSV, formato TSV o formato TXT delimitado por comas o tabulaciones

Al crear/descargar una hoja de edición masiva, se crea en el formato de archivo especificado con todos los datos relevantes incluidos en el archivo. Utilice la siguiente información para editar los datos del archivo o crear su propia hoja de edición masiva manualmente.

## Contenido básico de una hoja de edición masiva

El primer registro (línea) de un archivo de hoja de edición masiva contiene un conjunto de nombres de columna específicos, conocidos colectivamente como <i>encabezado</i>. Los nombres de columna del encabezado están en un orden especificado y corresponden a cada uno de los campos de los registros de datos posteriores. Los nombres de columna requeridos en el encabezado varían según la red de publicidad.

Cada registro (línea) posterior contiene datos, con campos que contienen valores (o ningún valor) para cada columna en el encabezado.

## Tamaño máximo de archivo

Los archivos de hojas de edición masiva pueden tener hasta 2,5 GB, lo que equivale a unos 2,5 millones de filas.

>[!NOTE]
>
>Cuando se genera una hoja de edición masiva para varias campañas y los datos combinados constan de más de 500 000 filas, los datos se dividen por campaña en dos o más archivos, llamados `<bulksheet name>_1.tsv`, `<bulksheet name>_2.tsv`, etc.

## Requisitos de formato para diferentes tipos de archivo

Los campos de datos delimitados por tabulaciones y comas requieren un formato diferente.

### Archivos TSV y archivos TXT delimitados por tabulaciones

Los campos de datos de los archivos TSV y los archivos TXT delimitados por pestañas deben tener el siguiente formato:

* Los campos de cada registro están separados por caracteres de tabulación. Para omitir un valor para un campo, utilice solo el carácter de tabulación.

   Ejemplo: `Cruises<TAB>5000<TAB>Caribbean<TAB><TAB><TAB>`

* Los campos no pueden contener caracteres de tabulación incrustados.

### Archivos CSV y archivos TXT delimitados por comas

Los campos de datos de los archivos CSV y los archivos TXT delimitados por comas deben tener el siguiente formato:

* Los campos de un registro están separados por comas. Para omitir un valor para un campo, utilice solo la coma.

   Ejemplo: `Cruises,5000,Caribbean,,,`

* Cualquier campo puede incluirse opcionalmente entre comillas dobles (`""`).

   Ejemplo:  `"Cruises","5000","Caribbean",`

* Los campos con comas incrustados deben estar entre comillas dobles (`""`).

   Ejemplo: `Cruises,5000,Caribbean,"Luxurious, spacious cabins",`

* Los campos con comillas dobles incrustadas deben estar entre comillas dobles (`""`).

   Ejemplo: `Cruises,5000,Caribbean,"Customers say ""We wish we could stay forever."",`

* Los campos con espacios iniciales o finales deben estar entre comillas dobles (`""`).

   Ejemplo: `Cruises,5000,Caribbean,"  Come see what we mean.  ",`

>[!MORELIKETHIS]
>
>* [Administración de datos de campaña mediante hojas de edición masiva](../bulksheet-about.md)
>* [Operaciones que se pueden realizar en hojas de edición masiva](bulksheet-operations.md)
>* [Apéndice: Errores de hojas de edición masiva](../bulksheet-errors.md)
>* [Descargar/crear un archivo de hoja de edición masiva](../bulksheet-download.md)

