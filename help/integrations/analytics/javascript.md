---
title: JavaScript code for [!DNL Analytics for Advertising]
description: JavaScript code for [!DNL Analytics for Advertising]
feature: Integration with Adobe Analytics
exl-id: 18bfb32d-2754-44b2-86c1-d102836cc08c
TQID: https://experienceleague.adobe.com/g9onwe1IQl1kbyQ82W2KmODPGUAReKiotxy65yCZcNY
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
source-git-commit: 7845129ba6566c1aaaf160cc6f9ad33bf1731f75
workflow-type: tm+mt
source-wordcount: 941
ht-degree: 0%

---

# JavaScript code for [!DNL Analytics for Advertising]

*Advertisers with Advertising DSP only*

For Advertising DSP, the [!DNL Analytics for Advertising] integration tracks view-through and click-through site interactions. Click-through visits are tracked by the standard Adobe Analytics code on your webpages; the [!DNL Analytics] code captures the AMO ID and EF ID parameters in the landing page URL and tracks them in their respective reserved [!DNL eVars]. You can track view-through visits by deploying a JavaScript snippet in your webpages.

On the first page view of a visit to the site, the Adobe Advertising JavaScript code checks to see if the visitor has previously seen or clicked on an ad. If the user has previously entered the site via a click-through or hasn&#39;t seen an ad, then the visitor is ignored. If the visitor has seen an ad and hasn&#39;t entered the site via a click-through during the [click lookback window](/help/integrations/analytics/prerequisites.md#lookback-a4adc) set within Adobe Advertising, then the Adobe Advertising JavaScript code either a) uses the [Experience Cloud ID Service](https://experienceleague.adobe.com/docs/id-service/using/home.html) to generate a supplemental ID (`SDID`) or b) uses the Adobe Experience Platform [!DNL Web SDK] `generateRandomID` method to generate a `[!DNL StitchID]`. Either ID is used to stitch data from Adobe Advertising to the visitor&#39;s Adobe Analytics hit. Adobe Analytics then queries Adobe Advertising for the AMO ID and EF ID associated with the ad exposure. The AMO ID and EF IDs are then populated in their respective [!DNL eVars]. These values persist for a designated period (by default, 60 days).

[!DNL Analytics] sends site traffic metrics (such as page views, visits, and time spent) and any [!DNL Analytics] custom or standard events to Adobe Advertising hourly, using the EF ID as the key. These [!DNL Analytics] metrics then run through the Adobe Advertising attribution system to connect the conversions to the click and exposure history.

>[!NOTE]
>
>The Adobe Advertising JavaScript tracking logic occurs on the Adobe side and thus has virtually no impact to the page load time.
>
>In contrast, the logic for the [!DNL DCM] data connector to [!DNL Analytics] (using [!DNL Google Campaign Manager 360]) for Advertising DSP occurs on the client side. Client-side stitching slows down the page load and increases the risk of data loss. This occurs because the [!DNL Analytics] JavaScript must ping [!DNL DoubleClick] and wait for [!DNL DoubleClick] to pass back the last click/impression data to [!DNL Analytics]. When your [!DNL DSP] team sets up the [!DNL DCM] data connector, you must specify how long you&#39;re willing to delay the page.

<!--
## Deploying the JavaScript code

All users must deploy the standard JavaScript code.

