---
title: Personalización de las direcciones URL de seguimiento de una experiencia sin segmentación
description: Aprenda a personalizar las direcciones URL de seguimiento para cada elemento creativo de una experiencia sin segmentación del árbol de decisiones.
feature: Creative Experiences
exl-id: 03a10285-c0df-4bc3-92c7-c1c2ea3f8129
source-git-commit: 5d8b511708008c77e817ccdb00ae02c158dfe63e
workflow-type: tm+mt
source-wordcount: '371'
ht-degree: 0%

---

# Personalización de las direcciones URL de seguimiento de una experiencia sin segmentación del árbol de decisiones

*Beta cerrada*

En el caso de las experiencias sin segmentación del árbol de decisión, puede crear hasta cinco direcciones URL de seguimiento de impresiones personalizadas, cinco direcciones URL de seguimiento de clics personalizadas y una dirección URL de página de aterrizaje personalizada para cada elemento creativo individual utilizado para la etiqueta de experiencia publicitaria. Puede personalizar las direcciones URL de seguimiento desde [!UICONTROL Tag Manager].

Las direcciones URL personalizadas solo se usan para los anuncios creados a partir de la etiqueta de experiencia publicitaria y no se guardan en la configuración creativa base de [!UICONTROL Creative Libraries].

1. En el menú principal, haga clic en **[!UICONTROL Creative]** > **[!UICONTROL Experiences]**.

1. Realice una de las siguientes acciones:

   * En la vista de tarjeta, haga clic en **[!UICONTROL ...]** junto al nombre de la experiencia y, a continuación, haga clic en **[!UICONTROL Tag Manager]**.

   * En la vista de tabla, mantenga el cursor sobre la fila, haga clic en **[!UICONTROL More]** y, a continuación, en **[!UICONTROL Tag Manager]**

1. (Si no existe una etiqueta para el tamaño del anuncio) Cree una etiqueta para el tamaño creativo aplicable.

   Puede crear una o más etiquetas para cada tamaño creativo utilizado para la experiencia.

   1. En la esquina superior derecha, haga clic en **[!UICONTROL Create Tag]**.

   1. Escriba un(a) **[!UICONTROL Tag name]** único(a) y seleccione **[!UICONTROL Tag size]**.

      Los tamaños de los elementos creativos de imagen predeterminados para la experiencia determinan los tamaños disponibles.

   1. Haga clic en **[!UICONTROL Create]**.

1. Mantenga el cursor sobre la fila de la etiqueta de publicidad aplicable y haga clic en ![Editar URL de seguimiento](/help/creative/assets/edit-gray.png "Editar URL de seguimiento") **[!UICONTROL Tracking URLs]**. <!-- For targeted experiences, this is "EDIT Tracking URLs" -->&lt;!— A partir del segundo semestre, el Administrador de etiquetas solo tiene una vista de lista, pero no de tarjeta. >

   Las pestañas [!UICONTROL Click Tracking URLs], [!UICONTROL Impression Tracking URLs] y [!UICONTROL Landing URLs] enumeran los nombres de todos los creativos en los tamaños aplicables en los paquetes asignados. Los tamaños de los elementos creativos de imagen predeterminados para la experiencia determinan los tamaños disponibles.<!-- There's no distinct "Creative Sizes" setting. -->

1. En las fichas **[!UICONTROL Click Tracking URLs]**, **[!UICONTROL Impression Tracking URLs]** y **[!UICONTROL Landing URLs]**, haga lo siguiente para cada elemento creativo según sea necesario:

   1. Expanda la fila para el creativo.

   1. Realice una de las siguientes acciones:

      * Para añadir o editar una URL personalizada, introduzca la URL en el campo de entrada.

      * Para agregar otra dirección URL personalizada, haga clic en **[!UICONTROL +]** e introduzca la dirección URL en el campo de entrada.

      * Para quitar una dirección URL personalizada, mantén el cursor sobre la fila creativa y haz clic en ![Eliminar](/help/creative/assets/delete.png "Eliminar").

      Puede incluir hasta cinco direcciones URL de seguimiento de impresiones personalizadas, cinco direcciones URL de seguimiento de clics personalizadas y una dirección URL de página de aterrizaje personalizada.

1. Haga clic en **[!UICONTROL Save]**.

>[!MORELIKETHIS]
>
>* [Asignar elementos creativos a una etiqueta de anuncio para experiencias sin segmentación](experience-tag-assign-creatives.md)
>* [Personalice las direcciones URL de seguimiento para una experiencia con segmentación en el árbol de decisiones](experience-tracking-urls-targeting.md)
