---
title: "Convertir los ID de usuario de [!DNL ActionIQ] a los ID universales"
description: DSP "Aprenda a habilitar la ingesta de datos por parte de los [!DNL ActionIQ] segmentos de origen".
feature: DSP Audiences
source-git-commit: 87080d8152ccf3aa9249a88379ecc9f919c0854d
workflow-type: tm+mt
source-wordcount: '276'
ht-degree: 0%

---

# Conversión de ID de usuario [!DNL ActionIQ] a los ID universales

*Función beta*

DSP Uso de la integración de la con [!DNL ActionIQ] plataforma de datos del cliente para convertir las direcciones de correo electrónico con hash en ID universales para la publicidad de destino.

No hay <!-- NN --> pasos para compartir datos de [!DNL ActionIQ] DSP con la:

1. [DSP Creación de una fuente de audiencia en la](#source-create).

1. ?

## DSP Paso 1: Creación de una fuente de audiencia en el {#source-create}

1. [Crear una fuente de audiencia](source-manage.md) DSP para importar audiencias a su cuenta de o a una cuenta de anunciante, especificando la variable [formatos de ID universales](source-about.md) a los que desea convertir los identificadores de usuario.

1. Después de crear la fuente de audiencia, comparta la clave de código fuente con el [!DNL ActionIQ] usuario.

1. Una vez completados todos los pasos, consulte en la biblioteca de audiencias (que está disponible cuando crea o edita una audiencia desde ) [!UICONTROL Audiences] > [!UICONTROL All Audiences] o dentro de la configuración de ubicación) que el segmento se está rellenando en un plazo de 24 horas. Compare el número de ID universales con el número de direcciones de correo electrónico con hash originales.

   La tasa de traducción de las direcciones de correo electrónico con hash a los ID universales debe ser superior al 90 %. Por ejemplo, si envía 100 direcciones de correo electrónico con hash desde la plataforma de datos del cliente, deben traducirse a más de 90 ID universales. Una tasa de traducción del 90 % o menos es un problema. Para obtener más información sobre cómo pueden variar los recuentos de segmentos, consulte[Causas de variaciones de datos entre ID de correo electrónico e ID universales](#universal-ids-data-variances).&quot;

   Para obtener ayuda sobre la resolución de problemas, póngase en contacto con su equipo de cuenta de Adobe o `adcloud-support@adobe.com`.

Los segmentos se actualizan cada 24 horas.

## Paso 2:

>[!MORELIKETHIS]
>
>* [Acerca de las fuentes de audiencia de origen](/help/dsp/audiences/sources/source-about.md)
>* [Administrar fuentes de audiencia para activar audiencias de ID universal](source-manage.md)
>* [Conversión de ID de usuario [!DNL Adobe Real-Time CDP] a los ID universales](/help/dsp/audiences/sources/source-adobe-rtcdp.md)
>* [Conversión de ID de usuario [!DNL Tealium] a los ID universales](/help/dsp/audiences/sources/source-tealium.md)
>* [Acerca de Audience Management](/help/dsp/audiences/audience-about.md)
