---
title: Añadir creativos dinámicos a una biblioteca creativa
description: Aprenda a añadir creativos dinámicos a una biblioteca creativa.
feature: Creative Dynamic Creatives
exl-id: 26162314-bdaa-4d1c-b0c2-696ec6dbb138
source-git-commit: 84ef17f304fbd9eda82682368dfd59727971281d
workflow-type: tm+mt
source-wordcount: '516'
ht-degree: 0%

---

# Añadir creativos dinámicos a una biblioteca creativa

Añade creativos dinámicos a tus [bibliotecas creativas](creative-library-manage.md) para usarlos con [experiencias publicitarias](/help/creative/experiences/experience-about.md) dinámicas. Puede crear un único anuncio de HTML estático5 o anuncios de HTML5 dinámicos a partir de una única plantilla de anuncio. Para anuncios dinámicos de HTML5, utilice recursos de catálogos especificados creados a partir de archivos de fuente.

>[!PREREQUISITES]
>
>Antes de añadir elementos creativos dinámicos a una biblioteca creativa, debe completar otros pasos, como crear la plantilla de publicidad, cargar recursos y (anuncios dinámicos de HTML5) crear una plantilla de fuente y un catálogo. Consulte &quot;[Flujos de trabajo para anuncios dinámicos](/help/creative/introduction/workflow-dynamic-ads.md)&quot;.

<!-- This does't work for me 9/24 -- I still have to select a catalog:

## Add dynamic creatives using a static HTML5 ad template

1. In the main menu, click **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

1. Click the library name.

1. On the **[!UICONTROL Creatives]** tab, click **[!UICONTROL Create]** > **[!UICONTROL Creatives]** > **[!UICONTROL Dynamic Ad]**.

1. Specify the [dynamic ad settings](/help/creative/creative-libraries/creative-settings-dynamic.md#dynamic-ad-settings-static-html5):

   1. On the [!UICONTROL Basic Details] tab, specify the ad details and the clickURL.

   1. Click **[!UICONTROL Process]**.

   1. On the [!UICONTROL Attributes Details] tab, specify the dynamic ad attributes.

1. Click **[!UICONTROL Save]**.

-->

## Añada creativos dinámicos mediante una plantilla de anuncio dinámica de HTML5

1. Realice una de las acciones siguientes:

   * Desde una biblioteca creativa:

      1. En el menú principal, haga clic en **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

      1. Haga clic en el nombre de la biblioteca.

      1. En la ficha **[!UICONTROL Creatives]**, haga clic en **[!UICONTROL Create]** > **[!UICONTROL Creatives]** > **[!UICONTROL Dynamic Ad]**.

   * Desde una plantilla de anuncio:

      1. En el menú principal, haga clic en **[!UICONTROL Creative]** > **[!UICONTROL Ad Templates]**.

      1. Mantenga el cursor sobre la fila de la plantilla de anuncios y haga clic en **[!UICONTROL Create Dynamic Ad]**.

1. Especifique la [configuración de publicidad dinámica](/help/creative/creative-libraries/creative-settings-dynamic.md):

   1. Especifique los detalles básicos del anuncio, incluido el tipo creativo.

   1. Seleccione la plantilla de anuncio que desea utilizar para los creativos.

      Utilice una plantilla de anuncio de HTML5 para los anuncios en pantalla y una plantilla de anuncio de vídeo para los anuncios de vídeo.

   1. Seleccione el catálogo desde el que desea crear los anuncios.

   1. Seleccione los criterios para las filas de catálogo que se utilizarán para crear anuncios.

   1. Asigne cada atributo (campo de anuncio dinámico) de la plantilla de anuncio especificada a una columna del archivo de fuente especificado (etiqueta de catálogo) o introduzca valores estáticos.

   1. Haga clic en **[!UICONTROL Continue]** para obtener una vista previa de los creativos que se van a generar. Puede realizar cualquiera de las siguientes acciones en la previsualización:

      * Para filtrar los creativos por catálogo, filtrar el valor <!-- explain more--> y el tamaño del anuncio, utilice los filtros situados sobre el área de vista previa.

      * Para buscar un producto por su ID exclusivo, en el campo de búsqueda situado debajo del área de previsualización.

      * Para cambiar las columnas que se muestran, haga clic en ![Filtro de columna](/help/creative/assets/custom-columns.png "Filtro de columna") debajo del área de vista previa.

      * Para obtener una vista previa de un elemento creativo específico, active la casilla de verificación de la fila.

      * Cambiar el contenido:

         * (Solo anuncios de visualización) Para editar el valor de una celda dentro de la tabla, haga clic dentro de la celda y edite el valor. Haga clic fuera de la celda o presione la tecla **[!DNL Enter]** para guardar los cambios.

         * Para marcar un solo producto como predeterminado <!--Explain what this means. -->, mantenga el cursor sobre la fila y haga clic en **[!UICONTROL ...]** > **[!UICONTROL Set as Default]**.

         * (Cuando el anuncio incluya más de una oferta) Para marcar varios productos como predeterminados, seleccione las filas (hasta el número de ofertas) y haga clic en **[!UICONTROL Set as Default]** en la barra de herramientas de acciones por lotes.

      * Para eliminar un producto del catálogo, mantenga el cursor sobre la fila y haga clic en **[!UICONTROL ...]** > **[!UICONTROL Delete Row]**.

      * (Cuando el anuncio incluya más de una oferta) Para eliminar varios productos del catálogo, seleccione las filas (hasta el número de ofertas) y haga clic en **[!UICONTROL Delete Row]** en la barra de herramientas de acciones en bloque.

1. Guarde a los creativos:

   * Para guardar los anuncios y añadirlos a un [paquete creativo](/help/creative/creative-libraries/bundle-manage.md) en la biblioteca:

      1. Haga clic en **[!UICONTROL Save and Attach to Bundle]**.

      1. Haga clic **[!UICONTROL Save]** para guardar los anuncios.

      1. Seleccione los paquetes y haga clic en **[!UICONTROL Attach Creative to Bundles]**.

   * Para guardar los anuncios y salir de la configuración, haga clic en **[!UICONTROL Save]** y, a continuación, haga clic de nuevo en **[!UICONTROL Save]**.

>[!MORELIKETHIS]
>
>* [Configuración creativa dinámica](creative-settings-dynamic.md)
>* [Editar un elemento creativo dinámico en una biblioteca creativa](creative-edit-dynamic.md)
>* [Ver el registro de cambios de un elemento creativo](/help/creative/creative-libraries/creative-view-change-log.md)
>* [Flujos de trabajo para anuncios dinámicos](/help/creative/introduction/workflow-dynamic-ads.md)
