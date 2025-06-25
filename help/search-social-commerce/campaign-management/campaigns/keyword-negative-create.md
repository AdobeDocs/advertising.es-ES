---
title: Creación de palabras clave negativas
description: Aprenda a crear palabras clave negativas para campañas de búsqueda y grupos de anuncios.
exl-id: afe786bf-eda8-4590-b471-3fb696c420de
feature: Search Campaign Management
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '272'
ht-degree: 0%

---

# Creación de palabras clave negativas

*[!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads] y solo [!DNL Baidu] cuentas existentes*

Puede crear palabras clave negativas para un grupo de anuncios de búsqueda o una campaña que esté dirigido a la red de búsqueda, de visualización o nativa. Las palabras clave negativas no déclencheur los anuncios.

>[!NOTE]
>También puede crear y editar palabras clave negativas en las [configuraciones del grupo de anuncios](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md) y [configuraciones de campaña](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md).

>[!TIP]
>Para crear muchas palabras clave negativas a la vez, use [hojas de edición masiva de campañas](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

1. En el menú principal, haga clic en **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. En los submenús, haga clic en **[!UICONTROL Live]> [!UICONTROL Keywords] >[!UICONTROL Negatives]**.

1. En la barra de herramientas situada encima de la tabla de datos, haga clic en ![Crear](/help/search-social-commerce/assets/add.png "Crear") y, a continuación, haga clic en **[!UICONTROL Campaign]** para crear palabras clave negativas en el nivel de campaña o en **[!UICONTROL Ad Group]** para crear palabras clave negativas en el nivel de grupo de anuncios.

1. Seleccione la red de anuncios, la cuenta, la campaña y (cuando corresponda) el grupo de anuncios y haga clic en **[!UICONTROL Continue]**.

1. Introduzca las palabras clave negativas. Utilice la siguiente sintaxis, sin un signo menos (`-`):

   * Coincidencia amplia negativa: `keyword` (no admitido por [!DNL Microsoft Advertising])

   * Coincidencia de frase negativa: `"keyword"`

   * Coincidencia exacta negativa: `[keyword]`

   Separe varios valores con comas o introdúzcalos en líneas independientes. Puede escribir o pegar hasta 2000 palabras clave negativas en una operación. Consulte también los siguientes requisitos y restricciones:

   * Longitudes máximas de caracteres: [!DNL Baidu]: 30 bytes simples o 15 bytes dobles; [!DNL Microsoft Advertising]: 100 bytes simples o 50 bytes dobles; [!DNL Google Ads] y [!DNL Yahoo! Japan Ads]: 80 bytes simples o 40 bytes dobles.

   * [!DNL Baidu] solo permite un tipo de coincidencia por palabra clave y grupo de anuncios. Por ejemplo, el grupo de anuncios 1 no puede incluir `"keyword"` y `[keyword]`.

   * [!DNL Google Ads]: cada palabra clave no puede contener más de 10 palabras y solo puede incluir letras, dígitos y los siguientes caracteres especiales: espacio `# $ & _ - " [ ] ' + . / :`

   * [!DNL Yandex]: cada palabra clave puede tener un máximo de siete palabras, excluyendo las palabras de detención. Cada [!DNL Yandex ad group] puede incluir un máximo de 200 palabras clave.

1. Haga clic en **[!UICONTROL Post]**.

>[!MORELIKETHIS]
>
>* [Acerca de las palabras clave](keyword-about.md)
>* [Administrar palabras clave de oferta](keyword-manage.md)
>* [Cambiar el estado de palabras clave y palabras clave negativas](keyword-status-edit.md)
