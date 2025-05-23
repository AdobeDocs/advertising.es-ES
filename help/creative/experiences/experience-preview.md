---
title: Previsualización de una experiencia
description: Obtenga información sobre cómo previsualizar los elementos creativos en una experiencia publicitaria.
feature: Creative Experiences
exl-id: 2ac8f580-7d3d-4de6-ba14-5d72b30188d7
source-git-commit: 278104fb09797e781894a6894a0a53db4a8e28f8
workflow-type: tm+mt
source-wordcount: '556'
ht-degree: 0%

---

# Previsualización de una experiencia

*Beta cerrada*

Puede obtener una vista previa de los elementos creativos con un tamaño de anuncio específico que los espectadores de destino verán para una experiencia, incluidos todos los hipervínculos. En el caso de las experiencias con segmentación del árbol de decisiones, puede previsualizar un solo elemento creativo, los elementos creativos de una rama concreta (tipo de objetivo) o todos los elementos creativos de la experiencia. Para las experiencias sin segmentación del árbol de decisiones, puede previsualizar un solo elemento creativo. <!-- verify -->

* Al previsualizar todos los creativos de la experiencia o de una rama en particular, se muestran todos los creativos aplicables.

* Cuando previsualiza un solo elemento creativo y varios se ajustan a los criterios, el elemento creativo que ve cada vez que actualiza la vista previa se basa en la configuración de rotación del anuncio para la experiencia:

   * Para la rotación de anuncios algorítmicos, el elemento creativo se selecciona en función del objetivo de optimización.

   * Para la rotación de anuncios ponderada, el creativo se selecciona en función de las ponderaciones especificadas (por ejemplo, una probabilidad del 80 % de que se muestre el Creative A y una probabilidad del 20 % de que se muestre el Creative B) cada vez.

   * Para la rotación de anuncios programada, se muestra el primer elemento creativo de la programación. Puede seguir actualizando la vista previa para continuar con la secuencia.<!-- Refresh isn't there as of 2/3 -->

## Vista previa de elementos creativos en una experiencia con segmentación en árbol de decisiones

1. En el menú principal, haga clic en **[!UICONTROL Creative]** > **[!UICONTROL Experiences]**.

1. (Opcional) [Personalice la vista](/help/creative/introduction/customize-data-views.md) para incluir experiencias específicas.

1. Realice una de las siguientes acciones:

   * En la vista de tarjeta, haga clic en **[!UICONTROL ...]** junto al nombre de la experiencia y, a continuación, haga clic en **[!UICONTROL Preview]**.

   * En la vista de tabla, mantenga el cursor sobre la fila, haga clic en **[!UICONTROL More]** y, a continuación, en **[!UICONTROL Preview]**.

1. Seleccione los creativos que desea previsualizar:

   * Para previsualizar un solo elemento creativo:

      1. Haga clic en **[!UICONTROL Creative]**.

      1. Seleccione el tamaño del anuncio.

      1. En la sección [!UICONTROL Decision Tree Targeting], seleccione el destino creativo.

   * Para obtener una vista previa de los elementos creativos de una rama concreta:

      1. Haga clic en **[!UICONTROL Particular branch]**.

      1. Seleccione el tamaño del anuncio.

     <!-- I don't see this as of 2/3:
     1. Select whether to group the creatives by Rotation Type or Ad Size.
     -->

      1. Seleccione el destinatario creativo.

   * Para obtener una vista previa de todos los creativos de la experiencia, haga clic en **[!UICONTROL Entire Tree]**.

     <!-- I don't see this as of 2/3:
     1. Click **[!UICONTROL Entire Tree]**.
     1. Select the ad size.
     1. Select whether to group the creatives by Rotation Type or Ad Size.
     -->

1. (Opcional) Para incluir el nombre del creativo, el tipo y tamaño del creativo, la dirección URL de la página de aterrizaje o las direcciones URL de los clics, y los atributos flexibles debajo de cada creativo, seleccione **[!UICONTROL Display Creative Metadata]**.

1. Haga clic en **[!UICONTROL Preview]**.

1. (Vista previa solo para creativos; opcional) En la barra de herramientas, haga clic en **[!UICONTROL Refresh]** para obtener una vista previa de los elementos creativos adicionales que se puedan mostrar, según la configuración de rotación del anuncio.<!-- I don't see this as of 2/3 -->

1. (Opcional) Para copiar una URL de demostración de la experiencia para compartirla con otras personas sin iniciar sesión en [!DNL Creative]:

   1. En la parte superior derecha de la vista previa, haga clic en ![Compartir](/help/creative/assets/share.png "Compartir").

   1. En el cuadro de diálogo [!UICONTROL Share Demo URL], haga clic en **[!UICONTROL Copy]** para copiar la dirección URL en el portapapeles de modo que pueda compartirla con otra persona.

## Vista previa de elementos creativos en una experiencia sin segmentación de árbol de decisiones

1. En el menú principal, haga clic en **[!UICONTROL Creative]** > **[!UICONTROL Experiences]**.

1. (Opcional) [Personalice la vista](/help/creative/introduction/customize-data-views.md) para incluir experiencias específicas.

1. Realice una de las siguientes acciones:

   * En la vista de tarjeta, haga clic en **[!UICONTROL ...]** junto al nombre de la experiencia y, a continuación, haga clic en **[!UICONTROL Preview]**.

   * En la vista de tabla, mantenga el cursor sobre la fila, haga clic en **[!UICONTROL More]** y, a continuación, en **[!UICONTROL Preview]**.

1. (Opcional) Limite la lista de creativos seleccionando un tamaño de creativo específico.

   De forma predeterminada, se muestran los elementos creativos de todos los tamaños.

1. Haga clic en el nombre de una etiqueta de anuncio para expandir la fila y previsualizar los elementos creativos.

1. (Opcional) Para ir a la página de aterrizaje de un creativo, haga clic en el creativo.

   <!-- Verify:  Will the creative click be tracked like a regular ad click but not linked to a publisher and placement? Explain effect/consequences. -->

1. (Opcional) Para copiar una URL de demostración de la experiencia para compartirla con otras personas sin iniciar sesión en [!DNL Creative]:

   1. En la parte superior derecha de la vista previa, haga clic en ![Compartir](/help/creative/assets/share2.png "Compartir").

   1. En el cuadro de diálogo [!UICONTROL Share Demo URL], haga clic en **[!UICONTROL Copy]** para copiar la dirección URL en el portapapeles de modo que pueda compartirla con otra persona.

>[!MORELIKETHIS]
>
>* [Crear una experiencia con segmentación de árbol de decisión](experience-create-targeting.md)
>* [Crear una experiencia sin segmentación de árbol de decisión](/help/creative/experiences/experience-create-no-targeting.md)
