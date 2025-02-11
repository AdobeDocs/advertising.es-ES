---
title: Macros disponibles para URL de seguimiento
description: Haga referencia a las macros que puede agregar a las direcciones URL de seguimiento de la página de aterrizaje, y a los elementos creativos de terceros.
feature: Creative Experiences, Creative Experiences
exl-id: d0cbbb21-467d-4ed1-bc6e-ded1b045b98b
source-git-commit: 926d2a0db933a19f5ebef056eca2089f2de6ca64
workflow-type: tm+mt
source-wordcount: '227'
ht-degree: 0%

---

# Macros disponibles para URL de seguimiento

*Beta cerrada*

<!-- More feature metadata??? -->

Puede incluir cualquiera de las siguientes macros en los elementos creativos de terceros, en las direcciones URL de seguimiento de terceros para sus experiencias y en las direcciones URL de las páginas de aterrizaje para su propio uso.

Algunas de las macros disponibles, o sus equivalentes, se incluyen automáticamente en las etiquetas de experiencia.

<!-- Later: 

| Macro | Description | Automatically in experience tags for Advertising DSP? | Automatically in experience tags for [!DNL Google Campaign Manager 360]? |
| --- | --- | --- | --- |
| `${TM_CAMPAIGN_ID_NUM}` | Tracks and reports the campaign ID from the DSP | Yes | No, but tags include the equivalent [!DNL Google Campaign Manager 360] macro `%ebuy!` |
| `${TM_SITE_ID_NUM}` | Tracks and reports the site ID from the DSP | Yes | No, but tags include the equivalent [!DNL Google Campaign Manager 360] macro `%esid!` |
| `${TM_PLACEMENT_ID_NUM}` | Tracks and reports the placement ID from the DSP | Yes | No, but tags include the equivalent [!DNL Google Campaign Manager 360] macro `%epid!` |
| `${TM_AD_ID_NUM}` | Tracks and reports the ad ID from the DSP | Yes | No, but tags include the equivalent [!DNL Google Campaign Manager 360] macro `%eaid!` |
| `${TM_CREATIVE_ID_NUM}` | Tracks and reports the creative ID from the DSP | N/A | No, but tags include the equivalent [!DNL Google Campaign Manager 360] macro `%ecid!` |
| `${TM_SESSION_ID}` | Tracks and reports the impression ID from the DSP. If a value isn't returned, Advertising Creative generates one. | Yes | &mdash; |
| `${TM_ACC_EXPERIENCE_ID}` | Tracks and reports the Advertising Creative experience ID | &mdash; | &mdash; |
| `${TM_ACC_CREATIVE_ID}` | Tracks and reports the Advertising Creative creative ID | &mdash; | &mdash; |
| `${TM_RANDOM}` | A random number between 1 and 1000000 | &mdash; | &mdash; |
| `${TM_TIMESTAMP}` | The Unix Timestamp (in seconds) | &mdash; | &mdash; |
| `${TM_CLICK_URL_URLENC}` | (For third-party ads from vendors who require URL encoding) The encoded click redirect URL, which enables ad servers to track and count ad clicks. When the ad is served and the user clicks on it, the macro is activated, and the click is recorded and counted for reporting purposes. | Yes | &mdash; |

-->

| Macro | Descripción | ¿Usar automáticamente etiquetas de experiencia para Advertising DSP? |
| --- | --- | --- |
| `${TM_CAMPAIGN_ID_NUM}` | Registra e informa del ID de campaña de DSP | Sí |
| `${TM_SITE_ID_NUM}` | Registra e informa del ID del sitio desde DSP | Sí |
| `${TM_PLACEMENT_ID_NUM}` | Registra e informa del ID de ubicación de DSP | Sí |
| `${TM_AD_ID_NUM}` | Registra e informa del ID de anuncio de DSP | Sí |
| `${TM_CREATIVE_ID_NUM}` | Registra e informa del ID creativo de DSP | N/D |
| `${TM_SESSION_ID}` | Registra e informa del ID de impresión de DSP. Si no se devuelve un valor, Advertising Creative genera uno. | Sí |
| `${TM_ACC_EXPERIENCE_ID}` | Realiza un seguimiento del Experience ID de Advertising Creative y elabora informes sobre él | — |
| `${TM_ACC_CREATIVE_ID}` | Registra e informa del ID creativo de Advertising Creative | — |
| `${TM_RANDOM}` | Un número aleatorio entre 1 y 1000000 | — |
| `${TM_TIMESTAMP}` | La marca de tiempo Unix (en segundos) | — |
| `${TM_CLICK_URL_URLENC}` | (Para anuncios de terceros de proveedores que requieren codificación de URL) La URL de redireccionamiento de clics codificada, que permite a los servidores de publicidad rastrear y contar clics de publicidad. Cuando se publica el anuncio y el usuario hace clic en él, la macro se activa y el clic se registra y se cuenta para la creación de informes. | Sí |

>[!MORELIKETHIS]
>
>* 
>* 
