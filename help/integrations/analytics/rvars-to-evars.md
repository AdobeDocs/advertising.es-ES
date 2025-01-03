---
title: Recopilación de datos históricos para ID de AMO e ID de EF para su uso en Adobe Customer Journey Analytics
description: Obtenga información sobre cómo recopilar datos históricos para las variables reservadas en Adobe Analytics para su uso futuro en Adobe Customer Journey Analytics
feature: Integration with Adobe Analytics
source-git-commit: 4cd58fd995b3df9fb7837077108207ce910157c1
workflow-type: tm+mt
source-wordcount: '605'
ht-degree: 0%

---

# Recopilación de datos históricos para ID de AMO e ID de EF para su uso en Adobe Customer Journey Analytics

*Anunciantes con [!DNL Analytics for Advertising] y solo Adobe Customer Journey Analytics*

Si usa variables reservadas para capturar el [ID de AMO e ID de EF](ids.md) para su integración con [!DNL Analytics for Advertising], puede prepararse para una futura integración entre Adobe Advertising y [Adobe Customer Journey Analytics](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/cja-overview), que es la solución [!DNL analytics] de próxima generación de Adobe, copiando las variables reservadas para el ID de AMO y el ID de EF en [standard [!DNL eVars]](https://experienceleague.adobe.com/en/docs/analytics/components/dimensions/evar) lo antes posible. Esto permite recopilar datos históricos para los ID de AMO y los ID de EF en cuanto complete la tarea. El equipo de cuenta de Adobe le informará si utiliza variables reservadas y necesita completar esta tarea.

<!-- You can also do the same for any other reserved variables you use for your [!DNL Analytics for Advertising] implementation. -->

<!-- This will allow Adobe Experience Platform, which supplies data to Customer Journey Analytics, to begin collecting historical data for your [!DNL rVars] as soon as you complete the task. -->

## ¿Por qué necesito recopilar datos históricos de Customer Journey Analytics?

Customer Journey Analytics permite sincronizar datos de Adobe Experience Platform con Adobe Analytics Analysis Workspace. En este momento, el Experience Platform [!DNL Analytics Data Connector] al que se va no envía datos para variables reservadas de [!DNL Analytics] al Experience Platform. Como resultado, los datos de los ID de AMO y de EF capturados por variables reservadas no están disponibles actualmente en Customer Journey Analytics. <!-- Instead, XXXXXXXXXX what exactly? -->.<!-- Does the Analytics for Advertising implementation use the Analytics Data Connector in particular (why would it use anything?), and we're planning to implement the Web SDK to do it instead in the future? -->

El Adobe Advertising está planificando una futura implementación con Customer Journey Analytics. DSP Una vez lanzada la implementación, la integración de [!DNL Analytics for Advertising] seguirá exigiendo que recopile datos de clics y datos de visualizaciones (usuarios de la aplicación) mediante el seguimiento de [!DNL Analytics], pero podrá ver los datos en los Customer Journey Analytics {1\) [!DNL Analytics] <!-- (Analysis Workspace using data from [!DNL Analytics]) --> y {2\) <!-- (Analysis Workspace using data from Experience Platform)--> si su organización tiene ambos productos. Cuando se publique la función, Experience Platform empezará a recopilar datos para su ID de AMO y su ID de EF para utilizarlos en Customer Journey Analytics, pero no existirán datos históricos anteriores a la fecha de lanzamiento.

Sin embargo, puede empezar a recopilar datos para sus ID de AMO e ID de EF <!-- [!DNL rVars] --> antes creando una sencilla [[!DNL Analytics] regla de procesamiento](https://experienceleague.adobe.com/en/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/c-processing-rules/processing-rules) para copiar ahora sus ID de AMO y los ID de EF <!-- [!DNL rVars] --> en [!DNL eVars]. Una vez que cree la regla de procesamiento, empezará a acumular datos para los ID de AMO y los ID de EF <!-- [!DNL rVars] --> en cuanto rastreen nuevos eventos. Los datos históricos estarán disponibles en Customer Journey Analytics una vez que la implementación esté disponible.

>[!NOTE]
>
>Las reglas de procesamiento solo se aplican a los nuevos datos recibidos. No funcionan de forma retroactiva para recopilar datos pasados.

## Copie sus variables reservadas para ID de AMO e ID de EF en [!DNL eVars]

Este paso es manual y debe completarse para cada grupo de informes que realice un seguimiento de los ID de AMO y EF ID <!-- [!DNL rVars] --> que espera integrar con Adobe Advertising en el futuro.

1. [Crear una regla de procesamiento](https://experienceleague.adobe.com/en/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/c-processing-rules/c-processing-rules-configuration/t-processing-rules) con la siguiente configuración:

   * Seleccione el grupo de informes para el cual desea migrar los datos de ID de AMO e ID de EF <!-- [!DNL rVar] --> al Experience Platform para que los utilice el Customer Journey Analytics.

   * Para [!UICONTROL Rule Title], use un nombre descriptivo como &quot;Copiar ID de AMO e ID de EF en eVars&quot;.

   * En la sección [!UICONTROL Always Execute], agregue dos acciones para crear las nuevas eVars:

      * Para `AMO ID`: ```Overwrite value of <new/unused eVar> with amo.s_kwcid(Context Data)```

      * Para `EF ID`: ```Overwrite value of <new/unused eVar> With amo.ef_id(Context Data)```

   * Para [!UICONTROL Reason for rule], utilice una nota descriptiva, como &quot;El ID de AMO y el ID de EF se transportarán a AEP a través del conector de Adobe Analytics&quot;.

1. Valide la regla de procesamiento guardada.

   Una vez guardada la regla de procesamiento, los datos de `AMO ID` y `AMO EF ID` <!-- the existing reserved variables --> deben ser idénticos a los datos de las dos nuevas eVars a las que se copian.

   Por ejemplo, si el nuevo eVar `eVar142` está asignado a `amo.s_kwcid(Context Data)`, los datos de `eVar142` y `AMO ID` deben ser idénticos.

Para obtener más información acerca de cómo se aplican las reglas de procesamiento, vea &quot;[Funcionamiento de las reglas de procesamiento](https://experienceleague.adobe.com/en/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/c-processing-rules/c-processing-rules-configuration/processing-rules-about)&quot;.

>[!MORELIKETHIS]
>
>* [Información general de [!DNL Analytics for Advertising]](overview.md)
