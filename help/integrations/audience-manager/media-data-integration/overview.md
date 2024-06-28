---
title: DSP Información general sobre el envío de datos de exposición de medios de comunicación de a Adobe Audience Manager
description: Aprenda a utilizar los píxeles de evento del Audience Manager para capturar datos de nivel de impresión y de clic desde campañas de Advertising DSP
feature: Integration with Adobe Audience Manager
exl-id: c299cdf0-a83e-4026-8b8b-22ce08af0cc4
source-git-commit: c204955ec48826d00a5f78e5be4849f53d09e224
workflow-type: tm+mt
source-wordcount: '529'
ht-degree: 0%

---

# DSP Información general sobre el envío de datos de exposición de medios de comunicación de a Adobe Audience Manager

*Solo anunciantes con Advertising DSP*

*Anunciantes con solo integración de Adobe Advertising-Adobe Audience Manager*

Los clientes de Advertising DSP con Adobe Audience Manager pueden utilizar píxeles de evento del Audience Manager DSP para capturar datos de nivel de impresión y datos de nivel de clic de campañas de. Los píxeles de evento envían los datos como señales procesables al Audience Manager. DSP Estas señales habilitan varios casos de uso de, como la segmentación más avanzada, la administración de frecuencias, los análisis de marketing y las perspectivas de creación de informes.

DSP No te cobra por enviar estas señales a Audience Manager. Sin embargo, los costes de ingesta de Audience Manager estándar se pagan en función de las llamadas al servidor, según el contrato de Audience Manager. Audience Manager elimina los eventos duplicados que se rastrean de dos formas diferentes, de modo que cada evento se carga solo una vez.

>[!NOTE]
>
> Audience Manager también admite la captura de datos desde archivos de registro del servidor de publicidad, lo que proporciona menos flexibilidad. Ese proceso no se trata en esta documentación.

## Beneficios primarios

* DSP Los datos de campaña de la campaña de la campaña se transfieren a Audience Manager en tiempo real y se pueden utilizar para crear rasgos basados en reglas que se utilizan para definir segmentos.

* Los segmentos están disponibles para la segmentación inmediatamente después de la calificación de segmentos y características del usuario, lo que refuerza los esfuerzos de segmentación en tiempo real.

* Puede aprovechar los datos de campaña para casos de uso como límite de frecuencia en creativos, redireccionamiento de usuarios expuestos a campañas anteriores y análisis del comportamiento del sitio descendente y los puntos de entrada.

* Los datos agregados proporcionan una vista unificada del rendimiento de la campaña, ayudan a identificar rutas de conversión personalizadas y se pueden utilizar para mejorar la secuencia de eventos que generan conversiones mediante Audience Manager [!DNL Audience Optimization Reports] o a través de un [[!DNL Audience Analytics] integración con Adobe Analytics](/help/integrations/audience-manager/audience-analytics.md).

## Seguimiento de los datos

Los píxeles de evento de impresión y clic del Audience Manager se basan en cookies. Los píxeles no capturan eventos que se producen en entornos sin cookies, como aplicaciones móviles y TV conectada (CTV).<!-- 6/24: CTV inventory isn't clickable, and impression tracking would be lost when we convert users from IP to cookies. -->

### Píxeles de seguimiento de impresión

El Audience Manager realiza un seguimiento de los datos de impresión de un anuncio cuando se adjunta un píxel de seguimiento de evento transparente de 1xl píxeles al anuncio. El píxel de evento se carga cada vez que se sirve el anuncio a un usuario y se carga mediante el explorador web. El píxel se carga desde un subdominio específico del cliente de [`demdex.net`](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/demdex-calls.html), que es un dominio heredado de Audience Manager y contiene parámetros como pares clave-valor. La llamada de evento recopila datos de impresión y conversión y los envía a los servidores de recopilación de datos del Audience Manager.

### Píxeles de rastreo de clics

El Audience Manager rastrea los clics de manera similar a las impresiones, excepto que no carga el píxel de evento transparente cada vez que se publica el anuncio. En su lugar, los datos de clics se rastrean en la dirección URL de pulsaciones del anuncio. El anuncio apunta a un subdominio específico del cliente de [`demdex.net`](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/demdex-calls.html), que es un dominio heredado de Audience Manager, para su procesamiento por parte de los servidores de recopilación de datos de Audience Manager. A continuación, el servidor redirige al usuario a la página de aterrizaje deseada. La dirección URL contiene parámetros como pares clave-valor.

>[!NOTE]
>
>Si su organización utiliza [!DNL Analytics] seguimiento, es posible que no necesite el rastreo de clics del Audience Manager. Adobe Analytics captura las señales de clic y las puede enviar al Audience Manager mediante [reenvío del lado del servidor](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/server-side-forwarding/ssf.html).

>[!MORELIKETHIS]
>
>* [Recopilación de datos de clics e impresiones de campañas de Advertising DSP](collect.md)
>* [Casos de uso](use-cases.md)
