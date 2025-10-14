---
title: Replicar [!DNL Google Ads] campañas en [!DNL Microsoft Advertising]
description: Aprenda a exportar sus campañas sincronizadas en una cuenta de  [!DNL Google Ads] directamente a una cuenta sincronizada [!DNL Microsoft Advertising] de.
exl-id: e7714d3d-4a8e-44ef-a3a7-e5198c091660
feature: Search Tools
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '942'
ht-degree: 0%

---

# Replicar [!DNL Google Ads] campañas en [!DNL Microsoft Advertising]

Puede exportar sus campañas sincronizadas en una cuenta de [!DNL Google Ads] directamente a una cuenta sincronizada de [!DNL Microsoft Advertising] como campañas CPC (eCPC) mejoradas. Se escalan las ofertas y los presupuestos de campaña existentes. El seguimiento existente de búsqueda, medios sociales y Commerce no se importa.

Puede replicar los siguientes tipos de campañas y su estructura:

* [!DNL Google Ads] buscar y mostrar campañas en [!DNL Microsoft Advertising] buscar y mostrar campañas.

* [!DNL Google Display Network] campañas, incluidas imágenes de anuncios, en [!DNL Microsoft Advertising] campañas de audiencia en Microsoft Audience Network.

  Si desea replicar las campañas de visualización basadas en fuentes de compras, primero debe replicar las ofertas de producto de [!DNL Google Merchant Center] a [!DNL Microsoft Merchant Center]. Cuando duplique las campañas, seleccione el almacén de [!DNL Microsoft Merchant Center] en las opciones de importación para vincular el almacén a las campañas de audiencia basadas en fuentes.

* [!DNL Google Ads] campañas de rendimiento máximo, incluidos los anuncios de inventario local, en [!DNL Microsoft Advertising] campañas de rendimiento máximo.

Puede elegir actualizar las campañas una vez; diariamente, semanalmente o mensualmente; o según la programación recomendada de [!DNL Microsoft Advertising]. Si lo desea, puede configurar las notificaciones cada vez que se ejecute un trabajo de importación o cuando se produzcan errores o cambios. Una vez importadas las campañas en [!DNL Microsoft Advertising], puede comprobar el estado del trabajo de importación, revisar los registros de errores, ejecutar manualmente un trabajo de importación y editar, pausar, habilitar o eliminar la programación de importación.

