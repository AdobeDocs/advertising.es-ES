---
title: Acerca de la personalización de datos en vistas de administración de campañas
description: Obtenga información acerca de los tipos de datos que puede personalizar en las vistas de datos de Campaign.
exl-id: 89f36865-9275-494e-ac33-d41fa30faa2a
feature: Search Common Tasks, Search Custom Data Views
TQID: 'https://experienceleague.adobe.com/PnBql37yqK03DWH2OhLf8hnCBPOwFAVZxD65NNZu0VU'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: bcc57258-3285-5d02-a731-d86f57a58c47
    internal-label: Search Common Tasks
  - id: d6e2ef48-fac7-5a4a-96ff-9ac0264dc826
    internal-label: Search Custom Data Views
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
source-git-commit: 972ed9c0662fc3b74bc5c3597f010170fbce69d7
workflow-type: tm+mt
source-wordcount: '672'
ht-degree: 0%
---
# Acerca de la personalización de datos en vistas de administración de campañas

En la mayoría de las vistas de datos de campaña, puede personalizar los datos que aparecen en la tabla de datos. Puede personalizar los datos de las siguientes maneras:

* [Edite la configuración de toda la vista predeterminada](/help/search-social-commerce/common-tasks/data-views/custom-default-views-manage.md##view-edit) para una vista de entidad específica (como [!UICONTROL Campaigns]) con el fin de incluir un orden de columna específico, filtros, intervalo de fechas, regla de atribución y mucho más, y aplique la configuración temporalmente o guárdela. También puede [crear vistas personalizadas adicionales](/help/search-social-commerce/common-tasks/data-views/custom-default-views-manage.md#create-custom-view), [clonar vistas existentes](/help/search-social-commerce/common-tasks/data-views/custom-default-views-manage.md#view-clone) y [aplicar cualquiera de sus vistas](/help/search-social-commerce/common-tasks/data-views/custom-default-views-manage.md#apply-a-default-or-custom-view).

* [Cambie las columnas y su orden](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-set-edit-sort-icon.md) mediante el control [!UICONTROL Custom Columns] de la barra de herramientas. En la nueva IU, si la barra de herramientas es demasiado estrecha para mostrar el control, haga clic en **[!UICONTROL Actions]>[!UICONTROL Custom Columns]**. También puede [cambiar rápidamente solo las columnas](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-set-edit-column-heading.md) de cualquier encabezado de columna de la vista.

* (Solo interfaz de usuario heredada) [Desde el panel de navegación izquierdo](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/filter-using-left-panel.md), puede:

  * Examine o busque entidades por red de anuncios y filtre por el estado de la entidad y el estado de la cuenta, la campaña y el grupo de anuncios o conjunto de anuncios. Haga clic en cualquier entidad o grupo de entidades del panel para cargar una vista de las entidades secundarias (por ejemplo, haga clic en el nombre de una campaña para ver sus grupos de anuncios secundarios).

  * Examine o busque campañas por portafolio o grupo de portafolios, y filtre por el estado de la entidad y el estado del grupo de portafolios, portafolios y campaña. Haga clic en cualquier grupo del portafolio, portafolio o campaña del panel para cargar datos del grupo del portafolio, portafolio o campaña dentro de la vista de entidad actual.

  * Acceda, edite y restablezca sus vistas predeterminadas; y acceda, edite y elimine sus vistas personalizadas. Al hacer clic en cualquier nombre de vista, se carga la vista adecuada.

* Aplique filtros a cualquier columna de datos disponible para cambiar los datos que se muestran en la pestaña actual. Puede crear los filtros [de los encabezados de columna](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-column-heading.md) o [de un botón de la barra de herramientas](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-toolbar.md). En las vistas de administración de campañas, los filtros se mantienen según corresponda cuando se abren entidades secundarias. Por ejemplo, si ve campañas con \> 100 clics y luego abre un grupo de anuncios dentro de esa campaña, solo se muestran los grupos de anuncios con \> 100 clics.

* [Cambie el intervalo de fechas](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/date-filter.md) utilizado en todas las vistas predeterminadas y personalizadas para las que no ha guardado intervalos de fechas específicos.

* [Vuelva a ordenar los datos](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-sort.md) según los valores de una columna específica.

* Controle si desea mostrar 25 filas, 50 filas, 100 filas, (solo interfaz de usuario heredada) 200 filas o (solo interfaz de usuario heredada) [!UICONTROL Continuous Scroll] en la parte inferior de cualquier página.

## (Nueva IU) Controles de tabla de datos {#data-table-tools-new-ui}

Utilice la barra de herramientas situada encima de la tabla de datos para administrar los datos y cambiar cómo se muestran. Las herramientas disponibles dependen de la vista y de los permisos.

Si la barra de herramientas es demasiado estrecha para mostrar una herramienta, búsquela en el menú **[!UICONTROL Actions]**.

Si está disponible, puede:

* Seleccione *[!UICONTROL Click Date]* o *[!UICONTROL Transaction Date]* de [!UICONTROL Conversion based on] para controlar cómo se generan los informes de los datos de conversión.

* Compare el rendimiento durante dos períodos de tiempo y elija cómo mostrar la diferencia. Consulte &quot;[Filtrar datos por intervalo de fechas](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/date-filter.md#compare-periods-new-ui)&quot;.

* Activar o desactivar el espaciado compacto de la tabla con **[!UICONTROL Compressed Mode]** en la barra de herramientas o en el menú **[!UICONTROL Actions]**.

  El botón de la barra de herramientas está seleccionado cuando el modo comprimido está activado. En [!UICONTROL Actions], un modificador indica el estado actual.

* Mostrar u ocultar gráficos con **[!UICONTROL Charts]** en la barra de herramientas o el menú **[!UICONTROL Actions]**.

  El botón de la barra de herramientas se selecciona cuando se muestran gráficos. En [!UICONTROL Actions], un modificador indica si se muestran gráficos. Vuelva a hacer clic en el control para ocultar los gráficos.

## (Nueva IU) Anchos de columna y valores de tabla {#column-widths-values-new-ui}

En las tablas de datos de campaña:

* Cambiar el tamaño de una columna arrastrando el límite entre los encabezados de columna. También puede cambiar el tamaño de [columnas bloqueadas](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-set-edit-lock-unlock.md) aptas sin desbloquearlas primero. Las anchuras mínimas ayudan a mantener los valores legibles. Algunas columnas de iconos y acciones tienen anchuras fijas y no se pueden cambiar de tamaño.

* Mantenga el cursor sobre un nombre de entidad truncado para ver el nombre completo.

* Para abrir los detalles de una entidad cuyo nombre es un vínculo, presione **Tab** hasta que se resalte el nombre y, a continuación, presione **Entrar**.

* Un guión corto (-) indica un valor que falta, que es NULL o que no es aplicable. Los valores cero y falso permanecen visibles.
