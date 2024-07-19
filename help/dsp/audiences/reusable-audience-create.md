---
title: Crear una audiencia reutilizable
description: Obtenga información sobre cómo crear audiencias reutilizables compuestas de segmentos de audiencia y otras audiencias guardadas.
feature: DSP Audiences
exl-id: 5f4a0abb-c285-4452-a6c3-a91d5281df9b
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '485'
ht-degree: 0%

---

# Crear una audiencia reutilizable

<!-- "Saved audience" is used in UI (where?), but "saved" is a state, not a type. "Reusable audience" sounds better in a description. "Audience template" isn't right, either, since it implies you can edit it on the fly to create a new, different audience. Some other term? -->

Puede guardar y administrar audiencias reutilizables, que son grupos de segmentos de audiencia e incluso otras audiencias guardadas, que puede utilizar como destinos o exclusiones para varias ubicaciones.

1. En el menú principal, haga clic en **[!UICONTROL Audiences]** > **[!UICONTROL All Audiences]**.

1. Sobre la tabla de datos, haga clic en **[!UICONTROL Create]**.

1. Escriba un(a) **[!UICONTROL Audience Name]** único.

1. (Opcional) Anule la selección de la opción **[!UICONTROL Share with all advertisers in my account]**.

   Al compartir una audiencia, esta pasa a estar disponible como objetivo o exclusión para todos los anunciantes de la cuenta. Sin embargo, los segmentos individuales de la audiencia solo están disponibles para los usuarios con los que se comparten los segmentos. Por ejemplo, si comparte una audiencia que contiene segmentos de Adobe Analytics con un anunciante que no está asignado a la misma cuenta de [!DNL Analytics], el segmento no se previsualiza en esa audiencia para ese anunciante. En la audiencia solo se obtiene una vista previa de los segmentos disponibles para ese anunciante.

1. Haga clic en **[!UICONTROL Save]**.

1. Cree la audiencia:

   >[!NOTE]
   >
   >A medida que crea la audiencia, se actualizan [datos detallados del tamaño de la audiencia](audience-about.md) en el panel derecho

   * Para crear manualmente la lógica del segmento, mediante los segmentos disponibles en las fichas [[!UICONTROL Third Party Segments], [!UICONTROL First Party Segments], [!UICONTROL Adobe Segments], [!UICONTROL Custom Segments] y [!UICONTROL Saved Audiences]](audience-settings.md), haga lo siguiente.

      * Para añadir el primer segmento, localícelo en el panel izquierdo y active la casilla de verificación situada junto al nombre del segmento.

      * Para agregar un segmento a un grupo de segmentos existente:

         1. Haga clic en el grupo de segmentos en el panel derecho.

         1. (Opcional) Cambie la lógica de grupo a *[!UICONTROL Include Any]*, *[!UICONTROL Include All]* o *[!UICONTROL Exclude All]*, según sea necesario.

            *[!UICONTROL Exclude All]* no está disponible para el primer grupo de segmentos. Para una audiencia que incluya solo exclusiones, genere esta audiencia como *[!UICONTROL Include Any]* y luego, dentro de una ubicación, seleccione esa audiencia en el menú Audiencias excluidas.

         1. Busque el nuevo segmento en el panel izquierdo y active la casilla de verificación situada junto al nombre del segmento.

            El grupo de segmentos se actualiza automáticamente con el nuevo segmento.

      * Para agregar un nuevo grupo de segmentos:

         1. Haga clic en **[!UICONTROL + New Group]** en el panel derecho.

         1. (Opcional) Cambie la lógica entre el grupo anterior y el nuevo a *[!UICONTROL And]* o *[!UICONTROL Or]*, según sea necesario.

         1. Busque los segmentos para el nuevo grupo en el panel izquierdo y seleccione las casillas de verificación situadas junto a los nombres de los segmentos.

         1. (Opcional) Cambie la lógica de grupo a *[!UICONTROL Include Any]*, *[!UICONTROL Include All]* o *[!UICONTROL Exclude All]*, según sea necesario.

   * Para usar la lógica de segmento de una audiencia existente:

      1. Copie la lógica de segmento de la audiencia existente de cualquiera de las siguientes maneras:

         * En la vista Todas las audiencias, mantenga el cursor sobre la fila de audiencias y haga clic en **[!UICONTROL More]** > **[!UICONTROL Copy to Clipboard]**.

         * En la configuración de la audiencia existente, en la parte superior del panel de lógica de segmento, haga clic en **[!UICONTROL More]** > **[!UICONTROL Copy to Clipboard]**.

         * En un editor de texto, cree manualmente la lógica del segmento usando ID de segmento alfanuméricos y [sintaxis booleana](audience-segment-logic-syntax.md), y cópielo en el portapapeles.

      1. Haga clic en **[!UICONTROL paste in an audience rule to begin building]**, pegue la lógica de segmento existente en el campo de entrada y, a continuación, haga clic en **[!UICONTROL Apply]**.

         >[!NOTE]
         >
         >Si la audiencia ya incluye cualquier lógica de segmento, al pegar la nueva lógica de segmento se sobrescribe la lógica existente.

1. Haga clic en **[!UICONTROL Create]**.

>[!MORELIKETHIS]
>
>* [Acerca de la administración de audiencias](audience-about.md)
>* [Configuración de audiencia](audience-settings.md)
>* [Sintaxis de la lógica de segmento de audiencia](audience-segment-logic-syntax.md)
>* [Proveedores de datos de terceros disponibles](third-party-data-providers.md)
>* [Crear e implementar un segmento personalizado](custom-segment-create.md)
>* [Crear e implementar un segmento [!UICONTROL CCPA Opt-Out-of-Sale]](ccpa-opt-out-segment-create.md)
>* [Configuración de ubicación](/help/dsp/campaign-management/placements/placement-settings.md)
