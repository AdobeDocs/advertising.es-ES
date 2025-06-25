---
title: Crear una acción de conversión para una  [!DNL Google Ads] conversión mejorada para posibles clientes
description: Aprenda a crear una acción de conversión  [!DNL Google Ads] para una conversión mejorada para posibles clientes.
feature: Conversions
exl-id: faf4a6de-e82f-4afd-bda5-2602fb45aee5
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '459'
ht-degree: 0%

---

# Crear una acción de conversión para una conversión mejorada de [!DNL Google Ads] para posibles clientes

*[!DNL Google Ads]solo cuentas*

Puede crear acciones de conversión para [!DNL Google Ads] conversiones mejoradas para posibles clientes que se rastrearán en cuentas individuales de [!DNL Google Ads], no en conversiones seguidas a nivel de cuenta de administrador.

1. En el menú principal, haga clic en **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Admin] >[!UICONTROL Conversions]**, que abre la ficha **[!UICONTROL Summary]**.

1. En la barra de herramientas situada encima de la tabla de datos, haga clic en ![Crear](/help/search-social-commerce/assets/add.png "Crear").

1. Especifique la [configuración de acción de conversión](#conversion-action-settings-google).

   1. Seleccione la cuenta y, a continuación, seleccione el tipo de conversión: *[!UICONTROL Import conversion]*.

   1. Haga clic en **[!UICONTROL Next]**.

   1. Especifique las opciones de acción de conversión.

   1. Haga clic en **[!UICONTROL Generate]**.

1. Lea información sobre cómo crear una etiqueta de seguimiento para la conversión mejorada de posibles clientes y haga clic en **[!UICONTROL Next]**.

   Cree la etiqueta de conversión e impleméntelo según sea necesario en los sitios web desde los que desee rastrear la métrica de conversión. Para obtener instrucciones, consulte lo siguiente:

   * Para usar la etiqueta [!DNL Google], consulte las instrucciones de [!DNL Google Ads] para &quot;Configurar la configuración de la etiqueta [!DNL Google]&quot; en &quot;[Configurar conversiones mejoradas para posibles clientes con la etiqueta  [!DNL Google] tag](https://support.google.com/google-ads/answer/11347292)&quot;.&quot;

   * Para usar [!DNL Google Tag Manager], consulte las instrucciones de [!DNL Google Ads] para &quot;Configurar la configuración de etiquetas de [!DNL Google]&quot; y &quot;Verificar la configuración y publicar el contenedor&quot; en &quot;[Configurar conversiones mejoradas para posibles clientes con [!DNL Google Tag Manager]](https://support.google.com/google-ads/answer/11021502?#configure)&quot;.

1. Haga clic en **[!UICONTROL Done].**

Una vez que haya creado la acción de conversión e implementado una etiqueta de seguimiento de conversión, puede cargar los datos de conversión sin conexión que su organización captura y atribuirlos a la acción de conversión. Consulte &quot;[Cargar datos de conversión sin conexión para obtener conversiones mejoradas](/help/search-social-commerce/admin/conversion-metrics/upload-data-offline-conversions.md)&quot;.

## Configuración de acciones de conversión {#conversion-action-settings-google}

**[!UICONTROL Select an Account]:** La cuenta de Google Ads aplicable.

**[!UICONTROL Type of Conversion]:** Tipo de conversión para realizar el seguimiento: seleccione *[!UICONTROL Import conversion]*. Todos los demás tipos se utilizan para crear etiquetas de seguimiento de conversión (no acciones de conversión) para otros tipos de conversiones.

**[!UICONTROL Conversion Name]:** Un nombre único para la acción de conversión.

**\[Categoría de conversión\]:** La categoría de conversión, como *Cliente potencial cualificado* o *Registro*.

**\[Tipo de acción\]:** Si el objetivo es *[!UICONTROL Primary action used for bidding optimization]* o *[!UICONTROL Secondary action not used for bidding optimization]*.

**[!UICONTROL Value]:** Cómo medir el [valor de cada conversión](https://support.google.com/google-ads/answer/13064207):

* *[!UICONTROL Use the same value for each conversion],*, lo cual requiere que seleccione una moneda e introduzca el valor para cada conversión.

* *[!UICONTROL Use a different value for each conversion],*, lo cual requiere que seleccione una moneda e introduzca un valor predeterminado para cada conversión. Puede cambiar el valor predeterminado en la etiqueta con un valor específico de la transacción al implementar la etiqueta en una página web específica.

* *[!UICONTROL Don't use a value for this conversion action (Not recommended)]*

**[!UICONTROL Count]:** [Cuántas conversiones se van a contar por clic o interacción](https://support.google.com/google-ads/answer/3438531): *[!UICONTROL Every (Recommended for every purchases because every purchase is valuable)]* o *[!UICONTROL One (Recommended for leads, sign-ups and other conversions because only the first interaction is valuable)]*.

**[!UICONTROL Click Through Conversion Window]:** Número máximo de días después de una interacción publicitaria para los que se registran conversiones. Para campañas de búsqueda, visualización y compra, la ventana puede durar entre 1 y 90 días. Seleccione un número o seleccione **[!UICONTROL Custom]** e introduzca un número.

**[!UICONTROL View Through Conversion Window]:** Número máximo de días después de que un usuario vea los anuncios para los que se han registrado conversiones de visualización. Para campañas de búsqueda, visualización y compra, la ventana puede durar entre 1 y 90 días. Seleccione un número o seleccione **[!UICONTROL Custom]** e introduzca un número.

**[!UICONTROL Attribution Model]:** [Cuánto crédito recibe cada interacción de publicidad](https://support.google.com/google-ads/answer/6259715?sjid=8211249329930775138): *[!UICONTROL Data driven]* o *[!UICONTROL Last click]*.

>[!MORELIKETHIS]
>
>* [Cargar datos de conversión sin conexión para conversiones mejoradas](/help/search-social-commerce/admin/conversion-metrics/upload-data-offline-conversions.md)
>* [Implementar [!DNL Google Ads] conversiones mejoradas para posibles clientes](/help/search-social-commerce/campaign-management/special-workflows/google-enhanced-conversions-leads.md)
