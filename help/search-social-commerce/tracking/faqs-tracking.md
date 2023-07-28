---
title: Preguntas frecuentes sobre el seguimiento
description: Obtenga respuestas a preguntas comunes sobre el seguimiento, incluidos problemas de resolución de problemas.
exl-id: f559b977-dd44-4d29-b49e-c41c6fb783d1
feature: Search Tracking
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '1191'
ht-degree: 0%

---

# Preguntas frecuentes sobre el seguimiento

## Funciones de seguimiento

+++¿Puedo rastrear campañas que el Adobe Advertising no administra?

Sí. Si Search, Social y Commerce está sincronizando una de las cuentas de red de publicidad, rastreará los datos de clics de la red de publicidad para todos [tipos de campaña admitidos](/help/search-social-commerce/introduction/supported-inventory.md) en esa cuenta. También realiza un seguimiento de los datos de conversión si ha añadido el redireccionamiento de Search, Social y Commerce a las URL de destino de publicidad o palabra clave o a las plantillas de seguimiento, y si ha implementado el seguimiento de conversión en sus páginas de conversión. Aclarar con el equipo de cuenta de Adobe qué campañas desea que Search, Social y Commerce rastreen simplemente y cuáles desea que administren.
+++

+++¿Cómo obtengo la atribución de varios eventos?

Para los anunciantes que utilizan las etiquetas de seguimiento de conversión Search, Social y Commerce o Adobe Analytics, Adobe Advertising proporciona varias opciones para atribuir datos de conversión en una serie de eventos que generan una conversión. Una configuración de nivel de anunciante determina cómo atribuir datos de conversión entre eventos, incluso cuando se producen en varios canales de publicidad, siempre y cuando los canales permitan el seguimiento de impresiones en el nivel de evento. De forma predeterminada, las conversiones se atribuyen al último evento (el más reciente), pero la configuración puede ser diferente, como atribuir conversiones al primer evento o ponderar todos los eventos de forma uniforme. Cambiar la regla de atribución afecta a cómo se calculan las ofertas futuras.

Los anunciantes que proporcionan todos los datos de conversión en un archivo de fuente deben atribuir la conversión a los propios eventos de transacción relacionados.

>[!NOTE]
>
>En las vistas, los informes y las simulaciones personalizadas de administración de campañas y administración de portafolios (disponibles para algunos usuarios), puede cambiar la regla utilizada para atribuir datos de conversión dentro de las vistas y los resultados del informe, sin afectar a cómo se calculan las ofertas futuras.

+++

+++¿Cómo identifica el Adobe Advertising las transacciones duplicadas?

Las transacciones duplicadas pueden producirse cuando un usuario actualiza la página de confirmación después de completar una transacción. El Adobe Advertising utiliza el `ev_transid` para eliminar transacciones duplicadas con el mismo ID de transacción y valor de propiedad.

La siguiente es la lógica de deduplicación de Adobe Advertising:

* **Cuando un cliente envía un valor para `ev_transid` atributo:** Las solicitudes de píxeles posteriores se consideran duplicados de la anterior si todas las siguientes son iguales: `ev_transid`; el ID de seguimiento para la misma palabra clave, anuncio o ubicación; y el valor de una propiedad de transacción específica.

  Por ejemplo, si varias solicitudes de préstamo tienen el mismo ID de aplicación y el mismo importe de préstamo para la misma palabra clave en una red de publicidad específica, se consideran duplicados y solo se cuenta la primera solicitud de préstamo.

* **Cuando un cliente no envía un valor para `ev_transid` atributo:** Las transacciones posteriores se consideran duplicados de la anterior si comparten un ID de seguimiento para la misma palabra clave, anuncio o ubicación, y el mismo valor para una propiedad de transacción específica.

  Por ejemplo, si varias solicitudes de préstamo tienen el mismo ID de palabra clave y el mismo importe de préstamo, se consideran duplicados y solo se cuenta la primera solicitud de préstamo.
+++

## Tipos de implementación de seguimiento

+++Quiero dejar de usar el servicio de seguimiento de conversión de Adobe Advertising para una o más campañas o cuentas. ¿Cómo puedo eliminar rápidamente el código de seguimiento de las direcciones URL de seguimiento?

En primer lugar, consulte con su equipo de cuenta de Adobe para comprender las implicaciones de eliminar las URL de seguimiento.

En la cuenta o campaña, cambie el método de seguimiento a &quot;[!UICONTROL No EF Redirect].&quot; A continuación, cree una hoja de edición masiva utilizando la variable &quot;[!UICONTROL Generate Tracking URLs]&quot; y publicarla en la red de anuncios. Se reemplazarán todas las URL de seguimiento o URL de destino existentes.
+++

## Preguntas de datos

