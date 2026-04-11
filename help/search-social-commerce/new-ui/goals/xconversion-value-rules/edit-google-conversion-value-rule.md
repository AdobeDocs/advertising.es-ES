---
title: 'Editar una regla de valor de conversión  [!DNL Google Ads] '
description: Obtenga información sobre cómo editar  [!DNL Google Ads] reglas de valor de conversión.
source-git-commit: e15d34f3f32a8565735e53f1ce40e71008dbb4d9
workflow-type: tm+mt
source-wordcount: '259'
ht-degree: 0%

---

# Editar una regla de valor de conversión [!DNL Google Ads]

Puede editar una regla de valor de conversión en cuentas o campañas para las que se realiza un seguimiento de las conversiones en el nivel de cuenta individual o inferior. No puede editar una regla para una cuenta con conversiones entre cuentas que se rastrean en una cuenta maestra.

1. En el menú principal, haga clic en **[!UICONTROL Goals]>[!UICONTROL Conversion Value Rules]**.

   De manera predeterminada, la ficha **[!UICONTROL Campaign]** está seleccionada para mostrar todas las reglas de nivel de campaña.

1. (Opcional) Para ver todas las reglas de nivel de cuenta, haga clic en la ficha **[!UICONTROL Account]**.

1. Seleccione la casilla de verificación situada junto a la regla.

1. En la barra de herramientas de acciones masivas,

   * Para activar (habilitar) las reglas en pausa, haga clic en (/help/search-social-commerce/assets/edit-new.png &quot;Editar&quot;).

1. Edite la [configuración de regla de conversión](google-conversion-value-rule-settings.md).

   No puede editar los tipos de condición para una regla existente, pero puede editar las condiciones y los ajustes de valor.

   Debe configurar una condición principal y un ajuste de valor. Si lo desea, puede configurar una condición secundaria.

   **Nota:** Si agrega una condición secundaria, debe ser el mismo tipo de condición que otras reglas de la cuenta. Por ejemplo, si la regla 1 y otras reglas de la cuenta tienen la condición secundaria &quot;Ubicación&quot;, cuando las demás reglas incluyan una condición secundaria, la condición secundaria debe ser &quot;Ubicación&quot;. Cuando se incluye una condición secundaria, esta se une a la condición principal mediante el operador booleano ALL, de modo que se deben cumplir ambas condiciones para iniciar un ajuste de valor.

1. Haga clic en **[!UICONTROL Review and Save]** para revisar la configuración.

1. Haga clic en **[!UICONTROL Save]**.

>[!MORELIKETHIS]
>
>* [Acerca de [!DNL Google Ads] reglas de valor de conversión](about-google-conversion-value-rules.md)
>* [Crear una [!DNL Google Ads] regla de valor de conversión](create-google-conversion-value-rule.md)
>* [Cambiar el estado de una [!DNL Google Ads] regla de valor de conversión](change-the-status-of-google-conversion-value-rule.md)
>* [[!DNL Google Ads] configuración de regla de valor de conversión](google-conversion-value-rule-settings.md)

