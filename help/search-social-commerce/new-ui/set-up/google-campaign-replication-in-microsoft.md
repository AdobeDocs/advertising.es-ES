---
title: (Nueva IU) Replicar campañas de Google Ads en Microsoft Advertising
description: Obtenga información sobre cómo exportar las campañas sincronizadas en una cuenta de Google Ads directamente a una cuenta sincronizada de Advertising de Microsoft.
feature: Search Campaign Management
exl-id: d4f8e452-7b3d-4a1f-9c3e-6b8d2e5a4917
source-git-commit: 3f769f18ce006278b12a62f8d837d60affffda65
workflow-type: tm+mt
source-wordcount: '1047'
ht-degree: 0%

---

# (Nueva interfaz de usuario) Replicar [!DNL Google Ads] campañas en [!DNL Microsoft Advertising]

*característica de Beta*

Puede exportar sus campañas sincronizadas en una cuenta de [!DNL Google Ads] directamente a una cuenta sincronizada de [!DNL Microsoft Advertising] como campañas CPC (eCPC) mejoradas. Se escalan las ofertas y los presupuestos de campaña existentes. El seguimiento existente de búsqueda, medios sociales y Commerce no se importa.

Puede replicar los siguientes tipos de campañas y su estructura:

* [!DNL Google Ads] buscar y mostrar campañas en [!DNL Microsoft Advertising] buscar y mostrar campañas.

* [!DNL Google Display Network] campañas, incluidas imágenes de anuncios, en [!DNL Microsoft Advertising] campañas de audiencia en Microsoft Audience Network.

  Si desea replicar las campañas de visualización basadas en fuentes de compras, primero debe replicar las ofertas de producto de [!DNL Google Merchant Center] a [!DNL Microsoft Merchant Center]. Cuando duplique las campañas, seleccione el almacén de [!DNL Microsoft Merchant Center] en las opciones de importación para vincular el almacén a las campañas de audiencia basadas en fuentes.

* [!DNL Google Ads] campañas de rendimiento máximo, incluidos los anuncios de inventario local, en [!DNL Microsoft Advertising] campañas de rendimiento máximo.

Puede elegir actualizar las campañas una vez; diariamente, semanalmente o mensualmente; o según la programación recomendada de [!DNL Microsoft Advertising]. Si lo desea, puede configurar las notificaciones cada vez que se ejecute un trabajo de importación o cuando se produzcan errores o cambios. Una vez importadas las campañas en [!DNL Microsoft Advertising], puede comprobar el estado del trabajo de importación, revisar los registros de errores, ejecutar manualmente un trabajo de importación y editar, pausar, habilitar o eliminar la programación de importación.

