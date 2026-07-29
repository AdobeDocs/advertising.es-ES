---
title: Administración de campañas
description: Aprenda a crear y administrar campañas publicitarias.
feature: Search Campaign Management
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
subfeature_v2: id: f3d33161-c519-436e-bbbd-730ba428736b
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 6b67f3e2759ddd80300c86df610b36684b7a07e2
workflow-type: tm+mt
source-wordcount: 2285
ht-degree: 0%

---

# Administración de campañas

*característica de Beta*

Una campaña es el componente principal de una cuenta de red de publicidad. Para la mayoría de los tipos de campaña, consiste en un conjunto de grupos de anuncios o conjuntos de anuncios. La configuración de la campaña incluye parámetros de presupuesto de campaña, objetivos de publicidad y parámetros de seguimiento opcionales para todos los anuncios de la campaña. Los parámetros de seguimiento de nivel de campaña anulan los parámetros de nivel de cuenta, pero pueden anularse a su vez en un nivel inferior.

Una vez que [haga accesible una cuenta de red de anuncios a través de una conexión API](/help/search-social-commerce/new-ui/set-up/accounts/api-accounts/api-account-manage.md) y Search, Social y Commerce hayan sincronizado los datos de la cuenta con la red de anuncios, podrá crear nuevas campañas con [tipos de campañas compatibles](/help/search-social-commerce/introduction/supported-inventory.md). También puede editar y cambiar el estado de las campañas.

Para obtener detalles acerca de la funcionalidad disponible para cada red de anuncios, consulte &quot;[Inventario compatible](/help/search-social-commerce/introduction/supported-inventory.md)&quot;.

## Acerca de la vista [!UICONTROL Campaigns] {#campaign-view-about}

La vista [!UICONTROL Manage] > [!UICONTROL Campaigns] enumera todas las campañas de la vista filtrada para la cuenta de anunciante seleccionada. Puede abrir una lista de grupos de publicidad en la campaña haciendo clic en el nombre de la campaña.

A medida que agrega y edita datos de campaña en las vistas [!UICONTROL Campaigns], Search, Social y Commerce insertan inmediatamente los cambios de datos en la red publicitaria. Search, Social y Commerce también extraen datos de estructura de campaña y datos de clics diariamente, o con mayor frecuencia cuando se detectan nuevas campañas. Para todas las redes de anuncios sincronizadas, también puede sincronizar cuentas bajo demanda según sea necesario.

Search, Social y Commerce extrae datos de rendimiento cada hora de las cuentas sincronizadas de [!DNL Google Ads] y [!DNL Microsoft Advertising], y cada día de otras cuentas sincronizadas de red de anuncios.

### Acciones disponibles

