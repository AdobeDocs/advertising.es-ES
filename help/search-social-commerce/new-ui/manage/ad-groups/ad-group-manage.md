---
title: Administrar grupos de anuncios
description: Obtenga información sobre cómo crear y administrar grupos de anuncios.
feature: Search Campaign Management
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
subfeature_v2:
  - id: f3d33161-c519-436e-bbbd-730ba428736b
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: d45eb490f9dbb7da89bd1270582e5548b70cbd31
workflow-type: tm+mt
source-wordcount: 1676
ht-degree: 0%

---

# Administrar grupos de anuncios

<!-- Go through all -->

*característica de Beta*

Un grupo de anuncios incluye un conjunto de anuncios y sus palabras clave relacionadas. Un grupo de anuncios en una campaña que segmenta la red de visualización también puede incluir ubicaciones, que son ubicaciones en la red de visualización en la que pueden aparecer los anuncios. La configuración del grupo de publicidad, que se aplica a todos los componentes del grupo de publicidad, varía según la red de publicidad.

Una vez que [hagas accesible una cuenta de red de anuncios a través de una conexión API](/help/search-social-commerce/new-ui/set-up/accounts/api-accounts/api-account-manage.md) y Search, Social y Commerce hayan sincronizado los datos de la cuenta con la red de anuncios, puedes crear grupos de anuncios para un [tipo de campaña compatible](/help/search-social-commerce/introduction/supported-inventory.md). También puede editar y cambiar el estado de los grupos de anuncios.

Para obtener detalles acerca de la funcionalidad disponible para cada red de anuncios, consulte &quot;[Inventario compatible](/help/search-social-commerce/introduction/supported-inventory.md)&quot;.

## Acerca de la vista [!UICONTROL Ad Groups] {#ad-group-view-about}

La vista [!UICONTROL Manage] > [!UICONTROL Ad Groups] enumera todos los grupos de anuncios en la vista filtrada de la cuenta de anunciante seleccionada.

### Acciones disponibles

