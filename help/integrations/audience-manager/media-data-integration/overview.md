---
title: Información general sobre el envío de datos de exposición de medios de DSP a Adobe Audience Manager
description: Aprenda a utilizar los píxeles de evento de Audience Manager para capturar datos de nivel de impresión y de clic desde campañas de Advertising DSP
feature: Integration with Adobe Audience Manager
exl-id: c299cdf0-a83e-4026-8b8b-22ce08af0cc4
source-git-commit: 7fa058da06edadf9b98aa49b0e5a1110ea68808c
workflow-type: tm+mt
source-wordcount: '529'
ht-degree: 0%

---

# Información general sobre el envío de datos de exposición de medios de DSP a Adobe Audience Manager

*Anunciantes solo con Advertising DSP*

*Solo anunciantes con una integración Adobe Advertising-Adobe Audience Manager*

Los clientes de Advertising DSP con Adobe Audience Manager pueden utilizar los píxeles de evento de Audience Manager para capturar datos de nivel de impresión y datos de nivel de clic desde campañas de DSP. Los píxeles del evento envían los datos como señales procesables a Audience Manager. Estas señales habilitan varios casos de uso de DSP, como una segmentación más avanzada, administración de frecuencias, análisis de marketing y perspectivas de creación de informes.

DSP no cobra por enviar estas señales a Audience Manager. Sin embargo, los costes de ingesta estándar de Audience Manager se pagan en función de las llamadas al servidor, según el contrato de Audience Manager. Audience Manager elimina los eventos duplicados que se rastrean de dos formas diferentes, de modo que cada evento se carga solo una vez.

>[!NOTE]
>
> Audience Manager también admite la captura de datos desde archivos de registro del servidor de publicidad, lo que proporciona menos flexibilidad. Ese proceso no se trata en esta documentación.

## Ventajas principales

* Los datos de DSP campaign se transfieren a Audience Manager en tiempo real y se pueden usar para crear rasgos basados en reglas que se usan para definir segmentos.

* Los segmentos están disponibles para la segmentación inmediatamente después de la calificación de segmentos y características del usuario, lo que refuerza los esfuerzos de segmentación en tiempo real.

* Puede aprovechar los datos de campaña para casos de uso como límite de frecuencia en creativos, redireccionamiento de usuarios expuestos a campañas anteriores y análisis del comportamiento del sitio descendente y los puntos de entrada.

* Los datos agregados proporcionan una vista unificada del rendimiento de la campaña, ayudan a identificar las rutas de conversión personalizadas y se pueden usar para mejorar la secuencia de eventos que conducen a las conversiones a través de Audience Manager [!DNL Audience Optimization Reports] o a través de una [[!DNL Audience Analytics] integración con Adobe Analytics](/help/integrations/audience-manager/audience-analytics.md).

## Seguimiento de los datos

Los píxeles de evento de impresión y clic de Audience Manager están basados en cookies. Los píxeles no capturan eventos que se producen en entornos sin cookies, como aplicaciones móviles y TV conectada (CTV).<!-- 6/24: CTV inventory isn't clickable, and impression tracking would be lost when we convert users from IP to cookies. -->

### Píxeles de seguimiento de impresión

Audience Manager realiza un seguimiento de los datos de impresión de un anuncio cuando se adjunta un píxel de seguimiento de evento transparente de 1xl píxeles al anuncio. El píxel de evento se carga cada vez que se sirve el anuncio a un usuario y se carga mediante el explorador web. El píxel se carga desde un subdominio específico del cliente de [`demdex.net`](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/demdex-calls.html), que es un dominio heredado para Audience Manager, y contiene parámetros como pares clave-valor. La llamada de evento recopila datos de impresión y conversión y los envía a los servidores de recopilación de datos de Audience Manager.

### Píxeles de rastreo de clics

Audience Manager rastrea los clics de manera similar a las impresiones, excepto que no carga el píxel de evento transparente cada vez que se publica el anuncio. En su lugar, los datos de clics se rastrean en la dirección URL de pulsaciones del anuncio. El anuncio apunta a un subdominio específico del cliente de [`demdex.net`](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/demdex-calls.html), que es un dominio heredado de Audience Manager, para que lo procesen los servidores de recopilación de datos de Audience Manager. A continuación, el servidor redirige al usuario a la página de aterrizaje deseada. La dirección URL contiene parámetros como pares clave-valor.

>[!NOTE]
>
>Si su organización utiliza el seguimiento de [!DNL Analytics], es posible que no necesite el rastreo de clics de Audience Manager. Adobe Analytics captura las señales de clic y puede enviarlas a Audience Manager a través de [reenvío del lado del servidor](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/server-side-forwarding/ssf.html).

>[!MORELIKETHIS]
>
>* [Recopilar datos de clics e impresiones de campañas de Advertising DSP](collect.md)
>* [Casos de uso](use-cases.md)
