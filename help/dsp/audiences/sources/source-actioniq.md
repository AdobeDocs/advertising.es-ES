---
title: Convertir los identificadores de usuario de  [!DNL ActionIQ]  a identificadores universales
description: Aprenda a habilitar DSP para que ingrese sus  [!DNL ActionIQ] segmentos de origen.
feature: DSP Audiences
source-git-commit: 21ed5558a39ea9b097be8e70ef81bcf8e59c14b4
workflow-type: tm+mt
source-wordcount: '269'
ht-degree: 0%

---

# Convertir los identificadores de usuario de [!DNL ActionIQ] a identificadores universales

*característica de Beta*

Use la integración de DSP con la plataforma de datos del cliente [!DNL ActionIQ] para convertir las direcciones de correo electrónico con hash en identificadores universales para la publicidad de destino.

Hay <!-- NN --> pasos para compartir datos de [!DNL ActionIQ] con DSP:

1. [Crear un origen de audiencia en DSP](#source-create).

1. ?

## Paso 1: Crear una fuente de audiencia en DSP {#source-create}

1. [Cree una fuente de audiencia](source-manage.md) para importar audiencias a su cuenta de DSP o a una cuenta de anunciante, especificando los [formatos de ID universales](source-about.md) a los que desea convertir los identificadores de usuario.

1. Después de crear el origen de audiencia, comparta la clave de código fuente con el usuario [!DNL ActionIQ].

## Paso 2:

## Paso 3:

1. Compruebe en la biblioteca de audiencias (que está disponible cuando crea o edita una audiencia de [!UICONTROL Audiences] > [!UICONTROL All Audiences] o en la configuración de ubicación) que el segmento se está rellenando y compare el número de ID universales con el número de direcciones de correo electrónico con hash originales.

   Los segmentos deberían estar disponibles en DSP en un plazo de 24 horas. Una vez que DSP recibe los datos del segmento, el recuento de público debe ser visible en un plazo de nueve (9) horas. Para obtener información sobre las tasas de traducción de ID aceptables y por qué los recuentos de segmentos pueden variar, consulte &quot;[Variaciones de datos entre ID de correo electrónico e ID universales](#universal-ids-data-variances)&quot;.

Los segmentos se actualizan cada 24 horas.

## Resolución de problemas

Para solucionar problemas de tasa de traducción y recuento de usuarios, consulte &quot;[Compatibilidad con la activación de identificadores universales](/help/dsp/audiences/universal-ids.md)&quot;.

Para solucionar problemas con el procedimiento de conversión, póngase en contacto con el equipo de cuenta de Adobe o con `adcloud-support@adobe.com`.

>[!MORELIKETHIS]
>
>* [Acerca de las fuentes de audiencia de origen](/help/dsp/audiences/sources/source-about.md)
>* [Administrar fuentes de audiencia para activar audiencias de ID universal](source-manage.md)
>* [Convertir los identificadores de usuario de [!DNL Adobe Real-Time CDP] a identificadores universales](/help/dsp/audiences/sources/source-adobe-rtcdp.md)
>* [Convertir los identificadores de usuario de [!DNL Tealium] a identificadores universales](/help/dsp/audiences/sources/source-tealium.md)
>* [Acerca de la administración de audiencias](/help/dsp/audiences/audience-about.md)
