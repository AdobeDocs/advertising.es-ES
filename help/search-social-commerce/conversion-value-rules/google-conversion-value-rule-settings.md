---
title: '[!DNL Google Ads] configuración de regla de valor de conversión'
description: Haga referencia a la configuración de  [!DNL Google Ads] reglas de valor de conversión.
source-git-commit: efb4b80337b36b3b631898ca9ed66e99227468f1
workflow-type: tm+mt
source-wordcount: '685'
ht-degree: 0%

---

# [!DNL Google Ads] configuración de regla de valor de conversión

<!-- Go through all -->

| Sección | Parámetro | Descripción |
|---|---|---|
| [!UICONTROL Select Campaign] | [!UICONTROL Network] | La red de anuncios. |
| | [!UICONTROL Account] | La cuenta de red de publicidad. |
| | [!UICONTROL Campaign] | La campaña de publicidad. |
| [!UICONTROL Conditions] > [!UICONTROL Primary Condition] | \[Tipo de condición\] | (Solo lectura para reglas existentes) El tipo de condición que debe cumplirse para almacenar en déclencheur un ajuste de valor:<ul><li>**Dispositivo:** Para dirigirse a todos los tipos de dispositivos o a tipos específicos de dispositivos.</li><li>**Ubicación:** Para dirigirse a todos los países y territorios o para dirigirse y excluir ubicaciones específicas.</li><li>**Audiencias:** Para dirigirse a todas las audiencias o a audiencias específicas</li></ul>**Nota:** Todas las reglas de una cuenta deben usar el mismo tipo de condiciones principales y (opcionales) secundarias. Por ejemplo, si la Regla 1 incluye la condición principal &quot;Audiencia&quot; y la condición secundaria &quot;Ubicación&quot;, todas las demás reglas de la cuenta deben tener la condición principal &quot;Audiencia&quot;. Cuando las demás reglas incluyen una condición secundaria, debe ser &quot;Ubicación&quot;. |
| | Tipo de condición > Dispositivo | (Solo condiciones de dispositivo) Qué tipos de dispositivos se van a segmentar:<ul><li>**Todos los dispositivos**: para dirigirse a todos los tipos de dispositivos.</li><li>**Seleccionar dispositivos** — Para especificar uno o más tipos de dispositivos de destino: **Escritorio**, **Móvil** y **Tablet**.</li></ul>Dentro de una condición, se unen varios destinos utilizando el operador booleano OR, de modo que se pueda cumplir cualquier opción para iniciar un ajuste de valor. Ejemplo: Si \[Device is Mobile OR Tablet\], a continuación, añada 1,5. |
| | Tipo de condición > Ubicación | (Solo condiciones de ubicación) Los destinos y las exclusiones de ubicación:<ul><li>**Todos los países y territorios**: para dirigirse a todos los países y ubicaciones o para dirigirse y excluir ubicaciones específicas.</li><li>**Escriba una ubicación**: para destinar y excluir ubicaciones específicas.</li></ul><ul><li>Para expandir una ubicación o sububicación, haga clic en > después del nombre.</li><li>Para agregar un destino, selecciónelo una vez para mostrar una marca de verificación verde.</li><li>Para excluir un destino, selecciónelo por segunda vez para mostrar un **[!UICONTROL X]** rojo.</li><li>Para eliminar un destino o una exclusión, realice una de las acciones siguientes:<ul><li>Haga clic en ![Eliminar](/help/search-social-commerce/assets/delete.png "Eliminar") junto al elemento en la columna [!UICONTROL Selections].</li><li>Seleccione el destino hasta que no aparezca la marca de verificación o [!UICONTROL X].</li></ul></li></ul>Dentro de una condición, se unen varios destinos o exclusiones utilizando el operador booleano OR, de modo que se pueda cumplir cualquier opción para iniciar un ajuste de valor. Ejemplo: Si \[Location is Algeria OR Tunisia\], añada 1,5. |
| | Tipo de condición > Audiencia | (Solo condiciones de audiencia) Los destinatarios de la audiencia:<ul><li>**Todos los segmentos de audiencia**: para dirigirse a todos los [!DNL Google Ads] segmentos de audiencia.</li><li>**Introducir segmentos de audiencia**: para segmentar [!DNL Google Ads] segmentos de audiencia específicos.</li></ul><ul><li>Para expandir una categoría o subcategoría en sus segmentos, haga clic en > después del nombre.</li><li>Para añadir un objetivo, seleccione el objetivo.</li><li>Para quitar un destino, anule la selección del destino o haga clic en ![Eliminar](/help/search-social-commerce/assets/delete.png "Eliminar") junto al elemento en la columna Selección.</li></ul>Dentro de una condición, se unen varios destinos o exclusiones utilizando el operador booleano OR, de modo que se pueda cumplir cualquier opción para iniciar un ajuste de valor. Ejemplo: Si \[Audience es Viajeros de ganga O Vacacionistas familiares\], entonces Agregar 1.5.<br><br>**Nota:** Una vez guardado un destinatario de audiencia, puede agregar audiencias adicionales pero no puede quitarlas fuera del editor [!DNL Google Ads]. Si necesita quitar un destino de audiencia, inicie sesión directamente en [!DNL Google Ads] y use el editor [!DNL Google Ads]. |
| Condiciones > Condición secundaria | | (Opcional; solo lectura para reglas existentes) El tipo de condición que debe cumplirse para almacenar en déclencheur un ajuste de valor. Cuando se incluye una condición secundaria, esta se une a la condición principal mediante el operador booleano ALL, de modo que se deben cumplir ambas condiciones para iniciar un ajuste de valor. Ejemplo: Si \[Location is Algeria OR Tunisia\] AND \[Device is Mobile OR Tablet\], entonces Agregar 1.5.<br><br>Consulte las entradas de Condición principal para obtener descripciones.<br><br>**Nota:** Todas las reglas de una cuenta deben usar el mismo tipo de condiciones principales y (opcionales) secundarias. Por ejemplo, si la Regla 1 incluye la condición principal &quot;Audiencia&quot; y la condición secundaria &quot;Ubicación&quot;, todas las demás reglas de la cuenta deben tener la condición principal &quot;Audiencia&quot;. Cuando las demás reglas incluyen una condición secundaria, debe ser &quot;Ubicación&quot;. |
| Ajuste del valor | Valor | Especifique el tipo de ajuste y, a continuación, introduzca un valor positivo:<ul><li>**Agregar** — Agrega el valor especificado al valor de conversión pasado. El valor debe ser mayor que cero (0).</li><li>**Multiplicar**: multiplica el valor de conversión pasado por el valor especificado. El valor debe estar entre 0,5 y 10.</li></ul> |

>[!MORELIKETHIS]
>
>* [Acerca de [!DNL Google Ads] reglas de valor de conversión](about-google-conversion-value-rules.md)
>* [Crear una [!DNL Google Ads] regla de valor de conversión](create-google-conversion-value-rule.md)
>* [Editar una [!DNL Google Ads] regla de valor de conversión](edit-google-conversion-value-rule.md)
>* [Cambiar el estado de una [!DNL Google Ads] regla de valor de conversión](change-the-status-of-google-conversion-value-rule.md)

