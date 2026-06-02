---
title: (Nueva interfaz de usuario) Crear una acción de conversión para una  [!DNL Google Ads] conversión mejorada para posibles clientes
description: Aprenda a crear una acción de conversión  [!DNL Google Ads] para una conversión mejorada para posibles clientes.
feature: Conversions
feature_v2: id: aed5e38a-3e62-42fa-8d16-cd080729b2a0id: e6916c1b-e939-4e0b-99f5-768e83e1e99f
subfeature_v2: id: d068b149-b9d1-421c-9033-a51495366ddc
source-git-commit: 0bfee2b52410b5cab8e9b3dfba35effc36fc40e1
workflow-type: tm+mt
source-wordcount: 510
ht-degree: 0%

---

# (Nueva interfaz de usuario) Crear una acción de conversión para una conversión mejorada de [!DNL Google Ads] para posibles clientes

*característica de Beta*

*[!DNL Google Ads]solo cuentas*

Puede crear acciones de conversión para [!DNL Google Ads] conversiones mejoradas para posibles clientes que se rastrearán en cuentas individuales de [!DNL Google Ads], no en conversiones seguidas a nivel de cuenta de administrador.

Una vez que hayas creado la acción de conversión y hayas implementado una etiqueta de seguimiento de conversión, puedes [cargar los datos de conversión sin conexión que tu organización haya capturado](conversions-upload-offline-enhanced-conversions.md) y atribuirlos a la acción de conversión.

La compatibilidad no está disponible para las cuentas de [!DNL Microsoft Advertising].

## Crear una acción de conversión

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

## Configuración de acciones de conversión {#conversion-action-settings-google}

### Sección Ruta de configuración

**[!UICONTROL Setup Method]:** El tipo de acción: *[!UICONTROL Create Conversion]*

**[!UICONTROL Platform]:** La red de anuncios: *[!UICONTROL Google]*.

### Sección Detalles de conversión

**[!UICONTROL Select Account]:** La cuenta [!DNL Google Ads] aplicable.

**[!UICONTROL Type of conversions]:** Tipo de conversión para realizar el seguimiento: seleccione *[!UICONTROL Import conversion]*. Todos los demás tipos se utilizan para crear etiquetas de seguimiento de conversión (no acciones de conversión) para otros tipos de conversiones.

### Configuración de conversión, sección

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

>[!MORELIKETHIS]
>
>* [(Nueva IU) Cargar datos de conversión sin conexión para conversiones mejoradas](/help/search-social-commerce/admin/conversion-metrics/upload-data-offline-conversions.md)
>* [Cargar datos de conversión sin conexión para conversiones mejoradas](/help/search-social-commerce/admin/conversion-metrics/upload-data-offline-conversions.md)
>* [Implementar [!DNL Google Ads] conversiones mejoradas para posibles clientes](/help/search-social-commerce/campaign-management/special-workflows/google-enhanced-conversions-leads.md)
