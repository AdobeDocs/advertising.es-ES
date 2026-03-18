---
title: Acerca de [!UICONTROL CCPA Opt-out-of-Sale] segmentos e informes
description: Obtenga información sobre la creación de segmentos para rastrear los ID de las solicitudes de exclusión de la venta de la CCPA y cómo recuperar informes de los ID.
feature: CCPA, DSP Segments
exl-id: 28b5e00b-a695-46f1-abbf-7bbd78f05411
source-git-commit: e61f3c7d066a72f9a438ef292122cdf99370fd0c
workflow-type: tm+mt
source-wordcount: '245'
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
