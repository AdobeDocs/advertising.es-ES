---
title: (Nueva IU) Administrar plantillas de informe
description: Obtenga información sobre cómo crear, ver, editar y eliminar plantillas de informes reutilizables para informes programados y bajo demanda.
feature: Search Reports
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: 9166e3e1-13c1-5edf-bc2a-c6e22231df68
    internal-label: Search Reports
source-git-commit: eb12699872b7c89240f5340cd3b0a251c9c08366
workflow-type: tm+mt
source-wordcount: '765'
ht-degree: 0%
---
# (Nueva IU) Administrar plantillas de informe

Las plantillas de informe son diseños de informe predefinidos que se pueden reutilizar cuando se generan la mayoría de los informes. El uso de plantillas le ahorra tiempo si desea utilizar parámetros no predeterminados, ejecutar variaciones del mismo informe o ejecutar el mismo informe según una programación regular. Las plantillas guardadas están disponibles en la ficha **[!UICONTROL Templates]** de **[!UICONTROL Reports]>[!UICONTROL Reports]**.

Puede mantener hasta 100 plantillas a la vez.

Para ver los datos se requiere el permiso [!UICONTROL View Scheduled Reports]. Crear, duplicar, editar, ejecutar y eliminar plantillas, así como copiar datos de filas, requiere el permiso [!UICONTROL Edit Scheduled Reports]. Solo puede editar las plantillas que haya creado.

## Acciones disponibles

