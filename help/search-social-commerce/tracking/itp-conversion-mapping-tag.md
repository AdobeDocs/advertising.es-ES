---
title: La etiqueta de asignación de conversión de la publicidad de Adobe
description: Obtenga información acerca de la etiqueta de asignación de conversión basada en JavaScript para ITP 2.2, que permite a la publicidad de Adobe realizar un seguimiento de un evento de conversión que se produce en una página que no es la página de aterrizaje.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# La etiqueta de asignación de conversión JavaScript de Adobe Advertising

*Anunciantes con solo seguimiento de conversión de publicidad de Adobe*

La etiqueta de asignación de conversión basada en JavaScript de publicidad de Adobe, cuando se utiliza además de la etiqueta de seguimiento de conversión de JavaScript de publicidad de Adobe v2 o v3, permite a la publicidad de Adobe rastrear un evento de conversión que se produce en una página que no es la página de aterrizaje. La solución ITP 2.2 almacena la cookie de un usuario en el almacenamiento local en un iFrame propiedad del anunciante. El almacenamiento local puede entonces mantener el valor de la cookie desde el clic descendente hasta la página de conversión.

Utilice la etiqueta de asignación de Adobe para asegurarse de que la publicidad de conversión puede realizar un seguimiento de todas las conversiones que se producen en los exploradores Apple Safari y Mozilla Firefox, lo que limita la persistencia de cookies de origen. <!-- For all requirements to track conversions from Safari, see "Track Conversions from Apple Safari Browsers." -->

Para utilizar la etiqueta de asignación de conversión:

