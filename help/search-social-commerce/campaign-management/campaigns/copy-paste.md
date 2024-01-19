---
title: Cree y edite datos de campaña por lotes utilizando copiar y pegar
description: Obtenga información sobre cómo administrar los datos de campaña por lotes mediante la función de copiar y pegar.
exl-id: 2ae1b02f-46ac-4ea8-aa9f-9e26ccaf63d0
feature: Search Campaign Management
source-git-commit: c2a1ce841a9dc99c57239f817dbd2065b91cdfb9
workflow-type: tm+mt
source-wordcount: '486'
ht-degree: 0%

---

# Cree y edite datos de campaña por lotes utilizando copiar y pegar

*[!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads], [!DNL Yandex], y existentes [!DNL Baidu] solo cuentas*

*[!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords], y [!UICONTROL Ads] vistas*

Puede copiar hasta 10 000 filas de la [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords], y [!UICONTROL Ads] vistas y péguelas en [!DNL Microsoft Excel] u otro editor para editar campos que no sean ID. A continuación, puede copiar el [!DNL Excel] filas y péguelas como datos separados por tabulaciones de nuevo en la vista para realizar los cambios. La función utiliza el portapapeles del equipo.

Puede utilizar esta función para editar objetos de campaña existentes (con campos de ID) y crear nuevos objetos de campaña sin campos de ID.

## Copiar filas de datos

1. En el menú principal, haga clic en **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. En los submenús, haga clic en **[!UICONTROL Live]> \[[!UICONTROL Campaigns] \| [!UICONTROL Ad Groups] \| [!UICONTROL Keywords] \| [!UICONTROL Ads]\]**.

1. Active la casilla de verificación situada junto a cada fila que desee copiar.

   Puede copiar hasta 10 000 filas.

1. En la barra de herramientas sobre la tabla de datos, haga clic en ![Más](/help/search-social-commerce/assets/more.png "Más")y haga clic en **[!UICONTROL Copy]**.

   Como alternativa, puede utilizar el comando de teclado &quot;copiar&quot; de su sistema operativo, como **[!DNL Ctrl+C]** para [!DNL Microsoft Windows] o **[!DNL Command-C]** para [!DNL Apple Mac].

1. En el [!UICONTROL Copy to Clipboard] , haga clic en **[!UICONTROL Continue]**. Cuando los datos estén listos para copiarse, haga clic en **[!UICONTROL Copy]**.

1. Pegar las filas en [!DNL Excel] u otro editor.

## Edición y creación de filas de datos

1. Edite los datos según los siguientes requisitos:

   * Los datos pegados deben incluir una fila de encabezado y los valores de objeto de campaña necesarios; consulte las columnas de hoja de edición masiva necesarias para [Baidu](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-baidu.md), [Google Ads](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-google.md), [Microsoft Advertising](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-microsoft.md), [Naver](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-naver.md), [Yahoo! Mostrar red](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-yahoo-display-network.md), [Yahoo! Japón](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-yahoo-japan.md), y [Yandex](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-yandex.md). El orden de las columnas no importa.

      * Para los objetos existentes que desea editar, debe incluir todas las columnas de ID., nombres de entidad y el atributo relevantes que desea editar. No edite el ID numérico del objeto.

      * Para los nuevos objetos de campaña, incluya todos los nombres y atributos de entidad relevantes, pero no incluya los ID de objeto (que se generan automáticamente). Por ejemplo, si crea un anuncio nuevo, deje la variable [!UICONTROL Ad ID] en blanco. La red publicitaria crea automáticamente un ID al publicar el objeto.

   * El valor de cualquier columna no requerida puede ser nulo (en blanco), pero cada fila debe tener el mismo número de valores separados por tabulaciones.

1. Guarde los datos como valores separados por tabulaciones.

## Pegar filas de datos en las vistas de administración de campañas

>[!NOTE]
>
>Si las filas pegadas contienen datos idénticos a los de las entidades existentes o que duplican una entidad existente, los datos duplicados se omiten.

1. Entrada [!DNL Excel] Para cualquier otro editor, copie las filas separadas por tabulaciones relevantes.

1. En el menú principal Buscar, Social y Comercio, haga clic en **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Abra la vista en la que desea pegar los datos (**[!UICONTROL Live]> \[[!UICONTROL Campaigns] \| [!UICONTROL Ad Groups] \| [!UICONTROL Keywords] \| [!UICONTROL Ads]\]**).

1. En la barra de herramientas sobre la tabla de datos, haga clic en ![Más](/help/search-social-commerce/assets/more.png "Más")y haga clic en **[!UICONTROL Paste]**.

   Como alternativa, puede utilizar el comando de teclado &quot;pegar&quot; de su sistema operativo, como **[!DNL Ctrl+V]** para [!DNL Microsoft Windows] o **[!DNL Command-V]** para [!DNL Apple Mac].

1. Pegue los datos en el cuadro de entrada y haga clic en **[!UICONTROL Process]**.

1. (Opcional) Introduzca detalles adicionales:

   * (Si **[!UICONTROL Additional Details]** está comprimido) Haga clic en ![Abrir](/help/search-social-commerce/assets/chevron-up.png "Abrir") para ampliar los detalles.

   * Introduzca un opcional **[!UICONTROL Job Name]** y/o opcional **[!UICONTROL Job Description]**.

1. Clic **[!UICONTROL Post Now]**.


>[!MORELIKETHIS]
>
>* [Administración de datos de campaña mediante hojas de edición masiva](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md)
>* [Editar la configuración directamente dentro de una fila](/help/search-social-commerce/common-tasks/settings-edit-within-row.md)
>* [Administración de campañas](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md)
>* [Administrar grupos de anuncios](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md)
>* [Administrar palabras clave](/help/search-social-commerce/campaign-management/campaigns/keyword-manage.md)
>* [Administración de anuncios](/help/search-social-commerce/campaign-management/campaigns/ad-manage.md)
