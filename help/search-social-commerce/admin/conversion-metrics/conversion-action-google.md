---
title: Crear una acción de conversión para una  [!DNL Google Ads] conversión mejorada para posibles clientes
description: Aprenda a crear una acción de conversión  [!DNL Google Ads] para una conversión mejorada para posibles clientes.
feature: Conversions
exl-id: faf4a6de-e82f-4afd-bda5-2602fb45aee5
TQID: https://experienceleague.adobe.com/KqFHgxjc-4snyo3nf-3-ry6nsyapMPcwKEWvgi-pxGc
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: f97a636a55c6cc823f0041e7acd6f48dca769a3e
workflow-type: tm+mt
source-wordcount: 876
ht-degree: 0%

---

# Crear una acción de conversión para una conversión mejorada de [!DNL Google Ads] para posibles clientes

*[!DNL Google Ads]solo cuentas*

Puede crear acciones de conversión para [!DNL Google Ads] conversiones mejoradas para posibles clientes que se rastrearán en cuentas individuales de [!DNL Google Ads], no en conversiones seguidas a nivel de cuenta de administrador.

Una vez que haya creado la acción de conversión e implementado una etiqueta de seguimiento de conversión, puede cargar los datos de conversión sin conexión que su organización captura y atribuirlos a la acción de conversión.

## (Nueva IU) Crear una acción de conversión

*característica de Beta*

1. En el menú principal, haga clic en **[!UICONTROL Goals]>[!UICONTROL Conversions]**.

1. Sobre la tabla de datos, haga clic en **[!UICONTROL Set up Conversion]**.

