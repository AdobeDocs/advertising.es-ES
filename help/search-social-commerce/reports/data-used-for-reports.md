---
title: Los datos utilizados para los informes
description: Obtenga información sobre los distintos tipos de datos disponibles en las vistas de datos y los informes personalizados.
exl-id: ba808b21-4421-4de5-9293-a20ec67cc81c
feature: Search Reports
source-git-commit: f357d9a9ec0f8b38fbc43726265521e6fd77c7d0
workflow-type: tm+mt
source-wordcount: '599'
ht-degree: 0%

---

# Los datos utilizados para los informes

Search, Social y Commerce incluyen un conjunto completo de informes de rendimiento basados en datos de conversión y clics. Puede ver datos de rendimiento básicos de los distintos componentes de un portafolio o cuenta de publicidad desde las vistas [!UICONTROL Portfolios] y [!UICONTROL Campaigns], así como mediante la generación de varios informes básicos y avanzados.

Los anunciantes que usen el servicio de seguimiento de conversión de Adobes Advertising también pueden identificar el número de clics de una ubicación geográfica o el nombre de dominio de un sitio web de referencia, cómo los anuncios de cada canal y los distintos eventos que llevan a una conversión contribuyen a la tasa de conversión general y la distribución de conversiones para una sola [métrica de conversión](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md) por canal de marketing. Los informes disponibles varían según el tipo de cuenta de usuario. El equipo de cuenta de Adobe tiene acceso a todos los informes.

La mayoría de los informes se pueden personalizar para mostrar únicamente la información que desee ver. Las siguientes métricas estándar están disponibles en la mayoría de los informes y se calculan a nivel de anuncio:

* **Métricas de rendimiento estándar:**

   * **[!UICONTROL Impressions]:** Número total de veces que se colocó el anuncio.

   * **[!UICONTROL Clicks]:** Número total de veces que se hizo clic en un vínculo del anuncio.

   * **[!UICONTROL Cost]:** Coste total del anuncio. El coste de la publicidad de pago por clic (PPC) es siempre el número de clics multiplicado por el coste por clic.

   * **[!UICONTROL Cost per Click]:** Coste promedio de un clic para un anuncio, que es el coste del anuncio dividido por el número total de clics para el anuncio. Por ejemplo, si gasta 100 USD para una impresión de publicidad y el anuncio genera 10 clics, el coste por clic es 100 USD/10=10 USD por clic.

   * **[!UICONTROL Average Position]:** (cuando corresponda) La posición promedio de un anuncio que se ha colocado, ponderada por el número de impresiones.

   * **[!UICONTROL Estimated Clicks]:** (Incluido en los informes avanzados para anunciantes con el servicio de seguimiento de conversión de Adobe Advertising solamente) El número total de clics estimados para una ciudad o el nombre de dominio de un sitio web de referencia. Esto puede incluir datos de redes de anuncios para las que un anunciante no tiene una cuenta publicitaria.

* **Métricas de conversión:** Número total de conversiones para cada una de las métricas de conversión del anunciante o datos de transacción seguidos hacia una métrica de conversión. Esto puede incluir métricas de conversión y de participación del sitio, pero no métricas calculadas y métricas calculadas avanzadas, que se sincronizan desde Adobe Analytics.

  Esto también puede incluir [[!DNL Google Ads] conversiones ](/help/search-social-commerce/campaign-management/introduction/google-conversion-data.md) y [[!DNL Google Analytics] conversiones ](/help/search-social-commerce/admin/data-sources/data-source-about.md) con seguimiento sincronizadas para la cuenta del anunciante.

* **Métricas personalizadas:** Sus propias métricas, que se derivan de la creación de fórmulas basadas en métricas existentes (como el costo por pedido).

## Disponibilidad de datos

Al generar informes, puede elegir cómo atribuir datos de conversión en una serie de eventos que llevan a una conversión. Por ejemplo, puede elegir atribuir toda la conversión al último evento o ponderar el último evento más que los demás. De forma predeterminada, las conversiones se atribuyen al último evento.

Según la regla de atribución que especifique para el informe, los datos de cada tipo de informe estarán disponibles para las fechas siguientes.

| Grupo de informes | Informe | Fechas para las que hay datos disponibles |
| --- | --- | --- |
| [!UICONTROL Basic Reports] | [!UICONTROL Campaign Hourly Report] | A partir del 15 de mayo de 2021.<br><br><b>Excepción:</b> Los datos de métricas de prominencia están disponibles a partir del 8 de septiembre de 2022. |
| | Todos los demás [!UICONTROL Basic Reports] | Los 36 meses anteriores.<br><br><b>Excepción:</b> Los datos de métricas de prominencia están disponibles a partir del 8 de septiembre de 2022. |
| [!UICONTROL Advanced Reports] | [!UICONTROL Transaction Report] | Los 45 días previos. |
| | [!UICONTROL Domain Referral Report], [!UICONTROL Geo Distribution Report] | Los dos (2) meses anteriores más el mes actual. |
| [!UICONTROL Assist Reports] | Todo | Los 18 meses anteriores. |
| [!UICONTROL Specialty Reports] | [!UICONTROL AdWords Audience Target Report] | El año anterior. |
| | [!UICONTROL Google Asset Group Performance Report] | Sin limitaciones |
| | [!UICONTROL MSA Ad Extension by Ad Report], [!UICONTROL MSA Ad Extension by Keyword Report], [!UICONTROL MSA Ad Extension Detail Report], [!UICONTROL MSA Network Impression Share Report], [!UICONTROL MSA Network Performance Report] | Los últimos 180 días. |
| | [!UICONTROL RSA Assets Report] | A partir del 10 de agosto de 2022. |
| | Todos los demás [!UICONTROL Specialty Reports] | Los dos (2) meses anteriores. |
| [!UICONTROL Model Accuracy Reports] | [!UICONTROL Forecast Accuracy Report] | Los 18 meses anteriores. |
| [!UICONTROL Change History Report] | — | Los 31 días anteriores. |

>[!MORELIKETHIS]
>
>* [Acerca de los informes](report-about.md)
>* [Tareas de configuración iniciales para informes](initial-setup.md)
