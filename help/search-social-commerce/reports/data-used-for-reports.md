---
title: Los datos utilizados para los informes
description: Obtenga información sobre los distintos tipos de datos disponibles en las vistas de datos y los informes personalizados.
exl-id: 3e1f2967-5034-46bc-8473-63cffeeeecba
source-git-commit: 3aad445fc1a5a0e2210209f181b9756047f44999
workflow-type: tm+mt
source-wordcount: '576'
ht-degree: 0%

---

# Los datos utilizados para los informes

Search, Social y Commerce incluyen un conjunto completo de informes de rendimiento basados en datos de conversión y clics. Puede ver los datos de rendimiento básicos de los distintos componentes de una cartera de productos o una cuenta de publicidad en [!UICONTROL Portfolios] y [!UICONTROL Campaigns] vistas, así como mediante la generación de varios informes básicos y avanzados.

Los anunciantes que utilizan el servicio de seguimiento de conversiones también pueden identificar el número de clics de una ubicación geográfica o el nombre de dominio de un sitio web de referencia, cómo los anuncios de cada canal y los distintos eventos que llevan a una Adobe Advertising contribuyen a la tasa de conversión general y la distribución de conversiones para un solo sitio [propiedad de transacción](/help/search-social-commerce/admin/transaction-properties/transaction-property-about.md) por canal de marketing. Los informes disponibles varían según el tipo de cuenta de usuario. El equipo de cuenta de Adobe tiene acceso a todos los informes.

La mayoría de los informes se pueden personalizar para mostrar únicamente la información que desee ver. Las siguientes métricas estándar están disponibles en la mayoría de los informes y se calculan a nivel de anuncio:

* **Métricas de rendimiento estándar:**

   * **[!UICONTROL Impressions]:** Número total de veces que se colocó el anuncio.

   * **[!UICONTROL Clicks]:** Número total de veces que se hizo clic en un vínculo del anuncio.

   * **[!UICONTROL Cost]:** Coste total de la publicidad. El coste de la publicidad de pago por clic (PPC) es siempre el número de clics multiplicado por el coste por clic.

   * **[!UICONTROL Cost per Click]:** Coste promedio de un clic en un anuncio, que es el coste del anuncio dividido por el número total de clics para el anuncio. Por ejemplo, si gasta 100 USD para una impresión de publicidad y el anuncio genera 10 clics, el coste por clic es 100 USD/10=10 USD por clic.

   * **[!UICONTROL Average Position]:** (Cuando corresponda) La posición promedio de un anuncio que se ha colocado, ponderada por el número de impresiones.

   * **[!UICONTROL Estimated Clicks]:** (Incluido en los informes avanzados solo para anunciantes con el servicio de seguimiento de conversión de Adobes Advertising) El número total de clics estimados de una ciudad o el nombre de dominio de un sitio web de referencia. Esto puede incluir datos de redes de anuncios para las que un anunciante no tiene una cuenta publicitaria.

* **Métricas de conversión:** Número total de conversiones para cada uno de los anuncios del anunciante [propiedades de transacción](/help/search-social-commerce/glossary.md#s-t)o datos de transacción rastreados hasta un tipo de conversión. Esto puede incluir métricas de conversión y de participación del sitio, pero no métricas calculadas y métricas calculadas avanzadas, que se sincronizan desde Adobe Analytics.

  Esto también puede incluir [[!DNL Google Ads]Conversiones seguidas por](/help/search-social-commerce/campaign-management/introduction/google-conversion-data.md) y [[!DNL Google Analytics]Conversiones seguidas por](/help/search-social-commerce/admin/data-sources/data-source-about.md) que se sincronizan con la cuenta del anunciante.

* **Métricas personalizadas:** Sus propias métricas, que se derivan de la creación de fórmulas basadas en métricas existentes (como el coste por pedido).

## Disponibilidad de datos

Al generar informes, puede elegir cómo atribuir datos de conversión en una serie de eventos que llevan a una conversión. Por ejemplo, puede elegir atribuir toda la conversión al último evento o ponderar el último evento más que los demás. De forma predeterminada, las conversiones se atribuyen al último evento.

Según la regla de atribución que especifique para el informe, los datos de cada tipo de informe estarán disponibles para las fechas siguientes.

| Grupo de informes | Informe | Fechas para las que hay datos disponibles |
|---|---|---|
| [!UICONTROL Basic Reports] | [!UICONTROL Campaign Hourly Report] | A partir del 15 de mayo de 2021.<br><br><b>Excepción:</b> Los datos de métricas de prominencia estarán disponibles a partir del 8 de septiembre de 2022. |
| | Todos los demás [!UICONTROL Basic Reports] | Los 36 meses anteriores.<br><br><b>Excepción:</b> Los datos de métricas de prominencia estarán disponibles a partir del 8 de septiembre de 2022. |
| [!UICONTROL Advanced Reports] | [!UICONTROL Transaction Report] | Los 45 días previos. |
| | [!UICONTROL Domain Referral Report], [!UICONTROL Geo Distribution Report] | Los dos (2) meses anteriores más el mes actual. |
| [!UICONTROL Assist Reports] | Todo | Los 18 meses anteriores. |
| [!UICONTROL Specialty Reports] | [!UICONTROL AdWords Audience Target Report] | El año anterior. |
| | [!UICONTROL RSA Assets Report] | A partir del 10 de agosto de 2022. |
| | [!UICONTROL MSA Ad Extension by Ad Report], [!UICONTROL MSA Ad Extension by Keyword Report], [!UICONTROL MSA Ad Extension Detail Report] | Los últimos 180 días. |
| | Todos los demás [!UICONTROL Specialty Reports] | Los dos (2) meses anteriores. |
| [!UICONTROL Model Accuracy Reports] | [!UICONTROL Forecast Accuracy Report] | Los 18 meses anteriores. |
| [!UICONTROL Change History Report] | — | Los 31 días anteriores. |

>[!MORELIKETHIS]
>
>* [Acerca de los informes](report-about.md)
>* [Tareas de configuración iniciales para informes](initial-setup.md)