1. Especifique la [configuración de acción de conversión](#conversion-action-settings-google).

   1. Seleccione [!UICONTROL Setup Method] *[!UICONTROL Create Conversion]*.

   1. Seleccione la cuenta y, a continuación, seleccione el tipo de conversión: *[!UICONTROL Import conversion]*.

   1. Haga clic en **[!UICONTROL Next]**.

   1. Especifique las opciones de acción de conversión.

   1. Haga clic en **[!UICONTROL Review and Save]** para revisar la configuración.

   1. Haga clic en **[!UICONTROL Generate]**.

1. Lea información sobre cómo crear una etiqueta de seguimiento para la conversión mejorada de posibles clientes y haga clic en **[!UICONTROL Next]**.

   Debe crear la etiqueta de conversión e implementarla según sea necesario en los sitios web desde los que desea realizar un seguimiento de la métrica de conversión. También deberá habilitar conversiones mejoradas para posibles clientes y aceptar los términos y condiciones de los datos del cliente. Para obtener instrucciones, consulte las [!DNL Google Ads] instrucciones para &quot;[configurar la etiqueta [!DNL Google] para mejorar las conversiones de los posibles clientes](https://support.google.com/google-ads/answer/11021502)&quot;.

   Si desea rastrear valores de conversión específicos de transacción, [personalice el fragmento de evento](https://support.google.com/google-ads/answer/6095947).

1. Haga clic en **[!UICONTROL Close].**

### Configuración de acciones de conversión {#conversion-action-settings-google}

#### Sección Ruta de configuración

**[!UICONTROL Setup Method]:** El tipo de acción: *[!UICONTROL Create Conversion]*

**[!UICONTROL Platform]:** La red de anuncios: *[!UICONTROL Google]*.

#### Sección Detalles de conversión

**[!UICONTROL Select Account]:** La cuenta [!DNL Google Ads] aplicable.

**[!UICONTROL Type of conversions]:** Tipo de conversión para realizar el seguimiento: seleccione *[!UICONTROL Import conversion]*. Todos los demás tipos se utilizan para crear etiquetas de seguimiento de conversión (no acciones de conversión) para otros tipos de conversiones.

#### Configuración de conversión, sección

**[!UICONTROL Conversion Name]:** Un nombre único para la acción de conversión.

**[!UICONTROL Goal Category]:** La categoría de conversión, como *Cliente potencial calificado* o *Registro*.

**[!UICONTROL Preferred Action optimization]:** Si el objetivo es *[!UICONTROL Primary action used for bidding optimization]* o *[!UICONTROL Secondary action not used for bidding optimization]*.

**[!UICONTROL Conversion Value]:** Cómo medir el [valor de cada conversión](https://support.google.com/google-ads/answer/13064207):

* *[!UICONTROL Use the same value for each conversion],*, lo cual requiere que seleccione una moneda e introduzca el valor para cada conversión.

* *[!UICONTROL Use different values for each conversion],*, lo cual requiere que seleccione una moneda e introduzca un valor predeterminado para cada conversión. Puede cambiar el valor predeterminado en la etiqueta con un valor específico de la transacción al implementar la etiqueta en una página web específica.

* *[!UICONTROL Don't use a value for this conversion action (Not recommended)]*

**[!UICONTROL Count]:** [Cuántas conversiones se van a contar por clic o interacción](https://support.google.com/google-ads/answer/3438531): *[!UICONTROL Every (Recommended for every purchases because every purchase is valuable)]* o *[!UICONTROL One (Recommended for leads, sign-ups and other conversions for which only the first interaction is valuable)]*.

**[!UICONTROL Click-Through Conversion Window]:** Número máximo de días después de una interacción publicitaria para los que se registran conversiones. Para campañas de búsqueda, visualización y compra, la ventana puede durar entre 1 y 90 días. Seleccione un número o seleccione **[!UICONTROL Custom]** e introduzca un número.

**[!UICONTROL View-Through Conversion Window]:** Número máximo de días después de que un usuario vea los anuncios para los que se han registrado conversiones de visualización. Para campañas de búsqueda, visualización y compra, la ventana puede durar entre 1 y 90 días. Seleccione un número o seleccione **[!UICONTROL Custom]** e introduzca un número.

**[!UICONTROL Attribution Model]:** [Modelo de atribución que determina el crédito que recibe cada interacción de anuncio](https://support.google.com/google-ads/answer/6259715?sjid=8211249329930775138): *[!UICONTROL Data driven]* o *[!UICONTROL Last click]*.

## (IU heredada) Crear una acción de conversión

1. En el menú principal, haga clic en **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Admin] >[!UICONTROL Conversions]**, que abre la ficha **[!UICONTROL Summary]**.

1. En la barra de herramientas situada encima de la tabla de datos, haga clic en ![Crear](/help/search-social-commerce/assets/add.png "Crear").

1. Especifique la [configuración de acción de conversión](#conversion-action-settings-google-legacy).

   1. Seleccione la cuenta y, a continuación, seleccione el tipo de conversión: *[!UICONTROL Import conversion]*.

   1. Haga clic en **[!UICONTROL Next]**.

   1. Especifique las opciones de acción de conversión.

   1. Haga clic en **[!UICONTROL Generate]**.

1. Lea información sobre cómo crear una etiqueta de seguimiento para la conversión mejorada de posibles clientes y haga clic en **[!UICONTROL Next]**.

   Cree la etiqueta de conversión e impleméntelo según sea necesario en los sitios web desde los que desee rastrear la métrica de conversión. Para obtener instrucciones, consulte lo siguiente:

   * Para usar la etiqueta [!DNL Google], consulte las instrucciones de [!DNL Google Ads] para &quot;Configurar la configuración de la etiqueta [!DNL Google]&quot; en &quot;[Configurar conversiones mejoradas para posibles clientes con la etiqueta  [!DNL Google] tag](https://support.google.com/google-ads/answer/11347292)&quot;.&quot;

   * Para usar [!DNL Google Tag Manager], consulte las instrucciones de [!DNL Google Ads] para &quot;Configurar la configuración de etiquetas de [!DNL Google]&quot; y &quot;Verificar la configuración y publicar el contenedor&quot; en &quot;[Configurar conversiones mejoradas para posibles clientes con [!DNL Google Tag Manager]](https://support.google.com/google-ads/answer/11021502?#configure)&quot;.

1. Haga clic en **[!UICONTROL Done].**

### Configuración de acciones de conversión {#conversion-action-settings-google-legacy}

**[!UICONTROL Select an Account]:** La cuenta [!DNL Google Ads] aplicable.

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
