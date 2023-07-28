---
title: Replicar [!DNL Google Ads] campañas en [!DNL Microsoft® Advertising]
description: Obtenga información sobre cómo exportar las campañas sincronizadas en una [!DNL Google Ads] cuenta directamente en un [!DNL Microsoft® Advertising] cuenta.
exl-id: 1bb0d915-bf33-4c50-88a5-268d4de5ccff
feature: Search Tools
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '962'
ht-degree: 0%

---

# Replicar [!DNL Google Ads] campañas en [!DNL Microsoft® Advertising]

Puede exportar las campañas sincronizadas en un [!DNL Google Ads] cuenta directamente en un [!DNL Microsoft® Advertising] cuenta como campañas CPC mejoradas (eCPC). Se escalan las ofertas y los presupuestos de campaña existentes. El seguimiento existente de búsqueda, medios sociales y comercio no se importa.

Puede replicar los siguientes tipos de campañas y su estructura:

* [!DNL Google Ads] buscar y mostrar campañas en [!DNL Microsoft® Advertising] buscar y mostrar campañas.

* [!DNL Google Display Network] campañas de, incluidas imágenes de publicidad, en [!DNL Microsoft® Advertising] campañas de audiencia en Microsoft® Audience Network.

  Si desea duplicar las campañas de visualización basadas en fuentes de compras, primero debe duplicar la [!DNL Google Merchant Center] ofertas de productos a [!DNL Microsoft® Merchant Center]. Cuando duplique las campañas, seleccione la opción [!DNL Microsoft® Merchant Center] almacene en las Opciones de importación para vincular la tienda a las campañas de audiencia basadas en fuentes.

* [!DNL Google Ads] campañas de rendimiento máximo de, incluidos los anuncios de inventario local, en [!DNL Microsoft® Advertising] campañas de compras inteligentes.

Puede elegir actualizar las campañas una vez, diariamente, semanalmente o mensualmente, o según lo siguiente [!DNL Microsoft® Advertising]El horario recomendado de. Si lo desea, puede configurar las notificaciones cada vez que se ejecute un trabajo de importación o cuando se produzcan errores o cambios. Una vez importadas las campañas en [!DNL Microsoft® Advertising], puede comprobar el estado del trabajo de importación, revisar los registros de errores, ejecutar manualmente un trabajo de importación y editar, pausar, habilitar o eliminar la programación de importación.