Users who want to convert first-party segments from their customer data platforms to [!DNL RampIDs] or [!DNL ID5] IDs [!!!!VERIFY that it's not needed for importing segments directly from LiveRamp] must also deploy ID partner-specific JavaScript code to match conversions to view-throughs.

### The standard code

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

### Additional code to import first-party segments to [!DNL RampIDs] and [!DNL ID5] IDs

   * For [!DNL RampIDs], Contact your Adobe Account Team, who will give you instructions to register for a [!DNL LiveRamp] [!DNL LaunchPad] tag. Registration is free, but you must sign an agreement. Once you register, your Adobe Account Team will generate and provide a unique tag for your organization to implement on your webpages.

    [MAYBE PUT THIS BELOW] Place the [!DNL LaunchPad] tag on every page of your website, preferably as the first script within the page head tags but as high within the page head tags as possible.

   * For [!DNL ID5] IDs: Contact your Adobe Account Team, who will give you instructions to register for the tag with ID5. Registration is free, but you must sign an agreement. Once you register, a member of ID5's technical team will provide a unique tag for your organization to implement on your webpages.
-->

## Deploying the JavaScript code

The JavaScript library consists of two lines that allow [!DNL Analytics] and Adobe Advertising to communicate with each other. If the [!DNL Analytics for Advertising] integration was completed during the Adobe Advertising implementation, then you should have already received this code with instructions on how to deploy it.

### The code

#### Implementations that use the Experience Cloud Identity Service `visitorAPI.js` code

```
<script src="https://www.everestjs.net/static/le/last-event-tag-latest.min.js">
<script>
     if("undefined" != typeof AdCloudEvent) 
          AdCloudEvent('IMS ORG Id','rsid');
</script>
```

#### Implementations that use the Experience Platform [!DNL Web SDK] `alloy.js`code

```
<script src="https://www.everestjs.net/static/le/last-event-tag-latest.min.js">
<script>
     if("undefined" != typeof AdCloudEvent) 
          stitchId = AdCloudEvent('IMS ORG Id','rsid').generateRandomId();
</script>
```

### Where to place the code

The [!DNL Analytics for Advertising] JavaScript function must come after the Experience Cloud ID Service but before your Analytics App Measurement code. This ensures that the supplemental ID (`SDID`) or `[!DNL StitchID]` is included in your Analytics call.

![Code placement](/help/integrations/assets/a4adc-code-placement.png)

### Validating code deployment

You can perform validation using any packet sniffer type of tool (such as [!DNL Charles], [!DNL Fiddler], or [!DNL Chrome Developer Tools]) by comparing the values of the four IDs between the request going to Adobe Advertising and the request going to [!DNL Analytics], as outlined below.

#### How to confirm the code with [!DNL Chrome Developer Tools] {#validate-js-chrome}

1. Open [!DNL Chrome Developer Tools] and click the **Network** tab.

1. Load a website page that contains the [!DNL Analytics for Advertising] JavaScript.

1. Filter the [!UICONTROL Network] tab by `last` and review two rows:

   ![Filtering on last](/help/integrations/assets/a4adc-code-validation-filter-last.png)

   * The first row is the call to the JavaScript library and is titled `last-event-tag-latest.min.js`.
   * The second row is the call sending the request to Adobe Advertising. It begins as follows: `_les_imsOrgId=[your_imsOrgId_here]&_les_url=[your_encoded_url]`

     If you don&#39;t see the call to Adobe Advertising, then it might not be the first page view of your visit. For testing purposes, you can remove the cookie so that the next call is the first page view for the corresponding visit:

   1. On the Application tab, find the `adcloud` cookie, and verify that the cookie contains `_les_v` (last visit) with a value of `y` and a UTC epoch timestamp that expires in 30 minutes.
      1. Delete the `adcloud` cookie and refresh the page.

1. (Implementations that use the Experience Cloud Identity Service `visitorAPI.js` code) Filter on `/b/ss` to see the Analytics hit.

   ![Filtering on `/b/ss`](/help/integrations/assets/a4adc-code-validation-filter-bss.png)

1. (Implementations that use the Experience Platform [!DNL Web SDK] `alloy.js`code) Filter on `/interact` to verify that the request payload to the Edge Network contains `advertisingStitchID`.

   ![Filtrado en `/interact`](/help/integrations/assets/a4adc-code-validation-filter-interact.png)

1. Compare los valores de ID entre las dos visitas. Todos los valores deben estar en parámetros de cadena de consulta, excepto el ID del grupo de informes en la visita de Analytics, que es la ruta de la URL inmediatamente después de `/b/ss/`.

   | ID | Parámetro de Analytics | Edge Network | Parámetro de Adobe Advertising |
   | --- | --- | --- | --- |
   | Organización de IMS de Experience Cloud | `mcorgid` |  | `_les_imsOrgid` |
   | ID de datos suplementario | sdid |  | `_les_sdid` |
   | ID de unión | stitchId | `advertisingStitchID` bajo la propiedad `_adcloud` |  |
   | Analytics Report Suite | El valor después de `/b/ss/` | | `_les_rsid` |
   | ID de visitante de Experience Cloud | mid |  | `_les_mid` |

   Si los valores de ID coinciden, se confirma la implementación de JavaScript. Adobe Advertising envía al servidor [!DNL Analytics] cualquier detalle de seguimiento de clics o visualizaciones, si existe.

#### Cómo confirmar el código con [!DNL Adobe Experience Platform Debugger]

1. Abre [el [!DNL Adobe Experience Platform Debugger]](https://experienceleague.adobe.com/docs/debugger/using-v2/summary.html) en tu página de inicio.
1. Vaya a la ficha [!UICONTROL Network].
1. En la barra de herramientas [!UICONTROL Solutions Filter], haga clic en [!UICONTROL Adobe Advertising] y [!UICONTROL Analytics].
1. En la fila del parámetro [!UICONTROL Request URL - Hostname], busque `lasteventf-tm.everesttech.net`.
1. En la fila [!UICONTROL Request - Parameters], audite las señales generadas, de forma similar al Paso 3 de &quot;[Cómo confirmar el código con [!DNL Chrome Developer Tools]](#validate-js-chrome)&quot;.
   * (Implementaciones que utilizan el código `visitorAPI.js` del servicio de identidad de Experience Cloud) Asegúrese de que el parámetro `Sdid` coincida con `Supplemental Data ID` en el filtro de Adobe Analytics.
   * (Implementaciones que utilizan el código `alloy.js`Experience Platform [!DNL Web SDK]) Asegúrese de que el valor del parámetro `advertisingStitchID` coincida con el `Sdid` enviado a Experience Platform Edge Network.
   * Si el código no se está generando, asegúrese de que la cookie de Adobe Advertising se haya eliminado en la pestaña [!UICONTROL Application]. Una vez eliminada, actualice la página y repita el proceso.

   ![Auditando código JavaScript [!DNL Analytics for Advertising] en [!DNL Platform Cloud Debugger]](/help/integrations/assets/a4adc-js-audit-debugger.png)

>[!MORELIKETHIS]
>
>* [Información general de [!DNL Analytics for Advertising]](overview.md)
>* [Requisitos previos e información clave para implementar [!DNL Analytics for Advertising]](prerequisites.md)