No toda la información de la campaña está duplicada y es posible que tenga que agregar información a sus [!DNL Microsoft Advertising] campañas. Para obtener más información sobre los datos que se importan, consulte la ayuda de [!DNL Microsoft Advertising] en &quot;[Qué se importa desde [!DNL Google Ads]](https://help.ads.microsoft.com/#apex/ads/en/50851){target="_blank"}&quot;. Dado que el seguimiento de Search, Social y Commerce no se ha importado, también debería agregar seguimiento a la configuración de [account](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md), [campaign](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md), [ad group](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md) o [ad](/help/search-social-commerce/campaign-management/campaigns/ad-manage.md).

## Replicar [!DNL Google Ads] campañas

>[!NOTE]
>
>Si quieres replicar campañas de visualización basadas en fuentes de compras, primero [replica tus [!DNL Google Merchant Center] ofertas de productos en [!DNL Microsoft Merchant Center]](https://help.ads.microsoft.com/apex/index/3/en/56870){target="_blank"}. Cuando duplique las campañas, seleccione el almacén de [!DNL Microsoft Merchant Center] en las opciones de importación para vincular el almacén a las campañas de audiencia basadas en fuentes.

Ver [lo importado de [!DNL Google Ads] campañas](https://help.ads.microsoft.com/#apex/ads/en/50851/0-500){target="_blank"}.

1. En el menú principal, haga clic en **[!UICONTROL Setup]** \> **[!UICONTROL Import Campaigns]**.

1. Haga clic en **[!UICONTROL Import Campaigns]**.

1. Especifique la [configuración de importación](#campaign-import-settings):

   1. En el paso **[!UICONTROL Select accounts]**:

      1. Escriba un nombre para el trabajo de importación en el campo **[!UICONTROL Import Name]**.

      1. Seleccione la cuenta de origen [!DNL Google Ads] y la cuenta de destino [!DNL Microsoft Advertising].

      1. Escriba su **[!UICONTROL Credential ID]**. Póngase en contacto con el equipo de su cuenta de Adobe si no tiene un ID de credencial; la generación automática no está disponible debido a las limitaciones de [!DNL Microsoft Advertising].

      1. Haga clic en **[!UICONTROL Next]**.

   1. En el paso **[!UICONTROL Select campaigns & ad groups]**, especifique las campañas y los grupos de anuncios que desea importar y, a continuación, haga clic en **[!UICONTROL Next]**.

   1. En el paso **[!UICONTROL Customize your import]**, si lo desea, especifique los tipos de elementos, la configuración de ofertas y presupuestos y otras opciones que desea importar y, a continuación, haga clic en **[!UICONTROL Next]**.

   1. En el paso **[!UICONTROL Set schedule]**, especifique cuándo ejecutar el trabajo de importación y cómo recibir notificaciones.

1. Revise sus selecciones en el resumen y haga clic en **[!UICONTROL Start Import]**.

1. (Opcional) Agregue el seguimiento de búsqueda, medios sociales y Commerce en la configuración de [cuenta](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md), [campaña](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md), [grupo de anuncios](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md) o [anuncio](/help/search-social-commerce/campaign-management/campaigns/ad-manage.md).

## Editar la configuración de programación de un trabajo de importación de campañas

Ver [lo importado de [!DNL Google Ads] campañas](https://help.ads.microsoft.com/#apex/ads/en/50851/0-500){target="_blank"}.

1. En el menú principal, haga clic en **[!UICONTROL Setup]** \> **[!UICONTROL Import Campaigns]**.

1. Haga clic en la ficha **[!UICONTROL Jobs]**.

1. Haga clic en el nombre del trabajo de importación y luego haga clic en **[!UICONTROL Edit]**.

1. En el paso **[!UICONTROL Set schedule]**, especifique la [configuración de programación](#campaign-import-settings).

1. Haga clic en **[!UICONTROL Save]**.

## Ver los trabajos de importación de campañas

Puede enumerar todos los trabajos de importación, incluida la cuenta de origen [!DNL Google Ads], la cuenta de destino [!DNL Microsoft Advertising], la hora o programación de importación y el usuario que creó el trabajo. Cuando se ejecuta un trabajo de importación varias veces, incluso durante importaciones programadas regularmente, cada incidencia se muestra como un trabajo independiente.

1. En el menú principal, haga clic en **[!UICONTROL Setup]** \> **[!UICONTROL Import Campaigns]**.

   La vista se abre en la ficha **[!UICONTROL Jobs]** de forma predeterminada.

## Ejecutar un trabajo de importación de campaña

1. En el menú principal, haga clic en **[!UICONTROL Setup]** \> **[!UICONTROL Import Campaigns]**.

1. Haga clic en la ficha **[!UICONTROL Jobs]**.

1. Seleccione la casilla de verificación que hay junto al trabajo de importación y haga clic en **[!UICONTROL Run Now]**.

## Visualización de registros de los trabajos de importación de la campaña {#campaign-import-log}

Puede enumerar todos los trabajos de importación completados o fallidos, incluida la hora de inicio, la cuenta de origen [!DNL Google Ads], la cuenta de destino [!DNL Microsoft Advertising], el usuario que creó el trabajo, el número de operaciones correctas y fallidas y cualquier dirección de correo electrónico que recibió notificaciones para cada trabajo. Puede ver más detalles sobre los cambios realizados en la cuenta de destino [!DNL Microsoft Advertising] para cada trabajo, incluido el número de elementos agregados, sincronizados, eliminados y que produjeron errores para cada nivel de entidad (como campaña o palabra clave) en la cuenta.

1. En el menú principal, haga clic en **[!UICONTROL Setup]** \> **[!UICONTROL Import Campaigns]**.

1. Haga clic en la ficha **[!UICONTROL Logs]**.

1. (Opcional) Para ver los detalles de cualquier trabajo de importación, haga clic en el valor de la columna [!UICONTROL Summary].

## Configuración del trabajo de importación de Campaign {#campaign-import-settings}

### [!UICONTROL Select accounts]

**[!UICONTROL Import Name]:** Un nombre para identificar el trabajo de importación.

**[!UICONTROL Source Google Ads account]:** Cuenta sincronizada [!DNL Google Ads] desde la que se exportan los datos de la campaña.

**[!UICONTROL Target Microsoft Ads account]:** Cuenta sincronizada de [!DNL Microsoft Advertising] en la que se importan los datos de campaña.

**[!UICONTROL Credential ID]:** Identificador que [!DNL Microsoft Advertising] usa para representar sus credenciales de [!DNL Google Ads]. La generación automática de credenciales de [!DNL Microsoft Advertising] para la importación no está disponible debido a las limitaciones de [!DNL Microsoft Advertising]. Póngase en contacto con el equipo de cuenta de Adobe para que le proporcione las credenciales y el ID.

### [!UICONTROL Select campaigns & ad groups]

**\[Datos para importar\]:** Los datos para importar:

* *[!UICONTROL Import all new and existing campaigns]:* Para importar los datos de todas las campañas que ya existen y las que no existen en [!DNL Microsoft Advertising].

* *[!UICONTROL Import specific campaigns and adgroups]:* Para seleccionar campañas y grupos de anuncios específicos.

   * Para expandir una campaña a sus grupos de anuncios secundarios, haga clic en **[!UICONTROL >]** después del nombre de la campaña.

   * Para seleccionar una campaña o un grupo de anuncios, seleccione el elemento para que aparezca una marca de verificación.

   * Para quitar una campaña o un grupo de anuncios, anule la selección del elemento o haga clic en el icono Eliminar de la columna [!UICONTROL Selected].

### [!UICONTROL Customize your import]

**[!UICONTROL Choose specific import options]:** Permite especificar qué importar, pujas y presupuestos, y otras opciones.

**[!UICONTROL What to import]:** Define los elementos que se van a importar. Las opciones para importar categorías de elementos están seleccionadas de forma predeterminada, con todos los tipos de elementos seleccionados. Para incluir solo tipos de elementos específicos, haga clic en **[!UICONTROL Show advanced options]** y cambie los tipos de elementos que desea incluir. Si lo desea, también puede asociar un ID de etiqueta de UET con cualquier lista de remarketing o audiencia que no se haya importado previamente a [!DNL Microsoft Advertising].

**[!UICONTROL Bids and budgets]:** Define qué configuración de oferta y presupuesto se va a importar, actualizar y personalizar, incluidas las opciones para aumentar o disminuir las ofertas y los presupuestos en un porcentaje especificado para [!DNL Microsoft Advertising].

**[!UICONTROL Other options]:** define cómo administrar las direcciones URL de la página de aterrizaje importada, las plantillas de seguimiento y otras opciones de campaña, publicidad y segmentación, incluidas las opciones para buscar y reemplazar texto e insertar sufijos.

### [!UICONTROL Set schedule]

**[!UICONTROL When]:** Cuándo importar las campañas especificadas: *Automático* (para permitir que [!DNL Microsoft Advertising] establezca una programación para optimizar mejor sus campañas), *[!UICONTROL Now]* (para ejecutar el trabajo cuando publique la configuración del trabajo), *[!UICONTROL Once]* a una hora especificada, *[!UICONTROL Daily]* a una hora especificada, *[!UICONTROL Weekly]* a una hora especificada o *[!UICONTROL Monthly]* a una hora especificada.

**[!UICONTROL Receive email notifications]:** Indica si se enviarán notificaciones por correo electrónico sobre trabajos de importación a las direcciones del campo [!UICONTROL Send reports to] y cuándo hacerlo: *[!UICONTROL No emails]*, *[!UICONTROL Only if there are changes or errors]* (valor predeterminado), *[!UICONTROL Only if there are errors]* o *[!UICONTROL Every time this import runs]*.

**[!UICONTROL Send reports to]:** Direcciones de correo electrónico para recibir notificaciones sobre trabajos de importación. Separe las direcciones con comas (`,`).

>[!MORELIKETHIS]
>
>* [Administrar cuentas de red de anuncios](/help/search-social-commerce/new-ui/set-up/accounts/api-accounts/api-account-manage.md)