+++¿Cómo sé qué propiedad de transacción procede de una fuente de datos o se rastrea con la etiqueta de seguimiento de conversión de Adobe Advertising?

En un [!UICONTROL Transaction Report], puede saber si el píxel de seguimiento de conversión de Adobe Advertising ha rastreado una propiedad de transacción incluida si incluye la columna personalizada &quot;[!UICONTROL Tracking URL].&quot; Las direcciones URL de seguimiento con el píxel de seguimiento de Adobe Advertising comienzan por `http://pixel.everesttech.net`.
+++

+++¿Qué son las transacciones huérfanas?

Las transacciones huérfanas son eventos de transacción que no se pueden asociar con una palabra clave o publicidad específica. Adobe Advertising atribuye los /ingresos a una palabra clave o anuncio haciendo coincidir los ID de seguimiento recibidos con el evento de ingresos con el ID de seguimiento único de la URL de seguimiento de la palabra clave o del anuncio.

Cuando un equipo de cuenta de Adobes sospecha que las transacciones huérfanas son responsables de una caída en los ingresos, el equipo del Servicio de atención al cliente comprueba si hay huérfanos y, si encuentra alguno, investiga el problema.

Los huérfanos se producen en las siguientes situaciones.

**Implementaciones de píxeles**

Las transacciones huérfanas casi nunca ocurren en implementaciones de píxeles. Sin embargo, se han producido huérfanos de píxeles cuando:

* Los datos de clics no están disponibles para la fecha de clics de la conversión. En este caso, los datos se asignan de nuevo cuando Search, Social y Commerce obtienen los datos de clics de la red publicitaria.

* Los registros de clics no se procesan antes que los registros de conversión.

**Implementaciones de fuentes**

* El ID de seguimiento enviado en la fuente procede de una cuenta que Search, Social y Commerce no conocen.

* La cuenta no está sincronizada o se han producido errores durante el proceso de sincronización.

* El ID de seguimiento se añadió y eliminó de la red de anuncios mientras que Search, Social y Commerce no estaba sincronizado con la red de anuncios, por lo que Search, Social y Commerce no tiene información sobre el ID. Este problema sigue causando ingresos huérfanos si se produce un retraso en la recepción de ingresos.

* El cliente envió un ID de seguimiento con un formato incorrecto en la fuente y que no coincide con el ID de seguimiento de la dirección URL. Esto suele ocurrir debido a un problema de formato o cuando los ID de seguimiento se abrevian en la fuente.

* En el archivo de configuración, la expresión regular utilizada para extraer el ID de seguimiento de las direcciones URL es incorrecta o está obsoleta. A veces, el anunciante cambia el ID de seguimiento en la dirección URL o adopta un sistema de seguimiento completamente nuevo, que requiere que el equipo de implementación de Search, Social y Commerce actualice la expresión regular. En estos casos, una parte importante de los ingresos se queda huérfana.

**Implementaciones de fuentes mediante un ID de transacción**

No hay transacciones en línea disponibles antes de las fechas para las que los datos están disponibles en la fuente sin conexión.

**Implementaciones de fuentes mediante un token (ef_id)**

Search, Social y Commerce no pueden encontrar el clic correspondiente en su servidor o en la red de publicidad. Esto puede deberse a que los datos de clics no están disponibles para la fecha de clics de la conversión o (en raras ocasiones) a que los registros de clics no se procesaban antes que los registros de conversión. Cuando Search, Social y Commerce reciben los datos de clics de la red de anuncios o se procesan los registros de clics, los datos se asignan a la conversión.
+++

## Problemas de seguimiento de ingresos

+++¿Cómo corrijo datos antiguos o incorrectos de un archivo de fuente?

Póngase en contacto con el Servicio de atención al cliente con el archivo de datos corregido.
+++

+++Varias palabras clave tienen las mismas direcciones URL de seguimiento.

**Implicaciones**

En el caso de implementaciones de fuentes con varios ID de seguimiento, los datos se comunican usando varias palabras clave. En otras implementaciones, las conversiones pueden atribuirse a la palabra clave incorrecta porque el sistema asigna una conversión arbitrariamente a una de las palabras clave.

**Causa posible**

La dirección URL de una nueva palabra clave o anuncio se copió de otra palabra clave o anuncio.

Esto no debería suceder con anuncios en pantalla o en redes sociales.

**Posible solución o solución alternativa**

* Si administra sus propias palabras clave y anuncios, cree un archivo de hoja de edición masiva con las direcciones URL correctas para las direcciones URL duplicadas y publíquelo en la cuenta correspondiente mediante la variable **[!UICONTROL Generate Tracking URLs]** , que regenera las direcciones URL de todas las palabras clave y anuncios.

* Si un equipo de cuenta de Adobe administra sus palabras clave, pídale que cree nuevas direcciones URL para las direcciones URL duplicadas.
+++
