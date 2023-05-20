---
title: Preguntas frecuentes
description: xxx
source-git-commit: 1c13874967ec4ad264e5fa6a5e0dfeb6120f53cc
workflow-type: tm+mt
source-wordcount: '367'
ht-degree: 0%

---

# Preguntas frecuentes xxx

## title

https://adobeadcloud.zendesk.com/agent/tickets/14214 De forma predeterminada, Adobe Analytics informa de todos los eventos capturados en cada informe. &quot;[!UICONTROL Unspecified]&quot; eventos representan eventos de finalización de formularios que no estaban conectados a la publicidad de Adobe. Por ejemplo, en el informe Plataforma de publicidad, las conversiones orgánicas o impulsadas por una campaña de correo electrónico caerían en &quot;sin especificar&quot;.

Puede utilizar el filtro para eliminar eventos no especificados de los informes eliminando la marca de verificación de la opción &quot;Incluir no especificado (ninguno)&quot;. <!-- Not sure if this is in DSP or in Analytics Workspace -->

## title

https://adobeadcloud.zendesk.com/agent/tickets/24323 Coloque las etiquetas de evento de Analytics en los mismos puntos que los píxeles de Ad Cloud para asegurarse de que XXX coincida.

## title

https://adobeadcloud.zendesk.com/agent/tickets/24323

P: Durante nuestra auditoría de seguridad interna, se señalaron ciertas funciones como problemas de seguridad que habilitamos al integrar Ad Cloud en nuestra instalación de Adobe Analytics existente.

La integración en cuestión es entre AdCloud y Adobe Audience Manager. Esta función aumenta la tasa de coincidencia del ID de visitante entre AdCloud y Adobe Audience Manager. Para ello, envía solicitudes de red a pagead.l.doubleclick.net, star-mini.c10r.facebook.com y pug88000nf.pubmatic.com para determinar si estos servicios tienen un ID del visitante que se pueda aprovechar. Son las solicitudes de red que se han marcado como riesgo de seguridad y que se producen para todos los visitantes del sitio.

Nuestro auditor nos pide que deshabilitemos esta función. ¿Qué sucede si bloqueamos esas solicitudes de red?

R: Hemos consultado nuestro producto y han comentado que los píxeles en cuestión tienen el propósito de aumentar las tasas de coincidencia de cookies entre Ad Cloud DSP AAM, socios específicos de inventario/SSP (con respecto a la), y el número de píxeles en cuestión.  AAM Si se eliminan, es posible que el cliente vea algún nivel de tasa de coincidencia disminuida entre AAC/y los socios de inventario para los que están los píxeles respectivos, pero no esperarían que fuera sustancial.

Para la búsqueda de Ad Cloud, vemos que el ID de organización Experience Cloud del anunciante está configurado para Mathworks, pero nuestro equipo de productos no ve Mathworks configurado para activar audiencias en Ad Cloud. ¿Utiliza el Audience Manager de Adobe para enviar audiencias a la búsqueda de Ad Cloud? Si no es así, eliminarlos no afectará al flujo de trabajo actual. AAM El Servicio de atención al cliente de puede ayudarle con la eliminación de estos píxeles si no desea que se activen.