* [Crear un grupo de anuncios](#ad-group-create)

* [Cambiar el nombre de un grupo de anuncios desde la fila](#ad-group-rename)

* [Editar la configuración del grupo de anuncios](#ad-group-edit)

* [Cambiar el estado de un grupo de publicidad o eliminarlo desde la fila](#ad-group-status)

* [Ver un gráfico de rendimiento en la vista [!UICONTROL Ad Groups]](#ad-group-performance-graph)

* [Asignar restricciones de oferta a grupos de publicidad y quitar la asignación de restricciones de grupos de publicidad](#ad-group-constraints)

* [Asigne clasificaciones de etiquetas a grupos de anuncios y elimine clasificaciones de etiquetas de los grupos de anuncios](#ad-group-classifications)

* [Administrar informes de vista de datos desde la vista [!UICONTROL Ad Groups]](#ad-group-reports)

## Crear un grupo de anuncios {#ad-group-create}

>[!TIP]
>
>Para crear un gran número de grupos de anuncios a la vez, use<!-- Not available in new UI as of 7/21: the [copy and paste feature](/help/search-social-commerce/campaign-management/campaigns/copy-paste.md) or--> [hojas de edición masiva de campañas](/help/search-social-commerce/new-ui/set-up/bulksheets/about.md).

1. En el menú principal, haga clic en **[!UICONTROL Manage]>[!UICONTROL Ad Groups]**.

1. Haga clic en **[!UICONTROL Create Ad Group]**.

1. Especifique la configuración del grupo de anuncios [Baidu](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-settings-baidu.md), [Google Ads](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-settings-google.md), [LY Ads](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-settings-ly.md), [Microsoft Advertising](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-settings-microsoft.md) o [Yandex](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-settings-yandex.md).

1. Haga clic en **[!UICONTROL Review and Save]**.

1. Si es necesario, haz clic en ![Editar](/help/search-social-commerce/assets/edit-new.png "Editar") y cambia la configuración del grupo de anuncios.

1. Haga clic en **[!UICONTROL Create]**.

Posteriormente, si lo desea, puede anular las ofertas de nivel de grupo de anuncios definiendo ofertas para palabras clave o ubicaciones individuales en el grupo de anuncios.

## Cambiar nombre de grupo de publicidad {#ad-group-rename}

Cambie rápidamente el nombre de un grupo de anuncios sin abrir la configuración completa del grupo de anuncios.

1. En el menú principal, haga clic en **[!UICONTROL Manage]>[!UICONTROL Ad Groups]**.

1. Mantenga el cursor sobre la fila del grupo de anuncios y haga clic en **[!UICONTROL ...]>[!UICONTROL Rename]**.

1. Edite el nombre y haga clic en **[!UICONTROL Apply]**.

## Editar la configuración del grupo de anuncios {#ad-group-edit}

Puede editar la configuración de grupos de anuncios individuales. También puede editar algunos campos para varios grupos de anuncios a la vez, incluidos algunos detalles de grupos de anuncios, opciones de presupuesto y opciones de URL que son comunes a todos los grupos de anuncios seleccionados.

>[!TIP]
>
>También puede editar datos de forma masiva mediante <!-- Not available in new UI as of 7/21: the [copy and paste feature](/help/search-social-commerce/campaign-management/campaigns/copy-paste.md) or--> [hojas de edición masiva de campañas](/help/search-social-commerce/new-ui/set-up/bulksheets/about.md).

1. En el menú principal, haga clic en **[!UICONTROL Manage]>[!UICONTROL Ad Groups]**.

1. Realice una de las acciones siguientes:

   * Mantenga el cursor sobre el nombre de la entidad y haga clic en **[!UICONTROL ...]>[!UICONTROL Edit]**.

   * Seleccione la casilla de verificación situada junto al grupo de anuncios. En la barra de herramientas de acciones masivas, haga clic en **[!UICONTROL Edit]**.

1. Edite la configuración del grupo de anuncios [Baidu](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-settings-baidu.md), [Google Ads](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-settings-google.md), [LY Ads](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-settings-ly.md), [Microsoft Advertising](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-settings-microsoft.md) o [Yandex](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-settings-yandex.md).

1. Haga clic en **[!UICONTROL Review and Save]**.

1. Si es necesario, haz clic en ![Editar](/help/search-social-commerce/assets/edit-new.png "Editar") y cambia la configuración del grupo de anuncios.

1. Haga clic en **[!UICONTROL Update]**.

## Cambiar el estado de un grupo de publicidad {#ad-group-status}

Cambiar rápidamente el estado de un grupo de publicidad sin abrir la configuración completa del grupo de publicidad.

Puede pausar cualquier grupo de publicidad activo en una red de publicidad compatible para deshabilitar las pujas en él. Más tarde, puedes reanudar las pujas cambiando el estado de nuevo a activo.

También puede eliminar cualquier grupo de anuncios activo o en pausa. Los grupos de anuncios eliminados se eliminan de la red de anuncios. Siguen estando visibles cuando se incluyen en el filtro de datos, pero no se pueden cambiar.

### Activación o pausa de un grupo de publicidad

1. En el menú principal, haga clic en **[!UICONTROL Manage]>[!UICONTROL Ad Groups]**.

1. Mantenga el cursor sobre la fila del grupo de anuncios y haga clic en ![Editar](/help/search-social-commerce/assets/edit.png "Editar") junto a la columna [!UICONTROL Status].

1. Cambiar el estado:

   * Para activar un grupo de anuncios en pausa, seleccione **[!UICONTROL Active]**.

   * Para pausar un grupo de publicidad activo, seleccione **[!UICONTROL Paused]**.

### Eliminar un grupo de publicidad

1. En el menú principal, haga clic en **[!UICONTROL Manage]>[!UICONTROL Ad Groups]**.

1. Realice una de las acciones siguientes:

   * Mantenga el cursor sobre la fila del grupo de anuncios y haga clic en **[!UICONTROL ...]>[!UICONTROL Delete]**.

   * Mantenga el cursor sobre la fila del grupo de anuncios y haga clic en ![Editar](/help/search-social-commerce/assets/edit.png "Editar") junto a la columna [!UICONTROL Status]. Seleccione **[!UICONTROL Deleted]**.

## Administrar asignaciones de restricciones de oferta para grupos de anuncios {#ad-group-constraints}

Cada entidad solo puede tener una restricción. Las restricciones las heredan las entidades secundarias, por lo que no es necesario asignar restricciones para entidades secundarias a menos que desee anular los valores heredados.

Al anular la asignación de una restricción, se elimina la asociación con los componentes de la cuenta y todos sus componentes secundarios, y los datos del informe de la restricción ya no están disponibles para dichos componentes. Al anular la asignación de una restricción, no se eliminan ni la restricción ni los propios componentes de la cuenta.

### Asignar una restricción de oferta a los grupos de anuncios seleccionados desde la nueva vista [!UICONTROL Ad Groups]

1. En el menú principal, haga clic en **[!UICONTROL Manage]>[!UICONTROL Ad Groups]**.

1. Active la casilla de verificación situada junto a cada grupo de anuncios al que va a asignar una única restricción.

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

### Quitar las restricciones de oferta de los grupos de anuncios seleccionados de la nueva vista [!UICONTROL Ad Groups]

1. En el menú principal, haga clic en **[!UICONTROL Manage]>[!UICONTROL Ad Groups]**.

1. Seleccione la casilla de verificación situada junto a cada grupo de anuncios del que anulará la asignación de restricciones.

1. En la barra de herramientas de acciones masivas, haga clic en **-[!UICONTROL Unassign]** > **[!UICONTROL Constraint]**.

1. Haga clic en **[!UICONTROL Confirm]**.

### Eliminar las restricciones de oferta de las unidades de oferta de búsqueda de las vistas heredadas de [!UICONTROL Campaigns]

>[!NOTE]
>
>Para eliminar una restricción, de modo que no esté disponible para uso futuro, consulte &quot;Eliminar restricciones para unidades de oferta de búsqueda&quot; en el capítulo Guía de optimización sobre &quot;Restricciones de oferta&quot;, que está disponible en Buscar, Social y Commerce.

1. En **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**, seleccione la vista del componente de cuenta.

1. Seleccione la casilla de verificación situada junto a cada componente del que desea quitar la restricción.

   Para obtener sugerencias sobre cómo seleccionar varias filas, consulte &quot;[Seleccionar varias filas](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)&quot;.

1. En la barra de herramientas situada encima de la tabla de datos, haga clic en **[!UICONTROL More]** y, a continuación, en **[!UICONTROL Unassign]** > **[!UICONTROL Constraint]**.

1. En el diálogo de confirmación, seleccione **[!UICONTROL Yes, Unassign]**.

## Asignar clasificaciones de etiquetas a grupos de anuncios {#ad-group-classifications}

>[!NOTE]
>
>Las entidades secundarias heredan los valores de etiquetas, por lo que no introduzca valores para entidades secundarias a menos que desee anular los valores heredados.

### Asignar valores de clasificación a grupos de anuncios

1. En el menú principal, haga clic en **[!UICONTROL Manage]>[!UICONTROL Ad Groups]**.

1. Seleccione la casilla de verificación situada junto a cada grupo de anuncios al que va a asignar un valor de etiqueta.

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

### Quitar valores de clasificación de etiquetas de grupos de anuncios

Al eliminar un valor de clasificación, se elimina la asociación con el componente de cuenta y todos sus componentes secundarios. Los datos del informe para el valor de clasificación ya no están disponibles para esos componentes. Al eliminar un valor de clasificación, no se elimina el valor ni los componentes de la cuenta.

1. En el menú principal, haga clic en **[!UICONTROL Manage]>[!UICONTROL Ad Groups]**.

1. Seleccione la casilla de verificación situada junto a cada grupo de anuncios del que va a quitar un valor de etiqueta.

   Para obtener sugerencias sobre cómo seleccionar varias filas, consulte &quot;[Seleccionar varias filas](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)&quot;.

1. En la barra de herramientas de acciones masivas, haga clic en **[!UICONTROL Unassign]** > **[!UICONTROL Label Classification]**.

1. Seleccione la casilla de verificación situada junto a cada valor de clasificación que desee eliminar de las entidades seleccionadas.

   Para seleccionar todos los valores asignados, haga clic en **[!UICONTROL Select All]**. Para anular la selección de todos los valores asignados, haga clic en **[!UICONTROL Deselect All]**.

1. Haga clic en **[!UICONTROL Unassign Selected]**.

## Ver un gráfico de rendimiento en la vista [!UICONTROL Ad Groups] {#ad-group-performance-graph}

Abra y configure un gráfico de rendimiento con hasta tres métricas calculadas en total en todos los grupos de anuncios de la vista para el intervalo de fechas especificado.

### Ver un gráfico de rendimiento

1. Sobre la tabla de datos, haga clic en ![Gráficos](/help/search-social-commerce/assets/charts.png "Gráficos").

1. (Opcional) Especifique la moneda y hasta tres métricas para incluir en el gráfico.

### Ocultar un gráfico de rendimiento visible

* Sobre la tabla de datos, haga clic en ![Gráficos](/help/search-social-commerce/assets/charts.png "Gráficos").

## Administrar informes de vista de datos desde la vista [!UICONTROL Ad Groups] {#ad-group-reports}

Genere un informe que incluya las filas de datos de uno o varios grupos de anuncios en la vista [!UICONTROL Ad Groups] y, a continuación, descargue el informe como archivo de hoja de cálculo de Microsoft Excel (formato XLXS). El informe incluye todas las columnas visibles en la vista.

Puede eliminar cualquier informe generado.

Consulte también &quot;>* [(IU heredada) Descargar datos de una vista de administración de campañas](/help/search-social-commerce/common-tasks/navigation-editing-selection/download.md)&quot; y &quot;[(IU heredada) Eliminar un informe de datos de rendimiento o un archivo de hoja de edición masiva del menú [!UICONTROL Downloads]](/help/search-social-commerce/common-tasks/navigation-editing-selection/download-delete-data.md).&quot;

### Generación de un informe con las filas de datos filtradas

1. En el menú principal, haga clic en **[!UICONTROL Manage]>[!UICONTROL Ad Groups]**.

1. Especifique los grupos de anuncios cuyos datos desee descargar:

   * Para descargar datos de grupos de anuncios específicos, active las casillas de verificación situadas junto a los grupos de anuncios.

   * Para descargar los datos de todos los grupos de anuncios, no es necesario activar ninguna casilla de verificación. Todos los grupos de anuncios se incluyen de forma predeterminada.

1. En la barra de herramientas situada encima de la tabla de datos, haga clic en ![Descargar informe](/help/search-social-commerce/assets/download.png "Descargar informe") **[!UICONTROL Reports]**.

1. En la configuración de [!UICONTROL Grid Reports], escriba un nombre de informe único y haga clic en **[!UICONTROL Generate]**.

   De forma predeterminada, el nombre del archivo es &quot;ad group_YYYYMMDD_NNNN&quot;, donde &quot;NNNN&quot; es el número de trabajo secuencial (como &quot;ad group_20250402_1326).

   El archivo se agrega a la lista [!UICONTROL Recently Generated].

1. (Opcional) Para descargar el archivo una vez que se haya completado, haga clic en ![Descargar](/help/search-social-commerce/assets/download.png "Descargar") junto al nombre del archivo.

   El archivo se descarga según el procedimiento normal del explorador.

### Descargar un informe completado

1. En el menú principal, haga clic en **[!UICONTROL Manage]>[!UICONTROL Ad Groups]**.

1. En la barra de herramientas situada encima de la tabla de datos, haga clic en ![Descargar informe](/help/search-social-commerce/assets/download.png "Descargar informe") **[!UICONTROL Reports]**.

1. En la lista [!UICONTROL Recently Generated] del cuadro de diálogo [!UICONTROL Grid Reports], haga clic en ![Descargar](/help/search-social-commerce/assets/download.png "Descargar") junto al nombre del archivo.

   El archivo se descarga según el procedimiento normal del explorador.

### Eliminar un informe completado

1. En el menú principal, haga clic en **[!UICONTROL Manage]>[!UICONTROL Ad Groups]**.

1. En la barra de herramientas situada encima de la tabla de datos, haga clic en ![Descargar informe](/help/search-social-commerce/assets/download.png "Descargar informe") **[!UICONTROL Reports]**.

1. En la lista [!UICONTROL Recently Generated] del cuadro de diálogo [!UICONTROL Grid Reports], haga clic en ![Eliminar](/help/search-social-commerce/assets/delete-new.png "Eliminar") junto al nombre de archivo.

>[!MORELIKETHIS]
>
>* [Administrar restricciones para buscar unidades de oferta](/help/search-social-commerce/new-ui/goals/constraints-manage.md)
>* [Administrar asignaciones de restricción para campañas](/help/search-social-commerce/new-ui/manage/campaigns/campaign-constraint-assignments-manage.md)
>* [Administrar asignaciones de restricción para palabras clave](/help/search-social-commerce/new-ui/target/keywords/keyword-constraint-assignments-manage.md)
>* [Administrar asignaciones de restricción para las ubicaciones](/help/search-social-commerce/new-ui/target/placements/placement-constraint-assignments-manage.md)
>* [(IU heredada) Descargar datos de una vista de administración de campañas](/help/search-social-commerce/common-tasks/navigation-editing-selection/download.md)
>* [(IU heredada) Eliminar un informe de datos de rendimiento o un archivo de hoja de edición masiva del menú [!UICONTROL Downloads]](/help/search-social-commerce/common-tasks/navigation-editing-selection/download-delete-data.md)
>* [[!DNL Baidu] configuración del grupo de anuncios](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-settings-baidu.md)
>* [[!DNL Google Ads] configuración del grupo de anuncios](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-settings-google.md)
>* [[!DNL LY Ads] configuración del grupo de anuncios](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-settings-ly.md)
>* [[!DNL Microsoft Advertising] configuración del grupo de anuncios](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-settings-microsoft.md)
>* [[!DNL Yandex] configuración del grupo de anuncios](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-settings-yandex.md)
