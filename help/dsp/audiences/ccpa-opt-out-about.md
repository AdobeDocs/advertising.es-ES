---
title: Acerca de [!UICONTROL CCPA Opt-out-of-Sale] segmentos e informes
description: Obtenga información sobre la creación de segmentos para rastrear los ID de las solicitudes de exclusión de la venta de la CCPA y cómo recuperar informes de los ID.
feature: CCPA, DSP Segments
exl-id: 28b5e00b-a695-46f1-abbf-7bbd78f05411
source-git-commit: 4b9cc5956d573b346eacdf71a8ea490c162b4660
workflow-type: tm+mt
source-wordcount: '243'
ht-degree: 0%

---

# Acerca de [!UICONTROL CCPA Opt-out-of-Sale] segmentos e informes

Puede rastrear los ID de usuarios de las solicitudes de exclusión de venta de consumidores en su sitio web, según la Ley de Privacidad del Consumidor de California (CCPA), [creando e implementando un segmento de exclusión de venta de CCPA](ccpa-opt-out-segment-create.md). Los usuarios permanecen indefinidamente en los segmentos de exclusión de la venta de la CCPA.

Una vez implementada la etiqueta de píxel de segmento, el Adobe Advertising empieza a recopilar un grupo de ID en nombre del anunciante.

## Informes de exclusión de venta de consumidores

El Adobe Advertising de genera informes mensuales de los ID que los clientes han enviado para solicitudes de exclusión de venta de la cuenta. DSP Los datos consolidan las solicitudes capturadas mediante los segmentos de exclusión de la venta de la CCPA creados en y en cualquier envío realizado a través de la API de Privacy Service.  Los informes se generan el primer día de cada mes del mes anterior. Por ejemplo, la lista de usuarios mensual de para junio está disponible el 1 de julio.

Cada informe está disponible como archivo de texto separado por tabulaciones comprimido en formato GZIP. Los ID de usuario capturados en los segmentos de exclusión de la venta de la CCPA se identifican por segmento y por anunciante.

DSP DSP Puede [recuperar vínculos a los informes mensuales](ccpa-opt-out-segment-report-retrieve.md) que se crearon en los tres meses anteriores, ya sea desde dentro de los grupos de informes o usando el grupo de informes [!DNL Trafficking API] que se encuentra en el grupo de informes de la página de inicio de la página de inicio de la página de inicio de sesión de la página de inicio de sesión de la página de inicio de. Cada vínculo es válido durante siete días, pero se actualiza cada vez que un cliente intenta recuperar uno.

>[!MORELIKETHIS]
>
>* [Compatibilidad de Adobe Advertising con la Ley de privacidad del consumidor de California: compatibilidad con la exclusión del consumidor](/help/privacy/ccpa/ccpa-opt-out-of-sale.md)
>* [Crear e implementar un segmento [!UICONTROL CCPA Opt-Out-of-Sale]](ccpa-opt-out-segment-create.md)
>* [Recuperar informes de exclusión de venta de consumidores](ccpa-opt-out-segment-report-retrieve.md)
>* [Acerca de la administración de audiencias](audience-about.md)
