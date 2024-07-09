---
title: "Convertir los ID de usuario de [!DNL ActionIQ] a los ID universales"
description: DSP "Aprenda a habilitar la ingesta de datos por parte de los [!DNL ActionIQ] segmentos de origen".
feature: DSP Audiences
source-git-commit: 91b08bf54f067666c9c27949ff740639738887d0
workflow-type: tm+mt
source-wordcount: '269'
ht-degree: 0%

---

# Conversión de ID de usuario [!DNL ActionIQ] a los ID universales

*Función Beta*

DSP Uso de la integración de la con [!DNL ActionIQ] plataforma de datos del cliente para convertir las direcciones de correo electrónico con hash en ID universales para la publicidad de destino.

No hay <!-- NN --> pasos para compartir datos de [!DNL ActionIQ] DSP con la:

1. [DSP Creación de una fuente de audiencia en la](#source-create).

1. ?

## DSP Paso 1: Creación de una fuente de audiencia en el {#source-create}

1. [Crear una fuente de audiencia](source-manage.md) DSP para importar audiencias a su cuenta de o a una cuenta de anunciante, especificando la variable [formatos de ID universales](source-about.md) a los que desea convertir los identificadores de usuario.

1. Después de crear la fuente de audiencia, comparta la clave de código fuente con el [!DNL ActionIQ] usuario.

## Paso 2:

## Paso 3:

1. Verifique en su biblioteca de audiencias (que está disponible cuando crea o edita una audiencia desde [!UICONTROL Audiences] > [!UICONTROL All Audiences] o dentro de la configuración de ubicación) que está rellenando el segmento y compare el número de ID universales con el número de direcciones de correo electrónico con hash originales.

   DSP Los segmentos deben estar disponibles en un plazo de 24 horas para su uso en el mercado de la. DSP Una vez que reciba los datos del segmento, el recuento de audiencias debería ser visible en un plazo de nueve (9) horas. Para obtener información sobre las tasas de traducción de ID aceptables y por qué los recuentos de segmentos pueden variar, consulte &quot;[Variaciones de datos entre ID de correo electrónico e ID universales](#universal-ids-data-variances).&quot;

Los segmentos se actualizan cada 24 horas.

## Resolución de problemas

Para solucionar problemas de tasa de traducción y recuento de usuarios, consulte[Compatibilidad con la activación de ID universales](/help/dsp/audiences/universal-ids.md).&quot;

Para solucionar problemas con el procedimiento de conversión, póngase en contacto con el equipo de la cuenta de Adobe o `adcloud-support@adobe.com`.

>[!MORELIKETHIS]
>
>* [Acerca de las fuentes de audiencia de origen](/help/dsp/audiences/sources/source-about.md)
>* [Administrar fuentes de audiencia para activar audiencias de ID universal](source-manage.md)
>* [Conversión de ID de usuario [!DNL Adobe Real-Time CDP] a los ID universales](/help/dsp/audiences/sources/source-adobe-rtcdp.md)
>* [Conversión de ID de usuario [!DNL Tealium] a los ID universales](/help/dsp/audiences/sources/source-tealium.md)
>* [Acerca de Audience Management](/help/dsp/audiences/audience-about.md)
