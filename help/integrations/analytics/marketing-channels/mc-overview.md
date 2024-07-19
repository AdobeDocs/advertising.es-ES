---
title: Aspectos básicos de  [!DNL Marketing Channels]
description: Obtenga información clave acerca de [!DNL Analytics Marketing Channels] que [!DNL Analytics for Advertising] los usuarios deben entender.
feature: Integration with Adobe Analytics
exl-id: de02dff5-86ce-41e8-89c6-3c11f6375b77
source-git-commit: 29b49e8fa54580d7cdd62f9a10fd2616def4694b
workflow-type: tm+mt
source-wordcount: '548'
ht-degree: 0%

---

# Aspectos básicos de [!DNL Analytics Marketing Channels]

En esta página se explica la información clave acerca de [!DNL Analytics Marketing Channels] que los usuarios de [!DNL Analytics for Advertising] deben comprender.

Para obtener documentación completa sobre [!DNL Marketing Channels], consulte &quot;[Introducción a  [!DNL Marketing Channels]](https://experienceleague.adobe.com/docs/analytics/components/marketing-channels/c-getting-started-mchannel.html)&quot;.

## Información general de [!DNL Marketing Channels]

[!DNL Marketing Channels] son una característica clave de Adobe Analytics. Los informes de [!DNL Marketing Channels] muestran cómo llegan los clientes al sitio web a través de la ventana de informes y cómo cada canal afecta a los ingresos o al comportamiento en el sitio.

Consideremos el siguiente ejemplo de recorrido entre visitas. Cada visita al sitio web está indicada por el canal de marketing desde el que el visitante entró. La primera visita, también denominada Canal de primer contacto, es Correo electrónico. La visualización en la visita dos es un canal participante y la búsqueda natural se considera el canal de último contacto. Si usa [!UICONTROL Last Touch Attribution] en [!UICONTROL Attribution IQ], la búsqueda natural recibirá el crédito total del evento de conversión de 250 $. Con el servicio de ID de Experience Cloud, puede unir estas visitas individuales para revelar un recorrido de un único visitante.

![Ejemplo de recorrido de conversión entre visitas en los canales de marketing](/help/integrations/assets/a4adc-mc-sample-journey.png)

Al usar [!UICONTROL Marketing Channels] reglas de procesamiento, puede crear conjuntos de lógica para determinar los canales que generan tráfico y realizar un seguimiento de cada canal a medida que los usuarios llegan al sitio. Por ejemplo, el canal [!UICONTROL Email] se indicaría mediante un código de seguimiento único generado al hacer clic que, cuando Adobe Analytics lo registra, clasificaría la visita como originada a partir de una campaña de marketing por correo electrónico.

## Reglas de procesamiento y configuración de los canales de marketing

Cada vez que un usuario llega a un sitio web, lo hace a través de una dirección URL en la que hace clic o directamente ingresa en la barra de direcciones. Cuando el usuario entra al sitio web, [!DNL Analytics] realiza un seguimiento de la información que se puede usar para determinar el canal que condujo a la visita.

A menudo, los especialistas en marketing anexan códigos de seguimiento de parámetros de cadena de consulta a las direcciones URL de los canales para ayudar a realizar un seguimiento del impacto del canal en su sitio. Puede configurar [!DNL Marketing Channels] reglas de procesamiento para detectar parámetros y valores de seguimiento específicos y determinar el canal sin ningún seguimiento adicional. Por ejemplo, si todas las direcciones URL de campañas de correo electrónico siguen el formato `www.adobe.com?cid=email…` (donde la dirección URL contiene el parámetro de cadena de consulta y el valor `cid=email`), puede crear una regla para escuchar este código de seguimiento y agrupar la visita en el canal [!UICONTROL Email].

Otros canales no tienen rutas de URL a las que se pueda realizar un seguimiento y necesitan más lógica para su identificación. Por ejemplo, [!UICONTROL Earned Social], en el cual un usuario hace clic en un vínculo que otro usuario compartió orgánicamente en una red social, es un canal importante de seguimiento. Sin embargo, el experto en marketing no tiene forma de adjuntar un código de seguimiento de parámetros de cadena de consulta a la dirección URL compartida. En este caso, puede crear una regla de procesamiento para detectar el dominio de referencia de las redes sociales de interés y la ausencia de códigos de seguimiento de pago para determinar el canal. Las visitas que cumplan estos requisitos se rastrearán como ganadas en medios sociales en el informe Canales de marketing.

El Adobe recomienda trabajar con su equipo de Analytics para crear un conjunto completo de [!DNL Marketing Channels] reglas de procesamiento para rastrear todos los canales que sean relevantes para su negocio. Al hacerlo, puede crear potentes informes de atribución.

Para comprender cómo el Adobe Advertising puede contribuir a las señales necesarias para crear canales de marketing personalizados, consulte &quot;[Uso de Advertising ID para crear [!DNL Marketing Channels] reglas](mc-ids.md)&quot;.

>[!MORELIKETHIS]
>
>* [Usar ID de Adobe Advertising para crear [!DNL Marketing Channels] reglas de procesamiento](mc-ids.md)
>* [Por qué los datos de canal pueden variar entre el Adobe Advertising y [!DNL Marketing Channels]](mc-data-variances.md)
>* [Usando [!DNL Analytics Marketing Channels] con datos de Adobe Advertising](mc-ac-data.md)
>* [Vídeo: Usando [!DNL Marketing Channels] para informes de Adobe Advertising](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-reporting-a4adc.html)
>* [Información general de [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)
