---
title: Cree una etiqueta de conversión para [!DNL Google Ads]
description: Obtenga información sobre cómo crear un [!DNL Google Ads] etiqueta de conversión.
feature: Conversions
source-git-commit: 8f08151013ec63df14843733a0c83badcceba4c3
workflow-type: tm+mt
source-wordcount: '379'
ht-degree: 0%

---

# Cree una etiqueta de conversión para [!DNL Google Ads]

Puede crear etiquetas de conversión para nuevas conversiones de las que realizar un seguimiento individual [!DNL Google Ads] cuentas, sin seguimiento a nivel de cuenta de responsable.

Para generar etiquetas de conversión para las conversiones existentes, utilice el editor de la red de publicidad.

1. En el menú principal, haga clic en **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Conversions]**.

1. En la barra de herramientas sobre la tabla de datos, haga clic en ![Crear](/help/search-social-commerce/assets/add.png "Crear").

1. Especifique el [configuración de etiquetas de conversión](#conversion-tag-settings-google).

   1. Seleccione la cuenta y, a continuación, el tipo de conversión.

   1. Haga clic **[!UICONTROL Next]**.

   1. Especifique las opciones de conversión.

   1. Haga clic **[!UICONTROL Generate]**.

1. Copie la etiqueta de conversión e impleméntelo en los sitios web desde los que desee rastrear la métrica de conversión.

   Consulte &quot;Instalación de&quot; [!DNL Google] &quot; en el [!DNL Google Ads] ayuda para &quot;[2. Configurar la etiqueta de Google](https://support.google.com/google-ads/answer/12215519).&quot;

1. Haga clic **[!UICONTROL Done].**

Una vez que añada las etiquetas a su sitio web y comiencen a activarse, [!DNL Google Ads] registra las conversiones en el sitio web. Search, Social y Commerce sincronizan las conversiones diariamente. Para obtener más información sobre los datos sincronizados, consulte &quot;[[!DNL Google Ads] datos de conversión en Search, Social y Commerce](/help/search-social-commerce/campaign-management/introduction/google-conversion-data.md).

## Configuración de etiquetas de conversión {#conversion-tag-settings-google}

**[!UICONTROL Select an Account]:** La cuenta de Google Ads aplicable.

**[!UICONTROL Type of Conversion]:** El tipo de conversión que se va a rastrear: *[!UICONTROL Click on a webpage element]*, *[!UICONTROL Calls to a phone number on your website]*, o *[!UICONTROL Clicks to your number on your mobile website]*.

**[!UICONTROL Conversion Name]:** Un nombre único para la métrica de conversión.

**\[Categoría de objetivo\]:** La categoría de conversión. Las categorías disponibles varían según el tipo de conversión. Para *[!UICONTROL Calls to a phone number on your website]* y *[!UICONTROL Clicks to your number on your mobile website]*, &quot;[!UICONTROL Phone Call Lead]&quot; está seleccionado de forma predeterminada.

**\[Tipo de acción\]:** Si el objetivo es un *[!UICONTROL Primary action used for bidding optimization]* o una *[!UICONTROL Secondary action not used for bidding optimization]*.

**[!UICONTROL Value]:** Cómo medir el [valor de cada conversión](https://support.google.com/google-ads/answer/3419241):

* *[!UICONTROL Use the same value for each conversion],* que requiere que seleccione una moneda e introduzca el valor para cada conversión.

* *[!UICONTROL Use a different value for each conversion],* lo que requiere que seleccione una moneda e introduzca un valor predeterminado para cada conversión. Puede cambiar el valor predeterminado en la etiqueta con un valor específico de la transacción al implementar la etiqueta en una página web específica.

* *[!UICONTROL Don't use a value for this conversion action (Not recommended)]*

**[!UICONTROL Count]:** [Cuántas conversiones se cuentan por clic o interacción](https://support.google.com/google-ads/answer/3438531): *[!UICONTROL Every (Recommended for every purchases because every purchase is valuable)]* o *[!UICONTROL One (Recommended for leads, sign-ups and other conversions because only the first interaction is valuable)]*.

**[!UICONTROL Click Through Conversion Window]:** Número máximo de días después de una interacción publicitaria para los que se registran conversiones. Para campañas de búsqueda, visualización y compra, la ventana puede durar entre 1 y 90 días. Seleccione un número o seleccione **[!UICONTROL Custom]** e introduzca un número.

**[!UICONTROL View Through Conversion Window]:** La cantidad máxima de días después de que un usuario vea los anuncios para los que se registran conversiones de visualización. Para campañas de búsqueda, visualización y compra, la ventana puede durar entre 1 y 90 días. Seleccione un número o seleccione **[!UICONTROL Custom]** e introduzca un número.

**[!UICONTROL Attribution Model]:** [Cuánto crédito recibe cada interacción de publicidad](https://support.google.com/google-ads/answer/6259715?sjid=8211249329930775138): *[!UICONTROL Data driven]*, *[!UICONTROL Last click]*, *[!UICONTROL First click]*, *[!UICONTROL Linear]*, *[!UICONTROL Time decay]*, o *[!UICONTROL Position based]*.

>[!MORELIKETHIS]
>
>* [[!DNL Google Ads] datos de conversión en Search, Social y Commerce](/help/search-social-commerce/campaign-management/introduction/google-conversion-data.md)
