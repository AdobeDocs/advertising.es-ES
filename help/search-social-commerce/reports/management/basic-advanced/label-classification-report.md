---
title: '[!UICONTROL Label Classification Report]'
description: Más información acerca de [!UICONTROL Label Classification Report].
exl-id: 847fa384-b9c6-446f-9ebf-da7679ed35ae
feature: Search Reports, Search Basic Reports
TQID: https://experienceleague.adobe.com/75t5C8Cz-EE5vsPYYXHWHSE-6ZDhwSQaEgtAdirYHQU
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 227
ht-degree: 0%

---

# [!UICONTROL Label Classification Report]

[!UICONTROL Label Classification Report] incluye datos de costo, clics y (opcionalmente) conversión por clasificación de etiquetas de nivel de palabra clave o de anuncio agregada en redes de anuncios, cuentas, campañas o grupos de anuncios. De forma predeterminada, los datos incluyen una fila para cada clasificación de etiquetas de nivel de palabra clave aplicable para palabras clave, anuncios y ubicaciones que recibieron impresiones para cada unidad de tiempo en el intervalo de fechas especificado. Las filas están en orden ascendente, primero por la fecha de inicio de la unidad de tiempo, después por clasificación de etiquetas y, por último, por valor de etiqueta, de forma predeterminada.

Puede ver los datos de los 36 meses anteriores.

>[!NOTE]
>
>* Los informes de clasificaciones de etiquetas de nivel de anuncio no están disponibles para [!DNL Microsoft Advertising] campañas de anuncios dinámicos de búsqueda (DSA).
>* Se puede aplicar más de una clasificación de etiquetas a la misma entidad, por lo que el total de cada métrica puede ser superior al total real de la entidad. Por ejemplo, supongamos que una palabra clave &quot;zapatos de ante&quot; tiene dos valores de etiqueta, &quot;ante&quot; y &quot;calzado&quot;, y la palabra clave recibió 100 clics. La columna Clics mostraría &quot;100&quot; para cada uno de esos valores de etiqueta, por lo que el total para ambas filas sería &quot;200&quot;.
>* Cualquier cambio que realice en las clasificaciones de etiquetas y en los valores de etiquetas secundarias de una entidad será visible en aproximadamente una hora.

## Columnas predeterminadas

Para obtener descripciones de todas las columnas predeterminadas y personalizadas, consulte &quot;[Columnas de informe para informes básicos y avanzados](basic-advanced-report-columns.md)&quot;.

* [!UICONTROL Label Classification]
* [!UICONTROL Label Value]
* [!UICONTROL Start Date]
* [!UICONTROL End Date]
* [!UICONTROL Impressions]
* [!UICONTROL Cost]
* [!UICONTROL Clicks]
* [!UICONTROL CPC]
* [!UICONTROL Avg Position]
* [!UICONTROL Impr. (Abs. Top) %]
* [!UICONTROL Impr. (Top) %]

>[!MORELIKETHIS]
>
>* [Acerca de los informes básicos y avanzados](basic-advanced-report-about.md)
>* [Generar un informe básico o avanzado](basic-advanced-report-generate.md)
>* [Configuración básica y avanzada del informe](basic-advanced-report-settings.md)