* [Creación de una campaña](#campaign-create)

* [Cambiar el nombre de una campaña desde la fila](#campaign-rename)

* [Editar configuración de campaña](#campaign-edit)

* [Cambie el estado de una campaña o elimínela desde la fila](#campaign-status)

* [Asignar campañas a un portafolio y eliminar campañas de un portafolio](#campaign-portfolio)

* [Ver un gráfico de rendimiento en la vista [!UICONTROL Campaigns]](#campaign-performance-graph)

* [Asignar restricciones de oferta a campañas y anular la asignación de restricciones de campañas](#campaign-constraints)

* [Asignar restricciones de destino a campañas y anular la asignación de restricciones de destino a campañas](#campaign-target-constraints)

* [Asigne clasificaciones de etiquetas a las campañas y elimine clasificaciones de etiquetas de las campañas](#campaign-classifications)

* [Administrar informes de vista de datos desde la vista [!UICONTROL Campaigns]](#campaign-reports)

## Creación de una campaña {#campaign-create}

>[!NOTE]
>
>* Antes de crear una campaña, [implemente etiquetas de seguimiento de conversión](/help/search-social-commerce/tracking/conversion-tracking-about.md) en las páginas web del anunciante.
>* Para crear un gran número de campañas a la vez, use<!-- Not available in new UI as of 7/21: the [copy and paste feature](/help/search-social-commerce/campaign-management/campaigns/copy-paste.md) or--> [hojas de edición masiva de campañas](/help/search-social-commerce/new-ui/set-up/bulksheets/about.md).

1. En el menú principal, haga clic en **[!UICONTROL Manage]>[!UICONTROL Campaigns]**.

1. Haga clic en **[!UICONTROL Create Campaign]**.

1. Especifique la configuración de la campaña [Baidu](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings-baidu.md), [Google Ads](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings-google.md), [LY Ads](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings-ly.md), [Microsoft Advertising](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings-microsoft.md) o [Yandex](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings-yandex.md).

1. Haga clic en **[!UICONTROL Review and Save]**.

1. Si es necesario, haga clic en ![Editar](/help/search-social-commerce/assets/edit-new.png "Editar") y cambie la configuración de la campaña.

1. Haga clic en **[!UICONTROL Create]**.

Según la red de publicidad en la que se creó la campaña, es posible que tenga que crear grupos de publicidad y anuncios asociados antes de que la campaña se inserte en la red de publicidad.

## Cambiar nombre de campaña {#campaign-rename}

Cambie rápidamente el nombre de una campaña sin abrir la configuración completa de la campaña.

1. En el menú principal, haga clic en **[!UICONTROL Manage]>[!UICONTROL Campaigns]**.

1. Mantenga el cursor sobre la fila de la campaña y haga clic en **[!UICONTROL ...]>[!UICONTROL Rename]**.

1. Edite el nombre y haga clic en **[!UICONTROL Apply]**.

## Editar configuración de campaña {#campaign-edit}

Puede editar la configuración de campañas individuales. También puede editar algunos campos para varias campañas a la vez, incluidos algunos detalles de campaña, opciones de presupuesto y opciones de URL que son comunes a todas las campañas seleccionadas.

>[!TIP]
>
>También puede editar datos de forma masiva mediante <!-- Not available in new UI as of 7/21: the [copy and paste feature](/help/search-social-commerce/campaign-management/campaigns/copy-paste.md) or--> [hojas de edición masiva de campañas](/help/search-social-commerce/new-ui/set-up/bulksheets/about.md).

1. En el menú principal, haga clic en **[!UICONTROL Manage]>[!UICONTROL Campaigns]**.

1. Realice una de las acciones siguientes:

   * Mantenga el cursor sobre el nombre de la entidad y haga clic en **[!UICONTROL ...]>[!UICONTROL Edit]**.

   * Seleccione la casilla de verificación situada junto a la campaña. En la barra de herramientas de acciones masivas, haga clic en **[!UICONTROL Edit]**.

1. Editar [Baidu](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings-baidu.md), [Google Ads](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings-google.md), [LY Ads](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings-ly.md), <!-- [Meta Ads](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings-meta.md), --> Configuración de la campaña [Microsoft Advertising](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings-microsoft.md) o [Yandex](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings-yandex.md).

1. Haga clic en **[!UICONTROL Review and Save]**.

1. Si es necesario, haga clic en ![Editar](/help/search-social-commerce/assets/edit-new.png "Editar") y cambie la configuración de la campaña.

1. Haga clic en **[!UICONTROL Update]**.

Según la red de publicidad en la que se creó la campaña, es posible que la campaña tenga que incluir grupos de publicidad y anuncios antes de insertarla en la red de publicidad.

## Cambio del estado de una campaña {#campaign-status}

Cambie rápidamente el estado de una campaña sin abrir la configuración completa de la campaña.

Puede pausar cualquier campaña activa en una red de publicidad compatible para deshabilitar las pujas en ella. Más tarde, puedes reanudar las pujas cambiando el estado de nuevo a activo.

También puede eliminar cualquier campaña activa o en pausa. Las campañas eliminadas se eliminan de la red de anuncios. Siguen estando visibles cuando se incluyen en el filtro de datos, pero no se pueden cambiar.

### Activación o pausa de una campaña

1. En el menú principal, haga clic en **[!UICONTROL Manage]>[!UICONTROL Campaigns]**.

1. Mantenga el cursor sobre la fila de la campaña y haga clic en ![Editar](/help/search-social-commerce/assets/edit.png "Editar") junto a la columna [!UICONTROL Status].

1. Cambiar el estado:

   * Para activar una campaña en pausa, seleccione **[!UICONTROL Active]**.

   * Para pausar una campaña activa, seleccione **[!UICONTROL Paused]**.

### Eliminación de una campaña

1. En el menú principal, haga clic en **[!UICONTROL Manage]>[!UICONTROL Campaigns]**.

1. Realice una de las acciones siguientes:

   * Mantenga el cursor sobre la fila de la campaña y haga clic en **[!UICONTROL ...]>[!UICONTROL Delete]**.

   * Mantenga el cursor sobre la fila de la campaña y haga clic en ![Editar](/help/search-social-commerce/assets/edit.png "Editar") junto a la columna [!UICONTROL Status]. Seleccione **[!UICONTROL Deleted]**.

## Asignación de campañas a un portafolio {#campaign-portfolio}

Asignar una campaña a un portafolio optimizado permite a Search, Social y Commerce optimizar ofertas, presupuestos de campaña y objetivos de estrategia de oferta para palabras clave y anuncios en la campaña. Puede asignar campañas a un portafolio desde la vista [!UICONTROL Campaigns], al crear el portafolio o al editar la configuración de un portafolio.

No todos los tipos de campañas y redes de anuncios cumplen los requisitos para la optimización; vea una lista de [tipos de campañas compatibles](/help/search-social-commerce/introduction/supported-inventory.md) que puede incluir en un portafolio. Además, compruebe la compatibilidad con la optimización [para cada estrategia de oferta de campaña](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-about.md#optimization-by-bid-strategy).

>[!NOTE]
>
>Cada campaña solo se puede asignar a un portafolio. Si asigna una campaña que ya está asociada con otro portafolio a un nuevo portafolio, se elimina del portafolio original.

### Asignar campañas a un portafolio existente desde la vista [!UICONTROL Campaigns]

1. En el menú principal, haga clic en **[!UICONTROL Manage]>[!UICONTROL Campaigns]**.

1. Seleccione la casilla de verificación situada junto a cada campaña para asignarla a un solo portafolio.

1. En la barra de herramientas de acciones masivas, haga clic en **+[!UICONTROL Assign]** > **[!UICONTROL Existing Portfolio]** .

1. Seleccione el portafolio.

1. Haga clic en **[!UICONTROL Assign Now]**.

### Asignar campañas a un nuevo portafolio desde la vista [!UICONTROL Campaigns]

1. En el menú principal, haga clic en **[!UICONTROL Manage]>[!UICONTROL Campaigns]**.

1. Seleccione la casilla de verificación situada junto a cada campaña para la que desea crear el nuevo portafolio.

1. En la barra de herramientas de acciones masivas, haga clic en **+[!UICONTROL Assign]** > **[!UICONTROL New Portfolio]**.

1. En la pantalla [!UICONTROL Create Portfolio], especifique la configuración del portafolio.

   Las campañas seleccionadas anteriormente ya están asignadas a la campaña. Si lo desea, puede editar la lista de campañas del portafolio.

   Para obtener más información sobre la configuración del portafolio, consulte la Guía de optimización, que está disponible en Search, Social y Commerce.

1. Haga clic en **[!UICONTROL Review and Save]**.

### Cambiar asignaciones de campaña para un portafolio desde la vista [!UICONTROL Portfolios]

Al eliminar una campaña de un portafolio, Buscar, Social y Commerce no pueden optimizar ofertas, presupuestos de campaña y objetivos de estrategia de oferta para esa campaña.

La acción se registra en el historial de cambios del portafolio.

Para obtener más información sobre la optimización, consulte la Guía de optimización, que está disponible en Search, Social y Commerce.

1. En el menú principal, haga clic en **[!UICONTROL Manage]>[!UICONTROL Portfolios]**.

1. Seleccione la casilla de verificación situada junto al portafolio.

1. En la barra de herramientas de acciones masivas, haga clic en **[!UICONTROL Edit]**.

1. En la configuración del portafolio, vaya a la sección [!UICONTROL Assign Campaigns] y cambie las asignaciones de campaña.

   Para obtener más información sobre la configuración del portafolio, consulte la Guía de optimización, que está disponible en Search, Social y Commerce.

1. Haga clic en **[!UICONTROL Review and Save]**.

1. Revise la configuración y realice los cambios que sean necesarios y, a continuación, haga clic en **[!UICONTROL Save]**.

## Administrar asignaciones de restricciones de oferta para campañas {#campaign-constraints}

Cada entidad solo puede tener una restricción. Las restricciones las heredan las entidades secundarias, por lo que no es necesario asignar restricciones para entidades secundarias a menos que desee anular los valores heredados.

Al anular la asignación de una restricción, se elimina la asociación con los componentes de la cuenta y todos sus componentes secundarios, y los datos del informe de la restricción ya no están disponibles para dichos componentes. Al anular la asignación de una restricción, no se eliminan ni la restricción ni los propios componentes de la cuenta.

>[!NOTE]
>
>Las restricciones activas restringen las ofertas solo para las unidades de oferta asignadas en portafolios optimizados de nivel de palabra clave heredados. Se ignoran para las unidades de oferta que están en portafolios activos, en portafolios híbridos o que no están en portafolios.

### Asignar una restricción de oferta a las campañas seleccionadas desde la nueva vista [!UICONTROL Campaigns]

Puede asignar una sola restricción a una o varias campañas.

1. En el menú principal, haga clic en **[!UICONTROL Manage]>[!UICONTROL Campaigns]**.

1. Seleccione la casilla de verificación situada junto a cada campaña a la que desea asignar una sola restricción.

1. En la barra de herramientas de acciones masivas, haga clic en **+[!UICONTROL Assign]** > **[!UICONTROL Constraint]**.

1. Seleccione la restricción.

1. Haga clic en **[!UICONTROL Assign Now]**.

### Asignar una restricción de oferta a las unidades de oferta de búsqueda seleccionadas desde las vistas heredadas de [!UICONTROL Campaigns]

1. En **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**, seleccione la vista del componente de cuenta.

1. Seleccione la casilla de verificación situada junto a cada fila correspondiente.

   Para obtener sugerencias sobre cómo seleccionar varias filas, consulte &quot;[Seleccionar varias filas](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)&quot;.

1. En la barra de herramientas situada encima de la tabla de datos, haga clic en **[!UICONTROL More]** y, a continuación, en **[!UICONTROL Assign]** > **[!UICONTROL Constraint]**.

1. Seleccione la restricción aplicable.

1. (Opcional) Introduzca detalles adicionales:

   1. Junto a [!UICONTROL Additional Details], haga clic en **[!UICONTROL Open]** para expandir los detalles.

   1. Escriba un(a) **[!UICONTROL Project Name]** opcional(a) y/o un(a) **[!UICONTROL Description]** opcional.

1. Haga clic en **[!UICONTROL Save]**.

### Quitar las restricciones de oferta de las campañas seleccionadas de la nueva vista [!UICONTROL Campaigns]

1. En el menú principal, haga clic en **[!UICONTROL Manage]>[!UICONTROL Campaigns]**.

1. Seleccione la casilla de verificación situada junto a cada campaña para anular la asignación de restricciones.

1. En la barra de herramientas de acciones masivas, haga clic en **-[!UICONTROL Unassign]** > **[!UICONTROL Constraint]**.

1. Haga clic en **[!UICONTROL Confirm]**.

### Eliminar las restricciones de oferta de las unidades de oferta de búsqueda de las vistas heredadas de [!UICONTROL Campaigns]

>[!NOTE]
>
>Para eliminar una restricción, de modo que no esté disponible para uso futuro, consulte &quot;Eliminar restricciones para unidades de oferta de búsqueda&quot; en el capítulo Guía de optimización sobre &quot;Restricciones de oferta&quot;, que está disponible en Buscar, Social y Commerce.<!-- verify convention for referencing Optimization Guide here -->

1. En **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**, seleccione la vista del componente de cuenta.

1. Seleccione la casilla de verificación situada junto a cada componente del que desea quitar la restricción.

   Para obtener sugerencias sobre cómo seleccionar varias filas, consulte &quot;[Seleccionar varias filas](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)&quot;.

1. En la barra de herramientas situada encima de la tabla de datos, haga clic en **[!UICONTROL More]** y, a continuación, en **[!UICONTROL Unassign]** > **[!UICONTROL Constraint]**.

1. En el diálogo de confirmación, seleccione **[!UICONTROL Yes, Unassign]**.

## Administrar asignaciones de restricciones de destino para campañas {#campaign-target-constraints}

### Asignar una restricción de destino a las campañas seleccionadas desde la nueva vista [!UICONTROL Campaigns]

Puede asignar una sola restricción de destino a una o varias campañas.

1. En el menú principal, haga clic en **[!UICONTROL Manage]>[!UICONTROL Campaigns]**.

1. Seleccione la casilla de verificación situada junto a cada campaña a la que desea asignar una sola restricción de destino.

1. En la barra de herramientas de acciones masivas, haga clic en **+[!UICONTROL Assign]** > **[!UICONTROL Target Constraint]**.

1. Seleccione la restricción.

1. Haga clic en **[!UICONTROL Assign Now]**.

### Quitar restricciones de destino de campañas seleccionadas de la nueva vista [!UICONTROL Campaigns]

1. En el menú principal, haga clic en **[!UICONTROL Manage]>[!UICONTROL Campaigns]**.

1. Seleccione la casilla de verificación situada junto a cada campaña de la que desea anular la asignación de una restricción de destino.

1. En la barra de herramientas de acciones masivas, haga clic en **-[!UICONTROL Unassign]** > **[!UICONTROL Target Constraint]**.

1. Haga clic en **[!UICONTROL Confirm]**.

## Asignar clasificaciones de etiquetas a las campañas {#campaign-classifications}

>[!NOTE]
>
>Las entidades secundarias heredan los valores de etiquetas, por lo que no introduzca valores para entidades secundarias a menos que desee anular los valores heredados.

### Asignar valores de clasificación a las campañas

1. En el menú principal, haga clic en **[!UICONTROL Manage]>[!UICONTROL Campaigns]**.

1. Seleccione la casilla de verificación situada junto a cada campaña a la que desea asignar un valor de etiqueta.

   Para obtener sugerencias sobre cómo seleccionar varias filas, consulte &quot;[Seleccionar varias filas](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)&quot;.

1. En la barra de herramientas de acciones masivas, haga clic en **+[!UICONTROL Assign]** > **[!UICONTROL Label Classification]**.

1. Para cada valor de clasificación aplicable, haga lo siguiente:

   1. En la columna **[!UICONTROL Classifications]**, especifique la clasificación:

      * Para utilizar una clasificación existente, haga clic en el nombre de la clasificación para expandirla.

      * Para crear una clasificación, haga clic en [!UICONTROL +] en el encabezado de la columna. En el campo de entrada, escriba el nombre de la clasificación y haga clic en ![Guardar](/help/search-social-commerce/assets/save-checkmark.png "Guardar") para guardar la clasificación inmediatamente. Para utilizar la nueva clasificación, haga clic en el nombre de la clasificación para expandirla.

        El nombre debe contener [caracteres ASCII 32-126](https://www.asciitable.com/) y la longitud máxima es de 27 caracteres de un solo byte.

   1. En la columna **[!UICONTROL Value Name]**, especifique el valor de la clasificación seleccionada:

      * Para utilizar un valor existente, seleccione el valor.

      * Para crear un valor, haga clic en [!UICONTROL +] en el encabezado de la columna. En el campo de entrada, escriba el valor y, a continuación, haga clic en ![Guardar](/help/search-social-commerce/assets/save-checkmark.png "Guardar") para guardar inmediatamente el valor y seleccionarlo de forma predeterminada.

        La longitud máxima es de 100 caracteres y puede incluir caracteres ASCII y no ASCII.

1. Haga clic en **+[!UICONTROL Assign Now]**.

### Eliminación de valores de clasificación de etiquetas de las campañas

Al eliminar un valor de clasificación, se elimina la asociación con el componente de cuenta y todos sus componentes secundarios. Los datos del informe para el valor de clasificación ya no están disponibles para esos componentes. Al eliminar un valor de clasificación, no se elimina el valor ni los componentes de la cuenta.

1. En el menú principal, haga clic en **[!UICONTROL Manage]>[!UICONTROL Campaigns]**.

1. Seleccione la casilla de verificación situada junto a cada campaña de la que desea quitar un valor de etiqueta.

   Para obtener sugerencias sobre cómo seleccionar varias filas, consulte &quot;[Seleccionar varias filas](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)&quot;.

1. En la barra de herramientas de acciones masivas, haga clic en **[!UICONTROL Unassign]** > **[!UICONTROL Label Classification]**.

1. Seleccione la casilla de verificación situada junto a cada valor de clasificación que desee eliminar de las entidades seleccionadas.

   Para seleccionar todos los valores asignados, haga clic en **[!UICONTROL Select All]**. Para anular la selección de todos los valores asignados, haga clic en **[!UICONTROL Deselect All]**.

1. Haga clic en **[!UICONTROL Unassign Selected]**.

## Ver un gráfico de rendimiento en la vista [!UICONTROL Campaigns] {#campaign-performance-graph}

Abra y configure un gráfico de rendimiento con hasta tres métricas calculadas en total en todas las campañas de la vista para el intervalo de fechas especificado.

### Ver un gráfico de rendimiento

1. Sobre la tabla de datos, haga clic en ![Gráficos](/help/search-social-commerce/assets/charts.png "Gráficos").

1. (Opcional) Especifique la moneda y hasta tres métricas para incluir en el gráfico.

### Ocultar un gráfico de rendimiento visible

* Sobre la tabla de datos, haga clic en ![Gráficos](/help/search-social-commerce/assets/charts.png "Gráficos").

## Administrar informes de vista de datos desde la vista [!UICONTROL Campaigns] {#campaign-reports}

<!-- Wording??????  Filtered data reports? -->

Genere un informe que incluya las filas de datos de una o varias campañas en la vista [!UICONTROL Campaigns] y, a continuación, descargue el informe como archivo de hoja de cálculo de Microsoft Excel (formato XLXS). El informe incluye todas las columnas visibles en la vista.

Puede eliminar cualquier informe generado.

Consulte también &quot;>* [(IU heredada) Descargar datos de una vista de administración de campañas](/help/search-social-commerce/common-tasks/navigation-editing-selection/download.md)&quot; y &quot;[(IU heredada) Eliminar un informe de datos de rendimiento o un archivo de hoja de edición masiva del menú [!UICONTROL Downloads]](/help/search-social-commerce/common-tasks/navigation-editing-selection/download-delete-data.md).&quot;

### Generación de un informe con las filas de datos filtradas

1. En el menú principal, haga clic en **[!UICONTROL Manage]>[!UICONTROL Campaigns]**.

1. Especifique las campañas cuyos datos desee descargar:

   * Para descargar datos de campañas específicas, seleccione las casillas de verificación de las campañas.

   * Para descargar los datos de todas las campañas, no es necesario seleccionar ninguna casilla de verificación. Todas las campañas se incluyen de forma predeterminada.

1. En la barra de herramientas situada encima de la tabla de datos, haga clic en ![Descargar informe](/help/search-social-commerce/assets/download.png "Descargar informe") **[!UICONTROL Reports]**.

1. En la configuración de [!UICONTROL Grid Reports], escriba un nombre de informe único y haga clic en **[!UICONTROL Generate]**.

   De forma predeterminada, el nombre del archivo es &quot;campaign_YYYYMMDD_NNNN&quot;, donde &quot;NNNN&quot; es el número de trabajo secuencial (como &quot;campaign_20250402_1326).

   El archivo se agrega a la lista [!UICONTROL Recently Generated].

1. (Opcional) Para descargar el archivo una vez que se haya completado, haga clic en ![Descargar](/help/search-social-commerce/assets/download.png "Descargar") junto al nombre del archivo.

   El archivo se descarga según el procedimiento normal del explorador.

### Descargar un informe completado

1. En el menú principal, haga clic en **[!UICONTROL Manage]>[!UICONTROL Campaigns]**.

1. En la barra de herramientas situada encima de la tabla de datos, haga clic en ![Descargar informe](/help/search-social-commerce/assets/download.png "Descargar informe") **[!UICONTROL Reports]**.

1. En la lista [!UICONTROL Recently Generated] del cuadro de diálogo [!UICONTROL Grid Reports], haga clic en ![Descargar](/help/search-social-commerce/assets/download.png "Descargar") junto al nombre del archivo.

   El archivo se descarga según el procedimiento normal del explorador.

### Eliminar un informe completado

1. En el menú principal, haga clic en **[!UICONTROL Manage]>[!UICONTROL Campaigns]**.

1. En la barra de herramientas situada encima de la tabla de datos, haga clic en ![Descargar informe](/help/search-social-commerce/assets/download.png "Descargar informe") **[!UICONTROL Reports]**.

1. En la lista [!UICONTROL Recently Generated] del cuadro de diálogo [!UICONTROL Grid Reports], haga clic en ![Eliminar](/help/search-social-commerce/assets/delete-new.png "Eliminar") junto al nombre de archivo.

>[!MORELIKETHIS]
>
>* [Administrar restricciones para buscar unidades de oferta](/help/search-social-commerce/new-ui/goals/constraints-manage.md)
>* [Administrar asignaciones de restricción para grupos de anuncios](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-constraint-assignments-manage.md)
>* [Administrar asignaciones de restricción para palabras clave](/help/search-social-commerce/new-ui/target/keywords/keyword-constraint-assignments-manage.md)
>* [Administrar asignaciones de restricción para las ubicaciones](/help/search-social-commerce/new-ui/target/placements/placement-constraint-assignments-manage.md)
>* [(IU heredada) Descargar datos de una vista de administración de campañas](/help/search-social-commerce/common-tasks/navigation-editing-selection/download.md)
>* [(IU heredada) Eliminar un informe de datos de rendimiento o un archivo de hoja de edición masiva del menú [!UICONTROL Downloads]](/help/search-social-commerce/common-tasks/navigation-editing-selection/download-delete-data.md)
>* [[!DNL Baidu] configuración de campaña](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings-baidu.md)
>* [[!DNL Google Ads] configuración de campaña](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings-google.md)
>* [[!DNL LY Ads] configuración de campaña](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings-ly.md)
>* [[!DNL Microsoft Advertising] configuración de campaña](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings-microsoft.md)
>* [[!DNL Yandex] configuración de campaña](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings-yandex.md)

<!-- >* [[!DNL Meta Ads] campaign settings](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings-meta.md) -->

