---
title: Acerca del seguimiento para Search, Social y Commerce
description: Obtenga información acerca de las opciones de seguimiento para Search, Social y Commerce.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Acerca del seguimiento para Search, Social y Commerce

Para realizar un seguimiento del rendimiento de sus anuncios, busque, Social y Commerce necesita datos de impresión, clics, costes y conversiones (transacciones) para sus anuncios. Search, Social y Commerce utilizan estos datos para crear los modelos de previsión de datos que necesita para optimizar sus portafolios de anuncios.

## Datos de costos, clics e impresiones

Search, Social y Commerce recupera datos de impresiones, clics y costes directamente de [redes de publicidad admitidas](/help/search-social-commerce/introduction/supported-inventory.md) cada día. Además, Search, Social y Commerce pueden añadir un código de seguimiento de clics único (incluida la redirección a un servidor de seguimiento) en las plantillas de seguimiento y en las URL de destino para rastrear las impresiones de visualización/contenido, los clics y el coste, y luego enlazar los eventos a las conversiones.

Si desea rastrear campañas en redes de anuncios con las que Search, Social y Commerce no sincroniza datos, debe proporcionar datos para esas campañas enviando un archivo de fuente diario con los datos de impresión, clics y costes.

### Etiquetas de rastreo de clics

Su equipo de implementación de Search, Social y Commerce configura el rastreo de clics actualizando las plantillas de seguimiento y las URL de destino para las extensiones de anuncios, palabras clave, ubicaciones, grupos de productos y vínculos de sitios en sus campañas de anuncios sincronizados para incluir una cadena de ID de seguimiento única y un redireccionamiento de publicidad de Adobe. También agregan seguimiento a los sufijos de la página de aterrizaje (sufijos finales de la URL) para su [!DNL Google Ads] y [!DNL Microsoft Advertising] cuentas y campañas.

Los parámetros de seguimiento permiten que la publicidad de Adobe rastree los clics en un nivel de palabra clave individual (campañas de búsqueda) o de variación de anuncio (campañas de búsqueda con direccionamiento de contenido o sitio, campañas de visualización y campañas sociales). Cada vez que un usuario ve un anuncio en pantalla/contenido o hace clic en uno de sus anuncios, la red de anuncios envía el evento a los servidores de píxeles de Adobe Advertising mediante una etiqueta de seguimiento de clics asociada a la palabra clave o al anuncio. Para clics:

* En el caso de los anuncios de Google Ads y los anuncios publicitarios de Microsoft en exploradores que admiten el seguimiento paralelo, la red de anuncios envía primero el clic a su sitio web y, a continuación, a los servidores de píxeles de Adobe Advertising, que luego colocan una cookie en el equipo del usuario, si es que aún no existe.

* En todos los demás casos, la red de publicidad envía el clic directamente a los servidores de píxeles de Adobe Advertising. El servidor de píxeles coloca una cookie en el equipo del usuario (si aún no existe) y luego redirige al usuario a la URL correspondiente del sitio web. La experiencia general para el usuario final es la misma que sería sin una redirección.

La cookie se establece en [!DNL Adobe] dominio (`everesttech.net`) como cookie de origen. Después de una redirección, el usuario se encuentra en el dominio del anunciante y la cookie se trata como una cookie de terceros. Para obtener más información sobre las cookies de Adobe Advertising, consulte &quot;[Adobe Cookies publicitarias](https://experienceleague.adobe.com/docs/core-services/interface/ec-cookies/cookies-advertising-cloud.html).&quot;

## Datos de conversión

Cuando un cliente hace clic en un anuncio o visualiza un anuncio en pantalla o social, Search, Social y Commerce deben asignar cada conversión resultante de nuevo al clic o a la impresión de visualización/social que lo origina.

El anunciante desempeña un papel en el suministro de los datos de conversión para todos los clics y visualizaciones/impresiones sociales. Los datos de conversión pueden incluir información sobre cualquier tipo de evento que se produce en un sitio web y que puede utilizarse para la optimización de ofertas. Puede proporcionar datos de conversión implementando el código de seguimiento de conversión en las páginas de conversión del anunciante (como la página de &quot;éxito&quot; que se muestra después de que un cliente complete una transacción) o enviando un archivo de fuente diario con datos de conversión capturados por otro método.

### Etiquetas de seguimiento de conversión

Puede utilizar [etiquetas de conversión de varios proveedores](/help/search-social-commerce/tracking/conversion-tracking-about.md).

Cuando utiliza una etiqueta de conversión de publicidad de Adobe y un usuario completa una transacción correcta y aterriza en una página de &quot;éxito&quot;, el servidor de píxeles de publicidad de Adobe comprueba la existencia de la cookie en el equipo del usuario, que se configuró en el momento de la redirección de clics. Cuando encuentra una cookie, la información sobre el evento de transacción se pasa mediante el parámetro ef_transid y la transacción se reconoce como una conversión y se acredita a la impresión de clic o visualización anterior.

Si el usuario hizo clic en más de uno de sus anuncios, Adobe Advertising acredita la transacción al clic final del anuncio o (para campañas de visualización o vídeo) a la impresión final del anuncio a menos que especifique lo contrario. Su [haga clic en ventana retrospectiva](/help/search-social-commerce/glossary.md#c-d) y [ventana retrospectiva de impresiones](/help/search-social-commerce/glossary.md#i-j) determine el número de días después de que se produzca un clic de pago o una impresión de visualización/vídeo (respectivamente) en los que el evento puede atribuirse a una conversión.

El equipo de implementación de la publicidad de Adobe trabaja con el anunciante para determinar el formato de las etiquetas de conversión que este debe implementar, identificar las páginas web en las que debe insertarse cada etiqueta de conversión y, a continuación, proporcionarle las etiquetas de conversión que debe implementar.