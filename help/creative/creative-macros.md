---
title: Macros disponibles para URL de seguimiento
description: Haga referencia a las macros que puede agregar a las direcciones URL de la página de aterrizaje, las direcciones URL de seguimiento y los elementos creativos de terceros.
feature: Creative Experiences, Creative Experiences
exl-id: d0cbbb21-467d-4ed1-bc6e-ded1b045b98b
TQID: https://experienceleague.adobe.com/J5jfIECrL29NngVOulEgHKZBHYqBmoz4680HzEzhIng
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dcid: aa2f3246-cb95-4b30-8899-fdf7d73550cc
source-git-commit: 3c3bffe0c28bb24c0df9385f9cc91be1376a66d2
workflow-type: tm+mt
source-wordcount: 319
ht-degree: 0%

---

# Macros disponibles para URL de seguimiento

<!-- More feature metadata???  -->

Puede incluir cualquiera de las siguientes macros en los elementos creativos de terceros, en las direcciones URL de seguimiento de terceros para sus experiencias y en las direcciones URL de las páginas de aterrizaje para su propio uso.

Algunas de las macros disponibles, o sus equivalentes, se incluyen automáticamente en las etiquetas de experiencia.

<!--
 Later: 

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
| `${TC_1}` | Custom tracking code 1. | &mdash; | &mdash; |
| `${TC_2}` | Custom tracking code 2. | &mdash; | &mdash; |
| `${TC_3}` | Custom tracking code 3. | &mdash; | &mdash; |
| `${TC_4}` | Custom tracking code 4. | &mdash; | &mdash; |
| `${TC_5}` | Custom tracking code 5. | &mdash; | &mdash; |
| `${GDPR_ENFORCED}` | Whether GDPR enforcement is required for the bid request. Values: **1** = GDPR should be enforced, **0** = GDPR should not be enforced. | &mdash; | &mdash; |
| `${GDPR_CONSENT}` | The GDPR consent value received from the supply partner in the bid request. Typically: **1** = consent provided, **0** = no consent provided. | &mdash; | &mdash; |
-->

| Macro | Descripción | ¿Usar automáticamente etiquetas de experiencia para Advertising DSP? |
| --- | --- | --- |
| `${TM_CAMPAIGN_ID_NUM}` | Registra e informa del ID de campaña de DSP | Sí |
| `${TM_SITE_ID_NUM}` | Registra e informa del ID del sitio desde DSP | Sí |
| `${TM_PLACEMENT_ID_NUM}` | Registra e informa del ID de ubicación de DSP | Sí |
| `${TM_AD_ID_NUM}` | Registra e informa del ID de anuncio de DSP | Sí |
| `${TM_CREATIVE_ID_NUM}` | Registra e informa del ID creativo de DSP | N/D |
| `${TM_SESSION_ID}` | Registra e informa del ID de sesión asociado con la solicitud de publicidad. Si no se devuelve un valor, Advertising Creative genera uno. | Sí |
| `${TM_ACC_EXPERIENCE_ID}` | Realiza un seguimiento del Experience ID de Advertising Creative y elabora informes sobre él | — |
| `${TM_ACC_CREATIVE_ID}` | Registra e informa del ID creativo de Advertising Creative | — |
| `${TM_RANDOM}` | Un número generado aleatoriamente entre 1 y 1.000.000. Se utiliza comúnmente para la eliminación de caché. | — |
| `${TM_TIMESTAMP}` | La marca de tiempo UNIX® (en segundos) | — |
| `${TM_CLICK_URL_URLENC}` | (Para anuncios de terceros de proveedores que requieren codificación de URL) La URL de redireccionamiento de clics codificada, que permite a los servidores de publicidad rastrear y contar clics de publicidad. Cuando un usuario hace clic en el anuncio, la macro se activa y el clic se registra y se cuenta para la creación de informes. | Sí |
| `${TC_1}` | Código de seguimiento personalizado 1. | — |
| `${TC_2}` | Código de seguimiento personalizado 2. | — |
| `${TC_3}` | Código de seguimiento personalizado 3. | — |
| `${TC_4}` | Código de seguimiento personalizado 4. | — |
| `${TC_5}` | Código de seguimiento personalizado 5. | — |
| `${GDPR_ENFORCED}` | Si se requiere el cumplimiento del RGPD para la solicitud de oferta. Valores: **1** = RGPD debe aplicarse, **0** = RGPD no debe aplicarse. | — |
| `${GDPR_CONSENT}` | El valor de consentimiento del RGPD recibido del socio de suministro en la solicitud de oferta. Normalmente: **1** = consentimiento proporcionado, **0** = sin consentimiento proporcionado. | — |

>[!MORELIKETHIS]
>
>* [Agregar elementos creativos estándar a una biblioteca creativa](/help/creative/creative-libraries/creative-add-standard.md#creative-add-third-party)
>* [Configuración creativa estándar](/help/creative/creative-libraries/creative-settings-standard.md#creative-settings-third-party)
>* [Configuración de experiencia de destino*[Configuración de experiencia sin destino](/help/creative/experiences/experience-settings-no-targeting.md)
