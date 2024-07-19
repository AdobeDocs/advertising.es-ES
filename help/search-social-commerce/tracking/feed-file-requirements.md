---
title: Requisitos de archivo para archivos de fuentes de conversión
description: Consulte los requisitos para los archivos de fuentes de conversión.
exl-id: abc28394-3e00-447f-a04e-078fa9883a64
feature: Search Tracking
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '360'
ht-degree: 0%

---

# Requisitos de archivo para archivos de fuentes de conversión

A continuación se indican los requisitos para el formato de archivo, los campos de datos obligatorios y opcionales, el nombre de archivo y el protocolo de transferencia de archivos para los archivos de fuente.

## Formato de archivo

El archivo de datos debe tener el formato de texto sin formato (TXT), valores separados por comas (CSV) o valores separados por tabuladores (TSV). El archivo puede constar de una fila de encabezado y filas de datos con valores separados por tabulaciones, comas u otro carácter (pero no espacios):

* **Fila de encabezado:** (opcional) La primera línea del archivo es un encabezado, que especifica los nombres de campo requeridos (o nombres de columna) en un orden específico, separados por tabulaciones o comas. Los nombres de columna requeridos incluyen las métricas de conversión que el Adobe Advertising está rastreando como conversiones.

* **Filas de datos:** Cada línea posterior incluye campos de datos en el mismo orden que el encabezado y separados por tabulaciones o comas. Si el primer registro no es un encabezado, cada fila de datos debe incluir todos los campos posibles, en el orden especificado. Los valores de todos los ID y las métricas de conversión deben ser alfanuméricos.

  Cuando varios clics en uno o varios anuncios conducen a una transacción, debe determinar el ID de clic y el ID de seguimiento a los que atribuir la transacción. Dado que se informa de un ID único para cada transacción, puede actualizar las transacciones individuales.

## Convenciones de nomenclatura de archivos

El nombre de archivo debe incluir la fecha y ser coherente. Por ejemplo, si utiliza el formato AAAAMMDD.txt, un archivo enviado el 15 de mayo de 2011 debe llamarse 20110515.txt.

## Protocolo de transferencia de archivos

Envíe el archivo a través del protocolo de transferencia SFTP mediante el puerto 22. Debe proporcionar la información de clave pública.  El equipo de cuenta de Adobe o el equipo de implementación le proporcionan la ubicación del servidor junto con las credenciales necesarias para que el sistema transfiera los archivos.

>[!TIP]
>
>Las fuentes de datos de conversión se procesan varias veces al día. Cargue la fuente diaria lo antes posible después de las 12:00 de la medianoche (hora local) para que el Adobe Advertising pueda procesar los datos y ponerlos a disposición en la interfaz de usuario del sistema de informes por la mañana temprano.

>[!MORELIKETHIS]
>
>* [Requisitos de datos para fuentes de datos que usan EF ID](/help/search-social-commerce/tracking/feed-ef-id-data-requirements.md)
>* [Requisitos de datos para fuentes de datos que usan un ID de transacción](/help/search-social-commerce/tracking/feed-transaction-id-data-requirements.md)
