---
title: Acerca de [!UICONTROL CCPA Opt-out-of-Sale] segmentos e informes
description: Obtenga información sobre la creación de segmentos para rastrear los ID de las solicitudes de exclusión de la venta de la CCPA y cómo recuperar informes de los ID.
feature: CCPA, DSP Segments
exl-id: 28b5e00b-a695-46f1-abbf-7bbd78f05411
TQID: 'https://experienceleague.adobe.com/Bp8Fj0z7lqSXmHd-aJQa6ocQyj6FVQuydArNBucpJp4'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
    internal-label: Demand Side Platform
  - id: 2b670c6e-542a-5afe-b96b-d9ce7818cd55
    internal-label: DSP Segments
  - id: b2025470-04ef-4dd9-bdd4-44407644aeb6
    internal-label: Compliance
subfeature_v2:
  - id: c193c532-b70e-4556-bde7-857186cbe140
    internal-label: Segments
  - id: c867fa1b-f589-43fa-b071-3c62f0038f23
    internal-label: CCPA
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
    internal-label: Privacy
source-git-commit: 6d95caf72d11c404d866e8d091e1ffa89814ae73
workflow-type: tm+mt
source-wordcount: '274'
ht-degree: 0%
---
# Acerca de [!UICONTROL CCPA Opt-out-of-Sale] segmentos e informes

Puede rastrear los ID de usuarios de las solicitudes de exclusión de venta de consumidores en su sitio web, según la Ley de Privacidad del Consumidor de California (CCPA), [creando e implementando un segmento de exclusión de venta de CCPA](ccpa-opt-out-segment-create.md). Los usuarios permanecen indefinidamente en los segmentos de exclusión de la venta de la CCPA.

Una vez implementada la etiqueta de píxel de segmento, Adobe Advertising empieza a recopilar un grupo de ID en nombre del anunciante.

## Informes de exclusión de venta de consumidores

Adobe Advertising genera informes mensuales de los ID que los clientes han enviado para solicitudes de exclusión de venta de la cuenta. Los datos consolidan las solicitudes capturadas mediante segmentos de exclusión de la venta de la CCPA creados en DSP y cualquier envío realizado mediante la API de Privacy Service.  Los informes se generan el primer día de cada mes del mes anterior. Por ejemplo, la lista de usuarios mensual de para junio está disponible el 1 de julio.

Cada informe está disponible como archivo de texto separado por tabulaciones comprimido en formato GZIP. Los ID de usuario capturados en los segmentos de exclusión de la venta de la CCPA se identifican por segmento y por anunciante.

Puede [recuperar vínculos a los informes mensuales](ccpa-opt-out-segment-report-retrieve.md) creados en los tres meses anteriores, ya sea desde DSP o mediante DSP [!DNL Trafficking API]. Cada vínculo es válido durante siete días, pero se actualiza cada vez que un cliente intenta recuperar uno.

>[!MORELIKETHIS]
>
>* [Compatibilidad de Adobe Advertising con la Ley de privacidad del consumidor de California: compatibilidad con la exclusión de la venta del consumidor](/help/privacy/ccpa/ccpa-opt-out-of-sale.md)
>* [Crear e implementar un segmento [!UICONTROL CCPA Opt-Out-of-Sale]](ccpa-opt-out-segment-create.md)
>* [Recuperar informes de exclusión de venta de consumidores](ccpa-opt-out-segment-report-retrieve.md)
>* [Acerca de la administración de audiencias](audience-about.md)
