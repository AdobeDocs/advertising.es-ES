---
title: 'Crear una regla de valor de conversión  [!DNL Google Ads] '
description: Aprenda a crear  [!DNL Google Ads] reglas de valor de conversión.
source-git-commit: e15d34f3f32a8565735e53f1ce40e71008dbb4d9
workflow-type: tm+mt
source-wordcount: '445'
ht-degree: 0%

---

# Crear una regla de valor de conversión [!DNL Google Ads]

Puede crear reglas de valor de conversión de nivel de cuenta y de nivel de campaña en cuentas de [!DNL Google Ads] para las que se realiza un seguimiento de las conversiones en el nivel de cuenta individual o inferior. No puede crear reglas para cuentas con conversiones entre cuentas cuyo seguimiento se realice a nivel de cuenta maestra.

Cada regla incluye hasta dos condiciones, así como el ajuste del valor de conversión que se aplicará cuando se cumplan las condiciones. Todas las reglas de una cuenta deben utilizar el mismo tipo de condiciones principales y (opcionales) secundarias. Por ejemplo, si la Regla 1 incluye la condición principal &quot;Audiencia&quot; y la condición secundaria &quot;Ubicación&quot;, todas las demás reglas de la cuenta deben tener la condición principal &quot;Audiencia&quot;. Cuando las demás reglas incluyen una condición secundaria, debe ser &quot;Ubicación&quot;.

Puede crear varias reglas de nivel de campaña para cada campaña. Sin embargo, [!DNL Google Ads] todavía no proporciona la capacidad de crear nuevas reglas de nivel de cuenta fuera del editor [!DNL Google Ads] cuando ya existe una regla de nivel de cuenta. Para crear reglas de nivel de cuenta adicionales, inicie sesión directamente en [!DNL Google Ads] y use el editor [!DNL Google Ads].

**Nota:** Las reglas de valor de conversión a nivel de campaña anulan las reglas a nivel de cuenta y sólo se puede aplicar una regla a una conversión. Para obtener más información, vea [cómo [!DNL Google Ads] determina qué regla se aplica a una conversión cuando esta cumple las condiciones para varias reglas](https://support.google.com/google-ads/answer/10520348).

1. En el menú principal, haga clic en **[!UICONTROL Goals]>[!UICONTROL Conversion Value Rules]**.

   De manera predeterminada, la ficha **[!UICONTROL Campaign]** está seleccionada para mostrar todas las reglas de nivel de campaña.

1. (Opcional) Para crear una regla de nivel de cuenta, haga clic en la ficha **[!UICONTROL Account]**.

1. En la barra de herramientas, haga clic en ![Crear](/help/search-social-commerce/assets/add.png "Crear").<!-- Upload newer icon -->

1. Seleccione la red publicitaria y la cuenta. Para las reglas de nivel de campaña, seleccione también la campaña. Luego haga clic en **[!UICONTROL Next]**.

1. Configurar [configuración de regla de conversión](google-conversion-value-rule-settings.md).

   Debe configurar una condición principal y un ajuste de valor. Si lo desea, puede configurar una condición secundaria.

   Dentro de una condición, se unen varios destinos o exclusiones utilizando el operador booleano OR, de modo que se pueda cumplir cualquier opción para iniciar un ajuste de valor. Cuando se incluye una condición secundaria, esta se une a la condición principal mediante el operador booleano ALL, de modo que se deben cumplir ambas condiciones para iniciar un ajuste de valor. Ejemplo: Si \[Location is Algeria OR Tunisia\] AND \[Device is Mobile OR Tablet\], añada 1,5.

   **Nota:** Todas las reglas de una cuenta deben usar el mismo tipo de condiciones principales y (opcionales) secundarias. Por ejemplo, si la Regla 1 incluye la condición principal &quot;Audiencia&quot; y la condición secundaria &quot;Ubicación&quot;, todas las demás reglas de la cuenta deben tener la condición principal &quot;Audiencia&quot;. Cuando las demás reglas incluyen una condición secundaria, debe ser &quot;Ubicación&quot;.

1. Haga clic en **[!UICONTROL Review and Save]** para revisar la configuración.

1. Haga clic en **[!UICONTROL Save]**.

>[!MORELIKETHIS]
>
>* [Acerca de [!DNL Google Ads] reglas de valor de conversión](about-google-conversion-value-rules.md)
>* [Editar una [!DNL Google Ads] regla de valor de conversión](edit-google-conversion-value-rule.md)
>* [Cambiar el estado de una [!DNL Google Ads] regla de valor de conversión](change-the-status-of-google-conversion-value-rule.md)
>* [[!DNL Google Ads] configuración de regla de valor de conversión](google-conversion-value-rule-settings.md)

