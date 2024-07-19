---
title: Operaciones que se pueden realizar en hojas de edición masiva
description: Consulte información general sobre cómo agregar, editar y eliminar datos de campaña mediante hojas de edición por lotes.
exl-id: 17ec9307-6dfd-45cb-b8bd-d0d7fcbf2d41
feature: Search Bulksheets
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '381'
ht-degree: 0%

---

# Operaciones que se pueden realizar en hojas de edición masiva

Puede agregar, editar y eliminar datos de campañas mediante hojas de edición por lotes para [redes de anuncios compatibles](../bulksheet-about.md#bulksheet-functionality-by-network).

Incluya una línea de datos independiente para cada componente de campaña (campaña, grupo de publicidad, palabra clave o anuncio de texto) que desee agregar, editar o eliminar, o cuyas propiedades desee agregar, editar o eliminar. Por ejemplo, si desea crear una campaña con un grupo de anuncios, una palabra clave y un anuncio (un total de cuatro componentes), necesita cuatro líneas de datos independientes. Sin embargo, para editar [!UICONTROL Ad Group Name] para un grupo de publicidad (un componente), solo necesita una línea. Del mismo modo, para editar cuatro propiedades diferentes para un grupo de anuncios (un componente), solo necesita una línea.

Las siguientes reglas se aplican al trabajo con componentes de campaña y sus propiedades.

* Añadiendo:

   * Para agregar un componente, incluya todos los campos necesarios para agregar ese componente y, opcionalmente, incluya campos para cualquiera de las propiedades del componente.

   * Para agregar una propiedad para un componente existente, como [!UICONTROL Ad Group End Date] para un grupo de anuncios, incluya todos los campos necesarios para editar ese componente (grupo de anuncios) más el campo de la propiedad ([!UICONTROL Ad Group End Date]).

* Para editar una propiedad para un componente existente, incluya todos los campos necesarios para editar ese componente más el campo de la propiedad.

  Si deja en blanco el campo de propiedad, se conserva el valor existente.

* Eliminando:

   * Para eliminar un componente existente, incluya todos los campos necesarios para editar ese componente y cambie su estado a [!UICONTROL Deleted]. Por ejemplo, para eliminar un grupo de anuncios de [!DNL Google Ads], debe incluir [!UICONTROL Campaign Name], [!UICONTROL Ad Group Name], [!UICONTROL Ad Group Status] con un valor de <i>[!UICONTROL Deleted]</i> y [!UICONTROL Ad Group ID].

   * ([!UICONTROL Param1], [!UICONTROL Param2] y [!UICONTROL Param3] valores solamente) Para eliminar un valor [!DNL paramN] existente de una palabra clave, incluya todos los campos necesarios para editar la palabra clave y también elimine el valor [!DNL paramN] existente al escribir el valor `[delete]` (incluidos los corchetes) en el campo correspondiente.

   * (Campos de propiedad permitidos) Para eliminar un valor de propiedad existente de un componente, incluya todos los campos necesarios para editar ese componente y también elimine el valor de propiedad introduciendo el valor `[delete]` (incluidos los corchetes). Los campos permitidos incluyen:

      * ([!UICONTROL Google Ads] solamente) [!UICONTROL Description Line 1], [!UICONTROL Description Line 2]

      * ([!DNL Google Ads] y [!DNL Microsoft Advertising] solamente) [!UICONTROL Product Scope Filter], [!UICONTROL Base URL/Final URL], [!UICONTROL Tracking Template]

>[!NOTE]
>
>Cuando se incluye un valor en un campo que no es aplicable a la acción, se ignora cualquier valor introducido en el campo.

>[!MORELIKETHIS]
>
>* [Acerca de la administración de datos de campaña mediante hojas de edición masiva](../bulksheet-about.md)
>* [Formatos de archivo de hojas de edición masiva admitidos](bulksheet-file-formats.md)
>* [Apéndice: errores de hojas de edición masiva](../bulksheet-errors.md)
>* [Descargar o crear un archivo de hoja de edición masiva](../bulksheet-download.md)