No toda la información de la campaña se duplica y es posible que tenga que agregar información a su [!DNL Microsoft® Advertising] campañas. Para obtener más información sobre los datos importados, consulte [!DNL Microsoft® Advertising] ayuda sobre &quot;[Qué se importa desde [!DNL Google Ads]](https://help.ads.microsoft.com/#apex/ads/en/50851).&quot; Dado que el seguimiento de búsqueda, social y comercial no se importa, también debe agregar seguimiento dentro de la variable [account](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md), [campaña](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md), [grupo de publicidad](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md), o [anuncio](/help/search-social-commerce/campaign-management/campaigns/ad-manage.md) configuración.

## Replicar [!DNL Google Ads] campañas

>[!NOTE]
>
>Si desea duplicar las campañas de visualización basadas en fuentes de compras, primero debe hacer lo siguiente [replique su [!DNL Google Merchant Center] ofertas de productos en [!DNL Microsoft® Merchant Center]](https://help.ads.microsoft.com/apex/index/3/en/56870). Cuando duplique las campañas, seleccione la opción [!DNL Microsoft® Merchant Center] almacene en las opciones de importación para vincular la tienda a las campañas de audiencia basadas en fuentes.

Consulte [de qué se importa [!DNL Google Ads] campañas](https://help.ads.microsoft.com/#apex/ads/en/50851/0-500).

1. En el menú principal Buscar, Social y Comercio, haga clic en **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Import Campaigns]**.

1. Haga clic **[!UICONTROL +Import]**.

1. Especifique el [importar configuración](#campaign-import-settings):

   1. En el **[!UICONTROL Select accounts]** sección:

      1. Seleccione las cuentas de origen y destino.

      1. Haga clic **[!UICONTROL Get Credential Id from MSA]**.

      1. Inicie sesión en el destino [!DNL Microsoft Advertising] cuenta, copie el ID de credencial que se muestra y pegue el valor en la variable **[!UICONTROL Credential ID]** field.

   1. En el **[!UICONTROL Select campaigns & ad groups]** , especifique las campañas y los grupos de anuncios que desea importar.

   1. En el **[!UICONTROL Customize your import]** , especifique los tipos de elementos que desea importar.

   1. En el **[!UICONTROL Set schedule]** , especifique cuándo ejecutar el trabajo de importación.

1. Haga clic **[!UICONTROL Post]**.

1. (Opcional) Añada el seguimiento de búsqueda, social y comercial dentro de la variable [account](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md), [campaña](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md), [grupo de publicidad](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md), o [anuncio](/help/search-social-commerce/campaign-management/campaigns/ad-manage.md) configuración.

## Editar la configuración de programación de un trabajo de importación de campañas

Consulte [de qué se importa [!DNL Google Ads] campañas](https://help.ads.microsoft.com/#apex/ads/en/50851/0-500).

1. En el menú principal, haga clic en **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Import Campaigns]**.

1. Seleccione la casilla de verificación situada junto al trabajo de importación y haga clic en ![Editar](/help/search-social-commerce/assets/edit.png "Editar").

1. En el **[!UICONTROL Set schedule]** , especifique la [configuración de programación](#campaign-import-settings).

1. Haga clic **[!UICONTROL Post]**.

## Ver los trabajos de importación de campañas

Puede enumerar todos los trabajos de importación, incluido el de origen [!DNL Google Ads] cuenta, el destinatario [!DNL Microsoft® Advertising] cuenta, la hora o programación de la importación y el usuario que creó el trabajo. Cuando se ejecuta un trabajo de importación varias veces, incluso durante importaciones programadas regularmente, cada incidencia se muestra como un trabajo independiente.

* Realice una de las acciones siguientes:

   * En el menú principal, haga clic en **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Import Campaigns]**.

     De forma predeterminada, la vista se abre en [!UICONTROL List of Import Jobs] pestaña.

   * Desde el [[!UICONTROL Import Logs] pestaña](#campaign-import-log), haga clic en **[!UICONTROL List of Import Jobs]** pestaña.

## Ejecutar un trabajo de importación de campaña

1. En el menú principal, haga clic en **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Import Campaigns]**.

1. Seleccione la casilla de verificación situada junto al trabajo de importación.

1. Clic ![Ejecutar ahora](/help/search-social-commerce/assets/run.png "Ejecutar ahora").

## Visualización de registros de los trabajos de importación de la campaña {#campaign-import-log}

Puede enumerar todos los trabajos de importación completados o fallidos, incluida la hora de inicio, el origen [!DNL Google Ads] cuenta, el destinatario [!DNL Microsoft® Advertising] cuenta, el usuario que creó el trabajo, el número de operaciones correctas y fallidas y las direcciones de correo electrónico que recibieron notificaciones para cada trabajo. Puede ver más detalles sobre los cambios en el destinatario [!DNL Microsoft® Advertising] cuenta que se produjo para cada trabajo, incluido el número de elementos agregados, sincronizados, eliminados y que produjeron errores para cada nivel de entidad (como campaña o palabra clave) en la cuenta.

1. En el menú principal, haga clic en **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Import Campaigns]**.

1. Haga clic en **[!UICONTROL Import Logs]** pestaña.

1. (Opcional) Para ver los detalles de cualquier trabajo de importación, haga clic en el valor en [!UICONTROL Summary] columna.

## Configuración del trabajo de importación de Campaign {#campaign-import-settings}

### [!UICONTROL Select accounts]

**[!UICONTROL Source Google Ads account]:** El sincronizado [!DNL Google Ads] cuenta desde la que se exportan los datos de la campaña.

**[!UICONTROL Credential ID]:** Un ID que [!DNL Microsoft® Advertising] utiliza para representar su [!DNL Google Ads] credenciales.

Generación automática de [!DNL Microsoft® Advertising] las credenciales para la importación no están disponibles debido a [!DNL Microsoft® Advertising] limitaciones. Póngase en contacto con el servicio de asistencia técnica de Adobe o con su equipo de cuenta de Adobe para que creen las credenciales y le proporcionen el ID.

**[!UICONTROL Target Microsoft® Ads account]:** El sincronizado [!DNL Microsoft® Advertising] cuenta en la que se importan los datos de la campaña.

### [!UICONTROL Select campaigns & ad groups]

**\[Datos para importar\]:** Especifique los datos que desea importar:

* *[!UICONTROL Import all new and existing campaigns]:* Para importar los datos de todas las campañas que ya existen y de las que no existen en [!DNL Microsoft® Advertising].

* *[!UICONTROL Import specific campaigns and adgroups]:* Para seleccionar campañas y grupos de publicidad específicos.

   * Para expandir una campaña a sus grupos de anuncios secundarios, haga clic en **[!UICONTROL >]** después del nombre de la campaña.

   * Para seleccionar una campaña o un grupo de anuncios, seleccione el elemento para que aparezca una marca de verificación.

   * Para eliminar una campaña o un grupo de publicidad:

      * En el [!UICONTROL Campaigns] o [!UICONTROL Adgroups] , anule la selección de la campaña o del grupo de anuncios para que desaparezca la marca de verificación.

      * En el [!UICONTROL Selected] , haga clic en ![Eliminar](/help/search-social-commerce/assets/delete.png "Eliminar").

### [!UICONTROL Customize your import]

**[!UICONTROL Choose specific import options]:** Permite especificar lo que se va a importar, las ofertas y los presupuestos, etc.

**[!UICONTROL What to import]:** Define los elementos que se van a importar. Las opciones para importar categorías de elementos están seleccionadas de forma predeterminada, con todos los tipos de elementos seleccionados. Para incluir solo tipos de elementos específicos, haga clic en **[!UICONTROL Show advanced options]** y cambie los tipos de elementos para incluirlos.

**[!UICONTROL Bids and budgets]:** Define qué configuración de oferta y presupuesto se va a importar, actualizar y personalizar.

**[!UICONTROL Other options]:** Define cómo administrar las direcciones URL de la página de aterrizaje importada, las plantillas de seguimiento y otras opciones de campaña, publicidad y segmentación.

### [!UICONTROL Set schedule]

**[!UICONTROL Import name]:** Nombre del trabajo de importación.

**[!UICONTROL When]:** Cuándo importar las campañas especificadas: *Automático* (para dejar [!DNL Microsoft® Advertising] establezca una programación para optimizar mejor sus campañas), *[!UICONTROL Now]* (para ejecutar el trabajo al publicar la configuración del trabajo), *[!UICONTROL Once]* a una hora determinada, *[!UICONTROL Daily]* a una hora determinada, *[!UICONTROL Weekly]* a una hora determinada, o *[!UICONTROL Monthly]* a una hora especificada.

**[!UICONTROL Receive email notifications]:** Si y cuándo enviar notificaciones por correo electrónico sobre trabajos de importación a las direcciones de correo electrónico en el campo Enviar informes a.

**[!UICONTROL Send reports to]:** Direcciones de correo electrónico para recibir notificaciones sobre trabajos de importación. Separe las direcciones con comas (`,`).
