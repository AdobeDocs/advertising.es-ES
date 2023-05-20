---
title: Aspectos básicos de [!DNL Marketing Channels]
description: Obtenga información clave sobre [!DNL Analytics Marketing Channels] que [!DNL Analytics for Advertising] Los usuarios de deben comprender.
feature: Integration with Adobe Analytics
exl-id: de02dff5-86ce-41e8-89c6-3c11f6375b77
source-git-commit: 7e614ecb517515217d812926f61ca10437820efd
workflow-type: tm+mt
source-wordcount: '568'
ht-degree: 0%

---

# Aspectos básicos de [!DNL Analytics Marketing Channels]

*Anunciantes con una integración de Adobe de Advertising-Adobe Analytics solamente*

Esta página explica la información clave sobre [!DNL Analytics Marketing Channels] que [!DNL Analytics for Advertising] Los usuarios de deben comprender.

Para obtener toda la documentación sobre [!DNL Marketing Channels], consulte &quot;[Introducción a [!DNL Marketing Channels]](https://experienceleague.adobe.com/docs/analytics/components/marketing-channels/c-getting-started-mchannel.html).&quot;

## Información general de [!DNL Marketing Channels]

[!DNL Marketing Channels] son una función clave de Adobe Analytics. [!DNL Marketing Channels] Los informes de muestran cómo llegan los clientes al sitio web a través de la ventana de informes y cómo cada canal afecta a los ingresos o al comportamiento en el sitio.

Consideremos el siguiente ejemplo de recorrido entre visitas. Cada visita al sitio web está indicada por el canal de marketing desde el que el visitante entró. La primera visita, también denominada Canal de primer contacto, es Correo electrónico. La visualización en la visita dos es un canal participante y la búsqueda natural se considera el canal de último contacto. Si utiliza [!UICONTROL Last Touch Attribution] dentro [!UICONTROL Attribution IQ], Natural Search recibiría crédito total por el evento de conversión de 250 $. Con el servicio de ID de Experience Cloud, puede unir estas visitas individuales para revelar un recorrido de un único visitante.

![Ejemplo de recorrido de conversión entre visitas en los canales de marketing](/help/integrations/assets/a4adc-mc-sample-journey.png)

Mediante [!UICONTROL Marketing Channels] Reglas de procesamiento: puede crear conjuntos de lógica para determinar los canales que generan tráfico y para rastrear cada canal a medida que los usuarios llegan al sitio. Por ejemplo, la variable [!UICONTROL Email] El canal se indicaría mediante un código de seguimiento único generado al hacer clic en que, cuando Adobe Analytics lo registra, clasificaría la visita como originada en una campaña de marketing por correo electrónico.

## Reglas de procesamiento y configuración de los canales de marketing

Cada vez que un usuario llega a un sitio web, lo hace a través de una dirección URL en la que hace clic o directamente ingresa en la barra de direcciones. Cuando el usuario entra en el sitio web, [!DNL Analytics] rastrea información que se puede utilizar para determinar el canal que condujo a la visita.

A menudo, los especialistas en marketing anexan códigos de seguimiento de parámetros de cadena de consulta a las direcciones URL de los canales para ayudar a realizar un seguimiento del impacto del canal en su sitio. Puede configurar [!DNL Marketing Channels] reglas de procesamiento para detectar parámetros y valores de seguimiento específicos y determinar el canal sin ningún seguimiento adicional. Por ejemplo, si todas las direcciones URL de la campaña de correo electrónico siguen el formato `www.adobe.com?cid=email…` (donde la dirección URL contiene el parámetro y el valor de la cadena de consulta) `cid=email`), puede crear una regla para detectar este código de seguimiento y agrupar la visita en [!UICONTROL Email] canal.

Otros canales no tienen rutas de URL a las que se pueda realizar un seguimiento y necesitan más lógica para su identificación. Por ejemplo, [!UICONTROL Earned Social], en el que un usuario hace clic en un vínculo que otro usuario ha compartido de forma orgánica en una red social, es un canal importante de rastrear. Sin embargo, el experto en marketing no tiene forma de adjuntar un código de seguimiento de parámetros de cadena de consulta a la dirección URL compartida. En este caso, puede crear una regla de procesamiento para detectar el dominio de referencia de las redes sociales de interés y la ausencia de códigos de seguimiento de pago para determinar el canal. Las visitas que cumplan estos requisitos se rastrearán como ganadas en medios sociales en el informe Canales de marketing.

Adobe recomienda trabajar con su equipo de análisis para crear un conjunto completo de [!DNL Marketing Channels] reglas de procesamiento para realizar un seguimiento de todos los canales pertinentes para su negocio. Al hacerlo, puede crear potentes informes de atribución.

Para comprender cómo la publicidad de Adobe puede contribuir a las señales necesarias para crear canales de marketing personalizados, consulte[Uso de ID de publicidad para crear [!DNL Marketing Channels] Reglas](mc-ids.md).&quot;

>[!MORELIKETHIS]
>
>* [Uso de ID de publicidad de Adobe para crear [!DNL Marketing Channels] Reglas de procesamiento](mc-ids.md)
>* [Por qué los datos de canal pueden variar entre la publicidad de Adobe y [!DNL Marketing Channels]](mc-data-variances.md)
>* [Uso de [!DNL Analytics Marketing Channels] con datos publicitarios de Adobe](mc-ac-data.md)
>* [Vídeo: Uso de [!DNL Marketing Channels] para informes de publicidad de Adobe](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-reporting-a4adc.html)
>* [Información general de [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)

