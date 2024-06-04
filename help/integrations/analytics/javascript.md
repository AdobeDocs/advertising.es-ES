---
title: Código JavaScript para [!DNL Analytics for Advertising]
description: Código JavaScript para [!DNL Analytics for Advertising]
feature: Integration with Adobe Analytics
exl-id: 18bfb32d-2754-44b2-86c1-d102836cc08c
source-git-commit: 5d07300ab49b96daf392cb51f8936fa4c0cd20ce
workflow-type: tm+mt
source-wordcount: '919'
ht-degree: 0%

---

# Código JavaScript para [!DNL Analytics for Advertising]

*DSP Solo anunciantes con Advertising*

DSP Para Advertising, la variable [!DNL Analytics for Advertising] La integración de rastrea las interacciones del sitio de visualizaciones y clics. Las visitas de clics se rastrean mediante el código estándar de Adobe Analytics en sus páginas web; la variable [!DNL Analytics] captura los parámetros de ID de AMO y de EF ID en la dirección URL de la página de aterrizaje y los rastrea en sus respectivos parámetros reservados [!DNL eVars]. Puede realizar un seguimiento de las visitas de visualización mediante la implementación de un fragmento de JavaScript en sus páginas web.

En la primera vista de página de una visita al sitio, el código JavaScript de Adobe Advertising comprueba si el visitante ha visto o hecho clic anteriormente en un anuncio. Si el usuario ha entrado anteriormente en el sitio mediante un clic o no ha visto un anuncio, se ignora al visitante. Si el visitante ha visto un anuncio y no ha entrado en el sitio mediante una pulsación durante el [haga clic en ventana retrospectiva](/help/integrations/analytics/prerequisites.md#lookback-a4adc) configurado en Adobe Advertising, el código JavaScript de Adobe Advertising a) utiliza el [Servicio de ID de Experience Cloud](https://experienceleague.adobe.com/docs/id-service/using/home.html) para generar un ID suplementario (`SDID`) o b) utiliza el Adobe Experience Platform [!DNL Web SDK] `generateRandomID` método para generar un `[!DNL StitchID]`. Cualquiera de los ID se utiliza para unir los datos del Adobe Advertising con la visita de Adobe Analytics del visitante. A continuación, Adobe Analytics consulta al Adobe Advertising el ID de AMO y el ID de EF asociados con la exposición del anuncio. A continuación, los ID de AMO y EF se rellenan en sus respectivos [!DNL eVars]. Estos valores persisten durante un periodo designado (de forma predeterminada, 60 días).

[!DNL Analytics] envía métricas de tráfico del sitio (como vistas de página, visitas y tiempo empleado) y cualquier [!DNL Analytics] eventos personalizados o estándar para almacenar en Adobe Advertising cada hora, utilizando el ID de EF como clave. Estos [!DNL Analytics] a continuación, las métricas se ejecutan mediante el sistema de atribución de Adobes Advertising para conectar las conversiones al historial de clics y exposiciones.

>[!NOTE]
>
>La lógica de seguimiento de JavaScript de Adobe Advertising se produce en el lado del Adobe y, por lo tanto, no tiene prácticamente ningún impacto en el tiempo de carga de la página.
>
>Por el contrario, la lógica del [!DNL DCM] conector de datos a [!DNL Analytics] (con [!DNL Google Campaign Manager 360]DSP ) para Advertising se produce en el lado del cliente. La vinculación del lado del cliente ralentiza la carga de página y aumenta el riesgo de pérdida de datos. Esto ocurre porque la variable [!DNL Analytics] JavaScript debe hacer ping [!DNL DoubleClick] y espere a que [!DNL DoubleClick] para devolver los datos del último clic/impresión a [!DNL Analytics]. Cuando su [!DNL DSP] El equipo de configura el [!DNL DCM] conector de datos, debe especificar cuánto tiempo está dispuesto a retrasar la página.

<!--
## Deploying the JavaScript Code

All users must deploy the standard JavaScript code.

Users who want to convert first-party segments from their customer data platforms to [!DNL RampIDs] or [!DNL ID5] IDs [!!!!VERIFY that it's not needed for importing segments directly from LiveRamp] must also deploy ID partner-specific JavaScript code to match conversions to view-throughs.

### The Standard Code

The standard JavaScript library consists of two lines that allow [!DNL Analytics] and Adobe Advertising to communicate with each other. If the [!DNL Analytics for Advertising] integration was completed during the Adobe Advertising implementation, then you should have already received this code with instructions on how to deploy it.

#### Implementations that use the Experience Cloud Identity Service `visitorAPI.js` code

```
<script src="https://www.everestjs.net/static/le/last-event-tag-latest.min.js">
<script>
     if("undefined" != typeof AdCloudEvent) 
          AdCloudEvent('IMS ORG Id','rsid');
</script>
```

#### Implementations that use the Experience Platform [!DNL Web SDK] `alloy.js`code

### Additional Code to Import First-Party Segments to [!DNL RampIDs] and [!DNL ID5] IDs

   * For [!DNL RampIDs], Contact your Adobe Account Team, who will give you instructions to register for a [!DNL LiveRamp] [!DNL LaunchPad] tag. Registration is free, but you must sign an agreement. Once you register, your Adobe Account Team will generate and provide a unique tag for your organization to implement on your webpages.

    [MAYBE PUT THIS BELOW] Place the [!DNL LaunchPad] tag on every page of your website, preferably as the first script within the page head tags but as high within the page head tags as possible.

   * For [!DNL ID5] IDs: Contact your Adobe Account Team, who will give you instructions to register for the tag with ID5. Registration is free, but you must sign an agreement. Once you register, a member of ID5’s technical team will provide a unique tag for your organization to implement on your webpages.
-->

## Implementación del código JavaScript

La biblioteca JavaScript de consta de dos líneas que permiten [!DNL Analytics] y el Adobe Advertising de comunicarse entre sí. Si la variable [!DNL Analytics for Advertising] La integración de se completó durante la implementación de Adobe Advertising, por lo que ya debería haber recibido este código con instrucciones sobre cómo implementarlo.

### El código

#### Implementaciones que utilizan el servicio de identidad de Experience Cloud `visitorAPI.js` código

```
<script src="https://www.everestjs.net/static/le/last-event-tag-latest.min.js">
<script>
     if("undefined" != typeof AdCloudEvent) 
          AdCloudEvent('IMS ORG Id','rsid');
</script>
```

#### Implementaciones que utilizan el Experience Platform [!DNL Web SDK] `alloy.js`código

```
<script src="https://www.everestjs.net/static/le/last-event-tag-latest.min.js">
<script>
     if("undefined" != typeof AdCloudEvent) 
          stitchId = AdCloudEvent('IMS ORG Id','rsid').generateRandomId();
</script>
```

### Dónde colocar el código

El [!DNL Analytics for Advertising] La función de JavaScript debe ser posterior al servicio de ID de Experience Cloud, pero anterior al código de App Measurement de Analytics. Esto garantiza que el ID suplementario (`SDID`) o `[!DNL StitchID]` se incluye en la llamada de Analytics.

![Ubicación del código](/help/integrations/assets/a4adc-code-placement.png)

### Validando implementación de código

Puede realizar la validación utilizando cualquier tipo de herramienta de analizador de paquetes (como [!DNL Charles], [!DNL Fiddler], o [!DNL Chrome Developer Tools]) comparando los valores de los cuatro ID entre la solicitud que se va al Adobe Advertising y la solicitud que se va a [!DNL Analytics], como se indica a continuación.

#### Cómo confirmar el código con [!DNL Chrome Developer Tools] {#validate-js-chrome}

1. Abrir [!DNL Chrome Developer Tools] y haga clic en **Red** pestaña.

1. Cargue una página web que contenga [!DNL Analytics for Advertising] JavaScript.

1. Filtrar el [!UICONTROL Network] tabular por `last` y revise dos filas:

   ![Filtrado en los últimos](/help/integrations/assets/a4adc-code-validation-filter-last.png)

   * La primera fila es la llamada a la biblioteca JavaScript y tiene el título `last-event-tag-latest.min.js`.
   * La segunda fila es la llamada que envía la solicitud al Adobe Advertising. Comienza de la siguiente manera: `_les_imsOrgId=[your_imsOrgId_here]&_les_url=[your_encoded_url]`

     Si no ve la llamada al Adobe Advertising, es posible que no sea la primera vista de página de la visita. Para realizar pruebas, puede eliminar la cookie de modo que la siguiente llamada sea la primera vista de página de la visita correspondiente:

   1. En la pestaña Aplicación, busque `adcloud` y compruebe que la cookie contiene `_les_v` (última visita) con un valor de `y` y una marca de tiempo UTC epoch que caduca en 30 minutos.
      1. Elimine el `adcloud` y actualice la página.

1. (Implementaciones que utilizan el servicio de identidad de Experience Cloud `visitorAPI.js` (código) Filtrar por `/b/ss` para ver la visita de Analytics.

   ![Filtrado en `/b/ss`](/help/integrations/assets/a4adc-code-validation-filter-bss.png)

1. (Implementaciones que utilizan el Experience Platform [!DNL Web SDK] `alloy.js`(código) Filtrar por `/interact` para comprobar que la carga útil de la solicitud al Edge Network contiene `advertisingStitchID`.

   ![Filtrado en `/interact`](/help/integrations/assets/a4adc-code-validation-filter-interact.png)

1. Compare los valores de ID entre las dos visitas. Todos los valores deben estar en parámetros de cadena de consulta, excepto el ID del grupo de informes en la visita de Analytics, que es la ruta de URL inmediatamente después de `/b/ss/`.

   | ID | Parámetro de Analytics | Edge Network | Parámetro de Adobe Advertising |
   | --- | --- | --- | --- |
   | Organización de IMS de Experience Cloud | `mcorgid` |  | `_les_imsOrgid` |
   | ID de datos suplementario | sdid |  | `_les_sdid` |
   | ID de unión | stitchId | `advertisingStitchID` en el `_adcloud` propiedad |  |
   | Analytics Report Suite | El valor después de `/b/ss/` | | `_les_rsid` |
   | ID de visitante de Experience Cloud | mid |  | `_les_mid` |

   Si los valores de ID coinciden, se confirma la implementación de JavaScript. El Adobe Advertising envía el [!DNL Analytics] datos de seguimiento de clics o visualizaciones del servidor, si los hay.

#### Cómo confirmar el código con [!DNL Adobe Experience Cloud Debugger]

1. Abra el [[!DNL Adobe Experience Cloud Debugger]](https://experienceleague.adobe.com/docs/debugger/using-v2/summary.html) en su página de inicio.
1. Vaya a la [!UICONTROL Network] pestaña.
1. En el [!UICONTROL Solutions Filter] , haga clic en [!UICONTROL Adobe Advertising] y [!UICONTROL Analytics].
1. En el [!UICONTROL Request URL - Hostname] fila de parámetros, localizar `lasteventf-tm.everesttech.net`.
1. En el [!UICONTROL Request - Parameters] , audite las señales generadas, de forma similar al Paso 3 en &quot;[Cómo confirmar el código con [!DNL Chrome Developer Tools]](#validate-js-chrome).&quot;
   * (Implementaciones que utilizan el servicio de identidad de Experience Cloud `visitorAPI.js` Código) Asegúrese de que la variable `Sdid` El parámetro coincide con `Supplemental Data ID` en el filtro Adobe Analytics.
   * (Implementaciones que utilizan el Experience Platform [!DNL Web SDK] `alloy.js`Código) Asegúrese de que el valor de `advertisingStitchID` El parámetro coincide con `Sdid` enviado al Edge Network Experience Platform.
   * Si el código no se está generando, asegúrese de que la cookie de Adobe Advertising se haya eliminado en la [!UICONTROL Application] pestaña. Una vez eliminada, actualice la página y repita el proceso.

   ![Auditoría [!DNL Analytics for Advertising] Código JavaScript en [!DNL Experience Cloud Debugger]](/help/integrations/assets/a4adc-js-audit-debugger.png)

>[!MORELIKETHIS]
>
>* [Información general de [!DNL Analytics for Advertising]](overview.md)
>* [Requisitos previos e información clave para la implementación [!DNL Analytics for Advertising]](prerequisites.md)
