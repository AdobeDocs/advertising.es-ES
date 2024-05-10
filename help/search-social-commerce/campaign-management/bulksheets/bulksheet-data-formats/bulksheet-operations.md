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

Puede añadir, editar y eliminar datos de campaña mediante hojas de edición por lotes para [redes de publicidad admitidas](../bulksheet-about.md#bulksheet-functionality-by-network).

Incluya una línea de datos independiente para cada componente de campaña (campaña, grupo de publicidad, palabra clave o anuncio de texto) que desee agregar, editar o eliminar, o cuyas propiedades desee agregar, editar o eliminar. Por ejemplo, si desea crear una campaña con un grupo de anuncios, una palabra clave y un anuncio (un total de cuatro componentes), necesita cuatro líneas de datos independientes. Para editar la variable [!UICONTROL Ad Group Name] sin embargo, para un grupo de publicidad (un componente), solo necesita una línea. Del mismo modo, para editar cuatro propiedades diferentes para un grupo de anuncios (un componente), solo necesita una línea.

Las siguientes reglas se aplican al trabajo con componentes de campaña y sus propiedades.

* Añadiendo:

   * Para agregar un componente, incluya todos los campos necesarios para agregar ese componente y, opcionalmente, incluya campos para cualquiera de las propiedades del componente.

   * Para agregar una propiedad para un componente existente, como [!UICONTROL Ad Group End Date] para un grupo de anuncios, incluya todos los campos necesarios para editar ese componente (grupo de anuncios) más el campo de la propiedad ([!UICONTROL Ad Group End Date]).

* Para editar una propiedad para un componente existente, incluya todos los campos necesarios para editar ese componente más el campo de la propiedad.

  Si deja en blanco el campo de propiedad, se conserva el valor existente.

* Eliminando:

   * Para eliminar un componente existente, incluya todos los campos necesarios para editar ese componente y cambie su estado a [!UICONTROL Deleted]. Por ejemplo, para eliminar un [!DNL Google Ads] grupo de anuncios, debe incluir el [!UICONTROL Campaign Name], [!UICONTROL Ad Group Name], [!UICONTROL Ad Group Status] con un valor de <i>[!UICONTROL Deleted]</i>, y [!UICONTROL Ad Group ID].

   * ([!UICONTROL Param1], [!UICONTROL Param2], y [!UICONTROL Param3] (solo valores de ) Para eliminar un [!DNL paramN] para una palabra clave, incluya todos los campos necesarios para editar la palabra clave y también elimine los campos existentes [!DNL paramN] al introducir el valor `[delete]` (incluidos los corchetes) en el campo correspondiente.

   * (Campos de propiedad permitidos) Para eliminar un valor de propiedad existente de un componente, incluya todos los campos necesarios para editar ese componente y también elimine el valor de propiedad introduciendo el valor `[delete]` (incluidos los corchetes). Los campos permitidos incluyen:

      * ([!UICONTROL Google Ads] solo) [!UICONTROL Description Line 1], [!UICONTROL Description Line 2]

      * ([!DNL Google Ads] y [!DNL Microsoft Advertising] solo) [!UICONTROL Product Scope Filter], [!UICONTROL Base URL/Final URL], [!UICONTROL Tracking Template]

>[!NOTE]
>
>Cuando se incluye un valor en un campo que no es aplicable a la acción, se ignora cualquier valor introducido en el campo.

>[!MORELIKETHIS]
>
>* [Administración de datos de campaña mediante hojas de edición masiva](../bulksheet-about.md)
>* [Formatos de archivo de hojas de edición masiva admitidos](bulksheet-file-formats.md)
>* [Apéndice: Errores de hojas de edición masiva](../bulksheet-errors.md)
>* [Descargar/crear un archivo de hoja de edición masiva](../bulksheet-download.md)
