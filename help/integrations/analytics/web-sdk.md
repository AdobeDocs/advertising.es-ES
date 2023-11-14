---
title: Uso del [!DNL Last Event Service] Biblioteca JavaScript con [!DNL Web SDK]
description: Conozca los pasos para dejar de utilizar el [!DNL Analytics] [!DNL visitorAPI] a la biblioteca de [!DNL Experience Platform] [!DNL Web SDK] biblioteca para su [!DNL Analytics for Advertising] implementación.
feature: Integration with Adobe Analytics
exl-id: 764724a2-536a-43b9-955d-28d6146db29a
source-git-commit: 7501c1f8f6477a4ee6de64c64d52b1aafaf16994
workflow-type: tm+mt
source-wordcount: '196'
ht-degree: 0%

---

# Uso del [!DNL Last Event Service] Biblioteca JavaScript con Adobe Experience Platform [!DNL Web SDK]

*Anunciantes con solo integración de Adobe Advertising-Adobe Analytics*

Si su organización utiliza el Adobe Analytics heredado `visitorAPI.js` para la recopilación de datos, puede cambiar a con la variable [Adobe Experience Platform [!DNL Web SDK]](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html) biblioteca (`alloy.js`), que le permite interactuar con los distintos servicios de Experience Cloud a través de [!DNL Edge Network].

El [!DNL Analytics for Advertising] [!DNL Last Event Service] La biblioteca JavaScript tal cual registra los eventos de visualizaciones y clics, y los vincula a las conversiones asociadas con un ID suplementario (`SDID`). El [!DNL Web SDK] La biblioteca, sin embargo, no proporciona un [!DNL stitch ID]. Para usar la variable [!DNL Web SDK] para [!DNL Analytics for Advertising], tendrá que modificar 1) la variable [!DNL Last Event Service] etiqueta que utiliza en sus páginas web y 2) su [!DNL Web SDK] `sendEvent` comandos en consecuencia.

## Paso 1: Editar su [!DNL Last Event Service] Etiqueta para generar un `[!DNL StitchID]`

En el [!DNL Analytics for Advertising] [!DNL Last Event Service] que utilice en sus páginas web, agregue código para generar el `[!DNL StitchID]` mediante el generador de ID aleatorio que se incluye en la biblioteca.

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

## Paso 2: Uso [!DNL Web SDK] para enviar el [!DNL StitchID] como datos XDM para [!DNL Analytics]

Inserte la siguiente propiedad en su [!DNL Web SDK] `sendEvent` para enviar el [!DNL StitchID] hasta [!DNL Experience Edge] as [!DNL Experience Data Model] Datos de (XDM) para [!DNL Analytics].<!-- The library will send the StitchID to [!DNL Experience Edge] as `[_adcloud.advertisingStitchID](https://github.com/adobe/xdm/blob/master/docs/reference/adobe/experience/adcloud/stitch.schema.md)`. --> [!DNL Analytics] utilizará el valor como un `SDID`.

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
