---
title: Crear una etiqueta de conversión para  [!DNL Google Ads]
description: Aprenda a crear una etiqueta de conversión  [!DNL Google Ads] .
feature: Conversions
exl-id: 214611f0-bd38-499e-a7de-3a5878995fb5
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '415'
ht-degree: 0%

---

# Crear una etiqueta de conversión para [!DNL Google Ads]

Puede crear etiquetas de conversión para las nuevas conversiones que se seguirán para cuentas individuales de [!DNL Google Ads], no para las que se seguirán a nivel de cuenta de administrador.

Para generar etiquetas de conversión para las conversiones existentes, utilice el editor de la red de publicidad.

1. En el menú principal, haga clic en **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Admin] >[!UICONTROL Conversions]**, que se abre en la ficha **[!UICONTROL Summary]**.

1. En la barra de herramientas situada encima de la tabla de datos, haga clic en ![Crear](/help/search-social-commerce/assets/add.png "Crear").

1. Especifique la [configuración de la etiqueta de conversión](#conversion-tag-settings-google).

   1. Seleccione la cuenta y, a continuación, el tipo de conversión.

   1. Haga clic en **[!UICONTROL Next]**.

   1. Especifique las opciones de conversión.

   1. Haga clic en **[!UICONTROL Generate]**.

1. Copie la etiqueta de conversión e impleméntelo en los sitios web desde los que desee rastrear la métrica de conversión.

   Consulte &quot;Instalación de la etiqueta [!DNL Google]&quot; en la ayuda de [!DNL Google Ads] para &quot;[2. Configure su etiqueta Google &#x200B;](https://support.google.com/google-ads/answer/12215519)&quot;.

1. Haga clic en **[!UICONTROL Done].**

Una vez que agregue las etiquetas al sitio web y comiencen a activarse, [!DNL Google Ads] registra las conversiones en el sitio web. Search, Social y Commerce sincronizan las conversiones diariamente. Para obtener más información sobre los datos sincronizados, consulte &quot;[[!DNL Google Ads] datos de conversión en Search, Social y Commerce](/help/search-social-commerce/campaign-management/introduction/google-conversion-data.md).

## Configuración de etiquetas de conversión {#conversion-tag-settings-google}

**[!UICONTROL Select an Account]:** La cuenta de Google Ads aplicable.

**[!UICONTROL Type of Conversion]:** Tipo de conversión para realizar el seguimiento: *[!UICONTROL Click on a webpage element]*, *[!UICONTROL Calls to a phone number on your website]* o *[!UICONTROL Clicks to your number on your mobile website]*. **Nota:** *[!UICONTROL Import conversion]* se usa para un propósito diferente; consulte &quot;[Crear una acción de conversión para una  [!DNL Google Ads] conversión mejorada para posibles clientes](/help/search-social-commerce/admin/conversion-metrics/conversion-action-google.md)&quot;.

**[!UICONTROL Conversion Name]:** Un nombre único para la métrica de conversión.

**\[Categoría de conversión\]:** La categoría de conversión. Las categorías disponibles varían según el tipo de conversión. Para *[!UICONTROL Calls to a phone number on your website]* y *[!UICONTROL Clicks to your number on your mobile website]*, &quot;[!UICONTROL Phone Call Lead]&quot; está seleccionado de manera predeterminada.

**\[Tipo de acción\]:** Si el objetivo es *[!UICONTROL Primary action used for bidding optimization]* o *[!UICONTROL Secondary action not used for bidding optimization]*.

**[!UICONTROL Value]:** Cómo medir el [valor de cada conversión](https://support.google.com/google-ads/answer/3419241):

* *[!UICONTROL Use the same value for each conversion],*, lo cual requiere que seleccione una moneda e introduzca el valor para cada conversión.

* *[!UICONTROL Use a different value for each conversion],*, lo cual requiere que seleccione una moneda e introduzca un valor predeterminado para cada conversión. Puede cambiar el valor predeterminado en la etiqueta con un valor específico de la transacción al implementar la etiqueta en una página web específica.

* *[!UICONTROL Don't use a value for this conversion action (Not recommended)]*

**[!UICONTROL Count]:** [Cuántas conversiones se van a contar por clic o interacción](https://support.google.com/google-ads/answer/3438531): *[!UICONTROL Every (Recommended for every purchases because every purchase is valuable)]* o *[!UICONTROL One (Recommended for leads, sign-ups and other conversions because only the first interaction is valuable)]*.

**[!UICONTROL Click Through Conversion Window]:** Número máximo de días después de una interacción publicitaria para los que se registran conversiones. Para campañas de búsqueda, visualización y compra, la ventana puede durar entre 1 y 90 días. Seleccione un número o seleccione **[!UICONTROL Custom]** e introduzca un número.

**[!UICONTROL View Through Conversion Window]:** Número máximo de días después de que un usuario vea los anuncios para los que se han registrado conversiones de visualización. Para campañas de búsqueda, visualización y compra, la ventana puede durar entre 1 y 90 días. Seleccione un número o seleccione **[!UICONTROL Custom]** e introduzca un número.

**[!UICONTROL Attribution Model]:** [Cuánto crédito recibe cada interacción de publicidad](https://support.google.com/google-ads/answer/6259715?sjid=8211249329930775138): *[!UICONTROL Data driven]* o *[!UICONTROL Last click]*. **Nota:** Las acciones de conversión que antes usaban los modelos *[!UICONTROL First click]*, *[!UICONTROL Linear]*, *[!UICONTROL Time decay]* o *[!UICONTROL Position based]*, que ahora no son compatibles, ahora usan el modelo *[!UICONTROL Data driven]*.

>[!MORELIKETHIS]
>
>* [Cargar datos de conversión sin conexión para conversiones mejoradas](/help/search-social-commerce/admin/conversion-metrics/upload-data-offline-conversions.md)
>* [[!DNL Google Ads] datos de conversión en Search, Social y Commerce](/help/search-social-commerce/campaign-management/introduction/google-conversion-data.md)
