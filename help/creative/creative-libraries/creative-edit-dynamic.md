---
title: Editar un elemento creativo dinámico en una biblioteca creativa
description: Aprenda a editar un elemento creativo dinámico en una biblioteca creativa.
feature: Creative Dynamic Creatives
exl-id: b75b9aeb-ffd0-4b86-aa7a-bd6a22e7a8e4
TQID: 'https://experienceleague.adobe.com/QoQ5p4sFV-ARIMNDbPkp7axfqkVEC3sxJ6MTlPIG22Y'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: d0d9f2ed-c163-44e1-97a1-4ace121416b8
    internal-label: Creative
subfeature_v2:
  - id: d70c54b0-f069-4a3c-8056-7069a25e110c
    internal-label: Creative Dynamic Creatives
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
source-git-commit: b7bf89dafd678490acc0749e2755ea7f0fec67f4
workflow-type: tm+mt
source-wordcount: '546'
ht-degree: 0%
---
# Editar un elemento creativo dinámico en una biblioteca creativa

## Desde la nueva IU

1. Abra la configuración creativa:

   * Desde una biblioteca creativa:

     1. En el menú principal, haga clic en **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

     1. Abra la biblioteca mediante cualquiera de estos métodos:

        * Haga clic en el nombre de la biblioteca.

        * Junto al nombre de la biblioteca, haga clic en **[!UICONTROL ...]** > **[!UICONTROL Open]**.

     1. En la ficha **[!UICONTROL Creatives]**, haga clic en **[!UICONTROL ...]** junto al nombre del elemento creativo y, a continuación, haga clic en **[!UICONTROL Edit]**.

   * De [!UICONTROL Creative Studio]:

     1. En el menú principal, haga clic en **[!UICONTROL Creative]>[!UICONTROL Creative Studio]**.

     1. En la ficha **[!UICONTROL Creatives]**, mantenga el cursor sobre la tarjeta creativa y haga clic en **[!UICONTROL ...]** > **[!UICONTROL Edit]**.

        Se abrirá un editor de pantalla completa con una vista previa del anuncio a la izquierda y un panel de configuración a la derecha.

1. Edite la configuración creativa mediante las fichas **[!UICONTROL Details]** y **[!UICONTROL Attribute Mapping]**:

   Ficha **[!UICONTROL Details]**:

   * **[!UICONTROL Advertiser]**, **[!UICONTROL Ad Library]** y **[!UICONTROL Ad template]** son de solo lectura.
   * **[!UICONTROL Dynamic creative name]:** El nombre para mostrar del creativo.
   * **[!UICONTROL Number of cards]:** Número de ofertas de catálogo incluidas en cada combinación de publicidad (1-50).
   * (Opcional) En **[!UICONTROL Catalogs]**, actualice la selección del catálogo:
     * Use **[!UICONTROL Catalog template]** para filtrar los catálogos disponibles. Si lo desea, puede descargar el archivo de plantilla haciendo clic en **[!UICONTROL Download feed template]**.
     * Busque y seleccione catálogos de la lista, o cargue un nuevo archivo de catálogo arrastrándolo al área de carga o haciendo clic en **[!UICONTROL Browse Files]** (formatos admitidos: JPG, PNG, JPEG, XLS, XLSX, CSV, TSV, ZIP, MP4; máximo 25 MB; un archivo a la vez). Los catálogos cargados están etiquetados **(cargados)** en la lista de chips.

     Todos los catálogos deben pertenecer a la misma familia de plantillas de catálogo.

   Ficha **[!UICONTROL Attribute Mapping]**:

   * En **[!UICONTROL Targeting]**, seleccione al menos un origen de datos: **[!UICONTROL Profile data]**, **[!UICONTROL Geographic data]**, **[!UICONTROL Data pass]** o **[!UICONTROL Audience Segment]**.
   * En **[!UICONTROL Attribute Mapping]**, actualice la asignación de cada nombre de capa de plantilla a la etiqueta de columna de catálogo correspondiente.

1. Haga clic en **[!UICONTROL Update Creative]**.

## Desde la IU heredada

1. En el menú principal, haga clic en **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

1. Haga clic en **[!UICONTROL Switch to classic UI]**.

1. Haga clic en el nombre de la biblioteca.

1. Mantenga el cursor sobre la fila creativa y haga clic en **[!UICONTROL Edit]**.

1. Editar la [configuración de publicidad dinámica](creative-settings-dynamic.md).

1. Haga clic en **[!UICONTROL Continue]** para previsualizar los elementos creativos que desea generar. Puede realizar cualquiera de las siguientes acciones dentro de la vista previa:

   * Para filtrar los elementos creativos por catálogo, valor de filtro <!-- explain more--> y tamaño de anuncio, utilice los filtros situados encima del área de vista previa.

   * Para buscar un producto por su ID único, vaya al campo de búsqueda debajo del área de vista previa.

   * Para cambiar las columnas mostradas, haga clic en ![Filtro de columna](/help/creative/assets/custom-columns.png "Filtro de columna") debajo del área de vista previa.

   * Para obtener una vista previa de un elemento creativo específico, active la casilla de verificación de la fila.

   * Cambiar el contenido:

     * (Solo anuncios de visualización) Para editar el valor de una celda dentro de la tabla, haga clic dentro de la celda y edite el valor. Haga clic fuera de la celda o presione la tecla **[!DNL Enter]** para guardar los cambios.

     * Para marcar un solo producto como predeterminado <!--Explain what this means. -->, mantenga el cursor sobre la fila y haga clic en **[!UICONTROL ...]** > **[!UICONTROL Set as Default]**.

     * (Cuando el anuncio incluya más de una oferta) Para marcar varios productos como predeterminados, seleccione las filas (hasta el número de ofertas) y haga clic en **[!UICONTROL Set as Default]** en la barra de herramientas de acciones por lotes.

     * Para eliminar un producto del catálogo, mantenga el cursor sobre la fila y haga clic en **[!UICONTROL ...]** > **[!UICONTROL Delete Row]**.

     * (Cuando el anuncio incluya más de una oferta) Para eliminar varios productos del catálogo, seleccione las filas (hasta el número de ofertas) y haga clic en **[!UICONTROL Delete Row]** en la barra de herramientas de acciones por lotes.

1. Guarde a los creativos:

   * Para guardar los anuncios y agregarlos a un [paquete creativo](bundle-manage.md) de la biblioteca:

     1. Haga clic en **[!UICONTROL Save and Attach to Bundle]**.

     1. Haga clic **[!UICONTROL Save]** para guardar los anuncios.

     1. Seleccione los paquetes y haga clic en **[!UICONTROL Attach Creative to Bundles]**.

   * Para guardar los anuncios y salir de la configuración, haga clic en **[!UICONTROL Save]** y, a continuación, haga clic de nuevo en **[!UICONTROL Save]**.

>[!MORELIKETHIS]
>
>* [Configuración creativa dinámica](creative-settings-dynamic.md)
>* [Agregar elementos creativos dinámicos a una biblioteca creativa](creative-add-dynamic.md)
>* [Ver el registro de cambios de un elemento creativo](/help/creative/creative-libraries/creative-view-change-log.md)
>* [Flujos de trabajo para anuncios dinámicos](/help/creative/introduction/workflow-dynamic-ads.md)
