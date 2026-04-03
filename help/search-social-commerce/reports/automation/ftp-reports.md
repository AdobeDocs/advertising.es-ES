---
title: Acceso FTP a informes
description: Obtenga información sobre cómo recibir informes en una ubicación FTP de solo lectura.
exl-id: eca9f033-5b1b-4afa-926b-b4c31e2dede3
feature: Search Reports
TQID: https://experienceleague.adobe.com/Dd72ha3yuVBLu-vCuBUFlc6lYeinKcIAu5agIco4zVY
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 428
ht-degree: 0%

---

# Acceso FTP a informes

Si lo desea, puede recibir informes en una ubicación FTP de solo lectura, desde la que podrá recuperar los archivos para procesos automatizados adicionales (por ejemplo, para analizar los datos con otro programa). Todos los informes básicos excepto [!UICONTROL Search Engine Account Report] y todos los informes avanzados se pueden enviar a una ubicación FTP como archivos TSV comprimidos (valor predeterminado) o archivos CSV, con la extensión de archivo .ZIP. Se incluyen los encabezados de archivo TSV o CSV y no se pueden suprimir.

El acceso FTP a los informes requiere el acceso a una cuenta de FTP específica. Las plantillas de informes se deben configurar según una convención de nombres y una programación específicos.

## Configuración de una cuenta de FTP para acceder a los informes

* Póngase en contacto con el equipo de su cuenta de Adobe para configurar una cuenta de FTP para el acceso a informes.

  El equipo de le proporciona su nombre de usuario y contraseña.

## Configuración de plantillas de informes para envío por FTP

Para generar informes en el directorio FTP designado, cree una [plantilla de informe](templates/template-create.md) con las siguientes convenciones de nomenclatura y programación.

>[!NOTE]
>
>Todos los informes avanzados y todos los informes básicos excepto [!UICONTROL Search Engine Account Report] se pueden enviar a una ubicación FTP.

1. En la plantilla de informe, incluya la siguiente información en cualquier parte del nombre de la plantilla:

   * `FTP` (en letras mayúsculas).

   * (Opcional) Cualquiera de las tres fechas del sistema, utilizando la siguiente sintaxis que distingue entre mayúsculas y minúsculas, incluidos los corchetes:

      * `[TODAY]`: para incluir la fecha, hora y minuto en que se ejecutó el informe. Como esto incluye la hora exacta, la misma plantilla se puede ejecutar varias veces al día sin sobrescribir el informe anterior.

      * `[SDATE]`: para incluir la fecha de inicio del intervalo de fechas del informe.

      * `[EDATE]`: para incluir la fecha de finalización del intervalo de fechas del informe.

   * (Opcional) `[CSV]` (en letras mayúsculas y entre corchetes) para crear archivos en formato CSV en lugar del formato TSV predeterminado.

   Ejemplo: `[TODAY]-Portfolio-FTP-[SDATE]-[EDATE]-[CSV]` crearía un archivo como 202305051656-Portfolio-FTP-20230428-20110504.csv.

1. Programe el informe para que se ejecute a una hora específica.

   Los informes se envían a la cuenta de FTP en el plazo de una hora después de completarse.

>[!NOTE]
>
>* Para enviar los informes completados por correo electrónico, simplemente introduzca las direcciones de todos los destinatarios de correo electrónico al generar el informe o la plantilla.
>* Los informes se ejecutan según las programaciones especificadas y se envían a la cuenta de FTP en el plazo de una hora después de completarse.

## Acceso a informes en un repositorio FTP

Para acceder a sus informes, conéctese a uno de los siguientes hosts de FTP mediante el inicio de sesión de su cuenta de FTP (`amo<userID>rpt`, como amo1234rpt) y una contraseña o una clave de conexión privada, si la hay configurada:

* Clientes internacionales: `ftp3.adobe.net`
* Clientes estadounidenses: `ftp5.adobe.net`

>[!NOTE]
>
>El repositorio de informes es de solo lectura y se purga cada 15 días.


>[!MORELIKETHIS]
>
>* [Crear una plantilla de informe](/help/search-social-commerce/reports/automation/templates/template-create.md)
