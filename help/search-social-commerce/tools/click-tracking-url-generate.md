---
title: Generar una URL de seguimiento de clics
description: Obtenga información sobre cómo generar manualmente una URL de seguimiento de clics de Search, Social y Commerce.
exl-id: 43a36869-146a-4c5f-b4f2-eddfb856480b
feature: Search Tools, Search Tracking
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '458'
ht-degree: 0%

---

# Generación de una URL de seguimiento de clics de Search, Social y Commerce con la herramienta URL de seguimiento

*Anunciantes con solo seguimiento de conversión de Adobe Advertising*

Para obtener información acerca de cuándo debe generar e implementar manualmente una dirección URL de seguimiento de clics, consulte &quot;[Cuándo y cómo generar direcciones URL de seguimiento de clics](/help/search-social-commerce/tracking/click-tracking-ways-to-generate.md)&quot;.

>[!NOTE]
>
>Esta función no implementa la plantilla de seguimiento o la dirección URL de destino en la cuenta de publicidad correspondiente.

1. En el menú principal, haga clic en **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Tools] >[!UICONTROL Tracking URL]**.

1. Seleccione la cuenta de red de anuncios de la lista.

   ([!DNL Google Ads] palabras clave; texto, instalación de aplicaciones móviles y anuncios dinámicos de búsqueda; ubicaciones; vínculos de sitios y grupos de productos) Se muestran las etiquetas de seguimiento del campo de la plantilla de seguimiento. No incluyen ningún parámetro de datos anexados de nivel de cuenta. Pasar al paso 4.

   Para el resto de tipos de etiquetas, introduzca información para generar una etiqueta.

1. (Si es necesario) Genere una etiqueta:

   1. Especifique las páginas de aterrizaje, con vínculos de sitio o nombres de producto cuando se solicite, de una de las siguientes maneras:

      * Especifique un archivo que contenga la información introduciendo la ruta de acceso completa y el nombre de archivo o haciendo clic en **[!UICONTROL Browse]** para localizar el archivo en su dispositivo o red. El archivo debe ser un archivo de texto delimitado por tabuladores con un elemento por línea en el formato siguiente:

         * (Creativos, anuncios estándar) `**landing_page**`

           donde `landing_page` es una dirección URL válida de la página de aterrizaje o una dirección URL base.

           Ejemplo: http://www.example.com/travel.html

         * ([!DNL Microsoft Advertising] enlaces de sitios) `sitelink <tab> ** <tab> landing_page`

           donde `sitelink` es el nombre del vínculo del sitio y `landing_page` es una dirección URL de página de aterrizaje o una dirección URL base válidas.

           Ejemplo: `Careers <tab> ** <tab> http://www.example.com/careers.html`

           El archivo puede incluir hasta 10 000 líneas.

         * ([!DNL Google Merchant Center] grupos de productos y [!DNL Microsoft Advertising] anuncios de productos) `product name <tab> ** <tab> landing_page`

           donde `product name` es el nombre del producto y `landing_page` es una dirección URL de página de aterrizaje o una dirección URL base válidas.

           Ejemplo: `Acme PR208 <tab> ** <tab> http://www.example.com/travel.html`

           El archivo puede incluir hasta 10 000 líneas.

      * En el campo de entrada, introduzca un elemento por línea en el siguiente formato:

         * (Creativos, anuncios estándar) `landing_page`

           donde `landing_page` es una dirección URL válida de la página de aterrizaje o una dirección URL base.

           Ejemplo: http://www.example.com/travel.html

         * ([!DNL Microsoft Advertising] enlaces de sitios) `sitelink**landing_page`

           donde `sitelink` es el nombre del vínculo del sitio y `landing_page` es una dirección URL de página de aterrizaje o una dirección URL base válidas.

           Ejemplo: `Careers**http://www.example.com/careers.html`

         * ([!DNL Google Merchant Center] grupos de productos y [!DNL Microsoft Advertising] anuncios de productos) `product name**landing_page`

           donde `product name` es el nombre del producto y `landing_page` es una dirección URL de página de aterrizaje o una dirección URL base válidas.

           Ejemplo: Acme PR208**http://www.example.com/travel.html

   1. Haga clic en **[!UICONTROL Generate Tracking URLs]**.

1. (Opcional) Copie las direcciones URL (empezando por &quot;http&quot; o &quot;https&quot;) de la pantalla o la página de salida e impleméntelas en la cuenta de búsqueda o social.

Para las cuentas con direcciones URL de destino, ingrese los valores en los campos correspondientes de [!UICONTROL Base URL].

En el caso de las cuentas con direcciones URL finales, introduzca el valor en pantalla en el campo [!UICONTROL Tracking Template] correspondiente. Debe agregar un parámetro para la dirección URL final después del parámetro `&url=` (como `{lpurl}`). Para cuentas de [!DNL Yahoo! Japan Ads], use el parámetro `{lpurl}`. Para obtener una lista de [!DNL Google Ads] y [!DNL Microsoft Advertising] parámetros que indiquen las direcciones URL finales en las plantillas de seguimiento, consulte la [[!DNL Google Ads] documentación](https://support.google.com/google-ads/answer/6305348) (vea los parámetros &quot;Solo plantilla de seguimiento&quot; en la sección sobre &quot;Parámetros disponibles [!DNL ValueTrack]&quot;) y la [[!DNL Microsoft Advertising] documentación](https://help.ads.microsoft.com/#apex/3/en/56799/2).

>[!MORELIKETHIS]
>
>* [Acerca de las herramientas para crear y descodificar etiquetas de seguimiento](tracking-tools-about.md)
>* [Cuándo y cómo generar URL de seguimiento de clics](/help/search-social-commerce/tracking/click-tracking-ways-to-generate.md)
>* [Descodificar una URL de rastreo de clics de Search, Social y Commerce](click-tracking-url-decode.md)
