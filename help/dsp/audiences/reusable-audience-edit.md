---
title: Editar una audiencia reutilizable
description: Obtenga información sobre cómo editar una audiencia reutilizable.
feature: DSP Audiences
exl-id: 4de6b9a4-2907-474d-92bf-83686a1f0b31
source-git-commit: 0afe1d9985c1451c28943aaa17c7d6f8a73a95ef
workflow-type: tm+mt
source-wordcount: '459'
ht-degree: 0%

---

# Editar una audiencia reutilizable

Cuando edita una audiencia que se usa en ubicaciones u otras audiencias reutilizables, los cambios se aplican inmediatamente a esas ubicaciones y audiencias.<!-- verify -->

>[!NOTE]
>
>(Anunciantes para los que DSP convierte ID de correo electrónico con hash en segmentos de RampID de LiveRamp) Los segmentos de RampID de origen que no están adjuntos a una ubicación activa, programada o en pausa se pausan. El segmento se indica en la lista de segmentos como &quot;En pausa automática&quot;.

1. En el menú principal, haga clic en **[!UICONTROL Audiences]** > **[!UICONTROL All audiences]**.

1. Mantenga el cursor sobre la fila de audiencia y haga clic en **[!UICONTROL Edit]**.

1. Edite la configuración de audiencia de cualquiera de estas formas:

   >[!NOTE]
   >
   >Si edita la lógica del segmento de audiencia, se actualizarán los [datos detallados del tamaño de la audiencia](audience-about.md) en el panel derecho.

   * (Opcional) Para editar **[!UICONTROL Audience Name]**, haga clic en ![Editar](/help/dsp/assets/edit.png) junto al nombre de la audiencia, escriba un nombre de audiencia único y haga clic en **[!UICONTROL Apply]**.

   * (Opcional) Para editar manualmente la lógica del segmento, utilizando los segmentos disponibles en las pestañas [[!UICONTROL Third Party Segments], [!UICONTROL First Party Segments], [!UICONTROL Adobe Segments], [!UICONTROL Custom Segments] y [!UICONTROL Saved Audiences]](audience-settings.md), haga lo siguiente.

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

1. Haga clic en **[!UICONTROL Save]**.

1. En el mensaje de confirmación, haga clic en **[!UICONTROL Continue]**.

>[!MORELIKETHIS]
>
>* [Acerca de la administración de audiencias](audience-about.md)
>* [Crear una audiencia reutilizable](reusable-audience-create.md)
>* [Duplicar una audiencia reutilizable](reusable-audience-duplicate.md)
>* [Ver detalles acerca de una audiencia reutilizable](reusable-audience-view-details.md)
>* [Compartir una audiencia reutilizable](reusable-audience-share.md)
>* [Exportar una audiencia reutilizable](reusable-audience-export.md)
>* [Copiar la clave del segmento para una audiencia reutilizable en el portapapeles](reusable-audience-clipboard.md)
>* [Eliminar una audiencia reutilizable](reusable-audience-delete.md)
>* [Configuración de audiencia](audience-settings.md)
>* [Sintaxis de la lógica de segmento de audiencia](audience-segment-logic-syntax.md)
>* [Proveedores de datos de terceros disponibles](third-party-data-providers.md)
