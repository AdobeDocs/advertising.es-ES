---
title: (Nueva IU) Administrar [!DNL Google Ads] reglas de valor de conversión
description: Aprenda a ver y administrar  [!DNL Google Ads] reglas de valor de conversión en Search, Social y Commerce.
feature: Conversions
feature_v2:
  - id: e6916c1b-e939-4e0b-99f5-768e83e1e99f
  - id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
subfeature_v2:
  - id: a2f79fa9-a8fe-4c1c-961e-75dc3c47f954
source-git-commit: bf1ca7f6133c19bb68dbe0395416dca8ef647464
workflow-type: tm+mt
source-wordcount: 1844
ht-degree: 0%

---

# (Nueva IU) Administrar reglas de valor de conversión de [!DNL Google Ads]

*característica de Beta*

[!DNL Google Ads] [reglas de valor de conversión](https://support.google.com/google-ads/answer/10518330) le permiten ajustar los valores de los eventos de conversión basándose en la información del usuario, incluido el tipo de dispositivo, la ubicación y el segmento de audiencia. Puede utilizar reglas para pujas basadas en valores en campañas de búsqueda, visualización, compras y rendimiento máximo con Google Smart Bidding. Para las campañas con estrategias de oferta Maximizar conversiones y ROAS de Target, los algoritmos [!DNL Google Ads] empezarán a preferir las conversiones con un valor más alto.

Las reglas de valor de conversión a nivel de campaña anulan las reglas a nivel de cuenta. Cuando una conversión cumple varias reglas de valor de conversión, solo se aplica una de las reglas. Normalmente, se aplica la regla más específica, pero consulte la [[!DNL Google Ads] documentación sobre prioridades para los diferentes tipos de condiciones de regla](https://support.google.com/google-ads/answer/10520348).

## La vista y funcionalidad de [!UICONTROL Conversion Value Rules]

Search, Social y Commerce sincronizan automáticamente las reglas de valor de conversión de sus cuentas de [!DNL Google Ads]. Todas las reglas creadas en la interfaz [!DNL Google Ads] se sincronizan en 24 horas y están disponibles en la vista [!UICONTROL Goals] > [!UICONTROL Conversion Value Rules].

Algunas cuentas pueden administrar sus reglas de valor de conversión:

* En las cuentas para las que se realiza un seguimiento de las conversiones en el nivel de cuenta individual o de campaña, puedes [crear](#google-conversion-value-rule-create), [editar](#google-conversion-value-rule-edit) y [cambiar el estado](#google-conversion-value-rule-change-status) de las reglas en el nivel de cuenta y de campaña.

  Las cuentas se pueden vincular a [[!DNL Google Ads] cuentas de administrador](/help/search-social-commerce/new-ui/), pero no pueden usar el seguimiento de conversiones entre cuentas (para el cual se realiza el seguimiento de las conversiones en todas las cuentas de la cuenta de administrador).

* En las cuentas que utilizan el seguimiento de conversión entre cuentas, las reglas de nivel de cuenta y de nivel de campaña se heredan de la cuenta del administrador y son de solo lectura.

## Reglas de valor de conversión con portafolios de Search, Social y Commerce

Cuando la cuenta del anunciante está configurada para cargar los objetivos de Search, Social y Commerce en [!DNL Google Ads], e incluye una campaña que usa una regla de valor de conversión en un portafolio con un objetivo, [!DNL Google Ads] aplica la regla de valor de conversión al valor de conversión original especificado en el objetivo. Como resultado, los datos de conversión de Buscar, Social y Commerce difieren de los datos de conversión de [!DNL Google Ads].

Por ejemplo, supongamos que el objetivo utiliza una única métrica de conversión &quot;Posibles clientes&quot; y proporciona a las conversiones desde dispositivos móviles un peso de 10 y a las conversiones desde dispositivos no móviles un peso de 10. Buscar, Social y Commerce cuenta un evento de cualquier tipo de dispositivo como una (1) conversión y acredita el valor de conversión como 10. Sin embargo, supongamos que una campaña de ese portafolio utiliza la regla de valor de conversión &quot;Si el dispositivo es móvil, multiplique por 2&quot;. Cuando se rastrea un evento de posibles clientes móvil para esa campaña, [!DNL Google Ads] también acredita el recuento de conversión como uno (1), pero el valor de conversión como (10 x 2) = 20.

Para obtener más información acerca de las reglas, incluidos los valores de conversión originales antes de que se aplicaran las reglas, vea el informe [reglas de valor de conversión en [!DNL Google Ads]](https://support.google.com/google-ads/answer/10519848).

## Crear una regla de valor de conversión [!DNL Google Ads] {#google-conversion-value-rule-create}

Puede crear reglas de valor de conversión de nivel de cuenta y de nivel de campaña en cuentas de [!DNL Google Ads] para las que se realiza un seguimiento de las conversiones en el nivel de cuenta individual o inferior. No puede crear reglas para cuentas con conversiones entre cuentas cuyo seguimiento se realice a nivel de cuenta maestra.

Cada regla incluye hasta dos condiciones, así como el ajuste del valor de conversión que se aplicará cuando se cumplan las condiciones. Todas las reglas de una cuenta deben utilizar el mismo tipo de condiciones principales y (opcionales) secundarias. Por ejemplo, si la Regla 1 incluye la condición principal &quot;Audiencia&quot; y la condición secundaria &quot;Ubicación&quot;, todas las demás reglas de la cuenta deben tener la condición principal &quot;Audiencia&quot;. Cuando las demás reglas incluyen una condición secundaria, debe ser &quot;Ubicación&quot;.

Puede crear varias reglas de nivel de campaña para cada campaña. Sin embargo, [!DNL Google Ads] todavía no proporciona la capacidad de crear nuevas reglas de nivel de cuenta fuera del editor [!DNL Google Ads] cuando ya existe una regla de nivel de cuenta. Para crear reglas de nivel de cuenta adicionales, inicie sesión directamente en [!DNL Google Ads] y use el editor [!DNL Google Ads].

**Nota:** Las reglas de valor de conversión a nivel de campaña anulan las reglas a nivel de cuenta y sólo se puede aplicar una regla a una conversión. Para obtener más información, vea [cómo [!DNL Google Ads] determina qué regla se aplica a una conversión cuando esta cumple las condiciones para varias reglas](https://support.google.com/google-ads/answer/10520348).

1. En el menú principal, haga clic en **[!UICONTROL Goals]>[!UICONTROL Conversion Value Rules]**.

   De manera predeterminada, la ficha **[!UICONTROL Campaign]** está seleccionada para mostrar todas las reglas de nivel de campaña.

1. (Opcional) Para crear una regla de nivel de cuenta, haga clic en la ficha **[!UICONTROL Account]**.

1. En la barra de herramientas, haga clic en **[!UICONTROL Create Campaign Rule]** (de la ficha [!UICONTROL Campaign]) o **[!UICONTROL Create Account Rule]** (de la ficha [!UICONTROL Account]).

1. Seleccione la red publicitaria y la cuenta. Para las reglas de nivel de campaña, seleccione también la campaña. Luego haga clic en **[!UICONTROL Next]**.

1. Configurar [configuración de regla de conversión](#google-ads-conversion-value-rule-settings).

   Debe configurar una condición principal y un ajuste de valor. Si lo desea, puede configurar una condición secundaria.

   Dentro de una condición, se unen varios destinos o exclusiones utilizando el operador booleano `OR`, de modo que se pueda cumplir cualquier opción para iniciar un ajuste de valor. Cuando se incluye una condición secundaria, esta se une a la condición principal mediante el operador booleano `ALL`, de modo que ambas condiciones deben cumplirse para iniciar un ajuste de valor. Ejemplo: Si \[Location is Algeria OR Tunisia\] AND \[Device is Mobile OR Tablet\], añada 1,5.

   **Nota:** Todas las reglas de una cuenta deben usar el mismo tipo de condiciones principales y (opcionales) secundarias. Por ejemplo, si la Regla 1 incluye la condición principal &quot;Audiencia&quot; y la condición secundaria &quot;Ubicación&quot;, todas las demás reglas de la cuenta deben tener la condición principal &quot;Audiencia&quot;. Cuando las demás reglas incluyen una condición secundaria, debe ser &quot;Ubicación&quot;.

1. Haga clic en **[!UICONTROL Review and Save]** para revisar la configuración.

1. Haga clic en **[!UICONTROL Save]**.

## Editar una regla de valor de conversión [!DNL Google Ads] {#google-conversion-value-rule-edit}

Puede editar una regla de valor de conversión en cuentas o campañas para las que se realiza un seguimiento de las conversiones en el nivel de cuenta individual o inferior. No puede editar una regla para una cuenta con conversiones entre cuentas que se rastrean en una cuenta maestra.

1. En el menú principal, haga clic en **[!UICONTROL Goals]>[!UICONTROL Conversion Value Rules]**.

   De manera predeterminada, la ficha **[!UICONTROL Campaign]** está seleccionada para mostrar todas las reglas de nivel de campaña.

1. (Opcional) Para ver todas las reglas de nivel de cuenta, haga clic en la ficha **[!UICONTROL Account]**.

1. Seleccione la casilla de verificación situada junto a la regla.

1. En la barra de herramientas de acciones masivas, haga clic en (/help/search-social-commerce/assets/edit-new.png &quot;Editar&quot;).

1. Edite la [configuración de regla de conversión](#google-ads-conversion-value-rule-settings).

   No puede editar los tipos de condición para una regla existente, pero puede editar las condiciones y los ajustes de valor.

   Debe configurar una condición principal y un ajuste de valor. Si lo desea, puede configurar una condición secundaria.

   **Nota:** Si agrega una condición secundaria, debe ser el mismo tipo de condición que otras reglas de la cuenta. Por ejemplo, si la regla 1 y otras reglas de la cuenta tienen la condición secundaria &quot;Ubicación&quot;, cuando las demás reglas incluyan una condición secundaria, la condición secundaria debe ser &quot;Ubicación&quot;. Cuando se incluye una condición secundaria, esta se une a la condición principal mediante el operador booleano `ALL`, de modo que ambas condiciones deben cumplirse para iniciar un ajuste de valor.

1. Haga clic en **[!UICONTROL Review and Save]** para revisar la configuración.

1. Haga clic en **[!UICONTROL Save]**.

## Cambiar el estado de una regla de valor de conversión [!DNL Google Ads] {#google-conversion-value-rule-change-status}

Puede pausar, activar o eliminar una regla de valor de conversión en cuentas y campañas para las que se realiza un seguimiento de las conversiones en el nivel de cuenta individual.

1. En el menú principal, haga clic en **[!UICONTROL Goals]>[!UICONTROL Conversion Value Rules]**.

   De manera predeterminada, la ficha **[!UICONTROL Campaign]** está seleccionada para mostrar todas las reglas de nivel de campaña.

1. (Opcional) Para ver todas las reglas de nivel de cuenta, haga clic en la ficha **[!UICONTROL Account]**.

1. Seleccione la casilla de verificación situada junto a cada fila que desee cambiar.

1. En la barra de herramientas de acciones masivas,

   * Para activar (habilitar) las reglas en pausa, haga clic en **[!UICONTROL ...]>[!UICONTROL Activate]**.

   * Para pausar las reglas activas, haga clic en **[!UICONTROL ...]>[!UICONTROL Pause]**.

   * Para eliminar las reglas activas o en pausa, haga clic en ![Eliminar](/help/search-social-commerce/assets/delete.png "Eliminar").

1. En el mensaje de confirmación, haga clic en **[!UICONTROL Confirm]**.

## [!DNL Google Ads] configuración de regla de valor de conversión {#google-conversion-value-rule-settings}

| Sección | Parámetro | Descripción |
|---|---|---|
| [!UICONTROL Select Campaign] | [!UICONTROL Network] | La red de anuncios. |
| | [!UICONTROL Account] | La cuenta de red de publicidad. |
| | [!UICONTROL Campaign] | (Solo reglas de valor de conversión de nivel de campaña) La campaña de publicidad. |
| [!UICONTROL Conditions] > [!UICONTROL Primary Condition] | \[Tipo de condición\] | (Solo lectura para reglas existentes) El tipo de condición que debe cumplirse para almacenar en déclencheur un ajuste de valor:<ul><li>*[!UICONTROL Device]:* Para dirigirse a todos los tipos de dispositivos o a tipos de dispositivos específicos.</li><li>*[!UICONTROL Location]:* Para dirigirse a todos los países y territorios o para dirigirse y excluir ubicaciones específicas.</li><li>*[!UICONTROL Audiences]:* Para dirigirse a todas las audiencias o a audiencias específicas</li></ul>**Nota:** Todas las reglas de una cuenta deben usar el mismo tipo de condiciones principales y (opcionales) secundarias. Por ejemplo, si la Regla 1 incluye la condición principal &quot;Audiencia&quot; y la condición secundaria &quot;Ubicación&quot;, todas las demás reglas de la cuenta deben tener la condición principal &quot;Audiencia&quot;. Cuando las demás reglas incluyen una condición secundaria, debe ser &quot;Ubicación&quot;. |
| | \[Tipo de condición\] > [!UICONTROL Device] y [!UICONTROL Device Level] | (Solo condiciones de dispositivo) Qué tipos de dispositivos se van a segmentar:<ul><li>*[!UICONTROL All devices]:** Para destinarlo a todos los tipos de dispositivos.</li><li>*[!UICONTROL Select devices]:* Para especificar uno o más tipos de dispositivos de destino: *[!UICONTROL Desktop]:*, *[!UICONTROL Mobile]* y *[!UICONTROL Tablet]:*.</li></ul>Dentro de una condición, se unen varios destinos mediante el operador booleano `OR`, de modo que se pueda cumplir cualquier opción para iniciar un ajuste de valor. Ejemplo: Si \[Device is Mobile OR Tablet\], a continuación, añada 1,5. |
| | \[Tipo de condición\] > [!UICONTROL Location] y [!UICONTROL Location Level] | (Solo condiciones de ubicación) Los destinos y las exclusiones de ubicación:<ul><li>*[!UICONTROL All countries and territories]:* Para dirigirse a todos los países y ubicaciones o para dirigirse y excluir ubicaciones específicas.</li><li>*[!UICONTROL Enter a location]:* Para destinar y excluir ubicaciones específicas.</li></ul><ul><li>Para expandir una ubicación o sububicación, haga clic en `>` después del nombre.</li><li>Para agregar un destino, selecciónelo una vez para mostrar una marca de verificación verde.</li><li>Para excluir un destino, selecciónelo por segunda vez para mostrar un **[!UICONTROL X]** rojo.</li><li>Para eliminar un destino o una exclusión, realice una de las acciones siguientes:<ul><li>Haga clic en ![Eliminar](/help/search-social-commerce/assets/delete.png "Eliminar") junto al elemento en la columna [!UICONTROL Selections].</li><li>Seleccione el destino hasta que no aparezca la marca de verificación o [!UICONTROL X].</li></ul></li></ul>Dentro de una condición, se unen varios destinos o exclusiones utilizando el operador booleano `OR`, de modo que se pueda cumplir cualquier opción para iniciar un ajuste de valor. Ejemplo: Si \[Location is Algeria OR Tunisia\], añada 1,5. |
| | \[Tipo de condición\] > [!UICONTROL Audience] y [!UICONTROL Audience Level] | (Solo condiciones de audiencia) Los destinatarios de la audiencia:<ul><li>*[!UICONTROL All audience segments]:* Para dirigirse a todos los [!DNL Google Ads] segmentos de audiencia.</li><li>*[!UICONTROL Enter audience segments]:* Para segmentar [!DNL Google Ads] segmentos de audiencia específicos.</li></ul><ul><li>Para expandir una categoría o subcategoría en sus segmentos, haga clic en `>` después del nombre.</li><li>Para añadir un objetivo, seleccione el objetivo.</li><li>Para quitar un destino, anule la selección del destino o haga clic en ![Eliminar](/help/search-social-commerce/assets/delete.png "Eliminar") junto al elemento en la columna [!UICONTROL Selection].</li></ul>Dentro de una condición, se unen varios destinos o exclusiones utilizando el operador booleano OR, de modo que se pueda cumplir cualquier opción para iniciar un ajuste de valor. Ejemplo: Si \[Audience es Viajeros de ganga O Vacacionistas familiares\], entonces Agregar 1.5.<br><br>**Nota:** Una vez guardado un destinatario de audiencia, puede agregar audiencias adicionales pero no puede quitarlas fuera del editor [!DNL Google Ads]. Si necesita quitar un destino de audiencia, inicie sesión directamente en [!DNL Google Ads] y use el editor [!DNL Google Ads]. |
| [!UICONTROL Conditions] > [!UICONTROL Secondary Condition] | \[Tipo de condición\] | (Opcional; solo lectura para reglas existentes) El tipo de condición que debe cumplirse para almacenar en déclencheur un ajuste de valor. Cuando se incluye una condición secundaria, esta se une a la condición principal mediante el operador booleano `ALL`, de modo que ambas condiciones deben cumplirse para iniciar un ajuste de valor. Ejemplo: Si \[Location is Algeria OR Tunisia\] AND \[Device is Mobile OR Tablet\], entonces Agregue 1.5.<br><br>Consulte las entradas de las condiciones principales para ver las descripciones.<br><br>**Nota:** Todas las reglas de una cuenta deben utilizar el mismo tipo de condiciones principales y (opcionales) secundarias. Por ejemplo, si la Regla 1 incluye la condición principal &quot;Audiencia&quot; y la condición secundaria &quot;Ubicación&quot;, todas las demás reglas de la cuenta deben tener la condición principal &quot;Audiencia&quot;. Cuando las demás reglas incluyen una condición secundaria, debe ser &quot;Ubicación&quot;. |
| [!UICONTROL Value Adjustment] | [!UICONTROL Adjustment Operation] y [!UICONTROL Adjustment Value] | Especifique el tipo de ajuste y, a continuación, introduzca un valor positivo:<ul><li>*[!UICONTROL Add]:* Agrega el valor especificado al valor de conversión pasado. El valor debe ser mayor que cero (0).</li><li>*[!UICONTROL Multiply]:* Multiplica el valor de conversión pasado por el valor especificado. El valor debe estar entre 0,5 y 10.</li></ul> |

<!--
>[!MORELIKETHIS]
>
>* 
-->