No toda la información de la campaña está duplicada y es posible que tenga que agregar información a sus [!DNL Microsoft Advertising] campañas. Para obtener más información sobre los datos que se importan, consulte la ayuda de [!DNL Microsoft Advertising] en &quot;[Qué se importa desde [!DNL Google Ads]](https://help.ads.microsoft.com/#apex/ads/en/50851)&quot;. Dado que el seguimiento de Search, Social y Commerce no se ha importado, también debería agregar seguimiento a la configuración de [account](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md), [campaign](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md), [ad group](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md) o [ad](/help/search-social-commerce/campaign-management/campaigns/ad-manage.md).

## Replicar [!DNL Google Ads] campañas

>[!NOTE]
>
>Si quieres replicar campañas de visualización basadas en fuentes de compras, primero [replica tus [!DNL Google Merchant Center] ofertas de productos en [!DNL Microsoft Merchant Center]](https://help.ads.microsoft.com/apex/index/3/en/56870). Cuando duplique las campañas, seleccione el almacén de [!DNL Microsoft Merchant Center] en las opciones de importación para vincular el almacén a las campañas de audiencia basadas en fuentes.

Ver [lo importado de [!DNL Google Ads] campañas](https://help.ads.microsoft.com/#apex/ads/en/50851/0-500).

1. En el menú principal Buscar, Social y Commerce, haga clic en **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Tools] >[!UICONTROL Import Campaigns]**.

1. Haga clic en **[!UICONTROL +Import]**.

1. Especifique la [configuración de importación](#campaign-import-settings):

   1. En la sección **[!UICONTROL Select accounts]**:

      1. Seleccione las cuentas de origen y destino.

      1. Haga clic en **[!UICONTROL Get Credential Id from MSA]**.

      1. Inicie sesión en la cuenta de destino [!DNL Microsoft Advertising], copie el identificador de credencial que se muestra y pegue el valor en el campo **[!UICONTROL Credential ID]**.

   1. En la sección **[!UICONTROL Select campaigns & ad groups]**, especifique las campañas y los grupos de anuncios que desea importar.

   1. En la sección **[!UICONTROL Customize your import]**, especifique los tipos de elementos que desea importar.

   1. En la sección **[!UICONTROL Set schedule]**, especifique cuándo ejecutar el trabajo de importación.

1. Haga clic en **[!UICONTROL Post]**.

1. (Opcional) Agregue el seguimiento de búsqueda, medios sociales y Commerce en la configuración de [cuenta](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md), [campaña](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md), [grupo de anuncios](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md) o [anuncio](/help/search-social-commerce/campaign-management/campaigns/ad-manage.md).

## Editar la configuración de programación de un trabajo de importación de campañas

Ver [lo importado de [!DNL Google Ads] campañas](https://help.ads.microsoft.com/#apex/ads/en/50851/0-500).

1. En el menú principal, haga clic en **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Tools] >[!UICONTROL Import Campaigns]**.

1. Seleccione la casilla de verificación situada junto al trabajo de importación y, a continuación, haga clic en ![Editar](/help/search-social-commerce/assets/edit.png "Editar").

1. En la sección **[!UICONTROL Set schedule]**, especifique la [configuración de programación](#campaign-import-settings).

1. Haga clic en **[!UICONTROL Post]**.

## Ver los trabajos de importación de campañas

Puede enumerar todos los trabajos de importación, incluida la cuenta de origen [!DNL Google Ads], la cuenta de destino [!DNL Microsoft Advertising], la hora o programación de importación y el usuario que creó el trabajo. Cuando se ejecuta un trabajo de importación varias veces, incluso durante importaciones programadas regularmente, cada incidencia se muestra como un trabajo independiente.

* Realice una de las acciones siguientes:

   * En el menú principal, haga clic en **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Tools] >[!UICONTROL Import Campaigns]**.

     De manera predeterminada, la vista se abre en la ficha [!UICONTROL List of Import Jobs].

   * En la ficha [[!UICONTROL Import Logs] &#x200B;](#campaign-import-log), haga clic en la ficha **[!UICONTROL List of Import Jobs]**.

## Ejecutar un trabajo de importación de campaña

1. En el menú principal, haga clic en **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Tools] >[!UICONTROL Import Campaigns]**.

1. Seleccione la casilla de verificación situada junto al trabajo de importación.

1. Haga clic en ![Ejecutar ahora](/help/search-social-commerce/assets/run.png "Ejecutar ahora").

## Visualización de registros de los trabajos de importación de la campaña {#campaign-import-log}

Puede enumerar todos los trabajos de importación completados o fallidos, incluida la hora de inicio, la cuenta de origen [!DNL Google Ads], la cuenta de destino [!DNL Microsoft Advertising], el usuario que creó el trabajo, el número de operaciones correctas y fallidas y cualquier dirección de correo electrónico que recibió notificaciones para cada trabajo. Puede ver más detalles sobre los cambios realizados en la cuenta de destino [!DNL Microsoft Advertising] para cada trabajo, incluido el número de elementos agregados, sincronizados, eliminados y que produjeron errores para cada nivel de entidad (como campaña o palabra clave) en la cuenta.

1. En el menú principal, haga clic en **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Tools] >[!UICONTROL Import Campaigns]**.

1. Haga clic en la ficha **[!UICONTROL Import Logs]**.

1. (Opcional) Para ver los detalles de cualquier trabajo de importación, haga clic en el valor de la columna [!UICONTROL Summary].

## Configuración del trabajo de importación de Campaign {#campaign-import-settings}

### [!UICONTROL Select accounts]

**[!UICONTROL Source Google Ads account]:** Cuenta sincronizada [!DNL Google Ads] desde la que se exportan los datos de la campaña.

**[!UICONTROL Credential ID]:** Identificador que [!DNL Microsoft Advertising] usa para representar sus credenciales de [!DNL Google Ads].

La generación automática de credenciales de [!DNL Microsoft Advertising] para la importación no está disponible debido a las limitaciones de [!DNL Microsoft Advertising]. Póngase en contacto con el equipo de cuenta de Adobe para que le proporcione las credenciales y el ID.

**[!UICONTROL Target Microsoft Ads account]:** Cuenta sincronizada de [!DNL Microsoft Advertising] en la que se importan los datos de campaña.

### [!UICONTROL Select campaigns & ad groups]

**\[Datos para importar\]:** Especifique los datos para importar:

* *[!UICONTROL Import all new and existing campaigns]:* Para importar los datos de todas las campañas que ya existen y las que no existen en [!DNL Microsoft Advertising].

* *[!UICONTROL Import specific campaigns and adgroups]:* Para seleccionar campañas y grupos de anuncios específicos.

   * Para expandir una campaña a sus grupos de anuncios secundarios, haga clic en **[!UICONTROL >]** después del nombre de la campaña.

   * Para seleccionar una campaña o un grupo de anuncios, seleccione el elemento para que aparezca una marca de verificación.

   * Para eliminar una campaña o un grupo de publicidad:

      * En las columnas [!UICONTROL Campaigns] o [!UICONTROL Adgroups], anule la selección de la campaña o del grupo de anuncios para que desaparezca la marca de verificación.

      * En la columna [!UICONTROL Selected], haga clic en ![Eliminar](/help/search-social-commerce/assets/delete.png "Eliminar").

### [!UICONTROL Customize your import]

**[!UICONTROL Choose specific import options]:** Permite especificar qué importar, pujas y presupuestos, y otras opciones.

**[!UICONTROL What to import]:** Define los elementos que se van a importar. Las opciones para importar categorías de elementos están seleccionadas de forma predeterminada, con todos los tipos de elementos seleccionados. Para incluir solo tipos de elementos específicos, haga clic en **[!UICONTROL Show advanced options]** y cambie los tipos de elementos que desea incluir.

**[!UICONTROL Bids and budgets]:** Define qué configuración de oferta y presupuesto importar, actualizar y personalizar.

**[!UICONTROL Other options]:** Define cómo administrar las direcciones URL de la página de aterrizaje importada, las plantillas de seguimiento y otras opciones de campaña, publicidad y segmentación.

### [!UICONTROL Set schedule]

**[!UICONTROL Import name]:** Nombre del trabajo de importación.

**[!UICONTROL When]:** Cuándo importar las campañas especificadas: *Automático* (para permitir que [!DNL Microsoft Advertising] establezca una programación para optimizar mejor sus campañas), *[!UICONTROL Now]* (para ejecutar el trabajo cuando publique la configuración del trabajo), *[!UICONTROL Once]* a una hora especificada, *[!UICONTROL Daily]* a una hora especificada, *[!UICONTROL Weekly]* a una hora especificada o *[!UICONTROL Monthly]* a una hora especificada.

**[!UICONTROL Receive email notifications]:** Si y cuándo enviar notificaciones por correo electrónico sobre trabajos de importación a las direcciones de correo electrónico en el campo Enviar informes a.

**[!UICONTROL Send reports to]:** Direcciones de correo electrónico para recibir notificaciones sobre trabajos de importación. Separe las direcciones con comas (`,`).