1. [Implementación de la etiqueta de asignación de conversión](#deploy-conversion-mapping-tag).

1. Si su organización utiliza varios ID de organización de Adobe Experience Cloud Identity Service (anteriormente denominados ID de organización de IMS), [actualización de las etiquetas de conversión](#update-conversion-tags) para incluir el ID de organización.

1. [Validación de la implementación de etiquetas](#validate-conversion-mapping).

## Implemente la etiqueta de asignación de conversión de JavaScript para ITP 2.2 {#deploy-conversion-mapping-tag}

>[!NOTE]
>
>Si está utilizando la etiqueta de asignación de conversión de JavaScript para ITP 2.0, reemplace la etiqueta existente en todas las páginas de conversión con una de las siguientes etiquetas.<!-- any other instructions, too? Point them to the other page on Track Conversions from Safari...." -->

* Si su organización utiliza un único ID de organización, que se utiliza en su cuenta de Search, Social y Commerce, utilice la siguiente etiqueta:

   `<script src="//www.everestjs.net/static/amo-conversion-mapper.js" userid="{AMO User ID}"></script>`

   dónde se reemplaza `{AMO User ID}` con el ID de usuario único para su cuenta de Search, Social y Commerce.

* Si su organización utiliza varios ID de organización, utilice la siguiente etiqueta:

   `<script src="//www.everestjs.net/static/amo-conversion-mapper.js" imsorgid="{xxxxxx@AdobeOrg}" userid="{AMO User ID}"></script>`

   donde:

   * reemplace el valor `{xxxxxx@AdobeOrg}` con el ID de organización para el que se realiza un seguimiento de las conversiones de la página. Utilice el mismo ID de organización para todas las páginas de conversión.

   * usted reemplaza `{AMO User ID}` con el ID de usuario único para su cuenta de Search, Social y Commerce.

* Si utiliza un sistema de administración de etiquetas que no admite la adición de `imsorgid` a la etiqueta de script y, a continuación, utilice el siguiente código en su lugar:

   *Si su organización utiliza un solo ID de organización:

   ```
   <script>
   window.ad_cloud = window.ad_cloud || {};
   window.ad_cloud.userid = "{AMO User ID}"
   </script>
   <script src="//www.everestjs.net/static/amo-conversionmapper.js"></script>
   ```

   dónde se reemplaza `{AMO User ID}` con el ID de usuario único para su cuenta de Search, Social y Commerce.

   * Si su organización utiliza varios ID de organización:

      ```
      <script>
      window.ad_cloud = window.ad_cloud || {};
      window.ad_cloud.imsorgid = "{xxxxxx@AdobeOrg}"
      window.ad_cloud.userid = "{AMO User ID}"
      </script>
      <script src="//www.everestjs.net/static/amo-conversionmapper.js"></script>
      ```

      donde:

      * reemplace el valor `{xxxxxx@AdobeOrg}` con el ID de organización para el que se realiza un seguimiento de las conversiones de la página. Utilice el mismo ID de organización para todas las páginas de conversión.

      * usted reemplaza `{AMO User ID}` con el ID de usuario único para su cuenta de Search, Social y Commerce.

Si no conoce el valor de su ID de organización de o su ID de usuario de Search, Social y Commerce, consulte con su administrador de cuentas de Adobe.

### Ejemplos

```
<script src="//www.everestjs.net/static/amo-conversion-mapper.js" imsorgid="abc12345@AdobeOrg" userid="99999"></script>`
```

```
<script>
window.ad_cloud = window.ad_cloud || {};
window.ad_cloud.imsorgid = "abc12345@AdobeOrg"
window.ad_cloud.userid = "99999"
</script>
<script src="//www.everestjs.net/static/amo-conversion-mapper.js"></script>
```

### Dónde se agrega la etiqueta

Añada la etiqueta en cualquier página que pueda ser una página de aterrizaje haciendo clic en la búsqueda (idealmente, en todas las páginas, ya que las páginas de aterrizaje pueden cambiar con el tiempo). Debe cargarse antes de la etiqueta de seguimiento de conversión de JavaScript v3 de Adobe Advertising.

Si se coloca dentro de una etiqueta iframe o de contenedor, entonces:

* El iframe debe estar en el mismo nivel que el dominio de nivel superior.

* La etiqueta de asignación de conversión debe estar solo un (1) nivel por debajo del dominio de nivel superior.

## Actualice las etiquetas de conversión de JavaScript {#update-conversion-tags}

Si su organización utiliza varios ID de organización, añada el ID de organización para el que se realiza el seguimiento de las conversiones de una página a las etiquetas de conversión de JavaScript existentes.

Si su organización utiliza un ID de organización, este paso no es necesario.

### Etiquetas de JavaScript V2

Agregue la siguiente cadena al principio de la etiqueta de script de conversión:

`ef_imsorgid="{xxxxxx@AdobeOrg}";`

donde se reemplaza el valor `{xxxxxx@AdobeOrg}` con el ID de organización para el que se realiza un seguimiento de las conversiones de la página.

Ejemplo:

```
<script language="javascript" src="https://www.everestjs.net/static/st.v2.js"></script>
<script language="javascript">
ef_imsorgid = "abc12345@AdobeOrg";
var ef_event_type="transaction";
var ef_transaction_properties = "ev_property name=<property name>&ev_transid=<transid>";
/*
 * Do not modify below this line
 */
var ef_segment = "";
var ef_search_segment = "";
var ef_userid="ef-userid";
var ef_pixel_host="pixel.everesttech.net";
var ef_fb_is_app = 0;
var ef_allow_3rd_party_pixels = 1;
effp();
</script>
<noscript><img src="https://pixel.everesttech.net/<ef-userid>/t?ev_property name=<property name>&ev_transid=<transid>" width="1" height="1"/></noscript>
```

### Etiquetas de JavaScript V3

Después `window.EF` se ha definido, añada la siguiente cadena:

`window.EF.imsorgid = "{xxxxxx@AdobeOrg}";`

donde se reemplaza el valor `{xxxxxx@AdobeOrg}` con el ID de organización para el que se realiza un seguimiento de las conversiones de la página.

Ejemplo:

```
<script type='text/javascript'>
    (function() {
        var f = function() {
              EF.init({ eventType: "transaction",
                        transactionProperties : "ev_property=<property name>&ev_transid=<transid>",
                        segment : "",
                        searchSegment : "",
                        sku : "",
                        userid : "ef-userid",
                        pixelHost : "pixel.everesttech.net"
                        
                        , allow3rdPartyPixels: 1});
              EF.main();
        };
        window.EF = window.EF || {};
        window.EF.imsorgid ="abc12345@AdobeOrg";
        if (window.EF.main) {
            f();
            return;
        }
        window.EF.onloadCallbacks = window.EF.onloadCallbacks || [];
        window.EF.onloadCallbacks[window.EF.onloadCallbacks.length] = f;
        if (!window.EF.jsTagAdded) {
            var efjs = document.createElement('script'); efjs.type = 'text/javascript'; efjs.async = true;
            efjs.src = 'https://www.everestjs.net/static/st.v3.js';
            var s = document.getElementsByTagName('script')[0]; s.parentNode.insertBefore(efjs, s);
            window.EF.jsTagAdded=1;
        }
    })();
</script>
<noscript><img src="https://pixel.everesttech.net/<ef-userid>/t?ev_property=<property name>&ev_transid=<transid>" width="1" height="1"/></noscript>
```

## Validación de la implementación de etiquetas {#validate-conversion-mapping}

Solicite ayuda al equipo de cuenta de Adobe para validar la etiqueta de asignación de conversión y la etiqueta de conversión normal (si la ha actualizado).