* [Crear una plantilla de informe](#template-create) como nueva plantilla o basada en una plantilla existente.

* [Ver la configuración de una plantilla de informe sin cambiar el original](#template-view).

* [Editar una plantilla de informe](#template-edit), incluida su programación.

* [Ejecutar informes bajo demanda para plantillas especificadas](#template-run).

* [Eliminar plantillas de informe](#template-delete).

* [Copie todos los datos de las filas seleccionadas en el portapapeles](#copy-to-clipboard).

## Creación de una plantilla de informe {#template-create}

1. En el menú principal, haga clic en **[!UICONTROL Reports]>[!UICONTROL Reports]**.

1. Haga clic en la ficha **[!UICONTROL Templates]**.

1. Realice una de las acciones siguientes:

   * Para crear una nueva plantilla, haga clic en **[!UICONTROL Create Template]**. En el panel **[!UICONTROL Create a New Template]**, seleccione la categoría y el tipo de informe, y luego haga clic en **[!UICONTROL Proceed]**.

   * Para crear una plantilla basada en una plantilla existente, mantenga el cursor sobre la fila de la plantilla y haga clic en ![Configuración de plantilla](/help/search-social-commerce/assets/settings-new.png "Configuración de plantilla") **[!UICONTROL Template Settings]** o **[!UICONTROL ...]>[!UICONTROL Duplicate]**.

1. Escriba un(a) **[!UICONTROL Report Name]** único(a) para la plantilla y asegúrese de que **[!UICONTROL Save as Template]** está habilitado.

   La configuración está habilitada de manera predeterminada al comenzar con **[!UICONTROL Create Template]**. Si lo deshabilita, la acción final cambia a **[!UICONTROL Run Report]**, lo que genera un informe en lugar de guardar una plantilla.

1. Configure las opciones del informe para [informes básicos y avanzados](/help/search-social-commerce/new-ui/reports/management/basic-advanced/basic-advanced-report-settings.md), [informes de asistencia](/help/search-social-commerce/new-ui/reports/management/assist/assist-report-settings.md), [informes de precisión de modelo](/help/search-social-commerce/new-ui/reports/management/model-accuracy/model-accuracy-report-settings.md) o [informes de especialidad](/help/search-social-commerce/new-ui/reports/management/specialty/specialty-report-settings.md).

   Haga clic en **[!UICONTROL Next]** para desplazarse entre las secciones de configuración.

1. (Opcional) Para generar informes automáticamente, configure **[!UICONTROL Frequency]** y la configuración de envío en **[!UICONTROL Scheduling]**.

1. Haga clic en **[!UICONTROL Create]**.

También puede guardar una plantilla mientras [crea un informe desde la ficha Informes más recientes](/help/search-social-commerce/new-ui/reports/management/report-manage.md) habilitando **[!UICONTROL Save as Template]** antes de enviar la configuración del informe.

## Ver la configuración de una plantilla de informe {#template-view}

Para inspeccionar la configuración sin cambiar la plantilla original, abra un duplicado. Esto requiere el permiso [!UICONTROL Edit Scheduled Reports]. Al abrir el duplicado, no se guarda una plantilla nueva.

1. En el menú principal, haga clic en **[!UICONTROL Reports]>[!UICONTROL Reports]**.

1. Haga clic en la ficha **[!UICONTROL Templates]**.

1. Mantenga el cursor sobre la fila de la plantilla y haga clic en ![Configuración de plantilla](/help/search-social-commerce/assets/settings-new.png "Configuración de plantilla") **[!UICONTROL Template Settings]**.

1. Revise la configuración del informe.

1. Haga clic en **[!UICONTROL Cancel]** cuando haya terminado. Si se le solicita que descarte la instalación, haga clic en **[!UICONTROL Discard]**.

Para guardar una copia, siga el [procedimiento de creación de plantillas](#template-create).

## Edición de una plantilla de informe {#template-edit}

Puede cambiar la configuración y la programación de cualquier plantilla que haya creado. Los cambios se aplican a los informes generados a partir de la plantilla en el futuro.

1. En el menú principal, haga clic en **[!UICONTROL Reports]>[!UICONTROL Reports]**.

1. Haga clic en la ficha **[!UICONTROL Templates]**.

1. Seleccione la casilla de verificación situada junto a una plantilla que haya creado.

1. En la barra de herramientas de acciones masivas, haga clic en **[!UICONTROL Edit]**.

   [!UICONTROL Edit] no está disponible cuando se seleccionan varias plantillas o la plantilla seleccionada fue creada por otro usuario.

1. Cambie la configuración del informe. Para agregar, cambiar o quitar una programación, edite **[!UICONTROL Frequency]** en **[!UICONTROL Scheduling]**.

   Seleccione una frecuencia diaria, semanal o mensual para los informes programados. Para quitar una programación recurrente, seleccione **[!UICONTROL Now]**.

   **[!UICONTROL Save as Template]** y **[!UICONTROL Type]** son de solo lectura al editar una plantilla existente. No es necesario que vuelva a habilitar [!UICONTROL Save as Template].

1. Haga clic en **[!UICONTROL Save]**.

## Ejecutar informes bajo demanda para plantillas especificadas {#template-run}

Puede ejecutar informes para una o más plantillas en cualquier momento.

1. En el menú principal, haga clic en **[!UICONTROL Reports]>[!UICONTROL Reports]**.

1. Haga clic en la ficha **[!UICONTROL Templates]**.

1. Realice una de las acciones siguientes:

   * (Para ejecutar una sola plantilla):

     1. Abra el menú de la fila de la plantilla y seleccione **[!UICONTROL Run]**.

     1. En el mensaje de confirmación, haga clic en **[!UICONTROL Confirm]**.

   * (Para ejecutar una o más plantillas):

     1. Active la casilla de verificación situada junto a cada plantilla que desee ejecutar.

     1. En la barra de herramientas de acciones masivas, haga clic en **[!UICONTROL Run]**.

     1. En el mensaje de confirmación, haga clic en **[!UICONTROL Confirm]**.

También puede ejecutar una plantilla mientras la edita si hace clic en **[!UICONTROL Run Report]** y, a continuación, en **[!UICONTROL Confirm]**. Guarde primero los cambios; esta acción ejecuta la plantilla guardada.

## Eliminar plantillas de informe {#template-delete}

Puede eliminar cualquier plantilla de informe disponible. Cuando se elimina una plantilla que incluye una programación, ese informe no se genera en el futuro.

1. En el menú principal, haga clic en **[!UICONTROL Reports]>[!UICONTROL Reports]**.

1. Haga clic en la ficha **[!UICONTROL Templates]**.

1. Realice una de las acciones siguientes:

   * (Para eliminar una sola plantilla):

     1. Abra el menú de la fila de la plantilla y seleccione **[!UICONTROL Delete]**.

     1. En el mensaje de confirmación, haga clic en **[!UICONTROL Confirm]**.

   * (Para eliminar una o varias plantillas):

     1. Active la casilla de verificación situada junto a cada plantilla que desee eliminar.

     1. En la barra de herramientas de acciones masivas, haga clic en **[!UICONTROL Delete]**.

     1. En el mensaje de confirmación, haga clic en **[!UICONTROL Confirm]**.

## Copiar todos los datos de las filas seleccionadas en el portapapeles {#copy-to-clipboard}

Copie la información visible en las filas seleccionadas, según los filtros aplicados y las columnas visibles en la vista. La información se guarda como valores separados por tabulaciones (TSV).

1. Active la casilla de verificación situada junto a cada fila cuyos datos desee copiar.

1. En la barra de herramientas de acciones masivas, haga clic en **[!UICONTROL Copy]**.

1. En el mensaje de confirmación, haga clic en **[!UICONTROL Confirm]**.
