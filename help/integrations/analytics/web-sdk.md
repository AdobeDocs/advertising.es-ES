---
title: Usando la  [!DNL Last Event Service] biblioteca de JavaScript con [!DNL Web SDK]
description: Conozca los pasos para dejar de usar la biblioteca  [!DNL Analytics] [!DNL visitorAPI] y pasar a la biblioteca  [!DNL Experience Platform] [!DNL Web SDK] para su implementación de  [!DNL Analytics for Advertising] sessionDetails.
feature: Integration with Adobe Analytics
exl-id: 764724a2-536a-43b9-955d-28d6146db29a
TQID: https://experienceleague.adobe.com/zT1lQV1yotCfJJdzTBGzSspsNEKQEB5ulxYE0qyWa9Q
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 193
ht-degree: 0%

---

# Usando la biblioteca de JavaScript [!DNL Last Event Service] con Adobe Experience Platform [!DNL Web SDK]

*Solo anunciantes con una integración Adobe Advertising-Adobe Analytics*

Si su organización utiliza la biblioteca heredada de Adobe Analytics `visitorAPI.js` para la recopilación de datos, puede cambiar a la biblioteca de [Adobe Experience Platform [!DNL Web SDK]](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=es) (`alloy.js`), que le permite interactuar con los distintos servicios de Experience Cloud a través de [!DNL Edge Network].

La biblioteca de JavaScript [!DNL Analytics for Advertising] [!DNL Last Event Service], tal como está, registra eventos de visualización y clics y los vincula a las conversiones asociadas con un identificador suplementario (`SDID`). Sin embargo, la biblioteca [!DNL Web SDK] no proporciona un [!DNL stitch ID]. Para usar [!DNL Web SDK] para [!DNL Analytics for Advertising], debe modificar 1) la etiqueta [!DNL Last Event Service] que usa en sus páginas web y 2) los comandos [!DNL Web SDK] `sendEvent` en consecuencia.

## Paso 1: Editar su etiqueta [!DNL Last Event Service] para generar un `[!DNL StitchID]`

En la etiqueta [!DNL Analytics for Advertising] [!DNL Last Event Service] que usa en sus páginas web, agregue código para generar `[!DNL StitchID]` mediante el generador de ID aleatorio que está empaquetado en la biblioteca.

**Etiqueta heredada:**

```
<script>
     if("undefined" != typeof AdCloudEvent) 
          AdCloudEvent('IMS ORG Id','rsid');
</script>
```

**Nueva etiqueta:**

```
<script>
     if("undefined" != typeof AdCloudEvent) 
          stitchId = AdCloudEvent('IMS ORG Id','rsid').generateRandomId();
</script>
```

## Paso 2: Use [!DNL Web SDK] para enviar [!DNL StitchID] como datos XDM para [!DNL Analytics]

Inserte la siguiente propiedad en el comando [!DNL Web SDK] `sendEvent` para enviar [!DNL StitchID] a [!DNL Experience Edge] como datos de [!DNL Experience Data Model] (XDM) para [!DNL Analytics].<!-- The library sends the StitchID to [!DNL Experience Edge] as `[_adcloud.advertisingStitchID](https://github.com/adobe/xdm/blob/master/docs/reference/adobe/experience/adcloud/stitch.schema.md)`. --> [!DNL Analytics] usa el valor como `SDID`.

**Propiedad que agregar:**

```
     "_adcloud": {
       "advertisingStitchID": stitchId
     }
```

**Ejemplo:**

```
<script>
  alloy("sendEvent", {
    "xdm": {
      "commerce": {
        "order": {
                ………
        }
     },
     "_adcloud": {
       "advertisingStitchID": stitchId
     }
    }
  });
</script>
```

>[!MORELIKETHIS]
>
>* [Información general de [!DNL Analytics for Advertising]](overview.md)
>* [Código JavaScript para [!DNL Analytics for Advertising]](/help/integrations/analytics/javascript.md)
