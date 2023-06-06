---
title: Acceso FTP a informes
description: Obtenga información sobre cómo recibir informes en una ubicación FTP de solo lectura.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Acceso FTP a informes

Si lo desea, puede recibir informes en una ubicación FTP de solo lectura, desde la que podrá recuperar los archivos para procesos automatizados adicionales (por ejemplo, para analizar los datos con otro programa). Todos los informes básicos excepto [!UICONTROL Search Engine Account Report] y todos los informes avanzados se pueden enviar a una ubicación FTP como archivos TSV comprimidos (opción predeterminada) o archivos CSV, con la extensión de archivo .ZIP. Se incluyen los encabezados de archivo TSV o CSV y no se pueden suprimir.

El acceso FTP a los informes requiere el acceso a una cuenta de FTP específica. Las plantillas de informes se deben configurar según una convención de nombres y una programación específicos.

## Configuración de una cuenta de FTP para acceder a los informes

* Póngase en contacto con el equipo de cuenta de Adobe para configurar una cuenta de FTP para el acceso al informe.

   El equipo le proporcionará su nombre de usuario y contraseña.

## Configuración de plantillas de informes para envío por FTP

Para generar informes en el directorio FTP designado, cree un [plantilla de informe](templates/template-create.md) con las siguientes convenciones de nomenclatura y programación.

>[!NOTE]
>
>Todos los informes avanzados y todos los informes básicos excepto el [!UICONTROL Search Engine Account Report] se puede enviar a una ubicación FTP.

1. En la plantilla de informe, incluya la siguiente información en cualquier parte del nombre de la plantilla:

   * `FTP` (en letras mayúsculas).

   * (Opcional) Cualquiera de las tres fechas del sistema, utilizando la siguiente sintaxis que distingue entre mayúsculas y minúsculas, incluidos los corchetes:

      * `[TODAY]` — Para incluir la fecha, hora y minuto en que se ejecutó el informe. Como esto incluye la hora exacta, la misma plantilla se puede ejecutar varias veces al día sin sobrescribir el informe anterior.

      * `[SDATE]` — Para incluir la fecha de inicio del intervalo de fechas del informe.

      * `[EDATE]` — Para incluir la fecha de finalización del intervalo de fechas del informe.
   * (Opcional) `[CSV]` (en letras mayúsculas y entre corchetes) para crear archivos en formato CSV en lugar del formato TSV predeterminado.

   Ejemplo: `[TODAY]-Portfolio-FTP-[SDATE]-[EDATE]-[CSV]` crearía un archivo como 202305051656-Portfolio-FTP-20230428-20110504.csv.

1. Programe el informe para que se ejecute a una hora específica.

   Los informes se envían a la cuenta de FTP en el plazo de una hora después de completarse.

>[!NOTE]
>
>* Para enviar los informes completados por correo electrónico, simplemente introduzca las direcciones de todos los destinatarios de correo electrónico al generar el informe o la plantilla.
>* Los informes se ejecutan según las programaciones especificadas y se envían a la cuenta de FTP en el plazo de una hora después de completarse.


## Acceso a informes en un repositorio FTP

Para acceder a sus informes, conéctese a uno de los siguientes hosts de FTP mediante el inicio de sesión de su cuenta de FTP (`amo<userID>rpt`, como amo1234rpt) y una contraseña o una clave de conexión privada si hay una configurada:

* Clientes internacionales: `ftp3.adobe.net`
* Clientes estadounidenses: `ftp5.adobe.net`

>[!NOTE]
>
>El repositorio de informes es de solo lectura y se purga cada 15 días.


>[!MORELIKETHIS]
>
>* [Creación de una plantilla de informe](/help/search-social-commerce/reports/automation/templates/template-create.md)

